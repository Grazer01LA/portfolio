---
layout: post
title: About
permalink: /about/
comments: true
---

## As a conversation Starter

<comment>
Flags are made using Wikipedia images
</comment>

<style>
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px;
        object-fit: contain;
    }
    .grid-item p {
        margin: 5px 0;
    }
    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
    }
    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    var container = document.getElementById("grid_container");
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", "greeting": "Hey", "description": "California"},
        {"flag": "a/a4/Flag_of_the_United_States.svg", "greeting": "Hello", "description": "USA"},
        {"flag": "4/41/Flag_of_India.svg", "greeting": "Namaste", "description": "India"},
    ];

    for (const location of living_in_the_world) {
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";
        var img = document.createElement("img");
        img.src = http_source + location.flag;
        img.alt = location.flag + " Flag";

        var description = document.createElement("p");
        description.textContent = location.description;

        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;

        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);
        container.appendChild(gridItem);
    }
</script>

### About Ishan Khandelwal

I am Ishan Khandelwal, a San Diego student who enjoys learning, staying active, and having fun.

### Education

- Elementary and middle school at Design 39 Campus in San Diego
- High school at Del Norte High School in San Diego

While taking AP CSP, I hope to learn and improve my coding skills.
I know a little bit of Python but my coding knowledge is relatively small

### San Diego

I have lived in both 4S Ranch and Black Mountain Ranch.
I like the beach, the San Diego Zoo and Safari Park, and Sea World.

### Languages

I speak English and Hindi.

### Interests

I love to ski and I've been to 6 different resorts and skied 29 days. I have skied many double blacks, with my hardest ski run being Think Again at Banff Sunshine Village. My favorite ski resort is Lake Louise.
I also play video games and tennis.
I enjoy watching F1 and soccer.
I love the travel based game show Jet Lag: The Game.
I love to travel, and have been to 19 countries and 16 states. Some of my favorite destinations are Norway, Austria, Switzerland, and Yukon.
I used to love rubiks cubing, and could solve it in an average of 15 seconds.
I also like to play video games, and currently mostly play geometry dash, brawl stars, F1, and FIFA. I used to play many other games like minecraft and among us.
I play piano and my favorite food is Mexican and Thai food.
My favorite dessert is snow cones. 
I am very knowledgeable about PC hardware.

### Family and Fun

Family and experiences are very important to me. I enjoy spending time with loved ones, traveling, and pursuing my passions.

<comment>
Gallery of Pics
</comment>
<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/screenshot_at_7_75_seconds.png" alt="Ishan skiing">
  <img src="{{site.baseurl}}/images/about/20230705_084248.jpg" alt="Ishan traveling">
  <img src="{{site.baseurl}}/images/about/hot_air_balloon.jpg" alt="Ishan family hot air balloon">
  <img src="{{site.baseurl}}/images/about/hallstatt.jpg.png" alt="Ishan Hallstatt">
  <img src="{{site.baseurl}}/images/about/familysnow.jpg.png" alt="Ishan family snow">
</div>