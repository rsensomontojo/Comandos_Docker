# Comandos Docker - Docker Cheat Sheet

## 📉 Información básica de Docker
| Comando | Descripción |
|---------|------------|
| `docker version` | Muestra la versión de Docker instalada. |
| `docker info` | Muestra información detallada del sistema Docker. |
| `docker system df` | Muestra el uso del disco por imágenes, contenedores y volúmenes. |

---

## 📦 Gestión de imágenes
| Comando | Descripción |
|---------|------------|
| `docker images` | Lista todas las imágenes locales. |
| `docker pull <imagen>` | Descarga una imagen desde Docker Hub. |
| `docker rmi <imagen>` | Elimina una imagen. |
| `docker build -t <nombre> .` | Construye una imagen desde un Dockerfile. |
| `docker tag <imagen> <nombre:nueva_etiqueta>` | Etiqueta una imagen con otro nombre. |
| `docker push <nombre>` | Sube una imagen a Docker Hub. |

---

## 📋 Gestión de contenedores
| Comando | Descripción |
|---------|------------|
| `docker ps` | Lista los contenedores en ejecución. |
| `docker ps -a` | Lista todos los contenedores (incluidos los detenidos). |
| `docker run -d --name <nombre> <imagen>` | Ejecuta un contenedor en segundo plano. |
| `docker stop <contenedor>` | Detiene un contenedor. |
| `docker start <contenedor>` | Inicia un contenedor detenido. |
| `docker restart <contenedor>` | Reinicia un contenedor. |
| `docker rm <contenedor>` | Elimina un contenedor. |
| `docker exec -it <contenedor> bash` | Accede a la terminal de un contenedor en ejecución. |
| `docker logs <contenedor>` | Muestra los logs de un contenedor. |

---

## 📂 Gestión de volúmenes y redes
### 🔹 Volúmenes
| Comando | Descripción |
|---------|------------|
| `docker volume ls` | Lista los volúmenes creados. |
| `docker volume create <nombre>` | Crea un volumen. |
| `docker volume rm <nombre>` | Elimina un volumen. |
| `docker volume inspect <nombre>` | Muestra información de un volumen. |

### 🔹 Redes
| Comando | Descripción |
|---------|------------|
| `docker network ls` | Lista las redes disponibles. |
| `docker network create <nombre>` | Crea una red. |
| `docker network rm <nombre>` | Elimina una red. |
| `docker network inspect <nombre>` | Muestra detalles de una red. |
| `docker network connect <red> <contenedor>` | Conecta un contenedor a una red. |
| `docker network disconnect <red> <contenedor>` | Desconecta un contenedor de una red. |

---

## 📊 Monitoreo y estadísticas
| Comando | Descripción |
|---------|------------|
| `docker stats` | Muestra en tiempo real el uso de recursos de los contenedores. |
| `docker top <contenedor>` | Muestra los procesos corriendo en un contenedor. |
| `docker inspect <contenedor/imagen>` | Muestra información detallada de un contenedor o imagen. |
| `docker events` | Muestra eventos en tiempo real del sistema Docker. |

---

## 🛠️ Limpieza y mantenimiento
| Comando | Descripción |
|---------|------------|
| `docker system prune` | Elimina contenedores, redes y volúmenes no utilizados. |
| `docker system prune -a` | Elimina TODO lo no usado, incluidas imágenes no referenciadas. |
| `docker container prune` | Elimina contenedores detenidos. |
| `docker volume prune` | Elimina volúmenes no utilizados. |
| `docker image prune` | Elimina imágenes sin usar. |

---


# Comandos Básicos de Docker Compose

## 1️⃣ Iniciar y Gestionar Contenedores

| Comando                        | Descripción                                          |
|---------------------------------|------------------------------------------------------|
| `docker-compose up`             | Inicia los contenedores definidos en `docker-compose.yml`. |
| `docker-compose up -d`          | Inicia los contenedores en **segundo plano** (modo desatendido). |
| `docker-compose down`           | Detiene y elimina los contenedores, pero mantiene volúmenes y redes. |
| `docker-compose down -v`        | Detiene y elimina contenedores **y los volúmenes asociados**. |
| `docker-compose restart`        | Reinicia todos los contenedores.                    |
| `docker-compose restart <servicio>` | Reinicia un servicio específico.                    |

---

## 2️⃣ Inspección y Monitoreo

| Comando                        | Descripción                                          |
|---------------------------------|------------------------------------------------------|
| `docker-compose ps`             | Lista los contenedores en ejecución.                 |
| `docker-compose logs`           | Muestra los logs de todos los servicios.             |
| `docker-compose logs -f`        | Muestra logs en **tiempo real**.                     |
| `docker-compose logs <servicio>`| Muestra los logs de un servicio específico.          |
| `docker-compose top`            | Muestra los procesos en ejecución dentro de los contenedores. |

---

## 3️⃣ Ejecutar Comandos Dentro de Contenedores

| Comando                        | Descripción                                          |
|---------------------------------|------------------------------------------------------|
| `docker-compose exec <servicio> <comando>` | Ejecuta un comando dentro de un contenedor.          |
| `docker-compose exec mysql bash`| Abre una terminal dentro del contenedor `mysql`.     |
| `docker-compose exec mysql mysql -u usuario -p` | Accede a MySQL dentro del contenedor.                |

---

## 4️⃣ Construcción y Gestión de Imágenes

| Comando                        | Descripción                                          |
|---------------------------------|------------------------------------------------------|
| `docker-compose build`          | Construye las imágenes definidas en `docker-compose.yml`. |
| `docker-compose build --no-cache`| Fuerza la reconstrucción sin usar caché.              |
| `docker-compose down --rmi all` | Elimina contenedores **y sus imágenes asociadas**.   |

---

## 5️⃣ Eliminación y Limpieza

| Comando                        | Descripción                                          |
|---------------------------------|------------------------------------------------------|
| `docker-compose rm`             | Elimina los contenedores sin afectar los volúmenes.  |
| `docker-compose down -v`        | Elimina los contenedores **y volúmenes**.            |

---

### 📌 **¿Necesitas más detalles o algún ejemplo adicional?**

