<template>
  <div class="d-flex align-center justify-space-between w-100 mt-12 mb-4">
    <p class="text-h6 text-sm-h5 font-weight-bold">{{ title }}</p>
    <div v-if="navigation">
      <v-btn
        icon="mdi-menu-left"
        density="compact"
        variant="text"
      ></v-btn>
      <v-btn
        icon="mdi-menu-right"
        density="compact"
        variant="text"
      ></v-btn>
    </div>
    <v-btn
      v-else
      variant="text"
      slim
      density="comfortable"
      text="View All"
      class="text-none"
    ></v-btn>
  </div>
  <v-row>
    <slot></slot>
  </v-row>
</template>

<script setup lang="ts">
defineProps<{
  title: string;
  navigation?: boolean;
}>();

</script>
