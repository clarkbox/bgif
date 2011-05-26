bacon.gif
=========

overview
--------
Inspired by the spacer.gif, bacon.gif is a little bitty javascript library for logging to http access logs, asyncronously and fast.

html
----
<a href="#" id="buynow">Buy Now</a>

javascript
----------
var track = new Tracker('http://featureblend.com/static/beacon.gif');
document.getElementById('buynow').addEventListener('mouseover', function(){
    track.log({type: 'mouseover', target: 'a', goal: 'buynow'});
});

access.log
----------
$ tail -f /var/log/access.log
XXX.XXX.XXX.XXX - - [26/May/2011:14:56:29 -0500] "GET /static/img/beacon.gif?v=32547type=mouseover&target=a&goal=buynow&_cb=1306439789042 HTTP/1.1" 200 356 "http://geobacon.com/" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.6; rv:2.0.1) Gecko/20100101 Firefox/4.0.1" "-"

