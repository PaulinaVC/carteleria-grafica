# carteleria-grafica
Repositorio para generar una plataforma online para carteleria grafica.

**Pasos para Implementar una Pantalla de Proyección de Actividades con Office 365
Configura los Datos en Excel Online:**

1. Crea un archivo de Excel en OneDrive o SharePoint que contenga los datos de tus eventos.
Estructura las columnas como en Google Sheets: Título, Descripción, Hora de inicio, Hora de fin, Sala, Fecha, Imagen.
Guarda este archivo y asegúrate de que tienes los permisos de compartición correctos para poder acceder a él públicamente o con una API.
Usa Power Automate para Exportar los Datos de Excel a JSON:

Power Automate (anteriormente Microsoft Flow) permite crear un flujo que lee los datos de Excel y los convierte en un formato JSON.
Configura un flujo en Power Automate que:
Conecte el archivo de Excel en OneDrive o SharePoint.
Extraiga las filas del archivo.
Convierta los datos en JSON.
Publique estos datos en un endpoint HTTP (o guárdalos en un archivo JSON público en SharePoint).
Nota: La configuración de este flujo requiere una cuenta de Office 365 con acceso a Power Automate.
Acceso al JSON desde el Código HTML:

Una vez que Power Automate genera el JSON, toma la URL de este archivo y úsala en tu código HTML.
Cambia la URL de jsonURL en el código HTML para que apunte al JSON generado en Office 365.
Ajusta el Código HTML para Cargar el JSON desde Office 365:

Aquí tienes un ejemplo del fragmento que debes modificar en el código HTML:

javascript
Copiar código
const jsonURL = 'URL_DEL_JSON_EN_SHAREPOINT_O_ONEDRIVE';
Asegúrate de que tu código de JavaScript está leyendo y mostrando los datos correctamente, igual que en el código de Google Sheets.

Aloja el Código HTML en SharePoint o en una Página de Power Apps (Opcional):

Puedes subir este archivo HTML a SharePoint como una página o utilizar Power Apps para mostrarlo en una pantalla interactiva.
Power Apps te permite integrar la visualización de datos de Office y personalizar la presentación.
Ejemplo de Flujo en Power Automate para Convertir Excel a JSON
Paso 1: Crea un flujo en Power Automate.
Paso 2: Usa la acción "Get rows" para extraer las filas del archivo de Excel.
Paso 3: Convierte estas filas en un array JSON.
Paso 4: Usa la acción "Create file" en OneDrive o SharePoint para guardar el JSON.
Resumen
Office 365: Usa Excel Online para almacenar los datos de los eventos.
Power Automate: Extrae los datos y conviértelos en JSON.
HTML y JavaScript: Carga los datos JSON en tu página de proyección.
Aunque el proceso en Office 365 es un poco más complicado que en Google Sheets, puedes lograr un sistema similar de proyección de actividades. ¡Déjame saber si necesitas más ayuda en algún paso específico! 😊
