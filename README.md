# dulcesartesanales
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Catálogo y Pedido por WhatsApp</title>
</head>
<body>
<h1>Catálogo de Productos</h1>

<div class="producto">
    <img src="producto1.jpg" alt="Producto 1">
    <h2>Producto 1</h2>
    <p>Descripción del producto 1.</p>
    <button class="pedido-btn" data-producto="Producto 1">Hacer Pedido</button>
</div>

<div class="producto">
    <img src="producto2.jpg" alt="Producto 2">
    <h2>Producto 2</h2>
    <p>Descripción del producto 2.</p>
    <button class="pedido-btn" data-producto="Producto 2">Hacer Pedido</button>
</div>

<!-- Agrega más productos aquí -->

<script>
    const buttons = document.querySelectorAll('.pedido-btn');

    buttons.forEach(button => {
        button.addEventListener('click', () => {
            const producto = button.getAttribute('data-producto');
            const mensaje = `¡Hola! Estoy interesado en comprar el producto: ${producto}`;
            const telefono = '+5493855797847'; // Reemplaza con tu número de WhatsApp

            window.open(`https://api.whatsapp.com/send?phone=${telefono}&text=${encodeURIComponent(mensaje)}`);
        });
    });
</script>
</body>
</html>
