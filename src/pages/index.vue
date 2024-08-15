<template>
  <GroupedMenu :entries="entries"/>
</template>

<script lang="ts" setup>
  const entries = [
  {name: "Entry 1",
  value: "Entry 1",
  subEntry: {
name: "Sub 1",
value: "Sub 1",
to: {query: {val: "queryVal"}}
  }},
  {name: "Entry 2",
  value: "Entry 2",
  subEntry: {
name: "Sub 2",
value: "Sub 2",
to: {query: {val: "queryVal"}}
  }}
  ]
</script>
