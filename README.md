# Ex.08 Design of Interactive Image Gallery
# Date:09-05-2025
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Gallery</title>

    
    
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            max-width: 1000px;
            width: 100%;
            margin: 20px auto;
        }

        .gallery img {
            width: 100%;
            height: auto;
            border-radius: 5px;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        .gallery img:hover {
            transform: scale(1.05);
        }

        .lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .lightbox img {
            max-width: 95%;
            max-height: 95%;
            border-radius: 5px;
        }

        .lightbox.active {
            display: flex;
        }
    </style>
</head>
<body bgcolor="plum">
    <h1 style="font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;">Image Gallery</h1>
    <div class="gallery">
        <img src="cat1.webp" alt="Image 1">
        <img src="cat10.jpg" alt="Image 2">
        <img src="cat3.webp" alt="Image 3">
        <img src="cat4.webp" alt="Image 4">
        <img src="cat5.webp" alt="Image 5">
        <img src="cat8.jpg" alt="Image 6">
        <img src="cat7.webp" alt="Image 7">
        <img src="cat9.jpg" alt="Image 8">
    </div>

    <div class="lightbox" id="lightbox">
        <img src="" alt="">
    </div>

    <script>
        const gallery = document.querySelectorAll('.gallery img');
        const lightbox = document.getElementById('lightbox');
        const lightboxImg = lightbox.querySelector('img');

        gallery.forEach(image => {
            image.addEventListener('click', () => {
                lightboxImg.src = image.src;
                lightbox.classList.add('active');
            });
        });

        lightbox.addEventListener('click', () => {
            lightbox.classList.remove('active');
        });

        
    </script>
</body>
</html>
```
# OUTPUT:
![Screenshot 2025-05-06 110823](https://github.com/user-attachments/assets/1bfb8647-7285-4461-ae13-6d29322bc0dd)
![Screenshot 2025-05-06 110836](https://github.com/user-attachments/assets/5eb424a9-da58-42a0-90ba-7344c9de57fc)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
