<h1 align="center">Hi 👋, I'm Rico Cooder</h1>
<h3 align="center">A passionate problem solver</h3>

<p align="left"> <img src="https://komarev.com/ghpvc/?username=ricocooder&label=Profile%20views&color=0e75b6&style=flat" alt="ricocooder" /> </p>

<!-- <p align="left"> <a href="https://github.com/ryo-ma/github-profile-trophy"><img src="https://github-profile-trophy.vercel.app/?username=ricocooder" alt="ricocooder" /></a> </p> -->

<p align="left"> <a href="https://twitter.com/" target="blank"><img src="https://img.shields.io/twitter/follow/?logo=twitter&style=for-the-badge" alt="" /></a> </p>

- 🔭 I’m currently working on ***this README :)***

- 🌱 I’m currently learning **Flutter, Python**

- 👯 I’m looking to collaborate on **ambitious projects**

<h3 align="left">Connect with me:</h3>
<p align="left">
</p>

<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://developer.android.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/android/android-original-wordmark.svg" alt="android" width="40" height="40"/> </a> <a href="https://www.arduino.cc/" target="_blank" rel="noreferrer"> <img src="https://cdn.worldvectorlogo.com/logos/arduino-1.svg" alt="arduino" width="40" height="40"/> </a> <a href="https://dart.dev" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/dartlang/dartlang-icon.svg" alt="dart" width="40" height="40"/> </a> <a href="https://firebase.google.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/firebase/firebase-icon.svg" alt="firebase" width="40" height="40"/> </a> <a href="https://flask.palletsprojects.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/pocoo_flask/pocoo_flask-icon.svg" alt="flask" width="40" height="40"/> </a> <a href="https://flutter.dev" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/flutterio/flutterio-icon.svg" alt="flutter" width="40" height="40"/> </a> <a href="https://kotlinlang.org" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/kotlinlang/kotlinlang-icon.svg" alt="kotlin" width="40" height="40"/> </a> <a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://www.sqlite.org/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/sqlite/sqlite-icon.svg" alt="sqlite" width="40" height="40"/> </a> <a href="https://www.tensorflow.org" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" alt="tensorflow" width="40" height="40"/> </a> </p>

<p><img align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=ricocooder&show_icons=true&locale=en&layout=compact" alt="ricocooder" /></p>

<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=ricocooder&show_icons=true&locale=en" alt="ricocooder" /></p>

<p><img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=ricocooder&" alt="ricocooder" /></p>


<div id="crawl-container" class="stretch">
  <div id="crawl"> <!-- our plane in 3d -->
    <div id="crawl-content">
      <h1>Episode IV</h1>
      <h2>A NEW HOPE</h2>
      <p>It is a period of civil war. 
      ...
    </div>
  </div>
</div>

const crawl = document.getElementById("crawl");
const crawlContent = document.getElementById("crawl-content");
const crawlContentStyle = crawlContent.style;

// start crawl at bottom of 3d plane
let crawlPos = crawl.clientHeight;

const moveCrawl = distance => {
  crawlPos -= distance;
  crawlContentStyle.top = crawlPos + "px";
  
  // if we've scrolled all content past the top edge
  // of the plane, reposition content at bottom of plane
  if (crawlPos < -crawlContent.clientHeight) {
    crawlPos = crawl.clientHeight;
  }
};

let prevTime;
const init = time => {
  prevTime = time;
  requestAnimationFrame(tick);
};

const tick = time => {
  let elapsed = time - prevTime;
  prevTime = time;
  
  // time-scale of crawl, increase factor to go faster
  moveCrawl(elapsed * 0.04);
  requestAnimationFrame(tick);
};

requestAnimationFrame(init);
