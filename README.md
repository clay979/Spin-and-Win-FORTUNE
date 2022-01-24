# Spin-and-Win-FORTUNE
# Full HTML just copy and paste in index.html file
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- <link rel="stylesheet" href="spin.css"> -->
    <style>
            *{
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  outline: none;
}
body{
  font-family: Open Sans;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  overflow: hidden;
  background: #F44336 ;
  background-size: cover;
}
.mainbox{
  position: relative;
  width: 500px;
  height: 500px;
}
.mainbox:before{
  position: absolute;
  content: '';
  width: 32px;
  height: 32px;
  background: url('https://learndesigntutorial.com/wp-content/uploads/2021/03/arrow-left.png') no-repeat;
  background-size: 32px;
  right: -30px;
  top: 50%;
  transform: translateY(-50%);
}
.box{
  width: 100%;
  height: 100%;
  position: relative;
  border-radius: 50%;
  border: 10px solid #333;
  overflow: hidden;
  transition: all ease 5s;
}
span{
  width: 50%;
  height: 50%;
  display: inline-block;
  position: absolute;
}

.span1{
  clip-path: polygon(0 92%, 100% 50%, 0 8%);
  top: 120px;
  left: 0;
  background-color: #ffeb3b;
}
.span2{
  clip-path: polygon(100% 92%, 0 50%, 100% 8%);
  top: 120px;
  right: 0;
  background-color: #e91e63;
}
.span3{
  clip-path: polygon(50% 0%, 8% 100%, 92% 100%);
  bottom: 0;
  left: 120px;
  background-color: #4caf50;
}
.span4{
  clip-path: polygon(50% 100%, 92% 0, 8% 0);
  top: 0;
  left: 120px;
  background-color: #3f51b5;
}

/*EXTRAS*/
.box1 .span3 b{
  transform: translate(-50%, -50%) rotate(-270deg);
}
.box1 .span1 b,
.box2 .span1 b{
  transform: translate(-50%, -50%) rotate(185deg);
}
.box2 .span3 b{
  transform: translate(-50%, -50%) rotate(90deg);
}
.box1 .span4 b,
.box2 .span4 b{
  transform: translate(-50%, -50%) rotate(-85deg);
}


.box2{
  width: 100%;
  height: 100%;
  transform: rotate(-135deg);
}
span b{
  width: 65px;
  height: 65px;
  line-height: 65px;
  border-radius: 50%;
  font-size: 26px;
  text-align: center;
  background-color: white;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  box-shadow: inset 0 3px 3px 0 #717171;
}
.spin{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 75px;
  height: 75px;
  border-radius: 50%;
  border: 4px solid #fff;
  background-color: #FF5722;
  color: #fff;
  box-shadow: 0 5px 20px #000;
  font-weight: bold;
  font-size: 22px;
  cursor: pointer;
}
.spin:active{
  width: 70px;
  height: 70px;
  font-size: 20px;
}
.mainbox.animate:before{
  animation: animateArrow 0.7s ease infinite; 
}
@keyframes animateArrow{
  50%{
    right: -40px;
  }
}
    </style>
    <title>Document</title>
</head>
<body>
    </html><div id="mainbox" class="mainbox">
        <div id="box" class="box">
            <div class="box1">
                <span class="span1"><b>1rs</b></span>
                <span class="span2"><b>1.2rs</b></span>
                <span class="span3"><b>0.5rs</b></span>
                <span class="span4"><b>3rs</b></span>
            </div>
            <div class="box2">
                <span class="span1"><b>0.2rs</b></span>
                <span class="span2"><b>1.1rs</b></span>
                <span class="span3"><b>0.15rs</b></span>
                <span class="span4"><b>2.5rs</b></span>
            </div>
        </div>
        <button class="spin" onclick="myfunction()">SPIN</button>
    </div>
    <script> function myfunction() {
        var x = 1024;
        var y = 9999;
        var deg = Math.floor(Math.random() * (x - y)) + y; 
        document.getElementById('box').style.transform = "rotate("+deg+"deg)";
    
        var element = document.getElementById('mainbox');
        element.classList.remove('animate');
        setTimeout(function(){
            element.classList.add('animate');
            var valueList = ["10","20","50","100","150","200","400","500",];
            var getValue = valueList[Math.floor(Math.random() * valueList.length)];
            // alert(getValue); 
        }, 5000);
    } </script>
</body>
