<template>
  <div>
    <b-table
      v-if="items.length > 0"
      striped
      hover
      :items="items"
      :fields="fields"
    ></b-table>
    <p v-else>Aguardando informações...</p>
  </div>
</template>

<script>
export default {
  name: "cardUser",
  data() {
    return {
      items: [],
    };
  },
  mounted() {
    fetch("https://jsonplaceholder.typicode.com/users")
      .then((res) => res.json())
      .then((data) => {
        for (let i = 0; i < data.length; i++) {
          this.items.push({
            name: data[i].name,
            user_name: data[i].username,
            email: data[i].email,
            website: data[i].website,
          });
        }
      });
  },
};
</script>
