# Ex.08 Design of Interactive Image Gallery
## Date:16/12/2024

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
gallery.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Photo Gallery</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            background-color: grey;
            color: #fff;
        }

        h1 {
            font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
            text-align: center;
            color: #000000;
        }

        h2 {
            font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
            text-align: center;
            color: #000000;
        }


        .gallery {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            max-width: 850px;
            padding: 20px;
            justify-content: center;
        }

        .gallery-item {
            cursor: pointer;
            text-align: center;
            width: 200px;
            margin: 10px;
            border: 2px solid #252b2b;
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s;
        }

        .gallery-item img {
            width: 100%;
            height: 190px;
            object-fit: cover;
        }

        .gallery-item:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 16px rgba(64, 175, 244, 0.3);
        }

        
        #modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(41, 39, 39, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        #modal img {
            max-width: 90%;
            max-height: 90%;
            border: 2px solid #2b828c;
        }
        #footer {
            font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
            color: black;
            text-align: center;
        }

        #modal .close {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 30px;
            color: #ffffff;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>Interactive Photo Gallery</h1>
    <h2>WILDLIFE PICTURES</h2>

    <div class="gallery">
        <div class="gallery-item"><img src="1.jpg" alt=""></div>
        <div class="gallery-item"><img src="2.avif" alt=""></div>
        <div class="gallery-item"><img src="3.webp" alt=""></div>
        <div class="gallery-item"><img src="4.jpeg" alt=""></div>
        <div class="gallery-item"><img src="5.jpg" alt=""></div>
        <div class="gallery-item"><img src="6.jpg" alt=""></div>
        <div class="gallery-item"><img src="7.webp" alt=""></div>
        <div class="gallery-item"><img src="8.webp" alt=""></div>
        <div class="gallery-item"><img src="9.webp" alt=""></div>
        <div class="gallery-item"><img src="10.webp" alt=""></div>
        <div class="gallery-item"><img src="11.jpg" alt=""></div>
        <div class="gallery-item"><img src="12.jpg" alt=""></div>
    </div>

    
    <div id="modal">
        <span class="close">&times;</span>
        <img id="modal-img" src="" alt="Enlarged">
    </div>

    <footer id="footer">
    Designed and Developed by Akshay Karthick ASR
    </footer>

    <script>
        
        const galleryItems = document.querySelectorAll('.gallery-item img');
        const modal = document.getElementById('modal');
        const modalImg = document.getElementById('modal-img');
        const closeModal = document.querySelector('.close');

        
        galleryItems.forEach(item => {
            item.addEventListener('click', () => {
                modal.style.display = 'flex';
                modalImg.src = item.src; 
            });
        });

        
        closeModal.addEventListener('click', () => {
            modal.style.display = 'none';
        });

        
        modal.addEventListener('click', (event) => {
            if (event.target === modal) {
                modal.style.display = 'none';
            }
        });
    </script>
</body>
</html>


```
## OUTPUT:
![alt text](<Screenshot (59).png>)
![alt text](<Screenshot (60).png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
