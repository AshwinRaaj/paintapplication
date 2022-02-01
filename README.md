# Web Page for Paint Application

## AIM:

To design a static website for Paint Application using HTML5 canvas.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML,CSS and canvas.

### Step 3:

Write javascript to capture move events.

### Step 4:

Perform the drawing operation based on the user input.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
~~~
[9:11 pm, 24/01/2022] Shriram Sec: <!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">

  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Volume Calculator</title>
</head>

<body>

  <div class="formelement">
    <h1><small>Volume Calculator For Cylinder And Cone</small></h1>
  </div>
  <div class="container">
    <div class="content">
      <h1>Volume Of Cylinder</h1>
      <form>
        <div class=formelement>
          <lable for="aedit">Height:</lable>
          <input id="aedit" placeholder="" />
          <label><small>
              Meters
            </small></label>
        </div><br>
        <div class=formelement>
          <lable for="bedit">Radius:</lable>
          <input id="bedit" placeholder="" />
          <label><small>
              Meters
            </small></label>
        </div><br>
        <div class=formelement>
          <lable for="cedit">Volume:</lable>
          <input type="number" min="0" value="0" step="any" id="cedit" placeholder="0" readonly="0" /><label><small>
              Meters³</small></label>
        </div><br><br>
        <div class=formelement>
          <input type="button" class="button" value="CALCULATE" id="calbutton1" />
          <input type="Reset" class="button" value="RESET">
        </div>
        <center>
          <p id="stats1"></p>
        </center>
        <br>
        <div class=formula>
          Formula is
          Volume V = π X Radius² X Height
        </div><br>
      </form>
    </div>

    <div class="content2">
      <h1>Volume of Cone</h1>
      <form>
        <div class="formelement">
          <lable for="radiusedit">Radius:</lable>
          <input id="radiusedit" placeholder="" />
          <label><small>
              Meters
            </small></label>
        </div><br>
        <div class="formelement">
          <lable for="heightedit">Height:</lable>
          <input id="heightedit" placeholder="" />
          <label><small>
              Meters
            </small></label>
        </div><br>
        <div class="formelement">
          <lable for="volumeedit">Volume:</lable>
          <input type="number" min="0" value="0" name="avol" step="any" id="volumeedit" placeholder="0"
            readonly="0" /><label><small> Meters³</small></label>
        </div><br><br>
        <div class="formelement">
          <input type="button" class="button" value="CALCULATE" id="calbutton2" />
          <input type="Reset" class="button" value="RESET">
        </div><br>
        <center>
          <p id="stats2"></p>
        </center>
        <div class="formula">
          Formula is:
          Volume V = π X Radius² X Height / 3
        </div>

        <br>
      </form>

    </div>
  </div>
  <div class="fbox">
    <div class="footer">
      <center>
        <p><br>
          © 2022
          <a><u> Website for Mathematical Calculations in Client Side.</u></a>  Developed By Ashwin Raaj 
        </p>
      </center>
    </div>
  </div>
</body>
<script type="text/javascript">
  var button;
  button = document.querySelector("#calbutton1");
  button.addEventListener("click", function () {
    var atext, btext, ctext;
    var aval, bval, cval;
    let text1
    atext = document.querySelector("#aedit");
    btext = document.querySelector("#bedit");
    ctext = document.querySelector("#cedit");

    if (Number(atext.value) && Number(btext.value)) {
      aval = parseInt(atext.value);
      bval = parseInt(btext.value);
      text1 = "The Answer Is Generated Successfully!!!";

    }
    else {
      window.alert("The Number You Entered Is `Invalid Format` / `Empty` Try Using Values Containing Postitive Integers. Click Reset And Try Again!!!");
      text1 = "Error or Invalid Format!!!";
    }

    cval = 3.14 * aval * aval * bval;
    ctext.value = "" + cval;

    document.getElementById("stats1").innerHTML = text1;

  });
</script>
<script type="text/javascript">
  var button;
  button = document.querySelector("#calbutton2");
  button.addEventListener("click", function () {

    var radiustext, heighttext, volumetext;
    var aval, bval, cval;
    var text2
    radiustext = document.querySelector("#radiusedit");
    heighttext = document.querySelector("#heightedit");
    volumetext = document.querySelector("#volumeedit");

    if (Number(radiustext.value) && Number(heighttext.value)) {
      aval = parseInt(radiustext.value);
      bval = parseInt(heighttext.value);
      text2 = "The Answer Is Generated Successfully!!!";
    }
    else {
      window.alert("The Number You Entered Is `Invalid Format` / `Empty` Try Using Values Containing Postitive Integers. Click Reset And Try Again!!!");
      text2 = "Error or Invalid Format!!!";
    }

    cval = 3.14 * aval * aval * bval / 3;
    volumetext.value = "" + cval;

    document.getElementById("stats2").innerHTML = text2;

  });

</script>

<style>

  /Background Region/

  body {
    background-color: #ff4e00;
    background-image: linear-gradient(315deg, #ff4e00 0%, #ec9f05 74%);
    background-image: url(https://papers.co/wallpaper/papers.co-ml15-sunset-lake-night-blue-dark-nature-25-wallpaper.jpg);
    background-repeat: no-repeat;
    background-attachment: fixed;
    position: sticky;
    background-size: cover;
  }

  .container {
    grid-gap: 50px;
    width: 1080px;
    margin-left: auto;
    margin-right: auto;
  }

  /Box Region/

  .content {
    display: block;
    width: 100%;
    background-color: white;
    opacity: 60%;
    min-height: 500px;
    margin-top: 50px;
    margin-bottom: 50px;
    box-shadow: inset 0 0 15px black;
    backdrop-filter: blur(9px);
    border-radius: 10px;
    border: 1px solid whitesmoke;
  }

  .content2 {
    display: block;
    width: 100%;
    background-color: white;
    opacity: 60%;
    min-height: 500px;
    margin-top: 50px;
    margin-bottom: 50px;
    box-shadow: inset 0 0 15px black;
    backdrop-filter: blur(9px);
    border-radius: 10px;
    border: 1px solid whitesmoke;
  }

  .fbox {
    display: block;
    width: 100%;
    background-color: whitesmoke;
    opacity: 60%;
    min-height: 100px;
    margin-top: 0px;
    margin-bottom: 0px;
    box-shadow: inset 0 0 15px black;
    backdrop-filter: blur(9px);
    border-radius: 10px;
    border: 1px solid whitesmoke;
  }

  .button {
    background-color: orangered;
    border: 2px solid grey;
    border-radius: 25px;
    color: white;
    padding: 15px 32px;
    text-align: center;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
  }

  /Text Region/
  * {
    box-sizing: border-box;
    font-family: Century Gothic, sans-serif;
  }

  h1 {
    text-align: center;
    padding-top: 50px;
    color:#F73A73 ;
  }

  .formelement {
    text-align: center;
    font-size: x-large;
    margin-top: 5px;
    margin-bottom: 5px;

  }

  .formula {
    text-align: center;
    font-size: large;
    margin-top: 5px;
    margin-bottom: 5px;
  }

  .footer p {
    margin: 0;
    line-height: 26px;
    font-size: 15px;
    color: #990099;
  }

  .footer p a {
    background: linear-gradient(to right, #f27121, #e94057, #8a2387);
    color: transparent;
    -webkit-background-clip: text;
    background-clip: text;
    text-decoration: none;
  }

  /Scroll Bar Configuration/

  ::-webkit-scrollbar {
    width: 10px;
  }

  ::-webkit-scrollbar-track {
    width: 5px;
    background: grey;
    box-shadow: inset 0 0 5px grey;
    border-radius: 10px;
  }

  ::-webkit-scrollbar-thumb {
    background: #d86939;
    border-radius: 3px;
  }

  ::-webkit-scrollbar-thumb:hover {
    background: orangered;
  }
</style>

</html>
[9:12 pm, 24/01/2022] Shriram Sec: ex 04 da ithu
[10:40 pm, 24/01/2022] Shriram Sec: <!DOCTYPE html>
<html>
<body id="Jaeger">
    <div id="light">
<canvas id="myCanvas" width="800" height="800" onclick="showCoords(event)"></canvas></div>
<center>
<button onclick="shape=1" id="Eren" >Solid Circle</button>
<button onclick="shape=2" id="Eren">circle</button>
<button onclick="shape=3" id="Eren">Solid Square</button>
<button onclick="shape=4" id="Eren">Square</button>
<button onclick="shape=5" id="Eren">Solid Triangle</button>
<button onclick="shape=6" id="Eren">Triangle</button>
<br>
<button onclick="size()" id="Eren" >Change size</button></center>
<center>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(54, 0, 124);"></button>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(0, 0, 0);"></button>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(153, 0, 255);"></button>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(46, 112, 255);"></button>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(94, 255, 45);"></button>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(7, 184, 1);"></button>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(49, 231, 255);"></button>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(252, 255, 60);"></button>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(213, 76, 255);"></button>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(255, 115, 1);"></button>
<button onclick="change_color(this)" id="Yagami" style="background: white;"></button>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(255, 72, 72);"></button>
</center>

<script>


const canvas = document.getElementById("myCanvas");
const ctx = canvas.getContext("2d");
ctx.fillStyle = "#FF0000";
canvas.height = canvas.width;
ctx.transform(1, 0, 0, -1, 0, canvas.height);
let xMax = canvas.height;
let yMax = canvas.width;
let csize= 20;
let sqsize= 50;
let tsize=30;
let tatakae="black";
function size()
{   
if (shape==1 ||shape==2){
    let c= prompt("Please enter size of circle", "ex:100,50");
    csize=c;
} 
if (shape==3 ||shape==4){
    let s = prompt("Please enter size of square", "ex:100,20");
    sqsize=s;
}
if (shape==5 || shape==6){
    let t= prompt("Please enter size of square","ex:50,84");
    tsize=t;
}
}
function change_color(element){
    tatakae=element.style.background;
}

    function showCoords(event)

    {
    var x = event.clientX-545;
    var y = yMax-event.clientY;
    var coords = "X coords: " + x + ", Y coords: " + y;
    document.getElementById("demo").innerHTML = coords;
    
        if (shape==1){
            ctx.beginPath();
            ctx.arc(x, y, csize, 0, 2 * Math.PI);
            ctx.fillStyle=tatakae;
            ctx.fill();
        }
        if (shape==2){
            ctx.beginPath();
            ctx.arc(x, y, csize, 0, 2 * Math.PI);
            ctx.strokeStyle=tatakae;
            ctx.stroke();
        }
        if (shape==3){
            ctx.beginPath();
            ctx.rect(x-(sqsize/2),y-(sqsize/2), sqsize,sqsize);
            ctx.fillStyle=tatakae;
            ctx.fill();
        }
        if (shape==4){
            ctx.beginPath();
            ctx.rect(x-(sqsize/2),y-(sqsize/2), sqsize,sqsize);
            ctx.strokeStyle=tatakae;
            ctx.stroke();
        }
        if (shape==6){
            ctx.beginPath();
            ctx.moveTo(x, y);
            ctx.lineTo(x-(tsize/2),y-(tsize*0.86602));
            ctx.lineTo(x+(tsize/2),y-(tsize*0.86602));
            ctx.lineTo(x,y)
            ctx.strokeStyle=tatakae
            ctx.stroke();
        }
        if (shape==5){
            ctx.beginPath();
            ctx.moveTo(x, y);
            ctx.lineTo(x-(tsize/2),y-(tsize*0.86602));
            ctx.lineTo(x+(tsize/2),y-(tsize*0.86602));
            ctx.fillStyle=tatakae
            ctx.fill();
        }
    
    
    }

</script>
<center><p id="demo" style="color: white;"></p></center>
<p style="color: white; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;" >Developed By Ashwin Raaj S</p>
<style>

#light{
    padding-left: 545px;
   
}
#myCanvas{
    background-color: #ffffff86; 
    box-shadow: inset 0 0 5px #b6b6b6;
    backdrop-filter: blur(15px);
    border-radius: 10px;
    border: 1px solid #ffffff;
}
#Eren{
    background-color: #cf95ffc2;
    border: 2px solid rgb(255, 255, 255);
    border-radius: 25px;
    color: white;
    padding: 15px 32px;
    text-align: center;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
}
#Eren:hover{
    background-color:#ffffff36;
    transition: 0.5s;
}
#Jaeger{
    background-image: url(https://wallpaperaccess.com/full/107891.jpg);
}
#Yagami{
    border: 2px solid #ffffff;
    border-radius: 25px;
    padding: 25px 25px;
    text-align: center;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
}
#Yagami:hover{
    opacity: 20%;
    transition: 0.21s;
}
</style>
</body>
</html>
~~~

## OUTPUT:
### Drawn Page:
![output](1.png)

### Size Change Page:
![output](3.png)

### Normal Page:
![output](2.png)
## Result:

Thus a website is designed and validated for paint application using HTML5 canvas.
