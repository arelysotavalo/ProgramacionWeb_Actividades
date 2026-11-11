# Perfil Profesional — Emanuel Jácome

## Descripción del proyecto

Este proyecto consiste en el desarrollo de un sitio web de presentación profesional, en el que se muestra información sobre mi formación académica, intereses profesionales y conocimientos relacionados con la Ingeniería en Software.

El sitio web fue desarrollado utilizando HTML5 para estructurar el contenido y CSS3 para mejorar su presentación visual. Además, se implementó un contenedor Docker con Nginx para ejecutar la página web en un entorno independiente.

## 1. Objetivo del proyecto

Desarrollar un sitio web de presentación profesional utilizando HTML5 y CSS3, aplicando principios de diseño web y utilizando Docker con Nginx para facilitar su ejecución y distribución mediante Docker Hub.

## 2. Tecnologías utilizadas

HTML5 -> Estructuración del contenido del sitio web.                         
CSS3 -> Diseño visual, colores, tipografía y distribución de los elementos. 
Docker -> Creación y ejecución de contenedores.                               
Nginx -> Servidor web utilizado para publicar el sitio.                      
Git -> Control de versiones del proyecto.                                  
GitHub -> Almacenamiento y publicación del código fuente.                     
Docker Hub -> Almacenamiento y distribución de la imagen Docker.                  
Visual Studio Code -> Editor utilizado para desarrollar el proyecto.                      

## 3. Estructura del proyecto

```text
perfil_profesional/
│
├── Dockerfile
├── index.html
├── estilos.css
├── foto_perfil.jpg
└── README.md
```

**Descripción de los archivos:**

* `index.html`: contiene la estructura y el contenido de la página web.
* `estilos.css`: contiene los estilos visuales del sitio.
* `foto_perfil.jpg`: imagen utilizada en la presentación profesional.
* `Dockerfile`: contiene las instrucciones para construir la imagen Docker con Nginx.
* `README.md`: documentación del proyecto.

## 4. Construcción de la imagen Docker

Para construir la imagen es necesario tener Docker instalado y en ejecución.

Primero, abrir una terminal en la carpeta principal del proyecto.

Ejecutar el siguiente comando:

```bash
docker build -t perfil-profesional-html .
```

Este comando construye una imagen Docker utilizando las instrucciones del archivo `Dockerfile`.

## 5. Ejecución del contenedor Docker

Una vez construida la imagen, ejecutar:

```bash
docker run -d -p 8085:80 --name perfil-web perfil-profesional-html
```

El comando permite ejecutar el servidor Nginx dentro de un contenedor Docker.

Para verificar que el contenedor se encuentra funcionando:

```bash
docker ps
```

Para detener el contenedor:

```bash
docker stop perfil-web
```

Para volver a iniciarlo:

```bash
docker start perfil-web
```

## 6. Visualización del sitio web

Una vez iniciado el contenedor, abrir un navegador e ingresar:

**http://localhost:8085**

El sitio mostrará la información profesional y académica desarrollada en HTML5 y CSS3.

## 7. Imagen publicada en Docker Hub

La imagen Docker del proyecto se encuentra publicada en el siguiente repositorio:

**Docker Hub:** https://hub.docker.com/r/ejacome9/perfil-profesional-html

También es posible descargar la imagen mediante:

```bash
docker pull ejacome9/perfil-profesional-html:latest
```

Para ejecutar directamente la imagen descargada:

```bash
docker run -d -p 8085:80 --name perfil-web ejacome9/perfil-profesional-html:latest
```

## 8. Repositorio de GitHub

El código fuente del proyecto está disponible en:

**GitHub:** https://github.com/EmaPinea/perfil-profesional

## 9. Autor

**Emanuel Jácome**

Estudiante de Ingeniería en Software.

Universidad de las Fuerzas Armadas — ESPE.

## 10. Conclusión

El desarrollo de este proyecto permitió aplicar conocimientos de HTML5 y CSS3 para construir un sitio web de presentación profesional. Asimismo, se utilizaron Docker y Nginx para ejecutar el proyecto dentro de un contenedor, facilitando su distribución mediante Docker Hub y el almacenamiento de su código fuente en GitHub.