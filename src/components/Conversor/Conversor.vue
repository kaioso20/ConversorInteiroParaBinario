<template>
  <div>
    <div class="box">
      <div class="taCenter pd50 divBoxShowResult">
        <div>{{ ResultShow }}</div>
      </div>
      <div class="taCenter pd50 divBoxInputNumber">
        <input
          type="number"
          class="taCenter inputDesign"
          @keyup="() => ConvertNumber()"
          v-model="NumeroInteiro"
        />
      </div>
    </div>
  </div>
</template>

<script>
import "./Conversor.css";
export default {
  name: "Conversor",
  data() {
    return {
      NumeroInteiro: "",
      ResultShow: "0",
    };
  },
  methods: {
    ConvertNumber() {
      this.ResultShow = "0";
      this.ResultShow = (parseInt(this.NumeroInteiro) >>> 0).toString(2);
    },
  },
};
</script>

<style>
</style>