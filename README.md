<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hover Cat</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
        }

        .cat-image {
            width: 300px;
            height: auto;
            cursor: pointer;
            transition: transform 0.2s ease;
        }

        .cat-image:hover {
            transform: scale(1.1);
        }
    </style>
</head>
<body>
    <img 
        src="cat1.png" 
        alt="A cute cat" 
        class="cat-image" 
        onmouseover="this.src='cat2.png';" 
        onmouseout="this.src='cat1.png';"
    >

    <script>
        // Ensure the images are preloaded to avoid flickering
        const images = ['cat1.png', 'cat2.png'];
        images.forEach(src => {
            const img = new Image();
            img.src = src;
        });
    </script>
</body>
</html>
