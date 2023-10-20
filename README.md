# RADDISH0.github.io
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Montserrat:wght@600&display=swap">
    <style>
        .image-container {
            display: inline-block;
            position: relative;
        }

        #clickable-image {
            max-width: 100%;
            transition: transform 0.2s cubic-bezier(0.25, 0.75, 0.5, 1.25); /* Match the given animation */
            cursor: pointer;
        }

        #click-counter-container {
            position: absolute;
            top: 70px; /* Adjust top positioning as needed */
            left: 430px; /* Adjust left positioning as needed */
            background-color: #333; /* Dark gray background color */
            color: #fff; /* White text color */
            border-radius: 50px; /* Adjust the border radius to control the roundness */
            padding: 10px; /* Adjust padding as needed */
        }

        #click-counter {
            font-family: 'Montserrat', sans-serif; /* Use Montserrat Semi-Bold or a suitable alternative */
            user-select: none; /* Prevent text selection on iPad Safari */
        }
    </style>
</head>
<body>
    <div class="image-container">
        <img id="clickable-image"<img src="https://bg-so-1.zippyimage.com/2023/10/19/99e96492320ff515b425ded0b5643aba.jpg" alt="Dv9cG3.jpg" border="0" />
        <div id="click-counter-container">
            <div id="click-counter">Clicks: 0</div>
        </div>
    </div>

    <script>
        const clickableImage = document.getElementById("clickable-image");
        const clickCounter = document.getElementById("click-counter");
        let clickCount = 0;

        function shrinkAndExpand() {
            clickableImage.style.transform = "scale(0.8)";
            
            setTimeout(function() {
                clickableImage.style.transform = "scale(1)";
            }, 200); // Match the given animation (0.2 seconds)

            // Increment click count
            clickCount++;
            clickCounter.textContent = `Clicks: ${clickCount}`;
        }

        clickableImage.addEventListener("click", shrinkAndExpand);
    </script>
</body>
</html>
