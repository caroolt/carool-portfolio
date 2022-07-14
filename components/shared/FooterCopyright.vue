<script>
import { mapState } from "vuex";

export default {
  data: () => {
    return {
      projectName: "Nuxt.js Portfólio",
      author: "Carolina Teixeira",
    };
  },
  computed: {
    ...mapState(["copyrightDate"]),
  },
};
</script>

<template>
  <div class="flex justify-center items-center text-center">
    <div
      class="
        font-general-regular
        text-lg text-ternary-dark
        dark:text-ternary-light
      "
    >
      &copy; {{ copyrightDate }}.
      <a
        href=""
        target="__blank"
        class="
          font-general-medium
          hover:underline hover:text-indigo-600
          dark:hover:text-indigo-300
          duration-500
        "
        >{{ projectName }}</a
      >
      . Developed with <i width="18px" height="18px" class='heart' data-feather="heart"/> by
      <a
        href=""
        target="__blank"
        class="
          font-general-medium
          text-secondary-dark
          dark:text-secondary-light
          hover:underline hover:text-indigo-600
          dark:hover:text-indigo-300
          duration-500
        "
        >{{ author }}</a
      >
    </div>
  </div>
</template>

<style lang="css" scoped>
.heart{
  color: #6366F1;
  display:inline-flex;
}
</style>
