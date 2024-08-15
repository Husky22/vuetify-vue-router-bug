<template>
  <v-btn>
    Click Me
    <v-menu activator="parent">
      <v-list>
        <v-list-group v-for="(entry, _idx) in props.entries">
          <template #activator="{ props }">
            <v-list-item v-bind="props" :title="entry.name"></v-list-item>
          </template>
          <v-list-item :to="entry.subEntry.to">{{
            entry.subEntry.name
          }}</v-list-item>
        </v-list-group>
      </v-list>
    </v-menu>
  </v-btn>
</template>

<script setup lang="ts">
import { RouteLocationRaw } from "vue-router";

type Entry = {
  name: string;
  value: string;
  subEntry: {
    name: string;
    value: string;
    to: RouteLocationRaw;
  };
};

const props = defineProps<{ entries: Entry[] }>();
</script>

