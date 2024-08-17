body {
      font-family: 'Arial', sans-serif;
      background-color: #000000;
      color: #FFFFFF ;
    }
h1 {
  color: #58a6ff;
}
div{
  border: 2px solid white ;
  padding-left: 20px;
  margin-bottom: 5px ;
}
/* Attribute Selector */
a {
  color: #8B949E
  text-decoration: none;
}

a:hover {
  color: #1F6FEB;
}

/*Child Selector */
ul > li {
  font-weight: bold;
}
/*Sibling Selector */
h1 + p{
  background-color: #1F6FEB;
  padding: 10px;
  border-radius: 5px;
}
/* :hover Pseudo-class */
ul li:hover {
  color: #4FACC9
}
/* nth-child Pseudo-class 
ul li:nth-child(3) {
  background-color : #21262D;
}

/* :not(selector) Pseudo-class */
p:not(:first-of-type) {
         text-decoration: underline;
}
/* ::before Pseudo-element */
ul li::before {
     content:  "🚀";
}
/* ::after Pseudo-element */
a::after {
   content: "🔗";
}
/* ::first-letter Pseudo-element */
p::first-letter {
  font-size: 200%;
  color: #FF7B72
}
<!DOCTYPE html>
<html>

<head>
 <link href="style.css" rel="stylesheet" type="text/css" />
</head>

<body>
<h1>Welcome to the Space Explorer Club! </h1>
<ul>
<li>Moon Mission</li>
<li>Mars Rovers</li>
<li>International Space Station</li>
<li>Telescopes and Stars</li>
<li>Black Holes Mysteries</li>
</ul>

<div>
<p>
          Space exploration has always 
          captivated human imagination.
          It is a journey to the unknown.</p>

<p>
          From the moon to distant galaxies,
          we continue to  explore the vastness
          of space.</p>
</div>
<a href="#">Join our mission</a>
<a href="#">Latest Space news</a>
<a href="https://unsplash.com/s/photos/universe">gallery of the universe</a>
<!-- Code injected by live-server -->
<script>
	// <![CDATA[  <-- For SVG support
	if ('WebSocket' in window) {
		(function () {
			function refreshCSS() {
				var sheets = [].slice.call(document.getElementsByTagName("link"));
				var head = document.getElementsByTagName("head")[0];
				for (var i = 0; i < sheets.length; ++i) {
					var elem = sheets[i];
					var parent = elem.parentElement || head;
					parent.removeChild(elem);
					var rel = elem.rel;
					if (elem.href && typeof rel != "string" || rel.length == 0 || rel.toLowerCase() == "stylesheet") {
						var url = elem.href.replace(/(&|\?)_cacheOverride=\d+/, '');
						elem.href = url + (url.indexOf('?') >= 0 ? '&' : '?') + '_cacheOverride=' + (new Date().valueOf());
					}
					parent.appendChild(elem);
				}
			}
			var protocol = window.location.protocol === 'http:' ? 'ws://' : 'wss://';
			var address = protocol + window.location.host + window.location.pathname + '/ws';
			var socket = new WebSocket(address);
			socket.onmessage = function (msg) {
				if (msg.data == 'reload') window.location.reload();
				else if (msg.data == 'refreshcss') refreshCSS();
			};
			if (sessionStorage && !sessionStorage.getItem('IsThisFirstTime_Log_From_LiveServer')) {
				console.log('Live reload enabled.');
				sessionStorage.setItem('IsThisFirstTime_Log_From_LiveServer', true);
			}
		})();
	}
	else {
		console.error('Upgrade your browser. This Browser is NOT supported WebSocket for Live-Reloading.');
	}
	// ]]>
</script>
</body>

</html>
