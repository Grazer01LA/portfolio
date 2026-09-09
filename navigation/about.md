---
---
layout: about
title: About
permalink: /about/
comments: true
---

## As a conversation Starter

Here are some places I have lived.

<comment>
Flags are made using Wikipedia images
</comment>

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
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

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", "greeting": "Hey", "description": "California - forever"},
        {"flag": "b/b9/Flag_of_Oregon.svg", "greeting": "Hi", "description": "Oregon - 9 years"},
        {"flag": "b/be/Flag_of_England.svg", "greeting": "Alright mate", "description": "England - 2 years"},
        {"flag": "e/ef/Flag_of_Hawaii.svg", "greeting": "Aloha", "description": "Hawaii - 2 years"},
    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
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
Gallery of Pics, scroll to the right for more ...
</comment>
<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/screenshot_at_7_75_seconds.png" alt="Ishan skiing">
  <img src="{{site.baseurl}}/images/about/20230705_084248.jpg" alt="Ishan traveling">
</div>