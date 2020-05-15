<template>
<div>
  <p>Current Token: {{ token }}</p>
  <slot name="area" :token="token" />
</div>
</template>

<script>
const generateToken = () => {
  return `${Math.ceil(Math.random() * 1e10)}`;
};

export default {
  data() {
    return {
      token: generateToken()
    }
  },
  beforeMount() {
    this.token = generateToken();
  }
}
</script>
