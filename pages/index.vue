<template>
<div>
  <h1>Welcome to our party.</h1>
  <sample-component>
    <template v-slot:area="{ token }">
      <p :data-token="token">Current token (in slot): {{ token }}</p>
    </template>
  </sample-component>
  <button @click="reload">Reload</button>
</div>
</template>

<script>
import SampleComponent from '../components/SampleComponent.vue';

export default {
  components: {
    SampleComponent
  },
  methods: {
    reload: () => {
      location.reload();
    }
  }
}
</script>
