# fanniiii.github.io
<!DOCTYPE html>
<html>

<head>
  <link rel="icon" type="image/png" href="https://i.postimg.cc/Jhy8tc3m/kr.png">
  <meta http-equiv="content-type" content="text/html; charset=UTF-8">
  <title>IDENTITY</title>
  <meta http-equiv="content-type" content="text/html; charset=UTF-8">
  <meta name="robots" content="noindex, nofollow">
  <meta name="googlebot" content="noindex, nofollow">
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <style>
    .NORTH,
    .SOUTH {
      position: relative;
    }

    img {
      position: absolute;
      top: 20;
      left: -62%;
      display: none;
      width: 120px;
      height: 80px;
      border: 1px;
    }



    .NORTH:hover>img,
    .SOUTH:hover>img {
      display: block;
    }
  </style>
  <script src="/scripts/snippet-javascript-console.min.js?v=1"></script>

  <script type="text/javascript" src="//code.jquery.com/jquery-1.8.3.js"></script>

  <link rel="stylesheet" type="text/css" href="/css/result-light.css">

  <style id="compiled-css" type="text/css">
    .canvas {
      width: 1200px;
      height: 800px;
    }

    .cell {
      float: left;
      position: relative;
      cursor: pointer;
    }

    .cell>.front {
      -webkit-backface-visibility: hidden;
      backface-visibility: hidden;
      -webkit-transform-style: preserve-3d;
      transition: all 1s;
    }

    .cell:not(.flipped)>.back {
      -webkit-transform: rotateY(180deg);
    }

    .cell.flipped>.front {
      -webkit-transform: rotateY(180deg);
    }

    .cell>.back {
      position: absolute;
      text-align: center;
      font-size: 30px;
      left: 0;
      top: 0;
      transition: all 1s;
    }

    .cell>.back:before {
      content: '';
      display: inline-block;
      height: 100%;
      vertical-align: middle;
    }

    .cell>* {
      border: 0.1px dotted lightgrey;
      box-sizing: content-box;
      width: 100%;
      height: 100%;
    }

    /* EOS */
  </style>

  <script id="insert"></script>

  <!-- switch-->

  <style>
    body {

      background-color: white;
      color: black;

    }

    .dark-mode {
      background-color: black;
      color: white;
    }
  </style>
</head>

<!-- switch-->

<body>
  <center>

    <br><h1 style="font-family: Helvetica Neue, Helvetica, Arial, sans-serif; font-size: 25px; text-align:center; font-weight:bold; text-decoration:overline"> UNIFICATION </h1><br>
    <h2 style="font-family: Helvetica Neue, Helvetica, Arial, sans-serif; font-size:15px; text-align:center; font-weight:lighter; word-spacing:650px"><span class="NORTH">NORTH<img src="https://i.postimg.cc/5NP2WxWT/northk2.gif" alt="Relevant textual alternative to the image" … /></span> <mark>KOREA</mark> <span class="SOUTH">SOUTH<img src="https://i.postimg.cc/hjV6Pwqd/southkr2.gif" alt="Relevant textual alternative to the image" … /></span></h2><br>

    <style>
      mark {
        background-color: white;
        color: black;
      }
    </style>

    <div class="canvas" data-background="file:///Users/fannizhao/Desktop/demo%20copy-01.jpg" data-foreground="file:///Users/fannizhao/Desktop/demo%20copy-02.jpg"></div>
  </center>

  <!-- switch-->
  <br>
  <style>
    .button {
      border: none;
      width: 21px;
      height: 21px;
      padding: 1px 1px;
      display: inline-block;
      margin: 1px 1px;
      transition-duration: 0.4s;
      cursor: pointer;
      border-style: none;
      border: none;
      outline: none;
      position: absolute;
      top: 0;
      right: 0;
    }

    .button1 {
      background-color: black;
      color: black;
      border: 1px dotted lightgrey;
      outline: none;
    }

    .button1:hover {
      background-color: white;
      color: white;
      border: 1px dotted lightgrey;
      outline: none;
    }
  </style>

  <button onclick="myFunction()" class="button button1"> </button>

  <script>
    function myFunction() {
      var element = document.body;
      element.classList.toggle("dark-mode");
    }
  </script>

</body>

<!-- switch-->

<script type="text/javascript">
  //<![CDATA[
  //get the canvas
  var canvas = $('div.canvas');
  var backgroundImage = canvas.data('background');
  var foregroundImage = canvas.data('foreground');
  var col = 20;
  var row = 14;
  var colWidth = canvas.width() / col;
  var rowHeight = canvas.height() / row;
  for (var i = 0; i < row; i++) {
    for (var j = 0; j < col; j++) {
      var cell = $("<div class='cell flipped'><div class='back'></div><div class='front'></div></div>")
        .width(colWidth).height(rowHeight).appendTo(canvas);
      cell.find('.front')
        .css('background', 'url(' + backgroundImage + ')')
        .css('background-position', -(j * colWidth) + 'px ' + -(i * rowHeight) + 'px');
      cell.find('.back')
        .css('background', 'url(' + foregroundImage + ')')
        .css('background-position', -(j * colWidth) + 'px ' + -(i * rowHeight) + 'px');
      cell.click(function() {
        $(this).toggleClass('flipped');
        var flipped = canvas.find('.flipped').length;
        if ((flipped == col * row) || !flipped) {
          alert('Full Image');
        }
      });
      if (Math.random() >= 0.5) cell.toggleClass('flipped');
    }
  }
  //]]>
</script>

<script>
  if (window.parent && window.parent.parent) {
    window.parent.parent.postMessage(["resultsFrame", {
      height: document.body.getBoundingClientRect().height,
      slug: "LdR29"
    }], "*")
  }
  window.name = "result"
</script>

</html>
