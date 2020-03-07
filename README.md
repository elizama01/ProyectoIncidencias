El Proyecto se encuentra en el siguiente repositorio.
https://github.com/elizama01/ProyectoIncidencias

Base de datos
Instalar Postgresql desde la página oficial.
Elegir según su sistema operativo.

Link Oficial del Gestor de Base de Datos Postgresql 
https://www.postgresql.org/download/
Link en opcional (Pgadmin v11)
https://www.pgadmin.org/download/

Lenguaje Python:
Una vez instalado Postgresql se  debe instalar Python 3.7.6 o última versión (recomendado)
Link Python Oficial para descargar según el sistema operativo.
https://www.python.org/downloads/ 

El Proyecto se encuentra en el siguiente repositorio.
https://github.com/elizama01/ProyectoIncidencias

Una vez instalado Python se debe crear un entorno virtual para trabajar.

En este caso python ya tiene en sus Biblioteca Virtualenv el cual servirá para montar el entorno.
Sumado a esto Virutualenv viene incluido con PIP para la instalación de paquetes.

Creamos un entorno virtual(windows 10).
Con la línea de comando python -m venv nombre_entorno ingresado en CMD se creará un carpeta con el nombre de el entorno (crear donde se almacenará el proyecto).

Como en el  siguiente ejemplo.

Esto crea las siguientes carpetas:





Una vez hecho esto y descargado proyecto del repositorio, se debe descomprimir proyectoincidencias.rar dentro de la carpeta entorno, en este caso  nombre_entorno.
Quedando de la siguiente manera.


Para iniciar entorno virtual se debe hacer lo siguiente:
Ubicarse en la carpeta de entorno en este caso nombre_entorno.Iniciar una consola de comandos.

Escribir e ingresar la línea de comando  nombre_entorno/Scripts/activate.

Marcando la carpeta con el nombre del entorno encerrado entre paréntesis.

Esto quiere decir que el entorno está activado y que es posible instalar las librerías y framework necesarios.

Instalación de Django y librerías de python.

Para instalar django v3.0.2 en el entorno se escribe el comando pip install django==3.0.2 en caso de que se necesite la versión más actualizada solo se escribe pip install django.


Para instalar psycopg2 v2.8.4 en el entorno se escribe el comando pip install psycopg2==2.8.4 en caso de que se necesite la versión más actualizada solo se escribe pip install psycopg2.



Para instalar django-crispy-forms en el entorno se escribe el comando pip install django-crispy-forms.



Para saber la lista de los paquetes instalados se debe ingresar pip list.






Crear base de datos en postgresql.

Una vez ingresado a la línea de comando  de postgres se ingresa el siguiente scripts para la creación de la base de datos dependiendo de la configuración que se tiene. Solo varía el OWNER y el nombre de la base de datos en este caso dbincidencias..

Configurar settings.py del proyecto para conectar a base de datos.

Al interior de la carpeta del proyecto en la carpeta  proyectoincidencias se encuentra el archivo settings.py se abre y se edita la el área de DATABASES.
En este caso ‘USER’ ,‘NAME’,’PASSWORD’, varían dependiendo de la configuración de la base de datos.


Importar Modelos desde Django a Base de datos.

Para importar los modelos creados y sus relaciones a la base de datos se debe ingresar las siguientes líneas de comandos.
En la carpeta donde se encuentra el archivo manage.py iniciar una consola.

Ingresar python manage.py makemigrations.




luego ingresar python manage.py migrate.

Línea de comando la cual deja la base de datos con las siguientes tablas.

Ingreso de estados y roles a la base de datos.

Ingreso de roles para Usuarios: En la consola de postgres, una vez ingresado a su respectiva base de datos se ingresa el siguiente comando para llenar los roles que pertenecen a usuarios.


Ingreso de estados para Proyectos: En la consola de postgres, una vez ingresado a su respectiva base de datos se ingresa el siguiente comando para llenar los estados que pertenecen al proyectos.



Ingreso de estados para Incidencias: En la consola de postgres, una vez ingresado a su respectiva base de datos se ingresa el siguiente comando para llenar los estados que pertenecen a la incidencias.


Crear Superusuario en django para ingresar al sistema.

Desde la carpeta del proyecto descomprimido proyectoincidencia, donde se encuentra el archivo manage.py  se inicia una linea de comando para ejecutar el comando python manage.py createsuperuser. 
Se ingresan sus datos personales pertenecientes a un super administrador en el sistema, por ende, no contará como usuario registrado(se recomienda crear y usar  usuario Administrador en el panel gestión de usuario) .



Inicio de proyecto de manera local.

Para iniciar en un servidor de manera local se debe ingresar el comando python manage,py runserver y luego ingresar a la ip que le indica la consola.



Una vez ingresado a  la ip del servidor se mostrará el inicio de sesión para el sistema,en el cual, ingresa con los datos del superusuario creado y permita ocupar el software.

