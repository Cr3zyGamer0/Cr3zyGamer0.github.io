
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Offical Clover Games Website </title>
    <link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@300;400;500&display=swap" rel="stylesheet">
</head>
<body>
    <style>
body {
    margin: 0;
    padding: 0;
    background-color: #111; /* Dark background for contrast */
    overflow: hidden;
    position: relative;
}

/* Shining effect overlay */
.shine-overlay {
    position: fixed;
    top: 0;
    left: -150%;
    width: 200%;
    height: 100%;
    background: linear-gradient(120deg, rgba(255, 255, 255, 0) 30%, rgba(255, 255, 255, 0.3) 50%, rgba(255, 255, 255, 0) 70%);
    pointer-events: none; /* Prevent interaction */
    opacity: 0;
    transition: opacity 0.005s ease-in-out;
}
body {
    font-family: 'Fredoka', sans-serif;
    font-weight: 300;
    margin: 0;
    padding: 0;
    background-color: white;
    overflow: hidden;
}
.value-box {
position: absolute;
bottom: 20px;
left: 50%;
transform: translateX(-50%);
background-color: rgb(255, 255, 255);
color: rgb(0, 0, 0);
padding: 10px 20px;
font-size: 1.2em;
text-align: center;
font-weight: bold;
width: auto;
}

/*
.value-box span.rainbow {
background: linear-gradient(90deg, rgb(255, 109, 109), rgb(255, 197, 89), rgb(255, 255, 94), rgb(118, 255, 118), rgb(118, 118, 255), rgb(195, 111, 255), violet);
-webkit-background-clip: text;
background-clip: text;
color: transparent;
}

.value-box span.shiny {
background: linear-gradient(90deg, #dddddd, #868686, #dddddd);
background-size: 200% auto;
background-clip: text;
color: transparent;
animation: shiny 2s infinite linear;
}
*/

/* Animation for shiny effect */
@keyframes shiny {
0% {
background-position: 200% 0;
}
100% {
background-position: -200% 0;
}
}
/* Ensuring no underline or text-decoration on .contact-btn */
.contact-btn {
background: linear-gradient(0deg, rgb(255, 170, 0), rgba(255, 221, 0, 0.87));
color: white;
padding: 10px 25px;
font-size: 1.3em;
font-weight: bold;
text-decoration: none;
border-radius: 30px;
margin-left: auto;
margin-right: 20px;
margin-top: -5px;
display: inline-block; /* Ensure it's visible */
}

@keyframes wobble {
0% { transform: rotate(0deg); }
25% { transform: rotate(-10deg); }
50% { transform: rotate(10deg); }
75% { transform: rotate(-5deg); }
100% { transform: rotate(0deg); }
}

.contact-btn:hover, 
.contact-btn:focus, 
.contact-btn:active {
text-decoration: none !important;  /* Prevent underline on hover/active */
color: white !important;  /* Keep color consistent */
animation: wobble 0.6s ease infinite;
}





nav {
    background: white;
    padding: 0px;
    position: fixed;
    width: 95%;
    top: 20px;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    align-items: center;
    justify-content: flex-start;
    z-index: 1000;
}

nav img {
    margin-left: 0px;
}

.nav-links {
    display: flex;
    gap: 10px;
    margin-left:20px;
}

nav a {
color: rgb(99, 99, 99);
text-decoration: none;
padding: 20px 20px;
font-weight: 500;
font-size: 1.25em;
position: relative;
transition: color 0.3s ease, transform 0.5s ease;
}

nav a:hover {
font-style: italic;
color: black;
transform: scale(1.05); /* Slight zoom effect */
}

/* Sliding underline effect */
nav a::after {
content: "";
position: absolute;
left: 50%;
bottom: 5px;
width: 0;
height: 3px;
background-color: black;
transition: width 0.3s ease, left 0.3s ease;
transform-origin: center;
}
.contact-btn::after {
content: none; /* Removes the sliding underline */
}

nav a:hover::after {
width: 100%;
left: 0;
}

/* Active link effect */
nav a.active {
color: black;
font-weight: 600;
text-decoration: underline;
}

body {
animation: fadeIn 3s ease-in;
user-select: none; /* Prevent text selection */
}

/* Disable image selection and dragging */
img {
user-select: none; /* Prevent image selection */
-webkit-user-drag: none; /* Prevent image drag in webkit-based browsers */
-moz-user-drag: none; /* Prevent image drag in Firefox */
}

section {


    width: 95vw;
    height: 90vh;
    margin: 5vh auto;
    display: none;
    align-items: center;
    justify-content: center;
    font-size: 1.5em;
    font-weight: normal;
    background-color: white;
}

#home, #about, #services, #contact {
    background: linear-gradient(to bottom, lightgrey, white);
}

.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 50px;
}

.text-content {
    flex: 1;
    text-align: left;
    padding: 20px;
}
@keyframes fadeIn {
from {
opacity: 0;
}
to {
opacity: 0.25;
}
to {
opacity: 0.75;
}
to {
opacity: 1;
}
}
@keyframes fadeInWithColor {
0% {
opacity: 0;
background-color: rgba(0, 0, 0, 0);
}
50% {
opacity: 1;
background-color: rgba(255, 255, 255, 0); /* Blue background */
}
100% {
opacity: 0;
visibility: hidden;
background-color: rgba(0, 0, 0, 0);
}
}

.full-screen-intro {
position: fixed;
top: 0;
left: 0;
width: 100%;
height: 100%;
display: flex;
justify-content: center;
align-items: center;
z-index: 9999;
animation: fadeInWithColor 5s ease-out forwards;
}

.welcome-message {
color: #3a3a3a;
font-size: 3.5em;
font-weight: bold;
text-transform: uppercase;
font-style: italic; /* Makes the text italic */
}

.text-content h1 {
font-size: 2.5em;
font-weight: 550;
margin: 0;
display: inline-flex;
align-items: center;
background: linear-gradient(90deg, rgb(255, 109, 109), rgb(255, 197, 89), rgb(255, 223, 94), rgb(118, 255, 118), rgb(118, 118, 255), rgb(195, 111, 255), violet);
-webkit-background-clip: text;
background-clip: text;
color: transparent; /* To make the gradient visible only on the text */
}


.pillows-text {
    margin-right: 2px;
}

.text-content p {
    font-size: 1em;
    color: #555;
    margin-top: -10px;
}

.shop-btn {
    background: linear-gradient(0deg, rgb(4, 255, 0), rgb(166, 255, 0));
    color: white;
    padding: 13.5px 27.5px;
    font-size: 1.2em;
    font-weight: bold;
    text-decoration: none;
    border-radius: 30px;
    display: inline-block;
    margin-top: -20px;
    animation: float 2s ease-in-out infinite;
    transition: background-color 0.3s ease, transform 0.3s ease;
}

.shop-btn:hover {
    font-style: italic;
    transform: scale(1.1);
}

.images {
    flex: 1;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 15px;
}

.image-container {
    position: relative;
}

.images img {
    width: 150px;
    height: 150px;
    transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.image-container:hover img {
    transform: scale(1.2) rotate(5deg); /* Zoom and slight rotation effect */
    box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.2);
}

.info {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    color: white;
    text-align: center;
    padding: 10px;
    font-size: 1em;
    display: none;
    opacity: 0;
    transition: opacity 0.3s ease-in-out;
}

.image-container:hover .info {
    display: block;
    opacity: 1;
}

.cards-container {
display: grid;
grid-template-columns: repeat(6, 1fr); /* Always 4 cards per row */
gap: 15px; /* Even spacing */
justify-content: center;
align-items: center;
width: 90%;
max-width: 1200px;
margin: 20px auto;
}
@keyframes float {
0% {
transform: translateY(0);
}
50% {
transform: translateY(-10px);
}
100% {
transform: translateY(0);
}
}

.card {
background-color: #fff;
width: 190px; /* Fixed width */
height: 230px; /* Fixed height */
display: flex;
flex-direction: column;
border-radius: 15px;
justify-content: flex-start;
align-items: center;
text-align: center;
transition: transform 0.3s ease-in-out;
}
/* Styling the footer */
.footer {
background-color: #f0f0f0;
color: rgb(0, 0, 0);
text-align: center;
padding: 10px 0;
position: fixed;
width: 95%;
bottom: 0;
display: flex;
justify-content: center;
align-items: center;
gap: 15px; /* space between copyright and button */
margin-left: 35px;
}
.YT-btn {
display: flex;
align-items: center;
background: linear-gradient(0deg, #ff0000, #ff5656);
color: white;
font-size: 1.1em;
font-weight: bold;
text-decoration: none;
padding: 7px 15px;
border-radius: 30px;
transition: background-color 0.3s ease, transform 0.2s ease;
}

.YT-btn:hover {
transform: scale(1.05);
}
.YT-icon {
width: 25px;
height: 25px;
margin-right: 0px;
}
.discord-btn {
display: flex;
align-items: center;
background: linear-gradient(0deg, #6f8eff, #92aaff);
color: white;
font-size: 1.1em;
font-weight: bold;
text-decoration: none;
padding: 7px 15px;
border-radius: 30px;
transition: background-color 0.3s ease, transform 0.2s ease;
}

.discord-btn:hover {
transform: scale(1.05);
}
.discord-icon {
width: 25px;
height: 25px;
margin-right: 0px;
}
.roblox-btn {
display: flex;
align-items: center;
background: linear-gradient(0deg, #232323, #3e3e3e);
color: white;
font-size: 1.1em;
font-weight: bold;
text-decoration: none;
padding: 7px 15px;
border-radius: 30px;
transition: background-color 0.3s ease, transform 0.2s ease;
}

.roblox-btn:hover {
transform: scale(1.05);
}
.roblox-icon {
width: 25px;
height: 25px;
margin-right: 0px;
}
.X-icon {
width: 25px;
height: 25px;
margin-right: 0px;
}
.X-btn {
display: flex;
align-items: center;
background: linear-gradient(0deg, #4090ff, #56cfff);
color: white;
font-size: 1.1em;
font-weight: bold;
text-decoration: none;
padding: 7px 15px;
border-radius: 30px;
transition: background-color 0.3s ease, transform 0.2s ease;
}

.X-btn:hover {
background-color: #007893;
transform: scale(1.05);
}
.X-icon {
width: 25px;
height: 25px;
margin-right: 0px;
}


.footer p {
margin: 0;
}

.card:hover {
    transform: perspective(1000px) rotateY(15deg);
font-style: italic;
}



#services {
padding-top: 10px;  /* Adjust the value as needed to move it down */
}

.values-container {
margin-top: 10px;  /* Add a bit of space from the top */
}

/* Adjust image inside card */
.card-image {
width: 60%; /* Keeping the same image width */
height: 100px; /* Increased image height */
object-fit: contain;
object-position: center;
margin: 5px auto; /* Center image horizontally */
display: block;
}

/* Adjust content inside card */
.card-content {
padding: 5px; /* Reduced padding to bring text closer */
text-align: center;
margin-top: -5px; /* Reduced margin for more compact layout */
}

/* Title inside card */
.card-content h3 {
font-size: 0.8em; /* Slightly bigger title font size */
font-weight: bold;
margin: 5px 0; /* Reduced margin between title and text */
}

/* Value inside card */
.card-content p {
font-size: 0.6em; /* Slightly bigger font size */
color: #333;
margin-top: 0;
margin-bottom: 3px;
}

/* Rarity inside card */
.rarity {
font-size: 0.75em; /* Slightly bigger font size for rarity */
color: #777;
margin-top: 3px;
display: block;
}

/* Page Navigation Styles */
.page-nav-container {
display: flex;
justify-content: center;
align-items: center;
gap: 20px;
margin-bottom: 20px;
}
section {
transition: opacity 0.5s ease-in-out, transform 0.5s ease-in-out;
}
.arrow-btn {
background: none;
border: none;
font-family: 'Fredoka', sans-serif;
font-size: 1.5em;
color: #555;
cursor: pointer;
width: 100px;
height: 40px;
text-align: center;
line-height: 40px;
border-radius: 30px;
transition: transform 0.3s ease
}

.info {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    background: rgb(255, 255, 255);
    color: rgb(0, 0, 0);
    padding: 10px;
    border-radius: 10px;
    z-index: 10;
    font-size: 0.7em;
    text-align: center;
    transition: opacity 0.3s ease;
}
    </style>
    <nav>
        <img src="file:///C:/Users/ynshm/OneDrive/Pictures/Screenshots/Screenshot%20(1554).png" alt="Logo" style="height: 65px;">
        <div class="nav-links">
            <a href="javascript:void(0);" onclick="showSection('home')">Home Page</a>
            <a href="javascript:void(0);" onclick="showSection('services')">Value List</a>
        </div>
        <a href="https://discord.com/channels/@me/1327313133978652795" class="contact-btn">Contact</a>
    </nav>

    <section id="home">
        <div class="container">
            <div class="text-content">
                <h1 ><span class="pillows-text"> DLC Huge Pet!</span> <span>&#x2B50;</span></h1>
                <p>Currently Sold Out!</p>
                <a href="#" class="shop-btn">Shop Later</a>
            </div>
            <div class="images">
                <div class="image-container">
                    <img src="file:///C:/Users/ynshm/Downloads/1279535762102026321.webp" alt="Pet Pillow 1">
                </div>
                <div class="image-container">
                    <img src="file:///C:/Users/ynshm/Downloads/Huge_Ice_Lucki.webp" alt="Pet Pillow 2">
                </div>
                <div class="image-container">
                    <img src="file:///C:/Users/ynshm/Downloads/1325183684529229975.webp" alt="Pet Pillow 3">
                </div>
                <div class="image-container">
                    <img src="file:///C:/Users/ynshm/Downloads/1325183686773047462%20(1).webp" alt="Pet Pillow 4">
                </div>
                <div class="image-container">
                    <img src="file:///C:/Users/ynshm/Downloads/Huge_Release_Chest%20(1).webp" alt="Pet Pillow 5">
                </div>
            </div>
        </div>
    </section>

    <section id="services">
        <div class="values-container">
            <button class="arrow-btn" id="prevPage">&#60;</button>
            <div class="cards-container" id="cardsContainer"></div>
            <button class="arrow-btn" id="nextPage">&#62;</button>
        </div>

            <!-- Add the box at the bottom here -->
    <div class="value-box">
        
    </div>
    </section>
    <!-- Inside the #services section, before the cards-container div -->

    <script>
        const pets = [
            { name: "Huge Volcano Noob", value: "200m", demand: "9/10", exist: "9",img: "file:///C:/Users/ynshm/Downloads/1279535762102026321.webp", shiny: true },
            { name: "Huge Ice Lucki", value: "250m", demand: "9/10", exist: "6",img: "file:///C:/Users/ynshm/Downloads/Huge_Ice_Lucki.webp" },
            { name: "Huge Firework", value: "55m", demand: "7/10", exist: "14",img: "file:///C:/Users/ynshm/Downloads/Huge_Firework.webp" },
            { name: "Huge Difference Ninja Cat", value: "65m", demand: "8/10", exist: "8",img: "file:///C:/Users/ynshm/Downloads/1330908907710714008.webp" },
            { name: "Huge Ice Kitsune", value: "750m", demand: "10/10", exist: "9",img: "file:///C:/Users/ynshm/Downloads/Huge_Ice_Kitsune_Fox.webp" },
            { name: "Huge Manager Dino", value: "72.5m", demand: "8/10", exist: "21", img: "file:///C:/Users/ynshm/Downloads/Huge_Manager_Dino.webp" },
            { name: "Huge Purple Fireball Monkey", value: "45m", demand: "5/10", exist: "154",img: "file:///C:/Users/ynshm/Downloads/Huge_Purple_Fireball_Monkey.webp" },
            { name: "Huge Difference Dragon", value: "42.5m", demand: "4/10", exist: "184", img: "file:///C:/Users/ynshm/Downloads/Huge_Difference_Dragon.webp" },
            { name: "Huge Difference Cat", value: "500m", demand: "10/10", exist: "0",img: "file:///C:/Users/ynshm/Downloads/Huge_Doodle_Difference_Cat.webp" },
            { name: "Huge Screech Axolotl", value: "82.5m", demand: "9/10", exist: "4",img: "file:///C:/Users/ynshm/Downloads/1322361674786930689.webp" },
            { name: "Huge Snow Globe Noob", value: "75m", demand: "8/10", exist: "27",img: "file:///C:/Users/ynshm/Downloads/Huge_Snow_Globe_Noob.webp" },
            { name: "Huge Guard Agony", value: "450m", demand: "10/10", exist: "2",img: "file:///C:/Users/ynshm/Downloads/1330908913603838045.webp" },
            { name: "Rideable Purple Fireball Noob", value: "425m", demand: "9/10", exist: "32",img: "file:///C:/Users/ynshm/Downloads/Huge_Purple_Fireball_Noob%20(1).webp" },
            { name: "Rideable Snow Globe Lucki", value: "750m", demand: "10/10", exist: "2",img: "file:///C:/Users/ynshm/Downloads/Rideable_Snow_Globe_Lucki.webp" },
            { name: "Titanic Lucy", value: "1.375b", demand: "10/10", exist: "17",img: "file:///C:/Users/ynshm/Downloads/Titanic_Lucy.webp" },
            
            
        ];
    
        let currentPage = 0;
        const petsPerPage = 12
        const cardsContainer = document.getElementById("cardsContainer");
        
        
        function renderPets() {
            cardsContainer.innerHTML = "";
            const start = currentPage * petsPerPage;
            const end = start + petsPerPage;
            const pagePets = pets.slice(start, end);
            
            pagePets.forEach(pet => {
                const card = document.createElement("div");
                card.classList.add("card");
                card.innerHTML = `
                    <img src="${pet.img}" alt="${pet.name}" class="card-image">
                    <div class="card-content">
                        <h3>${pet.name}</h3>
                        <p>Value: ${pet.value}</p>
                        <p>Demand: ${pet.demand}</p>
                        <p>Exist: ${pet.exist}</p>
                    </div>
                `;
                cardsContainer.appendChild(card);
            });
        }
    
        document.getElementById("prevPage").addEventListener("click", () => {
            if (currentPage > 0) {
                currentPage--;
                renderPets();
            }
        });
    
        document.getElementById("nextPage").addEventListener("click", () => {
            if ((currentPage + 1) * petsPerPage < pets.length) {
                currentPage++;
                renderPets();
            }
        });
    
        renderPets();
    </script>
    
    <style>
        .values-container {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 20px;
        }
    
        .arrow-btn {
    background: none;
    border: none;
    font-family: 'Fredoka', sans-serif; /* Using Fredoka font */
    font-size: 2em; /* Larger font size for arrow */
    color: #555;
    cursor: pointer;
    display: inline-flex; /* Use inline-flex for easy centering */
    align-items: center; /* Center vertically */
    justify-content: center; /* Center horizontally */
    width: 60px; /* Fixed width */
    height: 60px; /* Fixed height */
    border-radius: 50%; /* Circular shape */
    transition: transform 0.3s ease, color 0.3s ease;
}

.arrow-btn:hover {
    color: black;
    transform: scale(1.1); /* Slight zoom on hover */
}

.arrow-btn:active {
    transform: scale(1); /* Reset on click */
}




    </style>
    

    <section id="contact">Never share your Clan codes!</section>



<div class="footer">
    <a href="https://x.com/Nielzonn/status/1865517670646366402" target="_blank" class="X-btn">
        <img src="file:///C:/Users/ynshm/Downloads/twitter.c1a489e1.svg" alt="X" class="discord-icon">
        
    </a>
    <a href="https://www.youtube.com/@DemoTheNPC" target="_blank" class="YT-btn">
        <img src="file:///C:/Users/ynshm/Downloads/youtube.cd1802ae.svg" alt="X" class="YT-icon">
        
    </a>
    <p> 2025 &copy;Clover Games. All rights reserved.</p>
    <a href="https://discord.gg/mmcS8chksZ" target="_blank" class="discord-btn">
        <img src="file:///C:/Users/ynshm/Downloads/discord.763c98ce.svg" alt="Discord" class="discord-icon">
        
    </a>
    <a href="https://www.roblox.com/communities/33555312/Luckiy-Games#!/about" target="_blank" class="roblox-btn">
        <img src="file:///C:/Users/ynshm/Downloads/668ed10627b11c191c5aaf49b1a13408c0dc2c29.png" alt="Discord" class="roblox-icon">
        
    </a>
</div>
<div class="shine-overlay"></div>

    <!-- Full-screen intro with background color change -->
    <div class="full-screen-intro">
        <div class="welcome-message">
          
        </div>
    </div>
    <script>
        
        function showSection(sectionId) {
            const sections = document.querySelectorAll('section');
            sections.forEach(section => {
                section.style.display = 'none';
            });
            const selectedSection = document.getElementById(sectionId);
            selectedSection.style.display = 'flex';
        }
        window.onload = function() {
            showSection('home');
        }
   
     // Disable right-click (context menu) on the entire page
        document.addEventListener('contextmenu', function (e) {
            e.preventDefault();
        });
        
        // Disable right-click (context menu) on the entire page
document.addEventListener('contextmenu', function (e) {
    e.preventDefault();
});

// Disable `Ctrl + U` (View Source)
document.addEventListener('keydown', function (e) {
    if (e.ctrlKey && (e.key === 'u' || e.key === 'U')) {
        e.preventDefault();
    }
});

// Disable right-click (context menu)
document.addEventListener('contextmenu', function (e) {
    e.preventDefault();
});

// Disable `Ctrl + U` (View Source)
document.addEventListener('keydown', function (e) {
    // Disable Ctrl+U for view source
    if (e.ctrlKey && (e.key === 'u' || e.key === 'U')) {
        e.preventDefault();
    }
    
    // Disable `Ctrl + A` (Select All)
    if (e.ctrlKey && (e.key === 'a' || e.key === 'A')) {
        e.preventDefault();
    }
    
    // Disable `Ctrl + C` (Copy)
    if (e.ctrlKey && (e.key === 'c' || e.key === 'C')) {
        e.preventDefault();
    }
    
    // Disable `Ctrl + V` (Paste)
    if (e.ctrlKey && (e.key === 'v' || e.key === 'V')) {
        e.preventDefault();
    }
});

function showSection(sectionId) {
    const sections = document.querySelectorAll('section');
    sections.forEach(section => {
        section.style.opacity = "0";  // Set initial opacity to 0
        section.style.transform = "translateY(20px)"; // Move section slightly down
        section.style.display = 'none';
    });

    const selectedSection = document.getElementById(sectionId);
    selectedSection.style.display = 'flex';

    // Small delay before animation
    setTimeout(() => {
        selectedSection.style.opacity = "1";
        selectedSection.style.transform = "translateY(0)";
    }, 50);
}


    function triggerShine() {
        const shine = document.querySelector(".shine-overlay");
        shine.style.opacity = "1"; // Show shine
        shine.style.transition = "none"; // Reset transition
        shine.style.left = "-150%"; // Start from the left
        void shine.offsetWidth; // Force reflow
        shine.style.transition = "left 1.5s ease-out, opacity 0.5s ease-in-out"; // Smooth animation
        shine.style.left = "100%"; // Move to the right

        // Fade out after animation
        setTimeout(() => {
            shine.style.opacity = "0";
        }, 1200);
    }

    // Trigger effect every 5 seconds
    setInterval(triggerShine, 5000);

    
    </script>
        <script>
            gsap.to("h2", { opacity: 1, y: -10, duration: 1, delay: 0.5 });
            gsap.to("p", { opacity: 1, y: -10, duration: 1, delay: 1 });
            gsap.to("button", { opacity: 1, y: -10, duration: 1, delay: 1.5 });
        </script>
</body>

