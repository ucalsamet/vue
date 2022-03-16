<template>
  <b-container>
    <p class="text-sub">
      Give your website the
      <span class="font-weight-bold">speed it deserves.</span>
    </p>
    <p class="text-sub">With the fastest, next-generation CDN.</p>

    <b-form>
      <b-form-input
        v-model="$v.form.firstName.$model"
        placeholder="First Name*"
        :state="validateState('firstName')"
      />

      <b-form-input
        v-model="$v.form.lastName.$model"
        class="mt-3"
        placeholder="Last Name*"
        :state="validateState('lastName')"
      />

      <b-form-input v-model="form.company" class="mt-3" placeholder="Company" />

      <b-form-input
        v-model="$v.form.businessEmail.$model"
        class="mt-3"
        placeholder="Business E-mail*"
        :state="validateState('businessEmail')"
      />

      <b-form-input v-model="form.phone" class="mt-3" placeholder="Phone" />

      <b-form-input
        v-model="$v.form.password.$model"
        class="mt-3"
        placeholder="Password*"
        type="password"
        :state="validateState('password')"
      />

      <b-form-input
        v-model="$v.form.rePassword.$model"
        class="mt-3"
        placeholder="Re-enter Password*"
        type="password"
        :state="validateState('rePassword')"
      />

      <b-form-checkbox
        class="mt-3 checkbox-text"
        id="checkbox-1"
        v-model="$v.form.status.$model"
        name="checkbox-1"
        value="accepted"
        unchecked-value="not_accepted"
        :state="validateState('status')"
      >
        I have read and accept the privacy policy. I would like to receive
        emails from Medianova. I reserve the right to opt-out at anytime.
      </b-form-checkbox>

      <b-button @click="sendTrial" variant="danger" block class="mt-2"
        >START TRIAL</b-button
      >
    </b-form>
  </b-container>
</template>

<script>
import { validationMixin } from "vuelidate";
import { required, minLength, sameAs } from "vuelidate/lib/validators";
import axios from "@nuxtjs/axios";
export default {
  mixins: [validationMixin],
  data() {
    return {
      form: {
        firstName: "",
        lastName: "",
        company: "",
        businessEmail: "",
        phone: "",
        password: "",
        rePassword: "",
        status: "",
      },
    };
  },
  validations: {
    form: {
      firstName: {
        required,
      },
      lastName: {
        required,
      },
      businessEmail: {
        required,
      },
      password: {
        required,
        minLength: minLength(6),
      },
      rePassword: {
        sameAsPassword: sameAs("password"),
      },
      status: {
        required,
      },
    },
  },
  methods: {
    validateState(name) {
      const { $dirty, $error } = this.$v.form[name];
      return $dirty ? !$error : null;
    },
    async sendTrial() {
      this.$v.form.$touch();
      if (this.$v.form.$anyError) {
        return;
      }
      const response = await this.$axios.$post(
        "https://jsonplaceholder.typicode.com/users",
        this.form
      );
      if (response) {
        alert("Kayıt Başarılı");
        function pushMedianova() {
          location.replace("https://www.medianova.com/");
        }
        setTimeout(pushMedianova, 5000);
      }else{
          alert("Kayıt Hatalı")
      }
    },
  },
};
</script>

<style scoped>
.text-sub {
  font-family: "Archivo";
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 10px;
}
.checkbox-text {
  font-size: 10px;
}
</style>
