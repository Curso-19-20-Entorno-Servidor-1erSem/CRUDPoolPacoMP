# CRUDPoolPacoMP
Proyecto CRUD: Create, Read, Unifique, Delete. Se renombra proyecto. Nombre del anterior Proyecto: CRUDFranciscoAMP.

## Introducción.
Creación de proyecto **CRUDPoolFranciscoAMP** en el que se crean, actualizan, eliminan y muestran datos de las aves de la tabla aves de la base de datos *pruebajava*.

Antes de empezar, se ha procedido a eliminar todos los registros de la tabla *aves* de la base de datos *pruebasjava*, con el comando

~~~
TRUNCATE TABLE aves;
~~~

Además se madifica el valor del campo *fecha* por *DATE*, anteriormente *VARCHAR*.

~~~
ALTER TABLE aves MODIFY fecha DATE not null;
~~~

Se añade dependencia de **Mysql** en el archivo ***pom.xml***

Se configura conexión a la base de datos.

Se estrutura de la siguiente manera:

Dentro de Web Pages sustituimos el ***index.html*** por el archivo ***index.jsp***.

Creamos los directorios:
- **CSS**. Se copia el archivo de estilos del proyecto AccesoDirecto. En este archivo es donde van los estilos de todas las páginas del proyecto.
- **INC**. Se crea el archivo metas.inc, donde ván todas las referencias SEO del proyecto. Se hará referencia en todos los archivos jsp del proyecto.
- **JSP**. Se crean las carpetas:
	- *CREATE*. Hace referencia a la Inserción de datos. Consta de los archivos Insertar.jsp y finInsertar.jsp
	- *DELETE*. Hace referencia a la eliminación de datos de la tabla y controla que al eliminar un elemento de la tabla se decida si eliminarlo o no eliminarlo. Consta de los archivos ***eliminar.jsp, leerEliminar.jsp y finEliminar.jsp***
	- *READ*. Hace referencia a la consulta de elementos de la tabla y consta del archivo ***leer.jsp***
	- *UPDATE*. Hace referencia a la actualización de los elementos de la tabla. Consta de los archivos ***actualizar.jsp, leerActualizar.jsp y finActualizar.jsp***

En al carpeta **META-INF**, dentro del archivo ***context.xml*** configuramos la conexión a la base de datos, configurando los parámetros de conexión.

En **Source Packages**,los paquetes:

- **es.albarregas.conexion**, dentro del cual se crea el **Servlet** para el acceso a la base de datos ***AccesoBD.java***.
- **es.albarregas.beans**, dentro se crean la clase ***Ave.java***.
- **es.albarregas.controllers**, donde se crearán los controladores de la aplicación, es decir, los **Servlets** ***Concluir.java, ControladorFinal.java, Operación.java*** y ***Realizar.java***
- **es.albarregas.filters**, donde se crea el filtro para que se puedan reconocer los carácteres **UTF8**, ***UTF8Filter.java***
- **es.albarregas.utilidades**, se crea una clase Java con una utilidad de logeador.

01/11/19 22:36:51 
by Francisco Antonio Murillo Pacheco
