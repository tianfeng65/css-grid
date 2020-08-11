<template>
  <div id="app">
    <!-- example-1 -->
    <div class="example">
      <div class="container" id="container-1">
        <div v-for="item of 9" :key="item" :class="['item', 'item'+item]">
          <p>{{item}}</p>
        </div>
      </div>
      <div class="code">
        <h3>grid-template-columns & grid-template-rows</h3>
        <p></p>
        <code>
          #container-1{<br>
            display: grid;<br>
            grid-template-columns: repeat(3, 100px);<br>
            grid-template-rows: repeat(3, 100px);<br>
          }
        </code>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  }
}
</script>

<style lang="scss" scoped>
// custom css
#container-1{
  grid-template-columns: repeat(3, 100px);
  grid-template-rows: repeat(3, 100px);
}
</style>

<style lang="scss" scoped>
// common css
#app{
  display: grid;
  .example{
    display: grid;
    grid-template-columns: 50% 50%;
    padding: 10px;
    border: 1px solid black;
  }
  .container{
    margin-right: 10px;
    justify-self: right;
    display: grid;
    grid-gap: 1px;
    .item{
      display: flex;
      justify-content: center;
      align-items: center;
      background: rgb(241, 47, 80);
      font-size: 25px;
      color: rgb(255, 255, 255);
    }
  }
  .code{
    justify-self: left;
    margin-left: 10px;
  }
}
</style>
