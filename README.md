# Manual de Maven para principiantes

![banner](img/MAVEN.png)

## Tabla de Contenido
- [Manual de Maven para principiantes](#manual-de-maven-para-principiantes)
  - [Tabla de Contenido](#tabla-de-contenido)
  - [Conceptos Básicos](#conceptos-básicos)
  - [Comandos Básicos](#comandos-básicos)
  - [Arquetipo Básico](#arquetipo-básico)
  - [Descripción de Parametros](#descripción-de-parametros)
  - [Lista de arquetipos basicos de maven](#lista-de-arquetipos-basicos-de-maven)
  - [Estructura de Arquetipo Basico](#estructura-de-arquetipo-basico)
  - [Únete a la Comunidad Ninja Code](#únete-a-la-comunidad-ninja-code)

## Conceptos Básicos

En esta sección, aprenderás los conceptos fundamentales de Maven:

- **Proyecto Maven:** Un proyecto Maven se organiza en una estructura de directorios específica que incluye fuentes, recursos y configuraciones.

- **POM (Project Object Model):** Es un archivo XML llamado `pom.xml` que describe el proyecto y sus dependencias. Contiene información como el nombre del proyecto, la versión, las dependencias y los plugins.

- **Dependencias:** Son las bibliotecas externas que tu proyecto necesita para funcionar correctamente. Se definen en el archivo `pom.xml`.

- **Fase de Construcción:** Maven organiza las tareas en fases, como `clean`, `compile`, `test`, `package`, etc., que puedes ejecutar en tu proyecto.

- **Repositorio Maven:** Un repositorio en línea donde se almacenan las dependencias de Maven. Maven descarga automáticamente las dependencias de este repositorio.

## Comandos Básicos

Aquí encontrarás información sobre los comandos básicos de Maven que necesitas conocer.

**`mvn clean`**: Limpia el directorio de destino, eliminando todos los archivos generados previamente.

**`mvn compile`**: Compila el código fuente de tu proyecto.

**`mvn test`**: Ejecuta las pruebas unitarias en tu proyecto.

 **`mvn package`**: Empaqueta tu proyecto en un formato específico (por ejemplo, JAR, WAR).

 **`mvn install`**: Instala el artefacto (por ejemplo, un JAR) en el repositorio local de Maven para su uso en otros proyectos.

 **`mvn dependency:tree`**: Muestra un árbol de dependencias de tu proyecto.

 **`mvn clean install`**: Combina las tareas de limpieza y construcción en una sola ejecución.

 
## Arquetipo Básico

Aprenderás sobre los arquetipos básicos en Maven y cómo usarlos.


1. Para crear un nuevo proyecto Maven, ejecuta el siguiente comando:

   ```
   mvn archetype:generate -DgroupId=com.miempresa -DartifactId=mi-proyecto -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
   ```
    Esto generará una estructura de proyecto básica en un directorio llamado `mi-proyecto`.

2. Edita el archivo `pom.xml` para agregar las dependencias de tu proyecto y configurar otros aspectos del proyecto.

3. Ejecuta comandos Maven como `mvn clean compile` o `mvn test` en el directorio de tu proyecto para realizar tareas específicas.

4. Recuerda que Maven descargará automáticamente las dependencias desde el repositorio central de Maven.

## Descripción de Parametros

1. **`-DgroupId`**: Este parámetro se utiliza para especificar el identificador del grupo del proyecto. Es una convención de Maven que se utiliza para organizar los proyectos en una estructura jerárquica. Por lo general, es el dominio inverso de tu organización o empresa.

2. **`-DartifactId`**: Este parámetro define el identificador del artefacto del proyecto. El artefacto es la unidad principal que se crea en el proyecto Maven (por ejemplo, un JAR o un WAR). Debe ser un nombre único para tu proyecto.

3. **`-DarchetypeArtifactId`**: Este parámetro especifica el tipo de arquetipo que se utilizará para crear el proyecto. En el ejemplo, estamos utilizando `maven-archetype-quickstart`, que es un arquetipo predeterminado que crea una estructura de proyecto básica con un directorio de código fuente y pruebas.

4. **`-DinteractiveMode`**: Este parámetro determina si el proceso de creación del proyecto es interactivo o no. Si se establece en `false`, el proceso se ejecuta sin solicitar entrada del usuario. En un entorno de automatización o secuencias de comandos, es común establecerlo en `false`.

La ejecución de este comando generará un proyecto Maven en un directorio llamado `mi-proyecto` en el directorio actual con la estructura básica definida por el arquetipo especificado. Puedes personalizar aún más tu proyecto editando el archivo `pom.xml` y agregando dependencias, configuraciones y otros detalles específicos de tu proyecto.

## Lista de arquetipos basicos de maven

Maven proporciona una variedad de arquetipos para diferentes tipos de proyectos y tecnologías. Puedes ver la lista completa de arquetipos disponibles en el repositorio central de Maven. Para obtener una lista de arquetipos y sus descripciones, puedes usar el siguiente comando:

```bash
mvn archetype:generate -Dfilter=archetype
```

Esto te mostrará una lista de arquetipos disponibles para su selección. A continuación, te proporcionaré una lista de algunos de los arquetipos más utilizados y sus descripciones:

1. **`maven-archetype-quickstart`**:
   - Descripción: Un proyecto Java simple con una estructura básica que incluye código fuente y pruebas unitarias. Es útil para proyectos Java estándar.
   
2. **`maven-archetype-webapp`**:
   - Descripción: Un proyecto web Java EE con una estructura que incluye directorios para recursos web (como HTML y JSP) y archivos de configuración estándar.

3. **`maven-archetype-j2ee-simple`**:
   - Descripción: Un proyecto Java EE simple que incluye ejemplos de Servlets y JSP para comenzar con aplicaciones web empresariales.

4. **`maven-archetype-quickstart-jdk8`**:
   - Descripción: Similar al `maven-archetype-quickstart`, pero configurado para proyectos que utilizan Java 8 o superior.

5. **`maven-archetype-archetype`**:
   - Descripción: Este es el arquetipo utilizado para crear nuevos arquetipos personalizados. No es para proyectos reales, sino para definir plantillas de proyectos.

6. **`maven-archetype-plugin`**:
   - Descripción: Un arquetipo para crear un nuevo plugin Maven. Útil si deseas desarrollar tus propios plugins Maven.

7. **`maven-archetype-site-simple`**:
   - Descripción: Para crear un proyecto simple de sitio web con Maven. Es útil si deseas generar documentación o informes con Maven.

8. **`maven-archetype-ear-jee5`**:
   - Descripción: Para proyectos Java EE 5 que requieren un archivo de implementación de aplicaciones empresariales (EAR).

9. **`maven-archetype-ear-jee6`**:
   - Descripción: Similar al anterior, pero para proyectos Java EE 6.

10. **`maven-archetype-ear-jee7`**:
    - Descripción: Similar a los anteriores, pero para proyectos Java EE 7.

Estos son solo algunos ejemplos de arquetipos disponibles. La elección del arquetipo depende de tu tipo de proyecto y de las tecnologías que estés utilizando. Puedes explorar la lista completa y seleccionar el que mejor se adapte a tus necesidades específicas cuando ejecutes el comando `mvn archetype:generate`.



## Estructura de Arquetipo Basico 

El arquetipo `maven-archetype-quickstart` crea una estructura de proyecto Maven básica que se utiliza comúnmente para proyectos Java estándar. Aquí está la estructura de directorios y archivos que deja este arquetipo:


```
mi-proyecto
│
├── src
│   ├── main
│   │   └── java
│   │       └── com
│   │           └── miempresa
│   │               └── miproyecto
│   │                   └── App.java
│   ├── test
│   │   └── java
│   │       └── com
│   │           └── miempresa
│   │               └── miproyecto
│   │                   └── AppTest.java
│   └── resources
├── target
├── .gitignore
└── pom.xml
```

- `src/main/java`: Este directorio contiene el código fuente de tu proyecto Java. Por defecto, se crea un paquete `com.miempresa.miproyecto` y una clase `App.java` de ejemplo.

- `src/test/java`: Aquí se encuentran las pruebas unitarias de tu proyecto. Al igual que en el directorio de código fuente, se crea un paquete y una clase de prueba de ejemplo (`AppTest.java`).

- `src/main/resources`: Puedes colocar recursos (archivos de configuración, archivos de propiedades, etc.) en este directorio.

- `target`: Este directorio contiene archivos generados durante la compilación y construcción del proyecto. Por ejemplo, los archivos JAR generados se almacenarán aquí.

- `.gitignore`: Un archivo que especifica los archivos y directorios que deben ignorarse cuando se utiliza Git para el control de versiones.

- `pom.xml`: El archivo POM (Project Object Model) que describe tu proyecto y sus dependencias. Debes editar este archivo para agregar o modificar las dependencias de tu proyecto.

Este es un proyecto Maven básico que puedes usar como punto de partida para desarrollar aplicaciones Java estándar. Puedes agregar tus propias clases y recursos a la estructura del proyecto según sea necesario para tu proyecto específico.



[Ver la Licencia](./LICENSE.txt)


## Únete a la Comunidad Ninja Code

¡Gracias por utilizar nuestro Manual de Maven para principiantes! Te invitamos a unirte a la comunidad Ninja Code, donde puedes encontrar más recursos útiles y mantenerte al tanto de las últimas noticias de tecnologia y actualizaciones.

- Suscríbete a nuestro [canal de YouTube](https://www.youtube.com/channel/UCzJuow8qZWO758nWhPFLIPg) para tutoriales en video.
 <!-- - Síguenos en [Twitter](https://twitter.com/ninjacode) para conocer las últimas noticias y publicaciones. -->
- Sigue nuestra pagina en [Facebook](https://www.facebook.com/profile.php?id=100063566781985) para conocer las últimas noticias y publicaciones. 
<!-- - Visita nuestro sitio web en [www.ninjacode.com](https://www.ninjacode.com) para obtener más recursos y tutoriales. -->

¡Esperamos verte en la comunidad Ninja Code y que disfrutes aprendiendo y desarrollando con nosotros!
