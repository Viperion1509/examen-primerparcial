<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Three.js Scene</title>
  <style>
    body { margin: 0; }
    canvas { display: block; }
  </style>
</head>
<body>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
  <script>
    // Escena
    const scene = new THREE.Scene();

    // Cámara
    const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
    camera.position.z = 5;

    // Renderizador
    const renderer = new THREE.WebGLRenderer();
    renderer.setSize(window.innerWidth, window.innerHeight);
    document.body.appendChild(renderer.domElement);

    // Crear un cubo
    const cubeGeometry = new THREE.BoxGeometry();
    const cubeMaterial = new THREE.MeshStandardMaterial({ color: 0x00ff00 });
    const cube = new THREE.Mesh(cubeGeometry, cubeMaterial);
    scene.add(cube);

    // Crear el primer plano (más pequeño)
    const smallPlaneGeometry = new THREE.PlaneGeometry(2, 2);
    const smallPlaneMaterial = new THREE.MeshStandardMaterial({ color: 0x0000ff });
    const smallPlane = new THREE.Mesh(smallPlaneGeometry, smallPlaneMaterial);
    smallPlane.position.set(-3, 0, -1);
    scene.add(smallPlane);

    // Crear el segundo plano (más grande)
    const largePlaneGeometry = new THREE.PlaneGeometry(4, 4);
    const largePlaneMaterial = new THREE.MeshStandardMaterial({ color: 0xff0000 });
    const largePlane = new THREE.Mesh(largePlaneGeometry, largePlaneMaterial);
    largePlane.position.set(3, 0, -1);
    scene.add(largePlane);

    // Luz ambiental
    const ambientLight = new THREE.AmbientLight(0xffffff, 0.5);
    scene.add(ambientLight);

    // Luz direccional
    const directionalLight = new THREE.DirectionalLight(0xffffff, 1);
    directionalLight.position.set(1, 1, 1).normalize();
    scene.add(directionalLight);

    // Función de animación
    function animate() {
      requestAnimationFrame(animate);

      // Rotar el cubo
      cube.rotation.x += 0.01;
      cube.rotation.y += 0.01;

      renderer.render(scene, camera);
    }
    
    animate();
  </script>
</body>
</html>
