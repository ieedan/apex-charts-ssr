<script lang="ts">
    // If you import ApexCharts server returns 500 because window doesn't exist
    import ApexCharts from "apexcharts";
	import { onMount } from "svelte";

	onMount(() => {
		var options = {
			chart: {
				type: "line",
			},
			series: [
				{
					name: "sales",
					data: [30, 40, 35, 50, 49, 60, 70, 91, 125],
				},
			],
			xaxis: {
				categories: [1991, 1992, 1993, 1994, 1995, 1996, 1997, 1998, 1999],
			},
		};

		var chart = new ApexCharts(document.querySelector("#chart"), options);

		chart.render();
	});
</script>

<div id="chart"></div>
