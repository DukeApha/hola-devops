# 🚀 Hola DevOps con Python y Docker

Este proyecto demuestra el ciclo básico de DevOps mediante la creación, contenedorización y despliegue de una aplicación web simple utilizando Python (Flask) y Docker.

---

## 📌 Descripción

Se desarrolló una aplicación web "Hola Mundo" en Python usando Flask, la cual fue empaquetada en un contenedor Docker y publicada en Docker Hub para su distribución.

---

## 🛠️ Tecnologías utilizadas

* Python 3.10
* Flask
* Docker

---

## 📁 Estructura del proyecto

```
hola-devops/
│
├── app.py
├── requirements.txt
└── Dockerfile
```

---

## ⚙️ Instalación y ejecución

### 🔹 1. Clonar el repositorio

```
git clone https://github.com/tuusuario/hola-devops.git
cd hola-devops
```

---

### 🔹 2. Construir la imagen Docker

```
docker build -t hola-devops .
```

---

### 🔹 3. Ejecutar el contenedor

```
docker run -p 8080:80 hola-devops
```

---

### 🔹 4. Acceder a la aplicación

Abrir en el navegador:

```
http://localhost:8080
```

---

## 🐳 Imagen en Docker Hub

La imagen de la aplicación está disponible en:

👉 https://hub.docker.com/r/luisadameshernandez/hola-devops

Para descargarla:

```
docker pull luisadameshernandez/hola-devops:latest
```

Y ejecutarla:

```
docker run -p 8080:80 luisadameshernandez/hola-devops
```

---

## 📦 Dockerfile

```dockerfile
FROM python:3.10-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 80

CMD ["python", "app.py"]
```

---

## 📌 Resultados

* Aplicación web funcional desplegada en contenedor
* Imagen Docker creada correctamente
* Imagen publicada en Docker Hub
* Acceso vía navegador verificado

---

## 🎯 Conclusión

Este proyecto evidencia el flujo básico de DevOps:

1. Desarrollo de aplicación
2. Contenerización con Docker
3. Publicación en Docker Hub
4. Ejecución en entorno aislado

---

## 👤 Autor

Luis Manuel Adames
Ingeniero de Software

---
