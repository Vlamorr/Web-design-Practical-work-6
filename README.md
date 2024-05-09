<!DOCTYPE html>
<html>
<head>
<style>

footer {
  background-color: #003333;
  padding: 100px;
  text-align: center;
  color: white;
border-radius: 8px;
}

    .slider {
        position: relative;
        width: 100%;
        max-width: 600px;
        margin: auto;
        overflow: hidden;
        font-family: Arial, sans-serif;
    }
    .slide {
        display: none;
        padding: 20px;
        text-align: center;
    }
    .active {
        display: block;
    }
    .prev, .next {
        cursor: pointer;
        position: absolute;
        top: 50%;
        width: auto;
        margin-top: -22px;
        padding: 16px;
        color: white;
        font-weight: bold;
        font-size: 18px;
        transition: 0.6s ease;
        border-radius: 0 3px 3px 0;
        user-select: none;
    }
    .next {
        right: 0;
        border-radius: 3px 0 0 3px;
    }
    .prev:hover, .next:hover {
        background-color: rgba(0,0,0,0.8);
    }
    
    mark {
            background-color: #808080;
            color: #FFFF;
            padding: 2px 5px;
            border-radius: 8px;
        }
        
</style>
</head>
<body>

<div class="slider">
    <div class="slide active">
        <h2><mark>Repaint and Reflow</mark></h2>
        <footer>
        <p><mark>**Repaint**</mark> and <mark>Reflow</mark> are two important concepts in browser rendering process. Reflow is the process of browser re-calculating the layout and position of elements on the page. Repaint is the process of browser re-drawing elements on the page..</p>
        </footer>
       
    </div>
    <div class="slide">
        <h2><mark>JavaScript and Page Performance</mark></h2>
        <footer>
        <p><mark>JavaScript</mark> can affect page load speed and performance as it may block the main thread, delaying page rendering. Optimizing JavaScript execution and minimizing file sizes can improve performance.</p>
        <footer>
    </div>
    <div class="slide">
        <h2><mark>Minification of Scripts</mark></h2>
        <footer>
        <p><mark>**Minification**</mark> is the process of removing unnecessary characters from code without changing its functionality. This results in smaller file sizes, leading to faster page load times and improved performance.This includes the removal of whitespace, comments, and semicolons, along with the use of shorter variable names and functions.</p>
        </footer>
    </div>
    <div class="slide">
        <h2><mark>JS Web Workers</mark></h2>
        <footer>
        <p><mark>Web workers</mark> are useful when you have computationally expensive work that just can't be run on the main thread without causing long tasks that make the page unresponsive.</p>
        </footer>
    </div>
    <div class="slide">
        <h2><mark>Sources</mark></h2>
        <footer>
        <p>Here are the sources used for the answers:</p>
        <ul>
            <li><mark>Repaint and Reflow:</mark> [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Glossary/Reflow)</li>
            <li><mark>JavaScript Performance:</mark> [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn/Performance/JavaScript), [Publii](https://getpublii.com/blog/javascript-speed-and-performance.html)</li>
            <li><mark>Minification:</mark> [Elementor](https://elementor.com/resources/glossary/what-is-minification/), [Cloudflare](https://www.cloudflare.com/learning/performance/why-minify-javascript-code/)</li>
            <li><mark>JS Web Workers:</mark> [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers), [W3Schools](https://www.w3schools.com/html/html5_webworkers.asp)</footer></li>
        </ul>
    </div>

    <a class="prev" onclick="changeSlide(-1)">❮</a>
    <a class="next" onclick="changeSlide(1)">❯</a>
</div>

<script>
var slideIndex = 1;
showSlides(slideIndex);

function changeSlide(n) {
  showSlides(slideIndex += n);
}

function showSlides(n) {
  var i;
  var slides = document.getElementsByClassName("slide");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
      slides[i].style.display = "none";
  }
  slides[slideIndex-1].style.display = "block";
}
</script>

</body>
</html>
