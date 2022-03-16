<template>
  <div>
    <b-row>
      <b-col class="bgColor" sm="6" md="6"> <Icons /> </b-col>
      <b-col sm="6" md="6">
        <div class="text-center mt-5">
          <b-row>
            <b-col>
              <div>
                <p class="text-header">
                  Start a 14-day instant
                  <span class="font-weight-bold">free trial</span>
                </p>
              </div>
            </b-col>
          </b-row>
          <b-row class="justify-content-md-center">
            <b-col sm="12" md="8" class="p-2">
              <Form />
            </b-col>
          </b-row>
        </div>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.text-header {
   font-family: 'Archivo';
font-style: normal;
font-weight: 400;
font-size: 40px;
line-height: 44px;
}

.bgColor {
  background-color: #002133;
}
</style>
