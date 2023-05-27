<template>
  <div class="menu">
    <ul>
    <li v-for="link of menu" @click="linkClicked(link.link)" v-if='show'><a href='#'>{{link.link}}</a></li>
    <li><button @click="show = !show">{{ show ? 'hide' : 'show' }} menu</button></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Menu',
  data() {
    return {
      show: true,
      clicked: '',
      menu: [
        {id:1, link: 'Daniel'},
        {id:2, link: 'Sylwia'},
        {id:3, link: 'Pixel'},
      ]
    }
  },
  methods: {
    linkClicked(link) {
      this.clicked = link;
      this.$emit('linkClicked', link);
    }
  }
}
</script>