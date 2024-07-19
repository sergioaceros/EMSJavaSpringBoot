# Employee Management System Backend

Este proyecto es una aplicación backend para un sistema de gestión de empleados (Employee Management System, EMS) desarrollado con Spring Boot. La aplicación permite realizar operaciones CRUD (Crear, Leer, Actualizar, Eliminar) sobre los empleados.

## Descripción

El Employee Management System Backend proporciona una API RESTful que permite gestionar la información de los empleados en una base de datos Postgresql. Incluye funcionalidades como la creación, obtención, actualización y eliminación de empleados. Además, maneja excepciones de manera centralizada y utiliza una estructura de DTO (Data Transfer Object) para transferir datos entre la capa de presentación y la capa de persistencia.

## Tecnologías Utilizadas

### Backend
- **Java 17**: Lenguaje de programación principal.
- **Spring Boot**: Framework para el desarrollo de aplicaciones Java.
  - **Spring Web**: Para la creación de controladores REST.
  - **Spring Data JPA**: Para la persistencia de datos y la interacción con la base de datos.
  - **Spring Boot Starter Test**: Para pruebas unitarias e integración.
  
### Base de Datos
- **Postgresql**: Base de datos relacional utilizada para almacenar la información de los empleados.

### Construcción y Gestión de Dependencias
- **Maven**: Herramienta de automatización de compilación y gestión de dependencias.

### Pruebas
- **JUnit 5**: Framework de pruebas unitarias.
- **Spring Boot Test**: Extensiones para pruebas de Spring Boot.

### Otros
- **MapStruct**: Biblioteca para la generación automática de mapeos entre entidades y DTOs.
- **IntelliJ IDEA**: Entorno de desarrollo integrado (IDE) utilizado para el desarrollo del proyecto.
- **Git**: Sistema de control de versiones.

## Estructura del Proyecto

- **`src/main/java/com/sergio/ems`**: Contiene el código fuente principal del proyecto.
  - **`controller`**: Controladores REST que manejan las solicitudes HTTP.
    - `EmployeeController.java`: Define los endpoints para las operaciones CRUD de empleados.
  - **`dto`**: Clases de transferencia de datos.
    - `EmployeeDto.java`: Define el objeto de transferencia de datos para los empleados.
  - **`entity`**: Clases de entidad que representan las tablas de la base de datos.
    - `Employee.java`: Define la entidad `Employee`.
  - **`exception`**: Manejo de excepciones.
    - `ResourceNotFoundException.java`: Excepción lanzada cuando un recurso no es encontrado.
  - **`mapper`**: Clases para mapear entre entidades y DTOs.
    - `EmployeeMapper.java`: Define métodos para convertir entre `Employee` y `EmployeeDto`.
  - **`repository`**: Interfaces de repositorio que extienden `JpaRepository` para interactuar con la base de datos.
    - `EmployeeRepository.java`: Repositorio para la entidad `Employee`.
  - **`service`**: Interfaces de servicios que definen la lógica de negocio.
    - `EmployeeService.java`: Interfaz para los servicios relacionados con empleados.
  - **`service/impl`**: Implementaciones de los servicios.
    - `EmployeeServiceImpl.java`: Implementación de `EmployeeService`.

- **`src/main/resources`**: Contiene los archivos de configuración.
  - `application.properties`: Archivo de configuración de Spring Boot.

- **`src/test/java/com/sergio/ems`**: Contiene las pruebas unitarias.
  - `EmsBackendApplicationTests.java`: Pruebas unitarias para la aplicación.

- **Archivos de configuración y construcción**:
  - `.gitignore`: Archivos y directorios que deben ser ignorados por Git.
  - `pom.xml`: Archivo de configuración de Maven.
  - `HELP.md`: Documentación de ayuda generada por Spring Initializr.
  - `mvnw`, `mvnw.cmd`: Scripts de Maven Wrapper.

## Requisitos

- Java 17 o superior
- Maven 3.6.3 o superior
- Base de datos Postgresql
- Postman

## Instalación

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/sergioaceros/EMSJavaSpringBoot.git
   cd ems-backend
