# aroma-opita
Landing page de cafetería Aroma Opita - Taller Tailwind e IA FET


## Bitácora de Prompts e Iteraciones con IA

| # | PROBLEMA | PROMPT DE AJUSTE ENVIADO | RESULTADO OBTENIDO | ¿FUNCIONÓ? |
|---|---|---|---|---|
| 1 | El menú móvil hamburguesa no se cerraba automáticamente al hacer clic en uno de los enlaces. | *"El menú móvil se queda abierto tras hacer clic en un enlace. Ajusta el código JavaScript para que iteré sobre los enlaces '.mobile-link' y oculte el menú al hacer clic."* | Se agregó un `forEach` con un `addEventListener` que añade la clase `hidden` al contenedor. | Sí |
| 2 | Las tarjetas del menú se veían amontonadas en la vista de celular (3 columnas en móvil). | *"Las tarjetas están muy pequeñas en celular. Ajusta las clases de Tailwind del grid para que sea 1 columna en móvil, 2 en tablet y 3 en PC."* | Se modificaron las clases a `grid-cols-1 md:grid-cols-2 lg:grid-cols-3`. | Sí |
| 3 | Al dar clic en "Confirmar Reserva", la página se recargaba por completo y no se veía el Toast. | *"Al enviar el formulario la página se recarga. Usa `e.preventDefault()` en JavaScript para evitarlo y permitir que la animación del toast se ejecute."* | Se detuvo el comportamiento por defecto del formulario y el toast funciona correctamente. | Sí |
| 4 | El toast verde de confirmación aparecía desalineado y rompía el flujo del HTML. | *"El toast está empujando el contenido. Ajusta sus clases para que quede flotando fijo en la esquina inferior derecha usando position absolute o fixed."* | Se añadieron las clases `absolute bottom-6 right-6` para sobreponerlo en la interfaz. | Sí |
| 5 | El texto de los derechos de autor en el footer (pie de página) casi no se leía sobre el fondo café. | *"El texto pequeño del footer no tiene buen contraste con el fondo oscuro. Cambia la clase del texto a un gris más claro para mejorar la accesibilidad."* | Se cambió la clase a `text-gray-400`, superando el nivel de contraste WCAG requerido. | Sí |
