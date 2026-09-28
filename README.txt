DiMe - Control Comercial Web — versión corregida

PROBLEMA CORREGIDO
La versión anterior dependía de variables globales creadas implícitamente por los IDs HTML (clientId, type, date, etc.) y de crypto.randomUUID(). Eso puede fallar al abrir index.html directamente desde el explorador, especialmente con ciertos navegadores/configuraciones.

Esta versión:
- Usa document.getElementById() explícitamente.
- Genera IDs sin depender de crypto.randomUUID().
- Maneja mejor localStorage.
- Valida la próxima acción y su fecha.
- Escapa texto ingresado para evitar romper la interfaz.
- Mantiene los 15 registros iniciales.
- Exporta CSV y respaldo JSON.
- Funciona como archivo local, sin servidor ni internet.

CÓMO ABRIR
1. Extrae el ZIP.
2. Abre la carpeta.
3. Haz doble clic en index.html.
4. Usa Chrome o Edge.
5. Entra en “Registrar actividad” y guarda una visita de prueba.

IMPORTANTE
Los datos quedan guardados en el navegador y dispositivo donde uses la aplicación. No se sincronizan automáticamente entre computador y celular. Usa “Respaldar” para conservar una copia.
