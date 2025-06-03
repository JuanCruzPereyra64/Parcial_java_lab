# Parcial_java_lab
Parcial de la materia Programacion 2 laboratorio, realizado en java por Juan Cruz Pereyra Muñoz.

Sistema de Gestión de Biblioteca en Java (Consola + JDBC + H2)

Descripción:
Este proyecto es una aplicación de consola en Java para gestionar autores y libros. Usa JDBC con base de datos H2 en modo archivo, implementa el patrón DAO y está organizado en capas.

Cómo ejecutar:

1. Requisitos:
- Java 17 o superior
- Gradle instalado (opcional, incluye wrapper)

2. Clonar repositorio

3. Compilar y ejecutar:
./gradlew run
(En Windows: gradlew.bat run)

Funcionalidades:

Autores:
- Crear autor
- Listar todos los autores
- Buscar autor por ID
- Actualizar autor
- Eliminar autor

Libros:
- Crear libro (con autor existente)
- Listar todos los libros con autor y fecha
- Buscar libro por ID
- Actualizar libro (título, autor, fecha)
- Eliminar libro

Tecnologías y conceptos aplicados:

- Java 17+
- Gradle para gestión y ejecución
- JDBC para conexión con base de datos
- H2 en modo archivo (persistencia)
- Patrón DAO para separar acceso a datos
- Arquitectura en capas: model, dao, daoImpl, util, main
- Clase genérica DAO para reutilización
- Manejo de excepciones y logging con SLF4J
- Validación básica de entradas desde consola
- Relación entre entidades Libro → Autor mediante clave foránea

Estructura del proyecto:

src/
 └── main/
      ├── java/
      │    ├── model/        (clases Autor, Libro)
      │    ├── dao/          (interfaces DAO, GenericDAO)
      │    ├── daoImpl/      (implementaciones DAO)
      │    ├── util/         (conexión DB, inicializador)
      │    └── main/         (clase Main)
      └── resources/

Datos persistentes:

La base de datos H2 crea un archivo en ./data/biblioteca.mv.db donde se guardan los datos.

