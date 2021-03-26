# 3d-paper-fold-text-effect
.....html......
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>repl.it</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
  </head>
  <body>
    <script src="script.js"></script>
    <div class="wrapper">
	<h1 contenteditable data-heading="Summer">Summer</h1>
</div>
  </body>
</html>
......css.......
html, body {
  height: 100%;
}

body {
  background: linear-gradient(45deg, #00ffff 50%, #7fffd4 40%);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.wrapper {
  width: 50%;
  font-family: "Source Code Pro", monospace;
  margin: 0 auto;
  height: 200%;
}
.wrapper h1 {
  text-transform: uppercase;
  transform: translate(-50%, -50%) skew(10deg) rotate(-10deg);
  font-size: 20vw;
  top: 50%;
  left: 50%;
  margin: 0;
  position: absolute;
  text-rendering: optimizeLegibility;
  font-weight: 900;
  color: rgba(0, 10, 8, 0.925);
  text-shadow: 1px 4px 6px #ff24de, 0 0 0 #66303a, 1px 4px 6px #636160;
  white-space: nowrap;
}
.wrapper h1:before {
  content: attr(data-heading);
  position: absolute;
  left: 0;
  top: -4.8%;
  overflow: hidden;
  width: 100%;
  height: 50%;
  color: #c77b40;
  transform: translate(1.6vw, 0) skew(-13deg) scale(1, 1.2);
  z-index: 2;
  text-shadow: 2px -1px 6px rgba(0, 0, 0, 0.2);
}
.wrapper h1:after {
  content: attr(data-heading);
  position: absolute;
  left: 0;
  top: 0;
  overflow: hidden;
  width: 100%;
  height: 100%;
  z-index: 1;
  color: #d3cfcc;
  transform: translate(0vw, 0) skew(13deg) scale(1, 0.8);
  -webkit-clip-path: polygon(0 50%, 100% 50%, 100% 100%, 0% 100%);
          clip-path: polygon(0 50%, 100% 50%, 100% 100%, 0% 100%);
  text-shadow: 2px -1px 6px rgba(0, 0, 0, 0.3);
}
