<template>
  <div class="card">
    <h3>{{ news.title }}</h3>
    <h3>{{ news.author }}</h3>
    <button class="btn primary" @click="toggle">
      {{ news.isOpen === false ? "Открыть" : "Закрыть" }}
    </button>
    <p v-if="news.isOpen">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Officiis ullam
      porro quo. Suscipit, repellat? Aut nemo vel ab explicabo similique?
      Impedit sit qui quasi cumque quo nemo facere similique deserunt!
    </p>
  </div>
</template>

<script>
export default {
  props: {
    news: {
      type: Array,
    },
  },
  methods: {
    toggle() {
      this.news.isOpen = !this.news.isOpen;
    },
  },
};
</script>