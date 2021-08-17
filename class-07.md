# Class 07 Reading Notes

### Domain Modeling
an object oriented model will store data in properties and have behaviors in methods. 
```JavaScript 
var EpicFailVideo = function(epicRating, hasAnimals) {this.epicRating = epicRating;
this.hasAnimals = hasAnimals;}

var parkourFail = new EpicFailVideo(7, false);
var corgiFail = new EpicFailVideo(4, true);

console.log(parkourFail);
console.log(corgiFail);
```
domain modeling is js attempt at proper object oriented programming. the new keyword creates new instances of an object. 
```JavaScript
var EpicFailVideo = function(epicRating, hasAnimals) {
  this.epicRating= epicRating;
  this.hasAnimals = hasAnimals;
}

EpicFailVideo.prototype.generateRandom = function(min, max) {
  return Math.floor(Math.random()*(max-min+1)) + min;
}

var parkourFail = new EpicFailVideo(7, false);
var corgiFail = new EpicFailVideo(4, true);

console.log(parkourFail.generateRandom(1,5));
console.log(corgiFail.generateRandom(1,5));

var EpicFailVideo = function(epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals;
}

EpicFailVideo.prototype.generateRandom = function(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

EpicFailVideo.prototype.dailyLikes = function() {
  var viewers, percentage;

  viewers = this.generateRandom(10, 30) * this.epicRating;

  if (this.hasAnimals) {
    percentage = 0.75;
  } else {
    percentage = 0.40;
  }

  return Math.round(viewers * percentage);
}

var parkourFail = new EpicFailVideo(7, false);
var corgiFail = new EpicFailVideo(4, true);

console.log(parkourFail.dailyLikes());
console.log(corgiFail.dailyLikes());

var EpicFailVideo = function(epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals;
}

EpicFailVideo.prototype.generateRandom = function(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

EpicFailVideo.prototype.dailyLikes = function() {
  var viewers, percentage;

  viewers = this.generateRandom(10, 30) * this.epicRating;

  if (this.hasAnimals) {
    percentage = 0.75;
  } else {
    percentage = 0.40;
  }

  return Math.round(viewers * percentage);
}

EpicFailVideo.prototype.weeklyLikes = function() {
  var total = 0;

  for (var i = 0; i < 7; i++) {
    total += this.dailyLikes();
  }

  return total;
}

var parkourFail = new EpicFailVideo(7, false);
var corgiFail = new EpicFailVideo(4, true);

console.log(parkourFail.weeklyLikes());
console.log(corgiFail.weeklyLikes());
```

### HTML Ch 6 (126-145)
this chapter is on tables and how to create and edit them. a table is a grid shaped representation of information. there are three important tags when it comes to making tables. the table tag, tr tag, and td tag. table tag creates the table, the tr tag starts each row and a td tag to end each row. the th tag is used to control the heading of the columns. tables can be edited in many ways to included the spanning of mulitple cells. if you have particularly long tables you can us thead, tbody, and tfoot to divide the table up. 

### JS Ch 3 (106-144)
this chapter covers functions, methods, and objects and how they can all work together. specifically objects in this half of the chapter. objects can be created one by one or you could creat a function to make the process easier. you use the new keyword to creat new instances of an object. objects can have methods that are basically like functions and execute specific code when called. objects use dot notation which is the way that you access the variables of the object. this is a specific keyword that is used to describe which ever element you are currently in. it basically lets you make a function genearic so that you can plug in whatever name you want for that specific object and be describing it without putting in each individual part.  there are three built in groups of objects in js, browser object, document object, and global javascript objects. the most notable of these built in object that we use are the string, math, number, and date objects. 