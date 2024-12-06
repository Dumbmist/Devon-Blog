---
layout: page
title: About
permalink: /about/
---

---

## Background:

I am from Pennyslvania and moved to San Diego around 3rd grade.

## What I like:

Content coming in theaters near you... JK - (Im not an artist but I tried my best)

<style>
    /* Style looks pretty compact, trace grid-container and grid-item in the code */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 25px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 300%;
        height: 300px; /* Fixed height for uniformity */
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
        max-height: 200px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is for the CSS styling, the id is for JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://imgur.com";
    var living_in_the_world = [
        {"flag": "https://i.imgur.com/mml24lr.png", "greeting": "I play tennis with this racket", "description": "Yeonix Ezone 100+"},
        {"flag": "https://i.imgur.com/DnLwOfa.png", "greeting": "I have become slightly addicted to brawl stars", "description": "Brawl Stars"},
        {"flag": "https://i.imgur.com/HzI4zBx.png", "greeting": "I read a lot of books", "description": "Reading"},
        {"flag": "https://i.imgur.com/ws3MLoX.png", "greeting": "Pasta is my favorite food - red sauce is better", "description": "Pasta"},
        {"flag": "https://i.imgur.com/lZWpg8G.png", "greeting": "Who doesn't like money - it runs our lives!", "description": "$Money$"},
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

---

## My family:

Members  |   Mom |  Dad   | Sister |Son/Me | <-- really intresting huh
Names    | Redacted | Redacted | Redacted | Devon | <-- Amount of info is crazy
Fav Color|  Red  | Yellow |  Pink  | Black |
Fav Food | All?  |Chickin |  Ramen | Pasta | <-- * My mom has no favorite
Fav Day  | Friday| Sunday |Saturday| Monday|
Origin  |  PA!  |England |   PA!  |  PA!  | <-- *PA= Pensylvania

---
# The End... for now

<script src="https://utteranc.es/client.js" repo="Dumbmist/Devon-Blog" issue-term="title" label="blogpost-comment" theme="github-light" crossorigin="anonymous" async> </script>