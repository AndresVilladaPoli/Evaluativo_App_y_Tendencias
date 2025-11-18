  Aplicación POLIsales


POLIsales es una plataforma web desarrollada para la comunidad universitaria con el objetivo de facilitar la publicación, venta y llegada de artículos como libros, equipos, material académico y habitaciones. La aplicación permite gestionar las publicaciones mediante un módulo CRUD completo implementado en el frontend y consumiendo servicios desde el backend.
El sistema incluye un módulo de informes donde los registros almacenados en la base de datos son recuperados como JSON, convertidos a XML en el backend y presentados en una vista dedicada. Esta vista muestra el árbol XML, el valor total acumulado de los artículos y los porcentajes de participación de cada categoría, lo que permite analizar la composición del inventario publicado.

La arquitectura sigue un modelo cliente–servidor sencillo basado en tecnologías web ligeras. El frontend, ubicado en la carpeta public/, está compuesto por vistas HTML que implementan tanto el CRUD como la visualización del informe XML. El backend está desarrollado con Node.js y Express, proporcionando endpoints REST para gestionar las publicaciones, procesar los datos y generar archivos XML a partir de la información en formato JSON. La persistencia se maneja mediante una base de datos SQLite, almacenada localmente en el archivo “database.db”.

<img width="698" height="302" alt="Arquitectura" src="https://github.com/user-attachments/assets/edd6f70e-07b2-4403-aa69-dd52f0ad2688" />


El diagrama de clases representa la estructura lógica del sistema mostrando los módulos conceptuales y sus responsabilidades dentro del proyecto. Cada clase incluye sus atributos o métodos principales, y las relaciones indican cómo interactúan los componentes entre sí. Aunque el proyecto está implementado en Node.js sin clases formales, el diagrama se utiliza de manera conceptual para ilustrar los elementos funcionales: el controlador que gestiona las operaciones CRUD, el servicio que transforma JSON a XML y la capa de acceso a datos que interactúa con SQLite. La clase “Publicación” aparece sin relaciones directas porque funciona como un modelo de datos representado en JSON, no como una clase instanciada en el código.

<img width="509" height="490" alt="Diagrama de Clases" src="https://github.com/user-attachments/assets/f9eae736-d433-4820-b2f5-5e8ee8e9857c" />
