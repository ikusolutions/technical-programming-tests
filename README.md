# 🧪 Prueba Técnica – Desarrollador(a) FullStack Junior (React + Python/FastAPI)

## 🎯 Objetivo General

Crear una pequeña aplicación **FullStack** que permita visualizar y administrar una lista de **clientes y sus pedidos**.

El sistema debe contar con un frontend en **React**, un backend en **FastAPI**, y una base de datos en **PostgreSQL**. De forma opcional, puede simular la integración con **Odoo ERP** para obtener detalles adicionales de los clientes.

---

## 🧩 Parte 1 – Backend (Python + FastAPI)

### Requisitos:

1. Crear una API RESTful con FastAPI con los siguientes endpoints:

   - `GET /clients`: Listar todos los clientes
   - `POST /clients`: Crear un nuevo cliente
   - `GET /clients/{client_id}/orders`: Ver pedidos del cliente
   - `POST /clients/{client_id}/orders`: Crear un nuevo pedido

2. Estructura de datos:

```json
Client {
  id: int,
  name: str,
  email: str,
  created_at: datetime
}

Order {
  id: int,
  client_id: int,
  product: str,
  quantity: int,
  total_price: float,
  created_at: datetime
}
```

3. Validación básica con Pydantic (por ejemplo, email válido, cantidad mayor a 0, etc.)

4. Documentación de la API generada automáticamente con Swagger.

**Bonus (opcional):**

- Simular integración con Odoo (por ejemplo, un endpoint `GET /odoo/clients/{id}` que retorne data simulada).

---

## 🎨 Parte 2 – Frontend (React + Chart.js)

### Requisitos:

1. Crear una SPA con React que permita:

   - Ver la lista de clientes.
   - Crear un nuevo cliente (formulario).
   - Ver pedidos de un cliente.
   - Crear un nuevo pedido.

2. Utilizar Axios o Fetch para consumir la API creada.

3. Mostrar un gráfico de **pedidos por cliente** usando **Chart.js** (puede ser de barras o pastel).

**Bonus (opcional):**

- Uso de TypeScript.
- Uso de React Router para manejar vistas.

---

## 🗃 Parte 3 – Base de Datos (PostgreSQL)

### Requisitos:

- Crear un esquema sencillo para `clients` y `orders` en PostgreSQL.
- Conectar la API a la base de datos (usando SQLAlchemy o directamente con asyncpg, etc.)

**Bonus (opcional):**

- Archivo `docker-compose.yml` que levante la API y la base de datos.

---

## 🧪 Evaluación Técnica

### Lo que se evaluará:

- Calidad y estructura del código.
- Correcta separación de responsabilidades (lógica de negocio vs controladores).
- Uso adecuado de React y buenas prácticas de frontend.
- Diseño visual básico pero funcional.
- Conexión exitosa entre frontend y backend.
- Uso de control de versiones (Git, mínimo 3 commits claros).
- Comentarios y documentación (README con instrucciones para correr el proyecto).

---

## 📦 Entregables

- Repositorio **privado** en GitHub con el código fuente.
- Dar acceso al usuario **`iku-solutions`** como colaborador para permitir la revisión.
- Instrucciones claras para correr el proyecto (README).
- Capturas o video corto si no logra conectar todo, explicando el flujo.
