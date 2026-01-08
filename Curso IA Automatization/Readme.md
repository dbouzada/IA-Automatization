## Desarrollo de Worklfow Final
El objetivo de este workflow es establecer un sistema automatizado para la detección, ingestión, 
procesamiento, clasificación por IA, y notificación en tiempo real de nuevas entradas de noticias corporativas.

El flujo opera bajo un modelo de polling (sondeo), donde un disparador de Google Sheets revisa el origen de datos cada minuto.
Ingesta de Datos: Se detecta una nueva fila en Google Sheets (Titular y URL).
Extracción Web: Se realiza una solicitud HTTP a la URL para obtener el código fuente de la noticia.
Procesamiento de Contenido: Se filtra el contenido HTML para aislar el texto principal del artículo.
Clasificación AI: El texto filtrado se envía a un modelo de lenguaje (Gemini) para categorización.
Alerta: El resultado clasificado se envía al canal de Telegram designado.
