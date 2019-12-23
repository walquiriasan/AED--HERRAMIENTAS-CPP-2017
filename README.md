# :earth_americas: HERRAMIENTAS-CPP-2017

&nbsp;

# Lo necesario para compilar C++ 2017 en Sublime Text

&nbsp;
&nbsp;

## INSTALACIÓN DEL COMPILADOR (PASO A)

* Instalar el paquete "mingw32-gcc-g++", con el instalador mingw-get-setup
(prestar especial atención a la ubicación de esta instalación).
Al final, este paso, se realizará de este modo:
Installation -> Apply Changes -> Apply

* Edición de la variable de entorno PATH del sistema añadiendo en ella 
la ruta de la carpeta dónde se instaló el paquete en el paso 1.
Ejemplo de lo que se agrega en el PATH (esto varía de acuerdo a la ubicación de la instalación):
C:\MinGW\bin

&nbsp;
&nbsp;

## CÓDIGO JSON (PASO B)

* En Sublime Text:
Tools -> Build System -> New Build System 

* Pegar el siguiente código:

```boo
{
"cmd": ["g++", "-std=c++17", "-Wall", "-unicode","-pedantic-errors", 
"$file_name", "-o", "${file_base_name}.exe",
"&&", "start", "cmd", "/k" , "$file_base_name"], 	
"selector": "source.cpp",
"working_dir": "${file_path}", "shell": true
}
```

* Guardar con nombre elegido, seguido de la extensión:
.sublime-build

&nbsp;
&nbsp;

## SELECCIONAR EL TIPO DE COMPILADOR A USAR (PASO C)
 
* En Sublime Text:
Tools -> Build System->seleccionar el nombre que le coloco al archivo guardado en el PASO B.

&nbsp;
&nbsp;

## USAR EL COMPILADOR (PASO D)

* En Sublime Text:
Tools -> Build , o usar el atajo por teclas CTRL+B

&nbsp;
&nbsp;

# Páginas web de consulta 
+ <http://www.mingw.org/>  
+ <https://platzi.com/tutoriales/1469-algoritmos/1901-como-instalar-gcc-para-compilar-programas-en-c-desde-la-consola-en-windows/>  
+ <http://ayudasprogramacionweb.blogspot.com/2012/12/compilar-y-ejecutar-cpp-desde-sublime-text.html>  
+ <http://tucursovirtualya.blogspot.com/2017/03/como-compilar-codigo-c-c-en-sublime.html>  
+ <https://markdown.es/sintaxis-markdown/>  
+ <https://support.zendesk.com/hc/es/articles/203691016-Uso-de-Markdown-para-el-formato-de-texto#topic_xqx_mvc_43__row_vwt_yln_1n>  
+ <https://gist.github.com/rxaviers/7360908>
