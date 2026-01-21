# 📘 Moodle + Docker Compose

Este proyecto proporciona un entorno completo para ejecutar Moodle utilizando Docker Compose, facilitando la instalación, configuración y despliegue local. Incluye servicios para:
- Servidor web + PHP
- Base de datos (MySQL/MariaDB)
- Volúmenes persistentes
- Configuración modular y fácil de extender




## 🚀 Requisitos previos

Asegúrate de tener instalado:

- Docker
- Docker Compose
- Git (opcional, si clonas el repositorio)


## 📁 Estructura del proyecto

``` plaintext
├── compose.yml 
└── Dockerfile

```


## ⚙️ Configuración inicial

- clona el repositorio

``` bash
git clone <tu-repo>
cd <tu-repo>
```




## ▶️ Levantar el entorno

 Ejecuta:

 ``` bash
 docker compose up -d
 ```

Esto iniciará:

- Moodle en http://localhost:8080

- Base de datos accesible internamente desde el contenedor
## 🛠️ Variables de entorno

Puedes personalizar tu compose.yml con variables como:

- MOODLE_DB_HOST

- MOODLE_DB_USER

- MOODLE_DB_PASSWORD

- MOODLE_DB_NAME

Ejemplo

```yaml
environment:
  - MOODLE_DB_HOST=db
  - MOODLE_DB_USER=moodle
  - MOODLE_DB_PASSWORD=secret
  - MOODLE_DB_NAME=moodle
```
Detener el entorno
```bash
docker compose down
```
## 🔐 Acceso a la base de datos

Si usas MariaDB/MySQL:
```bash
  docker exec -it <nombre-contenedor-db> mysql -u root -p

```


## Authors
- Backend Developer & DevOps Jr
- [@renzomedina](https://github.com/RenzoMedina)

