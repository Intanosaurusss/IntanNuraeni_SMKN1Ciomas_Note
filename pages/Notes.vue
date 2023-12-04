<template>
  <div class="container-notes">
    <div class="allnots" v-for="note in Notes" :key="note.id">
      <header>
        <h1>{{ note.title }}</h1>
        <img
          src="@/assets/image/remove.png"
          alt=""
          @click="remove(note.index)"
        />
      </header>
      <section>
        <p>{{ note.des }}</p>
      </section>
    </div>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: "Notes"
    };
  },
  computed: {
    Notes() {
      return this.$store.getters.getnotes;
    }
  },
  methods: {
    remove(item) {
      this.$store.commit("removenote", item);
      console.log(item);
    }
  }
};
</script>

<style scoped>
.container-notes {
 background: linear-gradient(135deg, #435970, #00bfff);
 padding: 20px;
 box-sizing: border-box;
 width: 100%;
 height: 100%;
}
</style>