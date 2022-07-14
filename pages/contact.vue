<script>
import feather from "feather-icons";

export default {
  scrollToTop: true,
  data: () => {
    return {
      contacts: [
        {
          id: 1,
          name: "Belo Horizonte, Minas Gerais, Brasil",
          icon: "map-pin",
        },
        {
          id: 2,
          name: "carolinatc1405@gmail.com",
          icon: "mail",
        },
        {
          id: 3,
          name: "31 984659546",
          icon: "phone",
        },
      ],
    };
  },
  mounted() {
    feather.replace();
  },
  updated() {
    feather.replace();
  },
};
</script>

<template>
  <div
    class="
      container
      mx-auto
      flex flex-col-reverse
      md:flex-row md:py-10 md:mt-20
    "
  >
    <ContactForm />

    <ContactDetails :contacts="contacts" />
  </div>
</template>
