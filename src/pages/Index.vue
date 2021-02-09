<template>
  <q-page class="flex flex-center bg-grey-3">
    <div style="max-width: 1000px; width: 100%; height: 90vh" class="q-pa-lg">
      <div class="row q-gutter-md full-height full-width items-center justify-center">
        <q-card v-for="num in nums" :key="num.name" style="font-size: 30px; width: 20%; height: 25%" :class="{ 'text-bold': true, 'q-pa-lg': true, 'bg-red-6': num.value, 'bg-red-2': !num.value, 'text-white': true}" @click="num.value = !num.value">
          <div class="text-center absolute-center" style="font-size: 3em">{{num.label}}</div>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data() {
    return {
     nums: [
       { name: "two", label: "2", value: true },
       { name: "three", label: "3", value: true },
       { name: "four", label: "4", value: true },
       { name: "five", label: "5", value: true },
       { name: "six", label: "6", value: true },
       { name: "eight", label: "8", value: true },
       { name: "nine", label: "9", value: true },
       { name: "ten", label: "10", value: true },
       { name: "eleven", label: "11", value: true },
       { name: "twelve", label: "12", value: true },
     ]
    }
  }
}
</script>
