<script setup lang="ts">
interface NameProps {
  name: string;
  index: number;
}
const props = defineProps<NameProps>();
const emit = defineEmits(["remove"]);
const removeName = () => {
  emit("remove", props.index);
};
</script>

<template>
  <div class="card">
    <p>{{ name }} | <span @click="removeName">close</span></p>
  </div>
</template>
