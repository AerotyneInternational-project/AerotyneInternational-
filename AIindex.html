<!DOCTYPE html>
<html>
<head>
    <title>Natural Gas Price Chart</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/moment"></script>
    <script src="https://cdn.jsdelivr.net/npm/chartjs-adapter-moment"></script>
    <style>
        .chart-container {
            width: 80%;
            margin: 0 auto;
        }
    </style>
</head>
<body>
    <div class="chart-container">
        <h1>Natural Gas Price Chart</h1>
        <canvas id="priceChart"></canvas>
    </div>

    <script>
        // Your JavaScript code will go here
        async function fetchNaturalGasData() {
            const apiKey = 'JRTtd54Ar23G1YyCF2CFADaqOQJPvFmMts4Dt7bH'; // Replace with your actual API key
            const endpoint = 'https://api.eia.gov/v2/natural-gas/pri/fut/data/?frequency=daily&data[0]=value&facets[series][]=RNGWHHD&sort[0][column]=period&sort[0][direction]=desc&offset=0&length=5000';
            
            try {
                const response = await fetch(`${endpoint}&api_key=${apiKey}`);
                const data = await response.json();
                return data;
            } catch (error) {
                console.error('Error fetching data:', error);
                return null;
            }
        }

        function processData(apiData) {
            if (!apiData || !apiData.response || !apiData.response.data) return [];
            
            return apiData.response.data.map(item => ({
                x: new Date(item.period),
                y: item.value
            })).reverse(); // Reverse to show oldest first
        }

        async function createChart() {
            const rawData = await fetchNaturalGasData();
            const chartData = processData(rawData);
            
            const ctx = document.getElementById('priceChart').getContext('2d');
            const chart = new Chart(ctx, {
                type: 'line',
                data: {
                    datasets: [{
                        label: 'Henry Hub Natural Gas Spot Price (Dollars per Million Btu)',
                        data: chartData,
                        borderColor: 'rgb(75, 192, 192)',
                        tension: 0.1,
                        fill: false
                    }]
                },
                options: {
                    responsive: true,
                    scales: {
                        x: {
                            type: 'time',
                            time: {
                                unit: 'month'
                            }
                        },
                        y: {
                            title: {
                                display: true,
                                text: 'Price (Dollars per Million Btu)'
                            }
                        }
                    },
                    plugins: {
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `$${context.parsed.y.toFixed(2)}`;
                                }
                            }
                        }
                    }
                }
            });
        }

        createChart();
    </script>
</body>
</html>
