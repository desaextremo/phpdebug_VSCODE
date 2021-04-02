#	Como activar depurador php en Visual Studio Code en Windows?

[1. Modificar el archivo de propiedades de Visual Studio Code para indicar la ruta al ejecutable de PHP](#1-modificar-el-archivo-de-propiedades-de-visual-studio-code-para-indicar-la-ruta-al-ejecutable-de-php)
[2. Agregar PHP al PATH](#2-agregar-php-al-path)
[3. Instalar el plugin PHP DEBUG](#3-instalar-el-plugin-php-debug)
[4. Descargar XDEBUG compatible con el PHP de tu máquina](#4-descargar-xdebug-compatible-con-el-php-de-tu-máquina)
[5.	Configurar la extensión php debug y Visual Studio Code](#5-configurar-la-extensión-php-debug-y-visual-studio-code)
[6.	Utilizar el depurador en Visualstudio Code](#6-utilizar-el-depurador-en-visualstudio-code)

##	1. Modificar el archivo de propiedades de Visual Studio Code para indicar la ruta al ejecutable de PHP
* Abre el archivo settings.json para establecer la ruta del ejecutable de php:

<p align="center">
	<img src="images/phpdb_1.png" style="width: 50%; height: 50%">
</p>

<p align="center">
	<strong><em>Acceso el archivo settings.json</em></strong>
</p>

* Podemos abrir el archivo de configuración <strong><em>settings.json</em></strong> en modo <strong><em>UI</em></strong> tipo interfaz gráfica de administración, o en modo <strong><em>JSON</em></strong>.

<p align="center">
 <img src="images/phpdb_2.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>archivo settings.json Modo UI</em></strong>u
</p>

* Para abrir el archivo de configuración en formato json solo haz clic sobre el icono en forma de hoja que se ubica en la parte superior izquierda de tu pantalla.

<p align="center">
 <img src="images/phpdb_3.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>archivo settings.json Modo UI</em></strong>
</p>

* Modifica el archivo <strong><em>settings.json</em></strong> para asignar un valor a la propiedad <strong><em>"php.validate.executablePath":"Ruta al ejecutable de php"</em></strong>. 
<p align="center">
 <img src="images/phpdb_4.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>Editando el settings.json</em></strong>
</p>

## 2. Agregar PHP al PATH
	
* Para modificar la variable de entorno path solo tienes que hacer lo siguiente:
	
<p align="center">
 <img src="images/phpdb_5.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>Agregando php a la variable de entorno path</em></strong>
</p>

<p align="center">
 <img src="images/phpdb_6.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>Modificando la variable path</em></strong>
</p>

* En una instalación de <strong><em>xampp</em></strong> por defecto <strong><em>php</em></strong> suele ubicarse en: <strong><em>c:\xampp\php</em></strong>)

<p align="center">
 <img src="images/phpdb_7.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>Agregando la ubicación de la variable path</em></strong>
</p>

* Consultar la version de php <strong><em>php -v</em></strong> en la linea de comandos de <strong><em>Windows (cmd)</em></strong>
  
<p align="center">
 <img src="images/phpdb_8.png" style="width: 50%; height: 50%">
</p>

<p align="center">
	<strong><em>Consultando la versión de php con el comando php -v</em></strong>
</p>

## 3. Instalar el plugin PHP DEBUG
* El plugin [php debug](https://marketplace.visualstudio.com/items?itemName=felixfbecker.php-debug) nos permite configurar la opción depurador de Visual Studio Code para el lenguaje <strong><em>php</em></strong>

<p align="center">
 <img src="images/phpdb_9.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>Versión del plugin y ubicación en el marketplace</em></strong>
</p>


<p align="center">
 <img src="images/phpdb_10.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>Instalando php debug</em></strong>
</p>

## 4. Descargar XDEBUG compatible con el PHP de tu máquina
La extensión (librería dll en caso de windows) [xdebug](http://xdebug.org/) se adiciona a la instalación de tu php y junto a php debug permiten la magía de la depuración de código php en tu Visual Studio Code.

Es probable que xdebug ya se encuentre previamente instalado en tu entorno <strong><em>php</em></strong>. Puedes realizar esta comprobación utilizando un script de php que incluya la función [phpinfo()](https://www.php.net/manual/en/function.phpinfo.php). Esta función del lenguaje muestra información sobre la configuración del <strong><em>php</em></strong> instalado en tu maquina.
<p align="center">

<p align="center">
 <img src="images/phpdb_11.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>Script info.php para consultar la configuración de tu php</em></strong>
</p>

* Valida la versión de xdebug compatible con tu php

<p align="center">
 <img src="images/phpdb_12.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>Obteniendo información de tu sistema para instalar xdebug</em></strong>
</p>

* Selecciona y copia el resultado obtenido en la  consola, despues de haber ejecutado el comando **_php – i_**

<p align="center">
 <img src="images/phpdb_13.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>resultado de la ejecución del comando php -i</em></strong>
</p>

* Dirigete a la página de [xdebug wizard](https://xdebug.org/wizard)  y pega el resultado para obtener la versión de xdebug acorde a tu máquina

<p align="center">
 <img src="images/phpdb_14.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>Obteniendo información de la versión de xdbug acorde a tu máquina</em></strong>
</p>

* Descarga la versión de [xdebug](https://xdebug.org/download) sugerida

<p align="center">
 <img src="images/phpdb_15.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>Xdebug sugerido para tu máquina</em></strong>
</p>

* Mueve el archivo dll a <directorio instalación php>/php/ext, y modifica el archivo de configuración de php “php.ini”
  
<p align="center">
 <img src="images/phpdb_16.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>Copiando el la librería y editando el archivo php.ini</em></strong>
</p>

El cambio al archivo **_php.ini_** es:
>zend_extension = <ruta al ejecutable php>\<nombre de la librería dll>

**Ejemplo:**
zend_extension = C:\xampp\php\ext\php_xdebug-3.0.3-8.0-vs16-x86_64.dll

Recarga el servidor php y ejecuta el script **_info.php_** para verificar que [xdebug](https://xdebug.org/download) se encuentre habilitado.

<p align="center">
 <img src="images/phpdb_17.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>Validando la instalación de xdebug</em></strong>
</p>

<p align="center">
 <img src="images/phpdb_18.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>Comprobando la versión de xdebug instalada</em></strong>
</p>

* Modifica el archivo “**_php.ini_**” para configurar el xdebug según la versión
instalada en el paso anterior.


	>**_Para Xdebug v3.x.x agregar al php.ini_**:
xdebug.mode = debug
xdebug.start_with_request = yes
xdebug.client_port = 9000

	>**_Para Xdebug v2.x.x agregar al php.ini:_**:
xdebug.remote_enable = 1
xdebug.remote_autostart = 1

<p align="center">
 <img src="images/phpdb_19.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>archivo php.ini editado</em></strong>
</p>

Más adelante describire los pasos que debes seguir para crear el archivo de configuración **_launch.json_**. Este archivo es creado automáticamente por [Visual Studio Code](https://code.visualstudio.com/), y se utiliza para establecer parametros necesario para el depurador, como el puerto sobre el cual estará escuchando peticiones [xdebug](https://xdebug.org/download), y otras caracteristicas adicionales (para un mayor nivel de detalle consultar en la página de [PHP Debug](https://marketplace.visualstudio.com/items?itemName=felixfbecker.php-debug)).

El archivo **_launch.json_** contiene los apartados de configuración **_Listen for XDebug_** que se utiliza para depurar nuestras aplicaciones desde el navegador o browser y **_Launch currently open script_** que se utiliza para depurar en la consola de [Visual Studio Code](https://code.visualstudio.com/).

## 5. Configurar la extensión php debug y Visual Studio Code

A continuación detalleré la secuencia de pasos requeridos para la creación del archivo de configuración en formato json llamado **_launch.json_**.

<p align="center">
 <img src="images/phpdb_20.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>Accediendo al depurador</em></strong>
</p>

<p align="center">
 <img src="images/phpdb_21.png" style="width: 50%; height: 50%">
</p>
<p align="center">
	<strong><em>Configurando el depurador</em></strong>
</p>

<p align="center">
 <img src="images/phpdb_22.png" style="width: 50%; height: 50%">
</p>

<p align="center">
	<strong><em>Creando el archivo de configuración launch .json</em></strong>
</p>

## 6. Utilizar el depurador en Visualstudio Code

* Selecciona el archivo a depurar y establece los puntos de ruptura haciendo clic al costado izquierdo de la línea de codigo.

<p align="center">
 <img src="images/phpdb_23.png" style="width: 50%; height: 50%">
</p>

<p align="center">
	<strong><em>Estableciendo puntos de ruptura</em></strong>
</p>

* Haz clic sobre el icono **_Run and Debug_**

<p align="center">
 <img src="images/phpdb_24.png" style="width: 50%; height: 50%">
</p>

<p align="center">
	<strong><em>Seleccionando Run and Debug</em></strong>
</p>

* Inicia el depurador seleccionando  Listen for [Xdebug](https://xdebug.org/download) en la parte superior del IDE y luego haz clic sobre el icono en forma de flecha.
  
<p align="center">
 <img src="images/phpdb_25.png" style="width: 50%; height: 50%">
</p>

<p align="center">
	<strong><em>Seleccionando Listen for XDebug</em></strong>
</p>

* En este punto el depurador ya se encuentra activado. Inicia tu aplicación, y navega hasta que los puntos de ruptura inicien.

<p align="center">
 <img src="images/phpdb_26.png" style="width: 50%; height: 50%">
</p>

<p align="center">
	<strong><em>Depurador activado y en espera</em></strong>
</p>

* Una vez el depurador se encuentra activo podrás inspeccionar el valor de variables, constantes, variables superglobales y expresiones.

<p align="center">
 <img src="images/phpdb_27.png" style="width: 50%; height: 50%">
</p>

<p align="center">
	<strong><em>Inspeccionando variables</em></strong>
</p>

<p align="center">
 <a href="http://www.desarrolloextremo.com.co"><img src="images/footer.png" alt="Solo necesitas motivación"></a>
</p>
