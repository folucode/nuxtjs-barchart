<template>
    <div>
        <canvas id="bar-chart"></canvas>
    </div>
</template>

<script>
import { Chart, registerables } from 'chart.js';
import barChartData from "../data/chart-data";
barChartData

export default {
    name: "BarChart",
    data() {
        return {
            barChartData
        }
    },
    mounted() {
        const ctx = document.getElementById("bar-chart");
        Chart.register(...registerables);
        new Chart(ctx, this.barChartData);
    }
};
</script>