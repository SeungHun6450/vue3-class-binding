<!-- <template>
  <h1 
    :class ="{ active: isActive}"
    @click="activate">
    Hello?!({{isActive}})
  </h1>
</template>

<script>
export default {
  data() {
    return {
      isActive: false
    }
  },
  methods: {
    activate() {
      this.isActive = true
    }
  }
}
</script>

<style scoped>
  .active {
    color: red;
    font-weight: bold;
  }
</style>

-->

<template>
  <h1 
    :style ="[fontStyle, backgroundStyle]"
    @click="chageStyle">
    Hello?!
  </h1>
</template>

<script>
export default {
  data() {
    return {
      // 기본적으로는 객체데이터로 연결하지만 여러개의 객체데이터를 연결할떄는 배열구문 활용
      fontStyle: {
        color: 'orange',
        fontSize: '30px'
      },
      backgroundStyle: {
        backgroundColor: 'black'
      }
    }
  },
  methods: {
    chageStyle() {
      this.fontStyle.color = 'red'
      this.fontStyle.fontSize = '50px'
    }
  }
}
</script>