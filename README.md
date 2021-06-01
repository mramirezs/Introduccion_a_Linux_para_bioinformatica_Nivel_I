# Introducción a Linux para Bioinformática
Familiarizarse con los comandos básicos del sistema operativo Linux para el manejo de data relacionada con Next Generation Sequencing (NGS).

## Instructor 🤓  
Manuel Alain Ramírez Sáenz --> Llámame `MARS`


## Bioinformática 🚀

```
"La bioinformática comprende los métodos matemáticos, estadísticos y computacionales que pretenden solucionar 
problemas biológicos usando secuencias de ADN y aminoácidos e información relacionada".
                                                                            Fredj Tekaia - Instituto Pasteur
```

## Requerimientos

**Necesario:**
* Conocimiento y entendimiento del Dogma Central de la Biología molecular.
* Conocimiento en Biología Molecular (bioquímica, biología molecular, biofísica molecular).

**Muy necesario:**
* Conocimiento en el manejo de sistemas de cómputo.

**Recomendado:**
* _Manejo básico de linea de comandos en ambientes UNIX (GNU/Linux)._

**Muy deseable:**
* Experiencia con algún lenguaje de programación.

## Objetivo de la Bioinformática

```
"Profundizar en nuestro entendimiento acerca de los organismos vivos y sus relaciones, 
partiendo desde el genoma que los codifica"
```

## Campos de trabajo

* Genómica comparativa
* Análisis de DNA (ORFs, contenidos GC, etc.)
* Recuperación de secuencias.
* Ensamblajes de secuencias.
* Predicción de estructuras de proteícas.
* Visualización de estructuras de proteícas.
* Microarreglos.
* PCR.
* Filogenia.
* Educación.

```
La Bioinformática provee de algoritmos, bases de datos, interfaces y herramientas estadísticas para resolver nuestras 
preguntas biolólgicas.
```

## Sistema operativo Linux

Muchos desarrolladores de programas en Bioinformática prefieren el uso del sistema operativo Linux. Aqui algunos ejemplos sobre estos programas: FASTQC, trimmomatic, kraken, bwa, bowtie, SPAdes, etc. Dichos programas requieren de un usuario con un buen nivel en el manejo de Linux; sin embargo, muchos investigadores que necesitan trabajar con Next Generation Sequecing (NGS) no son familiares con el sistema operativo Linux y requieren de una introducción en el tema. Ahora, el usuario se preocupará entre conocer las características de Linux y los programas mientras aprende sobre las herramientas paa NGS.

## Objetivo

El objetivo de este módulo es **introducir a los participantes en el sistema oprativo Linux** y cubrir con algunas cosas básicas que les permitirán correr algunos de los programas en sus computadoras o laptops. 

## ¿Qué es LINUX?

LINUX es un sistema operativo que fue desarrollado por primera vez en la década de los 60’s y ha estado en constante desarrollo desde entonces. Por sistema operativo, nos referimos al conjunto de programas que hacen que la computadora trabaje. **Es un sistema multi-usuario estable, multi-tarea para servidores, equipos de escritorio y portátiles.**

El sistemas Linux disponen de una interfaz gráfica de usuario (GUI), similar a Microsoft Windows, que proporciona un entorno fácil de usar; sin embargo, se requieren conocimientos de Linux para las operaciones que no estén cubiertos por un programa gráfico, o cuando no hay una interfaz de ventanas disponibles, por ejemplo, cuando se trabaja en un servidor local o en una nube, ya que ellos tienen una sesion de telnet. Hay muchas versiones diferentes de Linux, aunque comparten similitudes comunes. Las variedades más populares de LINUX son los sistemas Sun Solaris, GNU/Linux y MacOS X.

## Sistema operativo Linux

El sistema operativo LINUX se compone de tres partes: **el núcleo (Kernel), el shell y los programas.**

![image](https://github.com/bioinfoperu/Introduccion_a_Linux_para_bioinformatica/blob/main/img/OS_Linux.PNG)
_Introduction to Linux and Command Line Tools for Bioinformatics_ (Figure 1.1)

## El nucleo (kernel)

El kernel de Linux es el centro del sistema operativo: asigna el tiempo y la memoria a los programas, maneja el almacenamiento de archivos y la comunicación en respuesta a las llamadas del sistema operativo.

Como ejemplo, la forma en que el **shell** y el **kernel** trabajan juntos, supongamos que un usuario escribe **rm myfile** (que tiene el efecto de eliminar el file myfile). El **shell** busca en el almacén de archivos, el archivo que contiene el programa rm, y luego pide al **kernel**, a través de las llamadas del sistema, ejecuta el programa rm en myfile. Cuando el proceso rm myfile ha terminado de ejecutarse, el shell devuelve el indicador de LINUX para el usuario, lo que indica que se está a la espera de nuevas órdenes.

## El shell
  
El **shell** actúa como una interfaz entre el **usuario** y el **kernel**. Cuando un usuario inicia una sesión, el programa  de inicio de sesión comprueba el nombre de usuario y contraseña, y luego se inicia otro programa llamado el shell. El shell es un **intérprete de línea de comandos** (ILC). Interpreta los comandos que el usuario escribe para que puedan ser llevadas a cabo. Los comandos son los mismos programas, cuando se terminan, el shell retorna al al usuario para los siguientes pasos a desarrollar (**$** en nuestros sistemas).

El usuario experto puede personalizar su propia shell, y los usuarios pueden utilizar diferentes shells en la misma máquina. Para el tema de hoy, el profesor y los alumnos la **bash** shell de forma predeterminada.

El bash shell tiene ciertas características que ayudan al usuario introducir comandos.

**Finalización del nombre** - Al escribir parte del nombre de un comando, nombre de archivo o directorio y pulsando el <Tab> (una vez), el bash shell completará el resto del nombre de forma automática. Si en el directorio se encuentra más de un nombre que empiece con esas letras que ha escrito, se emitirá un resultado, mostrará una cantidad de palabras o las palabras encontradas que empiezan con esas letras.

**Historial** - El shell mantiene una lista de comandos que ha escrito. Si usted tiene que repetir un comando, utilice las teclas de cursor para desplazarse hacia arriba y abajo en la lista de comandos anteriores o puede escribir el comando **history** para poder observar una lista de los comandos que estuvo trabajando. 

`$ history`

## Archivos y Procesos

**Todo en LINUX es un archivo.**

Un proceso es un programa en ejecución identificado por un PID único (identificador de proceso).

Un archivo es una colección de datos. Son creados por los usuarios que utilizan los editores de texto, compiladores en 
procesos, etc.

Ejemplos de archivos:

* Un documento (informe, ensayo, etc.)

* El texto de un programa escrito en un lenguaje de programación de alto nivel (Python, R, etc).

* Instrucciones comprensibles directamente a la máquina e incomprensible para un usuario ocasional, por ejemplo, una  colección de dígitos binarios (un archivo ejecutable o binaria);

* Un directorio, que contiene información acerca de su contenido, que puede ser una mezcla de otros directorios (subdirectorios) y archivos ordinarios.

## La estructura de los directorios

Todos los archivos se agrupan en la estructura de directorios. El sistema de archivos se organiza en una estructura jerárquica, como un **árbol invertido**. La parte superior de la jerarquía se denomina tradicionalmente root (escrita como una barra /)

![image](https://github.com/bioinfoperu/Introduccion_a_Linux_para_bioinformatica/blob/main/img/Estructure_Directories.PNG)

  _En clase mencionaremos que contiene cada diretorio_

## Empezamos con los comandos básicos 

## 1. Listado de archivos y directorios

### ls (list)

Al iniciar sesión, el directorio actual de trabajo es el directorio principal. Su directorio de usuario tiene el mismo nombre que su nombre de usuario, por ejemplo, **mars**, y es donde se guardan los archivos personales y subdirectorios.

![image](https://github.com/bioinfoperu/Introduccion_a_Linux_para_bioinformatica/blob/main/img/terminal.PNG)
  
Para averiguar lo que está en su directorio principal, escribimos:

```bash
$ ls
```

El comando ls (L minúscula y S minúscula) muestra el contenido del directorio actual de trabajo.

Puede que no haya archivos visibles en su directorio personal o **home**, en cuyo caso, regresará al prompt de LINUX. Alternativamente, puede haber ya algunos archivos incluidos por el administrador del sistema cuando se creó su cuenta.

ls lista todos los directorios o archivos contenidos en tu directorio personal; pero no aquellos cuyo nombre comienza con un punto (.). Los archivos que comienzan con un punto (.) son conocidos como archivos ocultos y por lo general contienen información de configuración importante. Ellos están ocultos porque no deben ser usados a menos que esté muy familiarizado con LINUX.

Para listar el contenido en el directorio personal incluyendo aquellos cuyos nombres comienzan con un punto, escribimos:

```bash
$ ls -a
```

Otras opciones:

```bash
$ ls -l
  _Respuesta_
$ ls -la
  _Respuesta_
$ ls -lh
  _Respuesta_
```

`NOTA 1`: Entre el comando y sus respectivas opciones se debe incluir un espacio. 

### 1.2 Crear directorios

### mkdir (make directory)

Crearemos subdirectorios dentro de nuestro directorio personal para guardar los archivos que se crearan y a ser usados en este tutorial. Crearemos un subdirectorio llamado

```bash
$ mkdir CursoLinux
```
![image](https://github.com/mramirezs/Manual-basico-de-Linux-para-Bioinformatica/blob/main/mkdir.png)
Para ver el directorio que acabas de crear, escribimos:

```bash
$ ls
```

### 1.3. Cambio a un directorio diferente

### cd (change directory)

El comando cd, significa cambio del actual directorio de trabajo a otro directorio. El directorio de trabajo actual puede ser pensado como el directorio donde se encuentra, es decir, su posición actual en el árbol del sistema de archivos.

Para cambiar hacia el directorio **CursoLinux**, escribimos:

```bash
$ cd CursoLinux
```

Luego, escribimos **ls** para ver el contenido (el cual deberá estar vacío).

***Ejercicio 1***

Crearemos otros directorios dentro del directorio CursoLinux. Ejemplos: Genómica, Proteómica y Transcriptómica.

## 1.4. Lo directorios . y ..

Aún en el directorio CursoLinux, escribir

```bash
$ ls -a 
```

Como se puede ver, en el directorio CursoLinux (y en todos los otros directorios), hay dos directorios especiales llamados (.) y (..)

### El directorio actual (.)

En LINUX, (.) significa el directorio actual, entonces escribimos:

```bash
$ cd .  
```

> NOTA 2: Hay un espacio entre el cd y el punto.

Significa quedarse donde está (el directorio CursoLinux).

### El directorio contiguo (..)

(..) Significa el contiguo al directorio actual, entonces escribimos:

```bash
$ cd ..   
```

Le llevará un directorio en la jerarquía (de nuevo a su directorio personal). **¡Inténtalo ahora!**

> NOTA 3: escribiendo **cd** sin argumentos siempre te devuelve a su directorio home. Esto es muy útil si se pierden en el sistema de archivos.

## 1.5. Nombre de rutas y pathnames

## pwd (print working directory)

Pathnames le permiten calcular dónde se encuentra en relación con el conjunto del sistema de archivos. Por ejemplo, para averiguar la ruta absoluta de un directorio home, escribimos cd para regresar a tu directorio home y luego escribimos:

```bash
$ pwd   
```

El pathname que veras es algo como esto:

```bash
$ pwd
/home/mars/CursoLinux   
```

***Exercise 2***

Use los comandos cd, ls y pwd para explorar el sistema de archivos.

## 1.6 Más información sobre el directorio home y pathnames

## Entendiendo pathnames

Primero escribiremos cd para volver a su directorio home, a continuación, escribiremos:

```bash
$ ls CursoLinux   
```

Para listar el contenido de tus directorios CursoLinux. Ahora escribamos

```bash
$ ls Genoma
```

Recibirás un mensaje como este:

***Genoma: No such file or directory***	

La razón es, Genomas no es tu directorio actual de trabajo. Para utilizar un comando en un archivo (o directorio) no en el directorio de trabajo actual (el directorio que se encuentran actualmente en), debe cambiar al directorio correcto, o especificar su ruta completa. Para listar los contenidos del directorio Genoma, debemos escribir: 

```bash
$ ls CursoLinux/Genomas
```

### ~ (tu directorio home) ###

Los directorios personales también pueden ser referidos por el carácter de tilde ~. Se puede utilizar para especificar rutas a partir de su directorio personal. Por lo que escribimos:

```bash
$ ls ~/CursoLinux
```

Mostrará una lista de los contenidos del directorio CursoLinux, no importa donde se encuentra actualmente en el sistema de archivos.

## Segundo tutorial de LINUX
       
## 2.1 Copiando archivos

### cp (copy)

cp es el comando que hace una copia del archivo en el directorio de trabajo actual.

Lo que vamos a hacer ahora, es tomar un archivo almacenado en un área de acceso abierto del sistema de archivos, y utilizar el comando cp para copiarlo en el directorio de CursoLinux.

```bash
$ cp sequence_1.fasta sequence_2.fasta
$ cp sequence_1.fasta CursoLinux/Genoma
$ cd CursoLinux/Genoma
$ cp /home/cursolinux/CursoLinux/sequence_2.fasta .
```

   
> NOTA 4: No olvide el punto (.) al final. Recuerde que el punto se refiere al directorio actual. 
2.2 Moviendo archivos

### mv (move)

mv es el comando que me permite mover un archivo de un lugar a otro. Esto tiene el efecto de mover en lugar de copiar el archivo, por lo que terminan con un único archivo en lugar de dos. También se puede utilizar para cambiar el nombre de un archivo, moviendo el archivo en el mismo directorio, pero que le da un nombre diferente.

```bash
$ mv sequence_2.fasta CursoLinux/Genoma
$ cd CursoLinux/Genoma
$ mv /home/cursolinux/CursoLinux/sequence_2.fasta	.
```

## 2.3 Borrar archivos y directorios

### rm (remove), rmdir (remove directory)

rm es el comando que me permite borrar (eliminar) un archivo. A modo de ejemplo, vamos a crear una copia de un archivo luego eliminarlo. Dentro de tu directorio CurosLinux, escribimos:


Puede utilizar el comando rmdir para eliminar un directorio (asegúrese de que esté vacío en primer lugar).

```bash
$ cp sequence_1.fasta sequence_3.fasta
$ ls
$ rm sequence_3.fasta
$ ls
```
Puede utilizar el comando rmdir para eliminar un directorio (asegúrese de que esté **vacío** en primer lugar).

## 2.4 Mostrar el contenido de un file

### clear (clear screen)

Antes de comenzar la siguiente sección, es posible que quiera borrar la ventana de terminal de los comandos anteriores por lo que la salida de los siguientes comandos puede ser claramente entendido.

En el prompt, escribimos

```bash
$ clear
```
Esto borrará todo el texto volviendo al símbolo $ en la parte superior de la ventana.

### cat (concatenate)

El comando cat se puede utilizar para mostrar el contenido de un archivo en la pantalla.

```bash
$ cat sequence_1.fasta
```

Como se puede ver, el archivo es más largo que el tamaño de la ventana, por lo que desfilan por la pantalla por lo que es ilegible.

### less

El comando less escribe el contenido de un archivo en la pantalla de una página a la vez. Escribimos:

```bash
$ less sequence_1.fasta	
```

Presione la **barra espaciadora** si quieres ver otra página y escribir **q** si quieres salir de la lectura. Como puedes ver, less es usado en preferencia a cat para largos archivos.

### head

El comando head escribe las primeras diez líneas de un archivo en la pantalla. En primer lugar, limpiamos la pantalla y a continuación, escribimos:

```bash
$ head sequence_1.fasta
```

Luego escribimos:

```bash
$ head -5 sequence_1.fasta
```

### tail

El comando tail escribe las diez últimas líneas de un archivo en la pantalla. Limpiamos la pantalla y escribimos:

```bash
$ tail sequence_1.fasta
```

¿Cómo se puede acceder a las últimas 15 líneas del archivo?

## 2.5 Buscar el contenido en un archivo

### Búsqueda sencilla usando less

Usando less, se puede buscar, a través de un archivo de texto, una palabra clave o patrón. Escribimos

```bash
$ less sequence_1.fasta	
```

A continuación, todavía con less, escriba una barra diagonal (/) seguido de la palabra a buscar:

/Mycobacterium

/GACGATGTCA

Como se puede ver, less busca y resalta la palabra clave. Escriba (n) para buscar la siguiente aparición de la palabra.

### grep (don't ask why it is called grep)

grep es una de las muchas utilidades estándar de LINUX. Se busca en los archivos de palabras o patrones específicos. En primer lugar, limpiamos la pantalla, a continuación, escriba

```bash
$ grep CACCGACGAGGCGCTGTT sequence_1.fasta	
```

Como se puede ver, grep ha impreso cada línea que contiene la palabra ciencia.

O si tiene?

Pruebe a escribir

```bash
$ grep Tumor sequence_1.fasta
```

El comando grep distingue entre mayúsculas y minúsculas. Para hacer caso omiso de las distinciones mayúsculas/minúsculas, utilice la opción -i, es decir, escribimos:

```bash
$ grep -i tumor sequence.fasta
```

Para buscar una frase o patrón, debe encerrarlo entre comillas simples (el símbolo de apóstrofo).

Algunas de las otras opciones de grep son:

    -v: mostrar aquellas líneas que no coinciden
    -n: preceder a cada línea coincidente con el número de línea
    -c: imprimir sólo el número total de líneas coincidentes

```bash
$ grep -ivc CACCGACGAGGCGCTGTT sequence.fasta	
```

### wc (word count)

Una pequeña utilidad práctica es el comando wc, abreviatura de recuento de palabras. Para hacer un recuento de palabras en sequence_1.fasta, escribimos:

```bash
$ wc -w sequence_1.fasta	
```
Para averiguar el número de líneas que tiene el archivo, escribimos:

```bash
$ wc -l sequence.fasta
```

# ¡Gracias!
