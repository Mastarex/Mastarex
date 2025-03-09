                                                                                       ** 3D Cube HTMLCSS Styles**

<style>
/* Flex container to hold both cube and cards */
.container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    gap: 50px;
    padding: 20px;
}

/* Cube styles (from your previous request) */
.scene {
    width: 300px;
    height: 300px;
    margin: 0 auto;
    perspective: 1000px;
    position: relative;
}

.cube {
    width: 100%;
    height: 100%;
    position: relative;
    transform-style: preserve-3d;
    animation: rotate 10s infinite linear;
}

.cube-face {
    position: absolute;
    width: 300px;
    height: 300px;
    background: #fff;
    opacity: 0.9;
    display: flex;
    justify-content: center;
    align-items: center;
}

.cube-face img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.cube-face.front { transform: translateZ(150px); }
.cube-face.back { transform: translateZ(-150px) rotateY(180deg); }
.cube-face.left { transform: translateX(-150px) rotateY(-90deg); }
.cube-face.right { transform: translateX(150px) rotateY(90deg); }
.cube-face.top { transform: translateY(-150px) rotateX(90deg); }
.cube-face.bottom { transform: translateY(150px) rotateX(-90deg); }

@keyframes rotate {
    from { transform: rotateY(0deg); }
    to { transform: rotateY(360deg); }
}



/* Responsive adjustments */
@media (max-width: 767px) {
    .container {
        flex-direction: column;
        gap: 30px;
    }
    .scene {
        width: 250px;
        height: 250px;
    }
    .cube-face {
        width: 250px;
        height: 250px;
    }
    .cube-face.front { transform: translateZ(125px); }
    .cube-face.back { transform: translateZ(-125px) rotateY(180deg); }
    .cube-face.left { transform: translateX(-125px) rotateY(-90deg); }
    .cube-face.right { transform: translateX(125px) rotateY(90deg); }
    .cube-face.top { transform: translateY(-125px) rotateX(90deg); }
    .cube-face.bottom { transform: translateY(125px) rotateX(-90deg); }
   
</style>

<div class="container">
   <div class="scene">
    <div class="cube">
        <div class="cube-face front"><img src="https://designstudio.douglasbranding.com/wp-content/uploads/2025/03/6746e0effd914c6da9cfada5_seo-galaxy-zZ7J5qri6qY-unsplash.avif" alt="Front"></div>
        <div class="cube-face back"><img src="https://designstudio.douglasbranding.com/wp-content/uploads/2025/03/6746e0effd914c6da9cfada5_seo-galaxy-zZ7J5qri6qY-unsplash.avif" alt="Back"></div>
        <div class="cube-face left"><img src="https://designstudio.douglasbranding.com/wp-content/uploads/2025/03/6746e0effd914c6da9cfada5_seo-galaxy-zZ7J5qri6qY-unsplash.avif" alt="Left"></div>
        <div class="cube-face right"><img src="https://designstudio.douglasbranding.com/wp-content/uploads/2025/03/6746e0effd914c6da9cfada5_seo-galaxy-zZ7J5qri6qY-unsplash.avif" alt="Right"></div>
        <div class="cube-face top"><img src="https://designstudio.douglasbranding.com/wp-content/uploads/2025/03/6746e0effd914c6da9cfada5_seo-galaxy-zZ7J5qri6qY-unsplash.avif" alt="Top"></div>
        <div class="cube-face bottom"><img src="https://designstudio.douglasbranding.com/wp-content/uploads/2025/03/6746e0effd914c6da9cfada5_seo-galaxy-zZ7J5qri6qY-unsplash.avif" alt="Bottom"></div>
    </div>

<script>
document.addEventListener('DOMContentLoaded', function() {
    const cube = document.querySelector('.cube');
    cube.addEventListener('mouseover', () => {
        cube.style.animationPlayState = 'paused';
    });
    cube.addEventListener('mouseout', () => {
        cube.style.animationPlayState = 'running';
    });
});
</script>










