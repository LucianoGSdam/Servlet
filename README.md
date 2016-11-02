# Servlet

Proyecto Servlet JDBC_Servlet
Módulo: Acceso de Datos / Desarrollo de Aplicaciones Multiplataforma

Descripción del proyecto:
creación de un servlet para permitir al usuario 
interactuar con una base de datos a través de un servidor TomCat.

Estructura del proyecto:

/Web -->
        
        /css      --> style.css

        /META-INF --> context.xml
        
        /WEB-INF  --> web. xml: fichero que almacena la ruta del servlet en el servidor
        
        index.jsp: fichero jsp que contiene el formulario para realizar la búsqueda
        
        resultado.jsp: fichero jsp que imprime la solución del query o consulta  

/src -->
         
         /java --> /alumnos  --> alumnos.java: clase que almacena los atributos de cada alumno que devuelve la consulta para luego imprimirlos

                  /Servlets --> Servlet.java: clase principal que contiene el servlet y los métodos doGet y doPost
                  
                  /conexion --> conexionMySQL.java: clase que realizar la conexion con la base de datos Curs haciendo uso de la libreria mysql-connector
                  
                                manejoBD.java: clase utilizada para hacer la consulta o query. Devuelve un ResultSet que manejamos posteriormente en el index.jsp
                                
/lib --> mysql-connector-java-5.1.16.java

Funcionamiento del programa:

1) Al ejecutar el servlet, abre en el navegador el index.jsp. Este documento imprimir por pantalla el resultado de nuestra consulta.

2) Nuestra consulta se encuentra en la clase "ManejoBD". Esta clase necesita a su vez, la clase "conexionMySQL" para establecer conexión con la base de datos. En caso contrario devolvería una SQLException.

3) La clase "ManejoBD" realiza la consulta y devuelve un ResultSet, el cual forma parte de la respuesta que da el servlet, mediante los métodos doGet o doPost, al index.jsp que albergaba nuestro formulario.

4) Finalmente el resultado se imprime de forma muy sencilla y rudimentaria en el documento resultado.jsp


        
