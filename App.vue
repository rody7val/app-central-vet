<template>
  <view class="container">
    <text class="text-color-primary">{{ message }}</text>
    <button title="Press me!" @press="exclaim" />
    <button :title="message" @press="handleBtnPress"/>
  </view>
</template>

<script>
export default {
  data() {
    return {
      message: "Hello World"
    };
  },
  methods: {
    exclaim() {
      this.message += "!";
    },
    handleBtnPress() {
      alert(this.message);
    }
  },
};
</script>

<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}
</style>
