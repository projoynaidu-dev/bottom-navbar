<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <link rel="import" href="https://fonts.googleapis.com/icon?family=Material+Icons">
  <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto:300,400,500,700,400italic">
  <link rel="stylesheet" href="style.css">
  <style>
    *{
    font-family: 'Roboto', sans-serif;
}

body{
    margin: 0;
    /* width: 50%; */
    padding: 0; 
    /* display: flex;
    justify-content: center;
    align-items: center; */
}
img{
    vertical-align: middle;
}
.container{
    width: 70%;
    position: relative;

}
.mySlides{
    display: none;
}
.curser{
    cursor: pointer;
}

.prev, .next{
    cursor: pointer;
    position: absolute;
    top: 40%;
    width: auto;
    padding: 16px;
    margin-top: -50px;
    color: white;
    font-weight: bold;
    font-size: 20px;
    border-radius: 0 3px 3px 0;
    user-select: none;
    -webkit-user-select: none;
    transition:  0.6s ease;
}
.next{
    right: 0;
    border-radius: 3px 0 0 3px;
}
.prev:hover, .next:hover{
    background-color: rgba(0,0,0,0.8);
}
.numbertext{
    color: white;
    padding: 8px 12px;
    position: absolute;
    top: 0;
}
.caption-container{
    text-align: center;
    background-color: black;
    color: white;
    padding: 2px 16px;
}
.row:after{
    content: "";
    display: table;
    clear: both;
}

.column{
    float: left;
    width: 16.66%;
    cursor: pointer;
}
.demo{
    opacity: 0.6;

}
.active, .demo:hover{
    opacity: 1;
}



  </style>

</head>
<body>
  <h2 style="text-align: center;"> Slideshow Gallery</h2>
  <div class="container">

    <div class="mySlides">
      <div class="numbertext">1 / 6</div>
      <img src="https://www.w3schools.com/howto/img_woods_wide.jpg" style="width:100%">
    </div>
    <div class="mySlides">
      <div class="numbertext">1 / 5</div>
      <img src="https://www.w3schools.com/howto/img_5terre_wide.jpg" style="width:100%">
    </div>
    <div class="mySlides">
      <div class="numbertext">1 / 4</div>
      <img src="https://www.w3schools.com/howto/img_mountains_wide.jpg" style="width:100%">
    </div>
    <div class="mySlides">
      <div class="numbertext">1 / 3</div>
      <img src="https://www.w3schools.com/howto/img_lights_wide.jpg" style="width:100%">
    </div>
    <div class="mySlides">
      <div class="numbertext">1 / 2</div>
      <img src="https://www.w3schools.com/howto/img_nature_wide.jpg" style="width:100%">
    </div>
    <div class="mySlides">
      <div class="numbertext">1 / 1</div>
      <img src="https://www.w3schools.com/howto/img_snow_wide.jpg" style="width:100%">
    </div>

    <a class="prev" onclick="plusSlides(-1)">❮</a>
    <a class="next" onclick="plusSlides(1)">❯</a>

    <div class="caption-container">
      <p id="caption"></p>
    </div>

    <div class="row">
      <div class="column">
        <img class="demo cursor" src="https://www.w3schools.com/howto/img_woods_wide.jpg" style="width:100%" onclick="currentSlide(1)" alt="Woods">
      </div>
      <div class="column">
        <img class="demo cursor" src="https://www.w3schools.com/howto/img_lights_wide.jpg" style="width:100%" onclick="currentSlide(1)" alt="Woods">
      </div>
      <div class="column">
        <img class="demo cursor" src="https://www.w3schools.com/howto/img_woods_wide.jpg" style="width:100%" onclick="currentSlide(1)" alt="Woods">
      </div>
      <div class="column">
        <img class="demo cursor" src="https://www.w3schools.com/howto/img_woods_wide.jpg" style="width:100%" onclick="currentSlide(1)" alt="Woods">
      </div>
      <div class="column">
        <img class="demo cursor" src="https://www.w3schools.com/howto/img_woods_wide.jpg" style="width:100%" onclick="currentSlide(1)" alt="Woods">
      </div>
      <div class="column">
        <img class="demo cursor" src="https://www.w3schools.com/howto/img_woods_wide.jpg" style="width:100%" onclick="currentSlide(1)" alt="Woods">
      </div>
  </div>
  <script >

    let slideIndex = 1;
showSlides(slideIndex);

function plusSlides(n) {
  showSlides(slideIndex += n);
}

function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  let i;
  let slides = document.getElementsByClassName("mySlides");
  let dots = document.getElementsByClassName("demo");
  let captionText = document.getElementById("caption");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";
  }
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";
  dots[slideIndex-1].className += " active";
  captionText.innerHTML = dots[slideIndex-1].alt;
}
  </script>
  
</body>
</html>
