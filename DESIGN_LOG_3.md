# DESIGN_LOG_3 – Manejo de Estados de Carga y Error en la UI

## Objetivo
El diseño de la interfaz de *Rumbo – Navegación Activa* considera explícitamente los estados de **Carga (Loading)** y **Error**, con el fin de mantener informado al usuario, evitar confusión y permitir la recuperación ante fallos de red o acciones incompletas.

## Estado de Carga (Loading)
El estado de carga se activa cuando el usuario realiza acciones que dependen de una operación asíncrona, como guardar una ruta o un punto en el mapa.

Las decisiones de diseño para este estado incluyen:

- **Indicador visual inmediato** mediante un *toast* flotante con ícono animado (`fa-circle-notch`).
- Uso del color principal (verde neón) para indicar que el sistema está procesando correctamente.
- Deshabilitación temporal de botones críticos (por ejemplo, el botón de grabar ruta) para evitar acciones duplicadas.
- Cambio visual en la polilínea de la ruta (línea punteada y color neutro) para representar que la información aún no ha sido confirmada.

Esto garantiza que el usuario entienda que la acción está en progreso y que el sistema no está congelado.

## Estado de Error
El estado de error se presenta cuando una operación falla, simulando problemas reales de red o conexión mediante una respuesta negativa de la API.

Las estrategias aplicadas en este estado son:

- **Retroalimentación clara e inmediata** usando un *toast* con color rojo e ícono de advertencia.
- Cambio visual de los elementos afectados:
  - Rutas mostradas con línea roja punteada.
  - Marcadores de error en color rojo con animación de sacudida (*shake*).
- Mensajes explícitos como “ERROR DE RED” o “ERROR AL GUARDAR” para evitar ambigüedad.
- Posibilidad de **reintentar la acción**, reabriendo automáticamente el popup de confirmación sin perder el contexto del usuario.

Esto evita que el error sea silencioso y le da al usuario control para decidir cómo proceder.

## Consistencia y Experiencia de Usuario
Los estados de carga y error mantienen coherencia visual en toda la interfaz:
- Verde para éxito y procesos activos.
- Rojo para errores y fallos.
- Animaciones sutiles para llamar la atención sin ser intrusivas.

Además, el sistema evita pérdidas de información, permitiendo reintentos y cancelaciones controladas.

## Conclusión
El manejo explícito de los estados de **Carga** y **Error** mejora significativamente la experiencia de usuario, al proporcionar feedback constante, reducir incertidumbre y permitir la recuperación ante fallos, logrando una interfaz más robusta, confiable y centrada en el usuario.
