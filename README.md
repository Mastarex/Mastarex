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
  </div>
</div>

<style>
/* Flex container to hold the cube */
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 50px;
  background: #19191B; /* Dark background for contrast (your adjustment) */
  position: relative;
}

/* Scene for the cube */
.scene {
  width: 350px; /* Updated width */
  height: 350px; /* Updated height */
  perspective: 1000px;
  position: relative;
  margin: 0 auto;
}

/* Cube styles */
.cube {
  width: 100%;
  height: 100%;
  position: relative;
  transform-style: preserve-3d;
  animation: rotate 20s infinite linear; /* Your slower rotation adjustment */
  transition: transform 0.3s ease; /* Smooth scaling on hover */
}

/* Hover effect for the cube */
.cube:hover {
  transform: scale(1.1); /* Slight scale on hover */
}

/* Cube faces */
.cube-face {
  position: absolute;
  width: 350px; /* Updated width */
  height: 350px; /* Updated height */
  background: #fff;
  opacity: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 0 0 0px rgba(255, 255, 255, 0.5); /* Your adjusted glow effect */
  transition: box-shadow 0.3s ease;
}

.cube-face:hover {
  box-shadow: 0 0 20px rgba(255, 255, 255, 0.8); /* Brighter glow on hover (your adjustment) */
}

.cube-face img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Positioning for each face */
.cube-face.front  { transform: translateZ(175px); } /* Adjusted for new size (350/2) */
.cube-face.back   { transform: translateZ(-175px) rotateY(180deg); }
.cube-face.left   { transform: translateX(-175px) rotateY(-90deg); }
.cube-face.right  { transform: translateX(175px) rotateY(90deg); }
.cube-face.top    { transform: translateY(-175px) rotateX(90deg); }
.cube-face.bottom { transform: translateY(175px) rotateX(-90deg); }

/* Updated rotation animation to show all faces */
@keyframes rotate {
  0% {
    transform: rotateX(0deg) rotateY(0deg);
  }
  25% {
    transform: rotateX(90deg) rotateY(90deg); /* Shows top and right faces */
  }
  50% {
    transform: rotateX(180deg) rotateY(180deg); /* Shows bottom and back faces */
  }
  75% {
    transform: rotateX(270deg) rotateY(270deg); /* Shows top and left faces */
  }
  100% {
    transform: rotateX(360deg) rotateY(360deg); /* Back to start */
  }
}

/* Reflective surface below the cube */
.scene::after {
  content: '';
  position: absolute;
  width: 350px; /* Updated width */
  height: 175px; /* Adjusted for new size (350/2) */
  bottom: -50px;
  left: 0;
  background: linear-gradient(180deg, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
  filter: blur(20px);
  z-index: -1; /* Behind the cube */
}

/* Responsive adjustments */
@media (max-width: 767px) {
  .container {
    padding: 30px;
  }
  .scene {
    width: 300px; /* Slightly smaller for mobile */
    height: 300px;
  }
  .cube-face {
    width: 300px;
    height: 300px;
  }
  .cube-face.front  { transform: translateZ(150px); }
  .cube-face.back   { transform: translateZ(-150px) rotateY(180deg); }
  .cube-face.left   { transform: translateX(-150px) rotateY(-90deg); }
  .cube-face.right  { transform: translateX(150px) rotateY(90deg); }
  .cube-face.top    { transform: translateY(-150px) rotateX(90deg); }
  .cube-face.bottom { transform: translateY(150px) rotateX(-90deg); }
  .scene::after {
    width: 300px;
    height: 150px;
  }
}
</style>

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
