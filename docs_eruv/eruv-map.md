<html>
<head>
    <title>Fair Lawn Eruv is currently {{ site.data.eruv_status.status }}</title>
    <link href="styles.css" rel="stylesheet" media="all">
    <link rel="icon" type="image/png" href="favicon.png">
    <link href="https://fonts.googleapis.com/css?family=Oswald|Open+Sans&display=swap" rel="stylesheet">
    <script type="text/javascript">
      window.location.replace("https://www.fairlawneruv.com");
    </script>
</head>


<body class="status{{ site.data.eruv_status.status | upcase }}">
        <div class="main">
                <div class="eruv {{ site.data.eruv_status.status }}">
                        <h2>Fair Lawn Eruv</h2>
                        <h3>The Eruv Is:</h3>
                        <h1>{{ site.data.eruv_status.status }}</h1>
                        <div class="details">{{ site.data.eruv_status.details }}</div>
                        <div class="date">The last inspection was completed on: <strong>{{ site.data.eruv_status.date }}</strong></div>
                </div>
                <button onclick="document.getElementById('map_container').style.display = (document.getElementById('map_container').style.display == 'none' ? 'block' : 'none')">View Eruv Map</button>
                <div id="map_container" style="display: none">
                        <iframe src="https://www.google.com/maps/d/embed?mid=1iF-7pT11IJHL9EPtOWFo0aYljwk&ll=40.941927244286354%2C-74.11637324999998&z=13" width="640" height="480"></iframe>
                </div>
        </div>
        <footer>
                <div class="shuls">
                        <p>The Fair Lawn Eruv is maintained as a community service by the following synagogues. For more information on a particular synagogue or to arrange a visit to the community, please click on the synagogue’s name below.</p>
                        <ul>
                                {% for shul in site.data.shuls %}
                                        <li><a href="{{ shul.url }}" target="_blank">{{ shul.name }}</a></li>
                                {% endfor %}
                        </ul>
                </div>
                <div class="info">
                        <p>The Fair Lawn Eruv is inspected every Friday.</p>
                        <p>Fair Lawn Eruv Hotline: <a href="tel:‪201-429-7066‬">‪201-429-7066</a></p>
                        <p>Other eruv questions?<br />Email the <a href="mailto:info@fairlawneruv.org">Eruv Inspector</a> or call <a href="tel:201-757-8365">201-757-8365</a></p>
                </div>
                <div class="subscribe">
                        <p><a href="https://groups.io/g/fairlawneruv/join">Subscribe to the Weekly Eruv Update</a></p>
                        <p class="copyright">&copy; {{ 'now' | date: "%Y" }} Fair lawn eruv. All rights reserved.</p>
                </div>
        </footer>
</body>
</html> 
