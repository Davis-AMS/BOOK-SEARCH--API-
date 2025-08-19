# BOOK-SEARCH--API-
API REST para buscar y gestionar libros 
API REST para **buscar y gestionar libros** con base de datos **H2 en memoria**.

## 🧰 Stack
- Spring Boot **3.2.5**
- Java **17**
- Spring Data JPA
- H2 (in-memory)

## 🚀 Cómo ejecutar
1. Requisitos: Java 17 y Maven 3.9+.
2. Descomprime este proyecto y ábrelo como **Maven Project** en tu IDE.
3. Desde terminal, en la carpeta del proyecto:
   ```bash
   mvn spring-boot:run
   ```
4. La API quedará disponible en: `http://localhost:8080/api/libros`  
5. Consola H2: `http://localhost:8080/h2-console`  
   - JDBC URL: `jdbc:h2:mem:booksdb`
   - User: `sa`, Password: *(vacío)*

## 📦 Datos de ejemplo
Se cargan automáticamente desde `src/main/resources/data.sql`.

## 🔗 Endpoints
- **Listar todo**
  ```http
  GET /api/libros
  ```
- **Obtener por ID**
  ```http
  GET /api/libros/{id}
  ```
- **Buscar por título**
  ```http
  GET /api/libros/buscar/titulo?q=quijote
  ```
- **Buscar por autor**
  ```http
  GET /api/libros/buscar/autor?q=cervantes
  ```
- **Buscar por categoría**
  ```http
  GET /api/libros/buscar/categoria?q=novela
  ```
- **Crear libro**
  ```http
  POST /api/libros
  Content-Type: application/json

  {
    "titulo": "El Principito",
    "autor": "Antoine de Saint-Exupéry",
    "categoria": "Fábula",
    "anioPublicacion": 1943
  }
  ```

## 🛠 Notas
- Ajusta el `language level` del proyecto a **Java 17** en tu IDE si es necesario.
- Puedes cambiar `spring.jpa.hibernate.ddl-auto` a `create` si quieres recrear el esquema en cada arranque.

---
Hecho con ❤️ para pruebas rápidas.
