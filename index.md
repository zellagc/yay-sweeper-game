<!DOCTYPE html>

<style>

.left {grid-area:left;}
.middle {grid-area:middle;}
.right {grid-area:right;}

.grid-container {
	display: grid;
	grid-template-areas: 'left middle right';
}

.left {
	grid-area:left;
	text-align: left;
	font-size: 20px;
	overflow: hidden;
	margin-left: 50px;
	margin-top: 150px;
	width: 400px;
}

.middle {
	grid-area: middle;
	overflow:hidden;
	width: 500px;
}

.right {
	grid-area:right;
	width: 400px;
}

.grid {
	display:grid;
	grid-template-columns:  auto auto auto auto auto auto auto auto auto auto;
	grid-column-gap: 0px;
	grid-row-gap: 0px;
	justify-content: center;
}

.grid > div {
	border: 1px solid black;
	height: 40px;
	width: 40px;
}

.boom {
	background-color: lightgray;
}

.nextToBoom {
	background-color: lightgray;
}

.unclicked {
	background-color: lightgray;
}

.clicked {
	background-color: gray;
}

.nextToBoomClicked {
	background-color: orange;
}

.boomClicked {
	background-color: blue;
}

.start {
	position: relative;
	left: 50%;
	transform: translate(-50%);
	margin-bottom: 25px;
	margin-top: 25px;
	text-decoration: none;
	text-align: center;
	width: 120px;
	height: 60px;
	font-size: 16px;
	font-weight: bold;
	text-transform: capitalize;
	color: white;
	border: 5px solid orange;
	box-shadow: 2px 2px lightgray;
	background-color: blue;
}

.start:active {
	box-shadow: 0px 0px;
}

.restart {
	position: relative;
	margin: 0;
	left: 50%;
	margin-top: 50px;
	transform: translate(-50%, -50%);
	text-decoration: none;
	text-align: center;
	width: 120px;
	height: 60px;
	font-size: 16px;
	font-weight: bold;
	text-transform: capitalize;
	color: white;
	border: 5px solid blue;
	box-shadow: 2px 2px lightgray;
	background-color: orange;
}

.restart:active {
	box-shadow: 0px 0px;
}

@media only screen and (max-width:620px) {
	/* For mobile phones: */
	.grid > div {
		height: 8.75vw;
		width: 8.75vw;
	}
	.grid-container {
		grid-template-areas:
		'left'
		'middle'
		'right';
		justify-content: center;
	}
	.middle {
		width: 100%;
		padding: 0px;
		margin: 0px;
	}
	.left {
		margin-top: 10px;
		text-align: center;
		margin-left: 0px;
		width: 100%;
	}
}

</style>


<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0"> 
<title>Yay Sweeper</title>
</head>

<body>
<h1 style="text-align:center;">YAY SWEEPER</h1>
<h3 style="text-align:center;font-style:italic;">Not exactly the same as Minesweeper</h3>
<p style="text-align:center;">Rules: This grid contains five blue <b style="color:blue">BOOM</b>s with an orange <b style="color:orange">YAY</b> on each face. Find <b style="color:orange">YAY</b>s to get points, and don't click a <b style="color:blue">BOOM</b>, or it's GAME OVER! Find all the <b style="color:orange">YAY</b>s as fast as you can to win!</p>
<div class="grid-container">

	<div class="left">
		<p><b>YAYS FOUND: </b><span id="score">0</span> OUT OF <span id="q">0</span></p>
		<p><b>TIME: </b><span id="stopwatch">0</span></p>
	</div>
	
	<div class="middle">
		<button id="start" class="start"><span id="startButton">Start Game</span></button>

		<div class="game">
			<div class="grid"> <!--5 x 5 for now-->
				<!--row 1-->
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<!--row 2-->
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<!--row 3-->
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<!--row 4-->
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<!--row 5-->
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<!--row 6-->
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<!--row 7-->
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<!--row 8-->
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<!--row 9-->
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<!--row 10-->
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>	
			</div>
		</div>

		<button class="restart" onclick="startOver()">Start Over</button>
	</div>
	
	<div class="right"></div>

</div>

<script>

//each "div" on the grid is a square
const square = document.querySelectorAll('.grid > div')

var a = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99];

//display a score (right now, basing it on how many "next to booms" clicked, which increases it, and how many "booms" clicked, which should kill you instantly and save your score)
var score = 0;
var remaining;
var newHours = "00";
var newMinutes = "00";
var newSeconds = "00";
var n = newHours + ":" + newMinutes + ":" + newSeconds;

document.getElementById("score").innerHTML = score;	
document.getElementById("stopwatch").innerHTML = n;	

randomNumbers = [],
i = a.length,
j = 0;


//orders all numbers in a randomly into randomNumbers. the (i-g) is necessary to avoid getting a blank value each time you splice to remove the "used" number
//add something so j cannot = j+1, j-1, j+10, j-10
for (let g = 0; g < 5; g++) {
	j = Math.floor(Math.random() * (i-(g*5)));
	randomNumbers.push(a[j]);
	a.splice(j+10,1);
	a.splice(j+1,1);
	a.splice(j,1);
	a.splice(j-1,1);
	a.splice(j-10,1);
}

//set all squares to "unclicked" class
for (let i = 0; i < 100; i++) {
	square[i].classList.add('unclicked');
}

//timer (not very nice right now)
document.getElementById('start').onclick = function() {
	makeBooms();
	document.getElementById("startButton").innerHTML = "pause";
	document.getElementById('start').onclick = function() {
		alert("PAUSED. RESUME?");
	}
	var myVar = setInterval(timer, 100)
	var g = new Date();
	var h = g.getTime();
	
	function padNumbers(hours, minutes, seconds) {
			return (hours < 10 ? '0' : '') + hours;
			return (minutes < 10 ? '0' : '') + minutes;
			return (seconds < 10 ? '0' : '') + seconds;
		}
	
	function timer() {
		//get hours, minutes, seconds
		var d = new Date();
		var g = d.getTime() - h;
		var hours = Math.floor((g/1000)/3600);
		var time = (g/1000) - (hours * 3600)
		var minutes = Math.floor(time/60);
		var seconds = Math.round(time - (minutes * 60));
		
		//format each number as 01, 02...10, 11, etc.
		newHours = ("0" + hours).slice(-2);
		newMinutes = ("0" + minutes).slice(-2);
		newSeconds = ("0" + seconds).slice(-2);
		
		n = newHours + ":" + newMinutes + ":" + newSeconds;
		document.getElementById("stopwatch").innerHTML = n;
	}
}

function makeBooms() {	
	//set all squares to "clicked" class on click
	for (let i = 0; i < 100; i++) {
		square[i].onclick = function() {
			square[i].classList.remove('unclicked');
			square[i].classList.add('clicked');
		}
	}
		
	//assign "nextToBoom" class to squares next to boom squares UNLESS this will lead to a "wrap-around" situation
	for (let g = 0; g < 5; g++) {
		if (randomNumbers[g]%10 <= 8) {
			square[randomNumbers[g]+1].classList.remove('unclicked');
			square[randomNumbers[g]+1].classList.add('nextToBoom');
			square[randomNumbers[g]+1].onclick = function() {
				square[randomNumbers[g]+1].classList.remove('nextToBoom');
				square[randomNumbers[g]+1].classList.add('nextToBoomClicked');
				remaining = document.getElementsByClassName("nextToBoom").length;
				document.getElementById("score").innerHTML = q - remaining;
				if (remaining == 0) {
					square[randomNumbers[g]+1].classList.remove('nextToBoom');
					square[randomNumbers[g]+1].classList.add('nextToBoomClicked');
					score = q - remaining;
					alert("YOU WIN! YOU FOUND ALL " + score + " YAY(S) IN " + n + ". GREAT JOB!");
					startOver();
				}
			}
		}
		if (randomNumbers[g]%10 >= 1) {
			square[randomNumbers[g]-1].classList.remove('unclicked');
			square[randomNumbers[g]-1].classList.add('nextToBoom');
			square[randomNumbers[g]-1].onclick = function() {
				document.getElementById("score").innerHTML = q - remaining;
				square[randomNumbers[g]-1].classList.remove('nextToBoom');
				square[randomNumbers[g]-1].classList.add('nextToBoomClicked');
				remaining = document.getElementsByClassName("nextToBoom").length;
				document.getElementById("score").innerHTML = q - remaining;
				if (remaining == 0) {
					square[randomNumbers[g]+1].classList.remove('nextToBoom');
					square[randomNumbers[g]+1].classList.add('nextToBoomClicked');
					score = q - remaining;
					alert("YOU WIN! YOU FOUND ALL " + score + " YAY(S) IN " + n + ". GREAT JOB!");
					startOver();
				}
			}
		}
		if (randomNumbers[g] <= 89) {
			square[randomNumbers[g]+10].classList.remove('unclicked');
			square[randomNumbers[g]+10].classList.add('nextToBoom');
			square[randomNumbers[g]+10].onclick = function() {
				document.getElementById("score").innerHTML = q - remaining;
				square[randomNumbers[g]+10].classList.remove('nextToBoom');
				square[randomNumbers[g]+10].classList.add('nextToBoomClicked');
				remaining = document.getElementsByClassName("nextToBoom").length;
				document.getElementById("score").innerHTML = q - remaining;
				if (remaining == 0) {
					square[randomNumbers[g]+1].classList.remove('nextToBoom');
					square[randomNumbers[g]+1].classList.add('nextToBoomClicked');
					score = q - remaining;
					alert("YOU WIN! YOU FOUND ALL " + score + " YAY(S) IN " + n + ". GREAT JOB!");
					startOver();
				}
			}
		}
		if (randomNumbers[g] >= 10) {
			square[randomNumbers[g]-10].classList.remove('unclicked');
			square[randomNumbers[g]-10].classList.add('nextToBoom');
			square[randomNumbers[g]-10].onclick = function() {
				document.getElementById("score").innerHTML = q - remaining;
				square[randomNumbers[g]-10].classList.remove('nextToBoom');
				square[randomNumbers[g]-10].classList.add('nextToBoomClicked');
				remaining = document.getElementsByClassName("nextToBoom").length;
				document.getElementById("score").innerHTML = q - remaining;
				if (remaining == 0) {
					square[randomNumbers[g]+1].classList.remove('nextToBoom');
					square[randomNumbers[g]+1].classList.add('nextToBoomClicked');
					score = q - remaining;
					alert("YOU WIN! YOU FOUND ALL " + score + " YAY(S) IN " + n + ". GREAT JOB!");
					startOver();
				}
			}
		}
	}
	
	//assign "boom" class to boom squares (and remove "nextToBoom" class if it exists)
	for (let g = 0; g < 5; g++) {
		square[randomNumbers[g]].classList.remove('unclicked');
		square[randomNumbers[g]].classList.remove('nextToBoom');
		square[randomNumbers[g]].classList.add('boom');
		square[randomNumbers[g]].onclick = function() {
			square[randomNumbers[g]].classList.remove('boom');
			square[randomNumbers[g]].classList.add('boomClicked');
			score = q - remaining;
			alert("YOU LOSE! YOU FOUND " + score + " YAY(S) IN " + n + ". BETTER LUCK NEXT TIME!");
			startOver();
		}
	}
	
	//display the number of unclicked "yay" tiles
	var remaining = document.getElementsByClassName("nextToBoom").length;
	
	//display the total number of "yay" tiles
	var q = document.getElementsByClassName("nextToBoom").length + document.getElementsByClassName("nextToBoomClicked").length;	
	document.getElementById("q").innerHTML = q;	
}

function startOver() {
	window.location.reload();
}

</script>
</body>