# Taskforce-Challenge
building an interactive photo gallery based on provided Figma designs.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Photo Gallery</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="gallery">
        <div class="preview">
            <img id="mainImage" src="https://picsum.photos/id/237/800/600" alt="Main Image">
            <div class="image-details" id="imageDetails">Image 1 of 5</div>
        </div>
        <div class="thumbnails">
            <img class="thumbnail" src="https://picsum.photos/id/237/200/150" alt="Thumbnail 1" onclick="showImage(1, 'https://picsum.photos/id/237/800/600', 'Image 1 of 5')">
            <img class="thumbnail" src="https://picsum.photos/id/238/200/150" alt="Thumbnail 2" onclick="showImage(2, 'https://picsum.photos/id/238/800/600', 'Image 2 of 5')">
            <img class="thumbnail" src="https://picsum.photos/id/239/200/150" alt="Thumbnail 3" onclick="showImage(3, 'https://picsum.photos/id/239/800/600', 'Image 3 of 5')">
            <img class="thumbnail" src="https://picsum.photos/id/240/200/150" alt="Thumbnail 4" onclick="showImage(4, 'https://picsum.photos/id/240/800/600', 'Image 4 of 5')">
            <img class="thumbnail" src="https://picsum.photos/id/241/200/150" alt="Thumbnail 5" onclick="showImage(5, 'https://picsum.photos/id/241/800/600', 'Image 5 of 5')">
        </div>
    </div>
    <script src="scripts.js"></script>
</body>
</html>

body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    background-color: #f0f0f0;
}

.gallery {
    max-width: 800px;
    width: 100%;
}

.preview {
    position: relative;
}

#mainImage {
    width: 100%;
    height: auto;
}

.image-details {
    position: absolute;
    bottom: 10px;
    left: 10px;
    background-color: rgba(0, 0, 0, 0.5);
    color: #fff;
    padding: 5px 10px;
    border-radius: 5px;
}

.thumbnails {
    display: flex;
    justify-content: space-between;
    margin-top: 10px;
}

.thumbnail {
    width: 18%;
    cursor: pointer;
    border: 2px solid transparent;
    transition: border 0.3s;
}

.thumbnail:hover {
    border: 2px solid #000;
}

function showImage(index, src, details) {
    document.getElementById('mainImage').src = src;
    document.getElementById('imageDetails').innerText = details;
}
