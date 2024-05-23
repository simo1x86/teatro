<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mappa Posti</title>
<style>
  /* Stili per la griglia */
  .grid-container {
    display: grid;
    grid-template-columns: repeat(10, 50px); /* 10 colonne di larghezza 50px */
    grid-gap: 5px; /* Spazio tra le celle */
  }
  .grid-item {
    background-color: red;
    border: 1px solid #999;
    padding: 10px;
    text-align: center;
    cursor: pointer;
  }
  .grid-item.booked {
    background-color: #ddd; /* Cambia colore al click */
  }
</style>
</head>
<body>

<div class="grid-container">
  <!-- Genera le celle della griglia -->
  <!-- Utilizziamo JavaScript per creare automaticamente le celle -->
  <script>
    // Numero di righe e colonne
    var rows = 10;
    var cols = 10;

    // Funzione per gestire il click sui posti
    function handleClick(event) {
      var gridItem = event.target;
      if (!gridItem.classList.contains('booked')) {
        var bookingName = prompt('Inserisci il nome della prenotazione:');
        if (bookingName !== null && bookingName !== '') {
          gridItem.classList.add('booked');
          gridItem.textContent = bookingName;
        }
      } else {
        var cancelBooking = confirm('Vuoi cancellare la prenotazione?');
        if (cancelBooking) {
          gridItem.classList.remove('booked');
          gridItem.textContent = '';
        }
      }
    }

    // Genera le celle
    for (var i = 1; i <= rows; i++) {
      for (var j = 1; j <= cols; j++) {
        var gridItem = document.createElement('div');
        gridItem.classList.add('grid-item');
        gridItem.textContent = 'R' + i + 'C' + j;
        gridItem.addEventListener('click', handleClick);
        gridItem.style.cursor = 'pointer'; // Imposta il puntatore come una manina
        document.body.querySelector('.grid-container').appendChild(gridItem);
      }
    }
  </script>
</div>

</body>
</html>
