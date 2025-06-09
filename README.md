# Sistema de Gestión Comercial - Java Web EE
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
![Apache Tomcat](https://img.shields.io/badge/apache%20tomcat-%23F8DC75.svg?style=for-the-badge&logo=apache-tomcat&logoColor=black)

## Descripción
Sistema web desarrollado en Java EE para la gestión de clientes, productos y pedidos. Implementa un sistema CRUD (Create, Read, Update, Delete) completo con autenticación de usuarios y manejo de sesiones.

## Características
- Autenticación de usuarios
- Gestión de clientes
- Gestión de productos
- Gestión de pedidos
- Interfaz web responsiva
- Conexión a base de datos MySQL

## Requisitos Previos
- JDK 1.8 (Java 8) - No compatible con versiones superiores
- Java EE 7 API
- Apache Tomcat 8.5
- MySQL 5.7 o superior
- NetBeans IDE 8.2 o superior con soporte para Java EE

### Dependencias específicas
- Java EE Web API 8.0
- JSTL 1.2
- MySQL Connector/J compatible con Java 8

### Notas de Compatibilidad
- El proyecto está desarrollado específicamente para Java 8
- No es compatible con JDK 9 o superior debido a cambios en los módulos
- Requiere específicamente Java EE 7 para su funcionamiento

## Configuración del Proyecto

### 1. Base de Datos
1. Crear una base de datos MySQL llamada `bd_rest`
2. Importar el script `bd_rest.sql` proporcionado en la raíz del proyecto

### 2. Configuración de la Conexión
Modificar el archivo `src/java/conexion/conexionBD.java`:
```java
static String url="jdbc:mysql://localhost:3306/bd_rest";
static String user="root";
static String pass="tu_contraseña";
```

### 3. Dependencias
El proyecto requiere las siguientes librerías en `WEB-INF/lib/`:
- `mysql-connector-java-x.x.xx.jar`
- `jstl-1.2.jar`
- `standard-1.1.2.jar`

## Estructura del Proyecto
```
ProyectWebDist/
├── src/
│   └── java/
│       ├── conexion/     # Clase de conexión a BD
│       ├── Controler/    # Controladores servlet
│       └── Entidades/    # Modelos de datos
├── web/
│   ├── WEB-INF/         # Configuración y librerías
│   └── *.jsp            # Vistas del sistema
└── bd_rest.sql          # Script de la base de datos
```

## Despliegue
1. Compilar el proyecto
2. Desplegar el archivo WAR generado en Tomcat
3. Acceder a través de: `http://localhost:8080/ProyectWebDist`

## Credenciales por Defecto
- Usuario: admin
- Contraseña: 1234

## Funcionalidades Principales
- **Gestión de Clientes**: CRUD completo de información de clientes
- **Gestión de Productos**: Catálogo de productos con precios
- **Gestión de Pedidos**: Sistema de pedidos vinculado a clientes

## Tecnologías Utilizadas
- Java EE
- Servlets & JSP
- JSTL
- MySQL
- Bootstrap (para el frontend)
- JavaScript

## Autores
- Nelson Correa

## Licencia
Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.