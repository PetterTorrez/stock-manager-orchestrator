# Orquestador del Sistema - Docker Compose

Este repositorio centraliza el despliegue contenerizado del proyecto. Utiliza Docker Compose para levantar y comunicar la base de datos, la API y la aplicación web de forma desacoplada.

## 🗂️ Estructura del Entorno

Para que los paths de construcción del `docker-compose.yml` funcionen correctamente, los proyectos deben estar clonados dentro de la misma raíz bajo la siguiente estructura de carpetas:

```text
/
├ repo-orquestador/         # Este repositorio
├──── docker-compose.yml        # Orquestador
├──── web-stock-manager/        # Frontend (Angular)
└──── api-stock-manager/        # Backend (Spring Boot)
```

---

## 🚀 Instrucciones para Levantar el Sistema

Sigue estos pasos para arrancar todo el entorno local en segundos:

### 1. Iniciar los contenedores
Abre una terminal dentro de la carpeta `repo-orquestador` y ejecuta el comando de construcción y arranque:
```bash
docker compose up -d --build
```

### 2. Puertos de Acceso
Una vez levantados los servicios, puedes acceder a los componentes del sistema en las siguientes direcciones:

* 🌐 **[Frontend (Web):](https://github.com/PetterTorrez/web-stock-manager)** `http://localhost:4200`
* ☕ **[Backend (API REST):](https://github.com/PetterTorrez/api-stock-manager)** `http://localhost:8080`
* 🗄️ **Base de Datos (MySQL):** Puerto `3306`

---

## 🛑 Detener el Sistema

Para apagar los servicios y limpiar los volúmenes de datos creados, ejecuta:
```bash
docker compose down -v
```
