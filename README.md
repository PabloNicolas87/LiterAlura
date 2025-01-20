# Proyecto Litealura

Este proyecto es una aplicación de consola en Java que permite buscar libros a través de una API, registrar libros y autores en una base de datos, y listar libros y autores registrados.

## Requisitos

- Java 11 o superior
- Maven
- PostgreSQL

## Configuración

1. Clona el repositorio:

    ```sh
    git clone https://github.com/tu-usuario/tu-repositorio.git
    cd tu-repositorio
    ```

2. Configura la base de datos PostgreSQL y actualiza el archivo `application.properties` con tus credenciales:

    ```ini
    spring.datasource.url=jdbc:postgresql://localhost/literalura
    spring.datasource.username=tu-usuario
    spring.datasource.password=tu-contraseña
    spring.datasource.driver-class-name=org.postgresql.Driver
    hibernate.dialect=org.hibernate.dialect.HSQLDialect
    spring.jpa.show-sql=true
    spring.jpa.format-sql=true
    spring.jpa.hibernate.ddl-auto=update
    ```

3. Agrega el archivo `application.properties` a `.gitignore` para evitar subir tus credenciales al repositorio:

    ```plaintext
    # .gitignore
    src/main/resources/application.properties
    ```

4. Compila y ejecuta la aplicación:

    ```sh
    mvn clean install
    mvn spring-boot:run
    ```

## Uso

Al ejecutar la aplicación, se mostrará un menú con las siguientes opciones:

1. Buscar libro por título
2. Listar libros registrados
3. Listar autores registrados
4. Listar autores vivos en un determinado año
5. Listar libros en un determinado idioma
6. Salir

Selecciona una opción ingresando el número correspondiente y sigue las instrucciones en pantalla.

## Estructura del Proyecto

- `src/main/java/br/com/alura/challenge/litealura`: Contiene las clases principales de la aplicación.
- `src/main/resources`: Contiene los archivos de configuración, incluyendo `application.properties`.

## Contribuciones

Las contribuciones son bienvenidas. Por favor, abre un issue o un pull request para discutir cualquier cambio que desees realizar.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.
