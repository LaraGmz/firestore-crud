# Firestore CRUD API con FastAPI

**API REST con operaciones CRUD integrado con Firestore y autenticación de Firebase, con despliegue en Azure.**

## Descripción

Este proyecto implementa una API CRUD segura utilizando FastAPI, Firebase Auth y Firestore.

Permite:

- Registrar e iniciar sesión de usuarios.
- Crear, leer, actualizar y eliminar documentos.
- Despliegue en Azure Service.

## Tecnologías

- Python 3.10+
- FastAPI
- Firebase Auth
- Firebase Firestore
- Azure App Service

## Estructura del proyecto

.
├── services/
│ └── firebase.json # Clave del Service Account (IGNORADA en git)
├── src/
│ ├── config/ # Configuración general
│ ├── models/ # Modelos Pydantic
│ ├── routes/ # Endpoints de la API
│ ├── services/ # Lógica de negocio
│ └── main.py # Punto de entrada de la app
├── tests/ # Pruebas unitarias
├── .env # Variables de entorno
├── .gitignore
├── requirements.txt
└── README.md

## Instalación y ejecución

1. Clonar el repositorio
   git clone https://github.com/usuario/firestore-crud.git

2. Crear entorno virtual
   python -m venv venv
   source venv/bin/activate # Mac/Linux
   venv\Scripts\activate # Windows

3. Instalar dependencias
   pip install -r requirements.txt

4. Cargar archivo .env

5. Ejecutar
   uvicorn src.main:app --reload

## Endpoints principales

- POST /auth/signup → Registro de usuario

- POST /auth/login → Inicio de sesión

- GET /items → Listar todos los recursos

- POST /items → Crear recurso

- PUT /items/{id} → Actualizar recurso

- DELETE /items/{id} → Eliminar recurso
