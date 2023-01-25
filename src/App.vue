<template>
  <div class="container pt-1">
    <div class="card">
      <h2>Актуальные новости {{ now }}</h2>
    </div>

    <app-news
      v-for="(item, index) in news"
      :key="index"
      :news="item"
    ></app-news>
  </div>
</template>

<script>
import AppNews from "./components/AppNews.vue";
export default {
  components: {
    AppNews,
  },
  data() {
    return {
      now: new Date().toLocaleDateString(),
      isOpen: false,
      news: [
        {
          title: "Аргентина выиграла Чемпионат Мира",
          author: "Aibol",
          isOpen: false,
        },
        {
          title: "В США начинаются президенсткие выборы",
          author: "Galymzhan",
          isOpen: true,
        },
        {
          title: "Ольга Рыбакина вышла в 1/2 финала",
          author: "Asylzhan",
          isOpen: false,
        },
      ],
    };
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    },
  },
};
</script>