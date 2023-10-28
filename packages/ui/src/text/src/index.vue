<template>
  <p>{{ config.text + a }}</p>
</template>

<script lang="ts" setup>
import { ref } from 'vue';

import { MComponent } from '@tmagic/schema';

import useApp from '../../useApp';

const props = withDefaults(
  defineProps<{
    config: MComponent;
    model?: any;
  }>(),
  {
    model: () => ({}),
  },
);
const a = ref('dfa');
useApp({
  config: props.config,
  methods: {},
});
</script>
