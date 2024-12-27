<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Random Image Viewer</title>
    <style>
        /* Basic Styling */
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f9;
            padding: 20px;
        }
        h1 {
            color: #333;
        }
        img {
            max-width: 80%;
            height: auto;
            margin: 20px 0;
            border: 2px solid #ddd;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            color: white;
            background-color: #007BFF;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <h1>Random Image Viewer</h1>
    <p>Click the button below to view a random image!</p>
    <img id="randomImage" src="images/image1.jpg" alt="Random Image">
    <br>
    <button onclick="showRandomImage()">Show Random Image</button>

    <script>
        // Array of image paths
        const images = [
            "images/image1.jpg",
            "images/image2.jpg",
            "images/image3.jpg"
        ];

        // Function to display a random image
        function showRandomImage() {
            const randomIndex = Math.floor(Math.random() * images.length);
            const randomImage = images[randomIndex];
            document.getElementById('randomImage').src = randomImage;
        }
    </script>
</body>
</html>
