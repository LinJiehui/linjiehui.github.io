# linjiehui.github.io
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="initial-scale=1, maximum-scale=1, user-scalable=no">
<title>Intro to SceneView - Create a 3D map</title>
<style>
  html, body, #viewDiv {
    padding: 0;
    margin: 0;
    height: 100%;
    width: 100%;
  }
</style>
<link rel="stylesheet" href="https://js.arcgis.com/4.9/esri/css/main.css">
<script src="https://js.arcgis.com/4.9/"></script>
<script>
require([
  "esri/Map",
  "esri/views/SceneView"
], function(Map, SceneView){
  var map = new Map({
    basemap: "streets",
    ground: "world-elevation"
  });
  var view = new SceneView({
    container: "viewDiv",     // Reference to the scene div created in step 5 引用在步骤5中创建的场景div
    map: map,                 // Reference to the map object created before the scene 引用场景之前创建的地图对象
    scale: 35000000,          // Sets the initial scale to 1:50,000,000 将初始比例设置为1：50,000,000
    center: [104.095352,35.295413]  // Sets the center point of view with lon/lat  30.295413° 114.095352°将初始比例设置为1：50,000,000
  });
});
</script>
</head>
<body>
  <div id="viewDiv"></div>
</body>
</html>
