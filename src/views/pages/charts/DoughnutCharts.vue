<template>
  <div class="w-full justify-center">
    <header class="px-5 py-4 border-b border-slate-100 dark:border-slate-700">
      <h2 class="font-semibold text-slate-800 dark:text-slate-100">Doughnut Charts</h2>
    </header>
    <DoughnutChart :chartData="chartData" :chartOptions="chartOptions"></DoughnutChart>
  </div>
</template>

<script>
import { ref } from 'vue'
import DoughnutChart from '@/views/charts/DoughnutChart.vue'
import { generateRandomData, chartOptions } from '@/services/ChartService.js';

export default {
  name: "DoughnutCharts",
  components: {
    DoughnutChart,
  },
  setup(props, context) {
    const chartData = generateRandomData();

    return {
      chartData,
      chartOptions
    }
  }
}
</script>
