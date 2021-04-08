<div id="card">
	<div id="blur">
		<div id="color"></div>
	</div>
	<div id="profile">
		<img src="https://i.imgur.com/NUwBvdM.jpg" alt="Anshuman" />
		<h1>Anshuman</h1>
		<p>Front-end Web Developer and UI developer</p>
		<div class="info">
			<i class="fa fa-info fa-1x block"></i>
			<i class="fa fa-angle-down fa-2x block"></i>
			<p>UI, App and Web Developer.</p>
			<p>Find me on:</p>
			<a class="link" href="https://www.youtube.com/channel/UCg8LEBkJZsSdkLC1vGyNqVg" target="_blank"><i class="fa fa-youtube fa-2x social"></i></a>
			<a class="link" href="https://github.com/anshuman2166AppproDev" target="_blank"><i class="fa fa-github fa-2x social"></i></a>
			<a class="link" href="https://codepen.io/anshuman2166appprodev" target="_blank"><i class="fa fa-codepen fa-2x social"></i></a>
		</div>
	</div>
</div>
<style>
	body {
	background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/225748/MD_background.png) no-repeat center center fixed;
	background-size: cover;
	overflow: hidden;
	cursor: default;
}

#card {
	width: 400px;
	height: 300px;
	position: relative;
	margin: 10% auto;
	border-radius: 8px;
	box-shadow: 0px 2px 6px rgba(0, 0, 0, 0.2), 0px 2px 6px rgba(0, 0, 0, 0.4);
	overflow: hidden;
}

#blur {
	background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/225748/MD_background.png) no-repeat center center fixed;
	background-size: cover;
	width: 430px;
	height: 330px;
	position: relative;
	top: -15px;
	left: -15px;
	border-radius: 8px;
	-webkit-filter: blur(8px);
	-moz-filter: blur(8px);
	filter: blur(8px);
}

#color {
	background: rgba(255, 255, 255, .60);
	width: 430px;
	height: 330px;
}

#profile {
	cursor: grab;
	width: 400px;
	height: 300px;
	position: relative;
	top: -330px;
	border-radius: 8px;
}

img {
	width: 100px;
	height: 100px;
	border-radius: 100px;
	position: relative;
	top: 32px;
	display: block;
	margin: 0 auto;
	-webkit-filter: sepia(.25);
	-moz-filter: sepia(.25);
	filter: sepia(.25);
}

h1 {
	color: rgba(38, 50, 56, 1);
	font-family: 'Roboto Condensed', sans-serif;
	font-size: 36px;
	font-weight: 700;
	text-align: center;
	position: relative;
	top: 48px;
}

p {
	color: rgba(38, 50, 56, .87);
	font-family: 'Roboto Condensed', sans-serif;
	font-size: 16px;
	font-weight: 400;
	text-align: center;
	position: relative;
	top: 56px;
}

a {
	color: rgba(255, 255, 255, 1);
	transition: color 0.4s;
	text-decoration: none;
}
a:hover {
	color: rgba(255, 255, 255, .70);
	transition: color 0.4s; 
}

.info {
	text-align: center;
	margin: 0 auto;
	position: relative;
	top: 86px;
	background: rgba(38, 50, 56, 1);
	width: 32px;
	height: 32px;
	border-radius: 100px;
	background-position: center center;
	background-size: cover;
	transition: all 0.2s ease;
	z-index: 0;
}

.info.active {
	width: 100%;
	height: 200%;
	position: relative;
	top: -100%;
	background: rgba(38, 50, 56, 1);
	transition: width .1s ease, height .2s ease, top .2s ease, z-index .2s ease;
	z-index: 999;
}

.info i.block {
	color: rgba(255, 255, 255, .6);
	display: block;
}

.info .fa-info {
	padding: 8px;
	cursor: pointer;
	visibility: visible;
 opacity: 1;
	transition: visibility 0s, opacity 0.4s ease;
}

.info.active .fa-info {
	visibility: hidden;
 opacity: 0;
 transition: visibility 0s, opacity 0.4s ease;
}

.info .fa-angle-down {
	cursor: pointer;
	visibility: hidden;
}

.info.active .fa-angle-down {
	position: relative;
	margin: 0 auto;
	width: 24px;
	height: 24px;
	padding: 4px;
	visibility: visible;
	position: relative;
	top: 128px;
	animation-name: visible;
	animation-duration: 0.3s;
}

@keyframes visible {
	0% {
		opacity: 0;
	}
	100% {
		opacity: 1;
	}
}

.info p {
	color: rgba(255, 255, 255, 1);
	font-family: 'Roboto Condensed', sans-serif;
	font-size: 18px;
	line-height: 110%;
	font-weight: 400;
	text-align: center;
	padding: 24px;
	position: relative;
	top: 144px;
	visibility: hidden;
}

.info.active p {
	visibility: visible;
	animation-name: entrance-first;
	animation-duration: 0.4s;
}

.info .link {
	visibility: hidden;
	margin: 24px 24px 0px 24px;
	padding: 16px 4px 4px 4px;
	cursor: pointer;
	position: relative;
	top: 144px;
}

.info.active .link {
	visibility: visible;
	animation-name: entrance-second;
	animation-duration: 0.5s;
}

@keyframes entrance-first {
	0% {
		top: 200px;
	}
	100% {
		top: 144px;
	}
}

@keyframes entrance-second {
	0% {
		top: 200px;
	}
	100% {
		top: 144px;
	}
}
</style>
<script>
	$(function() {
	$("#card").draggable();
	$(".block").on("click", function() {
		$(".info").toggleClass("active");
	});
});
</script>
