<template>
  <section class="flex flex-wrap p-5">
    <div class="p-2">
      <VueTelInput
        class="p-1"
        @input="
          (phone, object) => {
            test = object;
          }
        "
        autoDefaultCountry
        styleClasses="border border-red-600 "
        invalidMsg="ysta mesh sa7"
      ></VueTelInput>
    </div>

    <div class="p-2">Finaly Value: {{ yourValue }}</div>
    <div class="p-2 whitespace-pre">Finaly object: {{ test }}</div>

    <div class="p-2">
      <button
        @click="addNumbers()"
        class="px-3 py-2 text-sm rounded-md  bg-emerald-500 hover:bg-emerald-600 text-emerald-50"
      >
        submit
      </button>
    </div>
  </section>
</template>

<script>
import { VueTelInput } from "vue-tel-input";
import "vue-tel-input/dist/vue-tel-input.css";
export default {
  components: { VueTelInput },
  name: "IndexPage",
  data() {
    return {
      yourValue: "0",
      test: "",
    };
  },
  methods: {
    addNumbers() {
      const nums = [
        "01223618001",
        "+16045555555",
        "+447911123456",
        "+911234567890",
      ];
      this.yourValue = nums[Math.floor(Math.random() * nums.length)];
      // this.yourValue = "01223618001";
    },
  },
};
</script>
