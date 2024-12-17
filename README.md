<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jam e Gulab - Product Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: white;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #FF6347;
            color: white;
            padding: 10px 0;
            text-align: center;
            font-size: 30px;
            font-weight: bold;
        }
        .slider {
            position: relative;
            max-width: 100%;
            height: 300px;
            margin-top: 20px;
            overflow: hidden;
        }
        .slides {
            display: flex;
            transition: transform 1s ease;
        }
        .slide {
            min-width: 100%;
            height: 300px;
            object-fit: cover;
        }
        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            margin: 20px 0;
        }
        .gallery-item {
            width: 30%;
            margin: 10px;
            border: 2px solid #ddd;
            border-radius: 8px;
            overflow: hidden;
            background-color: #f9f9f9;
        }
        .gallery-item img {
            width: 100%;
            height: auto;
            display: block;
        }
        footer {
            text-align: center;
            background-color: #333;
            color: white;
            padding: 10px 0;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>

    <header>
        Jam e Gulab
    </header>

    <!-- Image Slider -->
    <div class="slider">
        <div class="slides">
            <img class="slide" src="https://via.placeholder.com/1500x300?text=Slide+1" alt="Slide 1">
            <img class="slide" src="https://via.placeholder.com/1500x300?text=Slide+2" alt="Slide 2">
            <img class="slide" src="https://via.placeholder.com/1500x300?text=Slide+3" alt="Slide 3">
        </div>
    </div>

    <!-- Product Gallery -->
    <div class="gallery">
        <div class="gallery-item">
            <img src="https://via.placeholder.com/400x300?text=Product+1" alt="Product 1">
            <div style="padding: 10px;">
                <h3>Product 1</h3>
                <p>Price: $15</p>
                <button>Buy Now</button>
            </div>
        </div>
        <div class="gallery-item">
            <img src="https://via.placeholder.com/400x300?text=Product+2" alt="Product 2">
            <div style="padding: 10px;">
                <h3>Product 2</h3>
                <p>Price: $20</p>
                <button>Buy Now</button>
            </div>
        </div>
        <div class="gallery-item">
            <img src="https://via.placeholder.com/400x300?text=Product+3" alt="Product 3">
            <div style="padding: 10px;">
                <h3>Product 3</h3>
                <p>Price: $25</p>
                <button>Buy Now</button>
            </div>
        </div>
    </div>

    <footer>
        &copy; 2024 Jam e Gulab | www.jamegulab.com
    </footer>

    <script>
        // Simple slider functionality
        let currentSlide = 0;
        const slides = document.querySelectorAll('.slide');
        const totalSlides = slides.length;

        function showSlide(index) {
            const slideWidth = slides[0].clientWidth;
            document.querySelector('.slides').style.transform = `translateX(-${slideWidth * index}px)`;
        }

        function nextSlide() {
            currentSlide = (currentSlide + 1) % totalSlides;
            showSlide(currentSlide);
        }

        setInterval(nextSlide, 3000); // Change slide every 3 seconds
    </script>

</body>
</html>
