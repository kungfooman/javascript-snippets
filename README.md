# javascript-snippets
Simple scripts for FireBug stuff

Looping HTML5 videos (like webm, mp4):

Full loop:

	v = document.getElementsByTagName("video")[0];
	v.loop = true; //v.onpause = function() { console.log("on pause"); v.play(); }

Partial loop:

	v = document.getElementsByTagName("video")[0];
	function checkLimit() { from = 7, to = 19; if (v.currentTime > to) v.currentTime = from; }
	function start() { timer = setInterval(checkLimit, 100); }
	function stop() { clearInterval(timer); }
	start();
