# Ex.08 Design of Interactive Image Gallery
# Date : 15.11.25
## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM

image.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>IMAGE GALLERY</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            background: url('vj.jpg') no-repeat center center/cover;
            height: 100vh;
            overflow-y: auto;
        }

        .overlay {
            background: rgba(0, 0, 0, 0.5);
            min-height: 100vh;
            padding: 20px;
        }

        h1 {
            text-align: center;
            color: #fff;
            margin-bottom: 20px;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            grid-template-rows: repeat(3, 200px);
            gap: 15px;
            padding: 10px;
        }

        .gallery img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 12px;
            transition: transform 0.3s;
            cursor: pointer;
        }

        .gallery img:hover {
            transform: scale(1.05);
        }

        /* Fullscreen popup */
        #popup {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            display: none;
            justify-content: center;
            align-items: center;
        }

        #popup img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <div class="overlay">
        <h1>IMAGE GALLERY(THALAPATHY)</h1>

        <div class="gallery">
            <img src="t1.jpg" alt="Image 1" />
            <img src="image copy 3.png" alt="Image 2" />
            <img src="t2.jpg" alt="Image 3" />
            <img src="t3.jpg" alt="Image 4" />
            <img src="t4.jpg" alt="Image 5" />
            <img src="t5.jpg" alt="Image 6" />
        </div>
    </div>

    <div id="popup" onclick="closePopup()">
        <img id="popupImg" />
    </div>

    <script>
        const images = document.querySelectorAll('.gallery img');
        const popup = document.getElementById('popup');
        const popupImg = document.getElementById('popupImg');

        images.forEach(img => {
            img.addEventListener('click', () => {
                popup.style.display = 'flex';
                popupImg.src = img.src;
            });
        });

        function closePopup() {
            popup.style.display = 'none';
        }
    </script>
</body>
</html>

```


## OUTPUT

<img width="1920" height="1200" alt="W1" src="https://github.com/user-attachments/assets/b3344a53-b735-4578-9675-7cfd901715e6" />
<img width="1920" height="1200" alt="W2" src="https://github.com/user-attachments/assets/57e145f7-6dae-4ad7-a6d5-17f8e6fbebf0" />
<img width="1920" height="1200" alt="W3" src="https://github.com/user-attachments/assets/1e5c7654-77ae-4414-ad8c-34de13c4a2ed" />
<img width="1920" height="1200" alt="W4" src="https://github.com/user-attachments/assets/331e0181-3c70-4b19-ae70-fa2bf64643cb" />
<img width="1920" height="1200" alt="W5" src="https://github.com/user-attachments/assets/4472d239-38b4-46a0-b9c9-c34ab33855db" />
<img width="1920" height="1200" alt="W6" src="https://github.com/user-attachments/assets/e4b8aae7-bfab-4ea7-9248-00917c76c1bc" />


## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
