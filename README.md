 Documentación Técnica - Sistema Breanrots
Planteamiento del Problema

Se requiere un sistema capaz de balancear peticiones y gestionar el cargado de datos de productos, integrando un backend en Java (Spring Boot) y un frontend en Angular. El sistema debe permitir la visualización y el alta manual de productos, asegurando una comunicación eficiente entre ambos módulos.

Especificación de Requerimientos
Requerimientos Funcionales

Visualizar un catálogo de productos generado dinámicamente desde el backend.

Permitir la adición manual de productos mediante un formulario web.

Balancear y gestionar múltiples peticiones concurrentes al backend.

Proveer una API REST para la comunicación entre frontend y backend.
Requerimientos No Funcionales

Interfaz web responsiva y amigable, basada en Bootstrap.

Backend escalable, preparado para grandes volúmenes de datos.

Seguridad básica en la comunicación, con CORS habilitado.

Documentación clara y facilidad de despliegue.

Informe General del Sistema

El sistema está compuesto por dos módulos principales:

Backend (Java Spring Boot): expone endpoints REST para la gestión de productos, genera productos de prueba mediante el endpoint /api/products/generate, permite integración con bases de datos relacionales de manera configurable e incluye controladores, servicios y modelos para la lógica de negocio.

Frontend (Angular + Bootstrap): permite visualizar el catálogo de productos en una tabla dinámica, ofrece navegación básica y un formulario para agregar productos manualmente, además consume la API REST del backend utilizando HttpClient.

Manual de Configuración de la Base de Datos

Configurar el archivo application.properties en el backend con la URL de la base de datos, usuario y contraseña, así como el parámetro spring.jpa.hibernate.ddl-auto en modo update.

Crear la base de datos en el gestor, por ejemplo en MySQL con el comando CREATE DATABASE breanrotsdb.

Verificar que el driver JDBC correspondiente esté declarado en el archivo pom.xml.

Al iniciar, el backend generará automáticamente las tablas necesarias en la base de datos configurada.

Manual de Usuario
Inicio

Para iniciar, se debe acceder al frontend en la dirección http://localhost:4200
. Desde allí, hacer clic en el botón “Visualizar” para ver el catálogo de productos.

 Agregar Producto

Para agregar un producto, se debe navegar a la opción de “Agregar Producto”, completar el formulario con los datos requeridos y presionar el botón “Agregar”. El nuevo producto aparecerá en la lista principal.

Requisitos

Para el correcto funcionamiento, el backend debe estar corriendo en http://localhost:8080
 y el frontend en http://localhost:4200
.

Tecnologías Utilizadas

El sistema utiliza como backend Java 17, Spring Boot, Spring Data JPA y MySQL. En el frontend se emplean Angular, Bootstrap y TypeScript. Para la infraestructura y gestión del proyecto se usa Maven y GitHub.

 
