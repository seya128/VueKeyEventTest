<template>
  <div class="keyeventtest">
    <h1 >{{ msg }}</h1>
    <div class="event">{{eventMessage}}</div>
    <input>
  </div>
</template>

<script>
export default {
  name: 'KeyEventTest',
  props: {
    msg: String,
  },
  data() {
    return {
      eventMessage: "イベントメッセージが入ります"
    }
  },
  methods: {
    eventKeydown(code) {
      this.eventMessage = `KeyDOWN keycode=${code}`;
    },
    eventKeyup(code) {
      this.eventMessage = `KeyUP keycode=${code}`;
    },
  },
  mounted() {
    window.addEventListener('keydown', (e) => {
      console.log(e.keyCode);
      this.eventKeydown(e.keyCode);
    });
    window.addEventListener('keyup', (e) => {
      console.log(e.keyCode);
      this.eventKeyup(e.keyCode);
    });

  },  

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


h1 {
  margin: 40px 0 0;
}

.event {
  margin: 40px;
}
</style>
