<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cars Information</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      background-color: #f4f4f4;
    }

    header {
      background: #333;
      color: white;
      padding: 1em;
      text-align: center;
    }

    .container {
      padding: 20px;
      max-width: 800px;
      margin: auto;
    }

    .car-card {
      background: white;
      padding: 15px;
      margin-bottom: 10px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      border-radius: 5px;
    }

    .car-card h3 {
      margin: 0 0 10px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Car Information</h1>
  </header>

  <div class="container" id="car-container">
    <!-- Cars will be listed here dynamically -->
  </div>

  <script>
    const cars = [
      { name: 'Tesla Model S', type: 'Electric', speed: '200 mph' },
      { name: 'Ford Mustang', type: 'Muscle', speed: '155 mph' },
      { name: 'Chevrolet Corvette', type: 'Sports', speed: '194 mph' },
      { name: 'BMW M3', type: 'Luxury', speed: '180 mph' }
    ];

    const carContainer = document.getElementById('car-container');

    function displayCars() {
      cars.forEach(car => {
        const carCard = document.createElement('div');
        carCard.classList.add('car-card');
        carCard.innerHTML = `
          <h3>${car.name}</h3>
          <p>Type: ${car.type}</p>
          <p>Top Speed: ${car.speed}</p>
        `;
        carContainer.appendChild(carCard);
      });
    }

    displayCars();
  </script>
</body>
</html>
