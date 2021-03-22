// List of icons to randomly choose between
var iconsList = ["icon://fa-heart", 
                 "icon://fa-music", 
                 "icon://fa-smile-o", 
                 "icon://fa-globe", 
                 "icon://fa-tree", 
                 "icon://fa-bolt", 
                 "icon://fa-moon-o",
                 "icon://fa-star"];
shapeChange();
locationChange();
colorChange();
onEvent("shapesButton", "click", function( ) {
  shapeChange();
});
onEvent("locationsButton", "click", function( ) {
  for (var i = 0; i < 20; i++) {
    setProperty("icon" + i, "x", randomNumber (5, 290));
    setProperty("icon" + i, "y", randomNumber (10, 400));
    setProperty("icon" + i, "width", randomNumber (25, 275));
    setProperty("icon" + i, "height", randomNumber (25,275));
  }
});
onEvent("colorsButton", "click", function( ) {
  colorChange();
});
function shapeChange() {
  var icons = randomNumber (0,iconsList.length - 1);
  for (var i = 0; i < 20; i++) {
    setProperty("icon" + i, "image", iconsList[icons]);
  }
}
function locationChange() {
  for (var i = 0; i < 20; i++) {
    setProperty("icon" + i, "x", randomNumber (5, 290));
    setProperty("icon" + i, "y", randomNumber (10, 400));
    setProperty("icon" + i, "width", randomNumber (25, 275));
    setProperty("icon" + i, "height", randomNumber (25,275));
  }
}
function colorChange() {
  for (var i = 0; i < 20; i++) {
    setProperty("icon" + i, "icon-color", rgb(randomNumber (0,255), randomNumber (0,255), randomNumber (0, 255), 0.5));
    setProperty("homeScreen", "background-color", rgb(randomNumber (0, 255), randomNumber (0, 255), randomNumber (0, 255), 0.5));
  }
}
