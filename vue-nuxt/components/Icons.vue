<template>
  <div class="text-center">
    <b-row>
      <b-col>
        <b-img class="mt-4" src="../assets/Group 731 1.png"></b-img>
      </b-col>
    </b-row>
    <b-row>
      <b-col>
        <b-img class="mt-5" src="../assets/Group 732.png"></b-img>
      </b-col>
    </b-row>

    <b-row>
      <b-col>
        <div class="d-flex flex-row iconContainer mt-4">
          <b-img src="../assets/Group 24.png"></b-img>
          <p class="text mt-2 ml-3">Powerful and reliable global network</p>
        </div>
      </b-col>
    </b-row>

    <b-row>
      <b-col>
        <div class="d-flex flex-row iconContainer mt-4">
          <b-img src="../assets/Group 23.png"></b-img>
          <p class="text mt-2 ml-3">Modern & Agile CDN infrastructure</p>
        </div>
      </b-col>
    </b-row>

    <b-row>
      <b-col>
        <div class="d-flex flex-row iconContainer mt-4">
          <b-img src="../assets/Group 25.png"></b-img>
          <p class="text mt-2 ml-3">15 years of CDN experience</p>
        </div>
      </b-col>
    </b-row>

    <b-row>
      <b-col>
        <div class="d-flex flex-row iconContainer mt-4 mb-3">
          <b-img src="../assets/Group 26.png"></b-img>
          <p class="text mt-2 ml-3">Direct access to engineers with Slack</p>
        </div>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.iconContainer {
  position: relative;
  left: 180px;
}

/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .iconContainer {
    left: 80px;
  }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {
  .iconContainer {
    left: 20px;
  }
  .text {
    color: white;
    font-size: 13px;
  }
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  .iconContainer {
    left: 100px;
  }
  .text {
    color: white;
    font-size: 15px;
  }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .iconContainer {
    left: 180px;
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  .iconContainer {
    left: 180px;
  }
}
</style>
