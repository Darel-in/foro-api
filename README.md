# API REST - Foro

API REST desarrollada con **Java y Spring Boot 3** que permite gestionar tópicos dentro de un foro.
Los usuarios pueden crear preguntas o sugerencias y otros usuarios pueden consultarlas, actualizarlas o eliminarlas mediante endpoints REST.

Este proyecto fue desarrollado como práctica de construcción de APIs seguras utilizando **Spring Boot, Spring Security y JWT**.

---

# Tecnologías utilizadas

* Java 17
* Spring Boot 3
* Maven
* Spring Data JPA
* Spring Security
* JWT (JSON Web Token)
* Flyway Migration
* MySQL
* Lombok
* Insomnia / Postman para pruebas de API

---

# Funcionalidades de la API

La API permite:

* Crear un nuevo tópico
* Listar todos los tópicos
* Obtener el detalle de un tópico
* Actualizar un tópico
* Eliminar un tópico
* Autenticación de usuarios mediante JWT

---

# Endpoints principales

## Autenticación

```
POST /login
```

Permite autenticar un usuario y obtener un **token JWT** para acceder a los endpoints protegidos.

---

## Crear tópico

```
POST /topicos
```

Crea un nuevo tópico en el foro.

Requiere autenticación mediante **JWT**.

---

## Listar tópicos

```
GET /topicos
```

Devuelve la lista de todos los tópicos registrados.

---

## Detalle de un tópico

```
GET /topicos/{id}
```

Muestra la información completa de un tópico específico.

---

## Actualizar tópico

```
PUT /topicos/{id}
```

Permite modificar un tópico existente.

Requiere autenticación.

---

## Eliminar tópico

```
DELETE /topicos/{id}
```

Elimina un tópico de la base de datos.

Requiere autenticación.

---

# Base de datos

La aplicación utiliza **MySQL** como sistema de base de datos.

Tabla principal:

```
topicos
```

Campos:

* id
* titulo
* mensaje
* fecha_creacion
* status
* autor
* curso

---

# Estructura del proyecto

El proyecto sigue una arquitectura típica de **Spring Boot**:

```
src/main/java
└── com.nayeli.foro
    ├── controller
    ├── domain
    ├── repository
    ├── service
    └── security
```

---

# Pruebas de la API

Las funcionalidades de la API pueden probarse utilizando herramientas como:

* Insomnia
* Postman

Ejemplo de URL base:

```
http://localhost:8080
```

---

# Objetivo del proyecto

Este proyecto tiene como objetivo practicar:

* Desarrollo de APIs REST con Spring Boot
* Implementación de seguridad con JWT
* Persistencia de datos con JPA
* Migraciones de base de datos con Flyway
* Buenas prácticas en desarrollo backend

---

# Autor

Proyecto desarrollado por **Nayeli Darel** como parte de su formación en desarrollo backend con **Java y Spring Boot**.
