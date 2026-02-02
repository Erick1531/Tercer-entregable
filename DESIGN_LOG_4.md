---

## Ajuste cromático de los puntos del mapa

- Se modificó el color de los puntos y marcadores del mapa a **azul neón**.
- Esta decisión se tomó para mantener coherencia visual con la temática de **bosques y áreas verdes** del proyecto.
- El azul neón ofrece un alto contraste sobre el fondo del mapa, facilitando la identificación de puntos sin generar confusión visual.
- Además, mejora la visibilidad en condiciones de poca luz y reduce la fatiga visual durante el uso prolongado.
- agregue también una lista con los puntos colocados que permite hacer zoom al punto seleccionado

## Promp utilizado

- Ahora has esto pporfavor : "Modifica la interfaz para tener dos columnas (o pestañas en móvil): 'Mapa' y 'Lista de Lugares'. Cuando se agregue un marcador en el mapa, debe aparecer también como un texto descriptivo en la sección de Lista (ej. 'Punto en Lat: X, Long: Y'). Asegúrate de que los botones del mapa tengan atributos 'aria-label' como 'Acercar mapa' o 'Alejar mapa'."

- Refinamiento UX:

- Sincronización: Si hago clic en el ítem de la lista, el mapa debe hacer "FlyTo" (animación de Leaflet) hacia ese marcador.
- Color: Revisa si los pines contrastan con el mapa (ej. no usar pines verdes sobre zonas de bosque).
