# ArgosTranslator
Interfaz de traduccion local utilizando el motor de traducción: Argos Translate

Esto esta pensado para correr en Windows 11 pero puede funcionar en otros entornos, se trata de una interfaz muy sencilla para ejecutar un traductor local con python y flask, accesible desde el navegador.

##  Instrucciones de Despliegue en Windows 11
1. Copia la carpeta traductor_argos a la ubicación deseada en tu PC con Windows.
2. Asegúrate de tener Python instalado en Windows.
3. Primer inicio (con consola):
   - Ejecuta run_server.bat (doble clic).
   - Verás una ventana negra. La primera vez tardará unos minutos descargando los modelos de idioma (aprox 300MB+).
     No la cierres hasta que veas que el servidor Flask ha iniciado o termine.
4. Uso Normal (Silencioso):
   - Una vez instalados los modelos, puedes usar start_silent.vbs para iniciar el servidor sin ventana negra.
   - Puedes poner un acceso directo a start_silent.vbs en tu carpeta shell:startup para que arranque con Windows.
5. Accede a la aplicación en: http://localhost:5000

## Estructura 
 - app.py: Núcleo lógico. Contiene la función install_languages y el algoritmo de pivoting.
- requirements.txt: Dependencias mínimas (flask, argostranslate, lxml, werkzeug).
- templates/index.html: Tu diseño exacto con JavaScript real conectado a la API.
- run_server.bat: Script para crear el entorno virtual (venv) e instalar dependencias automáticamente.
- start_silent.vbs: Script para ocultar la consola de comandos.
