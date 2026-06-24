# Contexto: Pokémon Egg Randomizer

## Descripción del proyecto

Página web para sortear huevos de Pokémon en un formato de contenido grabado para YouTube. El objetivo es elegir al azar un huevo entre todos los disponibles en el PC de almacenamiento del juego, mostrando el resultado de forma visual y entretenida para el video.

## Formato del juego

- **Cajas del PC:** 20 cajas en total
- **Tamaño de cada caja:** 6 columnas × 5 filas = 30 espacios por caja
- **Total de huevos disponibles:** 600 (20 cajas × 30 posiciones)
- **Mecánica:** se elige al azar una caja y luego, dentro de esa caja, una posición específica. El huevo en esa posición se abre y el Pokémon resultante se queda como parte del equipo/colección.

## Proceso de sorteo (cómo funciona la página)

1. **Paso 1 – Sortear caja:** se presiona el botón correspondiente y la página anima un "rolido" entre las 20 cajas hasta detenerse en una (ej. Caja 07).
2. **Paso 2 – Sortear posición:** una vez fijada la caja, se presiona el segundo botón. La grilla 6×5 (representada con coordenadas tipo planilla: columnas A–F, filas 1–5) anima un cursor saltando aleatoriamente hasta fijarse en una celda final (ej. B3).
3. **Resultado final:** se muestra de forma combinada, por ejemplo "Caja 07 → B3", con efecto de confetti y resaltado visual.
4. Existe un botón de **Nueva Ronda** para reiniciar el sorteo sin recargar la página.

## Diseño visual

- Estética **retro/pixel art** con tipografía "Press Start 2P" y "VT323"
- Fondo con efecto de estrellas y overlay de scanlines (referencia a pantallas CRT)
- Paleta de colores: amarillo dorado (acento principal), azul (paso "caja"), verde (paso "posición"), rojo (detalles)
- Indicador de progreso por pasos (puntos que se iluminan según el paso del sorteo)
- Contadores en pantalla: número de tiradas realizadas y Pokémon obtenidos (pensado para que se vea en el video)

## Archivo entregado

- `pokemon-egg-randomizer.html` — página standalone (HTML/CSS/JS sin dependencias externas más que las fuentes de Google Fonts), lista para abrir en navegador y compartir pantalla durante la grabación.

## Punto pendiente / mejora identificada

Actualmente **no hay control de repeticiones**: la misma casilla (caja + posición) puede salir sorteada más de una vez, lo cual no tiene sentido si los huevos se consumen al abrirse (cada huevo solo se puede abrir una vez).

**Mejora sugerida:** agregar un modo "sin reposición" que:
- Mantenga un registro de las casillas ya sorteadas
- Marque visualmente (ej. en gris) los huevos ya usados en la grilla
- Excluya esas posiciones de los sorteos futuros dentro de la misma caja

Esto también sumaría valor visual al video, porque la grilla se iría "vaciando" episodio a episodio, dando sensación de progreso real en el playthrough.
