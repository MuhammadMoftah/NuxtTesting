<template>
  <section
    class="flex flex-wrap w-screen h-screen p-5 bg-blue-400 dark:bg-red-300"
  >
    <button class="btn">Test</button>
  </section>
</template>

<script>
export default {
  name: "IndexPage",

  data() {
    return {
      yourValue: "0",
      test: "test",
    };
  },
  mounted() {
    console.log($nuxt);
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
