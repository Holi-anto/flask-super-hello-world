# flask-super-hello-world
![](https://images.unsplash.com/photo-1579403124614-197f69d8187b)¡Hola! Hoy tendremos nuestro segundo laboratorio del módulo **Software Libre de alta productividad.**.Este repositorio trae sólo estas instrucciones. Con ellas podrás crear una Web App en tu cuenta de GitHub.## ObjetivoCrear nuestra aplicación web profesional bajo la URL`PRODUCTION_URL=TU-FRAMEWORK-WEB.onrender.com`La estructura de nuestro proyecto será de la siguiente forma```shell
├── templates
  ├ index.html
  ├ welcome.html
├── .gitignore
├── app.py
├── LICENCE
├── README.md
├── requirements.txt
```NOTA: Recuerda que este repositorio solo contiene las instrucciones y NO lo necesitamos clonar este repositorio.## Actividad 11 - Abrte en una nueva pestaña la siguiente página: [https://github.com/booleancl/flask-super-hello-world](https://github.com/booleancl/flask-super-hello-world). Procura seleccionar tu cuenta personal. El nombre del proyecto debe ser:`flask-super-hello-world`2 - Busca las instrucciones del laboratorio pasado e identifica como vincular este nuevo proyecto llamado `flask-super-hello-world` a **render.com** al igual que lo hicimos con el proyecto anterior.3 - Navega a través de la Terminal hacia tu carpeta de proyectos, luego utiliza `git clone` y la URL SSH del proyecto `flask-super-hello-world` para DESCARGAR el proyecto en tu computador. Una vez descargado a través de clonar, navega hacia la carpeta recién descargada y ejecuta `code .`4 - Una vez abierto el proyecto en Visual Studio Code, compara el proyecto anterior con este:
**¿Que carpeta no está presente en esta oportunidad?**Modifica el proyecto para incluir esta carpeta y el archivo correspondiente.Pista: En la sección *Objetivo* de estas instrucciones también podrás ver cual es esta carpeta.5 - Compara el proyecto anterior con este:*¿Que diferencias tiene el archivo `app.py` anterior con el actual que tenemos?*Modifica el archivo `app.py` para que quede exactamente igual con el proyecto del laboratorio pasado.6 - Lista la Actividad 1, ya deberías utilizar los comandos de Git `add`, `commit` y `push`.---## Actividad 21 - A estas alturas ya deberías tener un archivo `index.html`. Reemplazado TODO su contenido con el siguiente:**index.html**```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mi Aplicación Web| Ingreso</title>  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css" rel="stylesheet"
    integrity="sha384-KK94CHFLLe+nY2dmCWGMq91rCGa5gtU4mk92HdvYe+M/SXH301p5ILy+dN9+nJOZ" crossorigin="anonymous">
</head>
<body>
  <h1>Mi Aplicación Web</h1>  <form action="welcome">
    <label for="username">Tu Nombre</label>
    <input type="text" name="username">    <input type="submit">
  </form>  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.bundle.min.js"
    integrity="sha384-ENjdO4Dr2bkBIFxQpeoTz1HIcje39Wm4jDKdf19U8gI4ddQ3GYNS7NTKfAdVQSZe"
    crossorigin="anonymous"></script>
</body>
</html>```2 - En la misma carpeta donde está el archivo `index.html`, crea un nuevo archivo llamado `welcome.html` con el siguiente contenido:```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mi Aplicación Web| Bienvenido</title>  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css" rel="stylesheet"
    integrity="sha384-KK94CHFLLe+nY2dmCWGMq91rCGa5gtU4mk92HdvYe+M/SXH301p5ILy+dN9+nJOZ" crossorigin="anonymous">
</head>
<body>
  <h1>Hola {{ user }}</h1>  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.bundle.min.js"
    integrity="sha384-ENjdO4Dr2bkBIFxQpeoTz1HIcje39Wm4jDKdf19U8gI4ddQ3GYNS7NTKfAdVQSZe"
    crossorigin="anonymous"></script>
</body>
</html>```3 - Modifica el archivo `app.py` para que quede de la siguiente forma:```py
from flask import Flask, render_template, request
app = Flask(__name__)@app.route('/')
def hello_world():
    return render_template('index.html')@app.route('/welcome')
def welcome():
    return render_template('welcome.html', user = request.args.get('username'))
```Modifica el archivo `welcome.html`4 - Lista la Actividad 2, ya deberías utilizar los comandos de Git `add`, `commit` y `push`.---## Actividad FinalActualiza el archivo `assigment-url` con la URL de render.com de tu aplicación en este repositorio y haz los comandos de Git para actualizar este repositorio.NOTA: Agregar esta URL es en ESTE repositorio y NO en el proyecto `flask-super-hello-world`