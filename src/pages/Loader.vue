<script>
export default {
    name: 'Loader'
}
</script>

<template>
  <div class="loader-container">
    <div class="loader"></div>
  </div>
</template>

<style scoped>
.loader-container {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgb(255, 255, 255);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9999;
}

.loader {
  width: 150px;
  height: 150px;
  border-left: 5px solid #38ff8e;
  border-radius: 50%;
  animation: right5231 0.9s linear infinite;
}

.loader::before,
  .loader::after {
  content: "";
  width: 120px;
  height: 120px;
  display: block;
  position: absolute;
  top: calc(50% - 60px);
  left: calc(50% - 60px);
  border-right: 5px solid #ffbe0b;
  border-radius: 50%;
  animation: left036 0.9s linear infinite;
}

.loader::after {
  width: 90px;
  height: 90px;
  top: calc(50% - 45px);
  left: calc(50% - 45px);
  border: 0;
  border-top: 5px solid #ff086e;
  animation: none;
}

@keyframes right5231 {
  from {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(360deg);
  }
}

@keyframes left036 {
  from {
    transform: rotate(720deg);
  }

  to {
    transform: rotate(0deg);
  }
}
</style>

