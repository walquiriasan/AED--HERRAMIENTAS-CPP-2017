# HERRAMIENTAS-GCC-2017

# Lo necesario para compilar C++ 2017 en Sublime Text

---

## INSTALACIÓN DEL COMPILADOR (PASO A)

* Instalar el paquete "mingw32-gcc-g++", con el instalador mingw-get-setup
(prestar especial atención a la ubicación de esta instalación)
Al final este paso se realizará de este modo:
Installation -> Apply Changes -> Apply

* Edición de la variable de entorno PATH del sistema añadiendo en ella 
la ruta de la carpeta dónde se instaló el paquete en el paso 1

---

## CÓDIGO JSON (PASO B)

* En Sublime Text:
Tools -> Build System -> New Build System 

* Pegar el siguiente código:
~~~
{
"cmd": ["g++", "-std=c++17", "-Wall", "-unicode","-pedantic-errors", "$file_name", "-o", "${file_base_name}.exe",
"&&", "start", "cmd", "/k" , "$file_base_name"], 	
"selector": "source.cpp",
"working_dir": "${file_path}", "shell": true
}
~~~
* Guardar con nombre elegido seguido de la extensión:
.sublime-build

---

## SELECCIONAR EL TIPO DE COMPILADOR A USAR (PASO C)
 
* En Sublime Text:
Tools -> Build System->seleccionar el nombre que le coloco al archivo guardado en el PASO B.

---

## USAR EL COMPILADOR (PASO D)

* En Sublime Text:
Tools -> Build , o usar el atajo por teclas CTRL+B
