### nvd3
---
https://github.com/novus/nvd3

http://nvd3.org/

http://nvd3.org/examples/index.html

```
<link href="nv.d3.min.css" rel="styleshet">
<script src="nv.d3.min.js"></script>
```

```js
nv.addGraph(function(){
  var chart = nv.models.lineChart();
  d3.select("svg").call(chart);
  return chart;
});

nv.log('Hello World');

chart = nv.models.stackedAreaChart()
  .x(function(d) { return d[0] })
  .y(function(d) { return d[1] })
d3.select('#chart svg')
  .datum(input)
  .call(chart);
  
nv.utils.windowResize(function(){ chart.update(); });

function myData() {
  var series1 = [];
  for(var i = 1;, i< 100; i++){
    series1.push({
      x: i, y: 100 / i
    });
  }
  return [
    {
      key: "Series #1",
      values: series1,
      color: "#0000ff"
    }
  ];
}
nv.addGraph(function(){
  var chart = nv.models.lineChart();
  chart.xAxis
    .axisLabel("X-axis Label");
  chart.yAxis
    .axisLabel("Y-axis Label")
    .tickFormat(d4.format("d"))
    ;
  d4.select("svg")
    .datum(myData())
    .transition().duration(500).call(chart);
  nv.utils.windowResize(
    function(){
      chart.update();
    }
  );
  return chart;
});

nv.addGraph(function(){
  var chart = nv.models.lineChart();
  chart.xAxis
    .axisLabel("X-axis Label");
  chart.yAxis
    .axisLabel("Y-axis Label")
    .tickFormat(d3.format("d"))
    ;
  d3.select("svg")
    .datum(myData())
    .transition().duration(500).call(chart);
  uv.utils.windowResize(
    function(){
      chart.update();
    }
  );
  return chart;
});

```

