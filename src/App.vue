<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <br>
        <button @click="selectComponent = 'appBlue'" class="btn btn-primary">Load Blue Template</button>
        <button @click="selectComponent ='appGreen'" class="btn btn-success">Load Green Template</button>
        <button @click="selectComponent = 'appRed'" class="btn btn-danger">Load Red Template</button>
        <hr>
        <p>{{ selectComponent }}</p>
        <component :is="selectComponent"></component>
        <!-- <app-blue></app-blue>
        <app-green></app-green>
        <app-red></app-red>-->
      </div>
    </div>
  </div>
</template>

<script>
import Blue from "./components/Blue.vue";
import Green from "./components/Green.vue";
import Red from "./components/Red.vue";

export default {
  data: function() {
    return {
      selectComponent: "appBlue"
    };
  },
  components: {
    appBlue: Blue,
    appGreen: Green,
    appRed: Red
  }
};
</script>

<style>
</style>
