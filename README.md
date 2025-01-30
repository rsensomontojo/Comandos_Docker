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

### 🚀 Espero que esta lista te ayude a gestionar Docker de manera eficiente. 💪

