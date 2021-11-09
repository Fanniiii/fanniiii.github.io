<body>
  <center>

    <br><h1 style="font-family: Helvetica Neue, Helvetica, Arial, sans-serif; font-size: 25px; text-align:center; font-weight:bold; text-decoration:overline"> IDENTITY </h1><br>
    <h2 style="font-family: Helvetica Neue, Helvetica, Arial, sans-serif; font-size:15px; text-align:center; font-weight:lighter; word-spacing:650px"><span 

    </style>

    <div class="canvas" data-background="https://i.postimg.cc/qRJyJqm4/north2.jpg" data-foreground="https://i.postimg.cc/PJf4R2Gb/south.jpg"></div>
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
