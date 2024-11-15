# TAREA GIT

> Despliegue de Aplicaciones Web: GIT
>
> Alejandro Miranda García

[TOC]

<u>URL Repositorio GITHUB</u>: https://github.com/alejandromg73/labowebs



### Trabajo en local

1.  **Inicializa un nuevo repositorio Git en una carpeta llamada `"labowebs"` y agrega los archivos proporcionados en el aula virtual. Renombra la rama master a main , si es necesario. Realiza el primer commit. Muestra el log del repositorio.**

​	Creo la carpeta `labowebs` en Documentos e inicializo el repositorio:

```bash
git init
```

La rama master ya se llama `main`: 

![image-20241114084709704](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114084709704.png)

Hago el commit y muestro el log:

![image-20241114084822664](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114084822664.png)

```bash
git log --all --decorate --oneline --graph
```

![](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114084911183.png)



2.  **Incluye un fichero .gitignore para que los ficheros README.md , LICENCE.txt y passwords.txt sean ignorados por el control de versiones. Realiza el commit y muestra los logs del repositorio en una línea.**

   ```bash
   touch .gitignore
   ```

   ![image-20241114085705416](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114085705416.png)

   Hago el commit y muestro los logs del repositorio

   ![image-20241114085830594](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114085830594.png)

   ![image-20241114085909640](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114085909640.png)

El archivo .gitignore incluye: ![image-20241114090609730](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114090609730.png)



3. **En el repositorio, crea los archivos README.md , LICENCE.txt y passwords.txt con algún contenido. Muestra el estado del repositorio. Muestra el listado de archivos ignorados.**

   ![image-20241114090650601](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114090650601.png)

   Muestro el estado del repositorio con git status:

   ```bash
   git status
   ```

   ![image-20241114090832894](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114090832894.png)

   Muestro el listado de archivos ignorados con 

   ```bash
   git status --ignored
   ```

   ![image-20241114091226113](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114091226113.png)

   

4. **Crea una rama feature-estilos . Cámbiate a ella. Modifica el archivo estilos.css : propiedad color del body y de h2 : #2a2a2a propiedad background-color de header y footer: #2a75ff**

   **Comprueba el estado del repositorio. Añade los cambios, realiza un commit con el mensaje "actualizados estilos a azules"**

   Creo una rama con

   ```bash
    git branch feature-estilos
   ```

   ![image-20241114091416026](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114091416026.png)

   Me cambio a esa rama con

   ```bash
    git checkout feature-estilos
   ```

   ![image-20241114091506561](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114091506561.png)

   Cambio el color del body y del h2 a: \#2a2a1a, y el background-color de header y footer a \#2a75fa

   Tras los cambios, muestro el estado del repositorio para ver los cambios pendientes y hago commit de los cambios:

   ![image-20241114092233910](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114092233910.png)

   

   5**. Vuelve a la rama main . En el archivo index.html añade un comentario donde se indique tu nombre como autor de la página. Comprueba el estado del repositorio. Añade los cambios, realiza un commit con el mensaje ' añadido autor en index'. Muestra los logs del repositorio en una línea, gráficamente y con 'decoración'**

   Vuelvo a la rama main con 

   ```bash
   git checkout main
   ```

   Añado un comentario en index con mi nombre

   ![image-20241114092543746](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114092543746.png)

   Compruebo estado repositorio y hago commit con el mensaje indicado:

   ![image-20241114093227678](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114093227678.png)

   Muestro logs del repositorio:

   ```bash
   git log --all --decorate --oneline --graph
   ```

   ![image-20241114093145572](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114093145572.png)

   

   6.**Fusiona la rama feature-estilos en la rama main. Muestra los logs del repositorio en una línea, gráficamente y con 'decoración'**

Fusiono la rama feature-estilos en la rama main con el comando

```bash
git merge feature-estilos
```

Muestro logs como siempre:

![image-20241114093413967](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241114093413967.png)





### Trabajo remoto

1. **Continúa con el repositorio labowebs . Añade el repositorio a Sourcetree.** 

   Añadido repositorio a Sourcetree: ![image-20241114093716726](./TAREAENTREGABLEGIT.assets/image-20241114093716726.png)

   

2. **Crea un repositorio remoto y sube al remoto los ficheros de tu repositorio local. Debes subir todas las ramas.** 

   Creo el repositorio remoto y subo los ficheros del local (las dos ramas que tengo)

   ![image-20241114094048557](./TAREAENTREGABLEGIT.assets/image-20241114094048557.png)

![image-20241114094109359](./TAREAENTREGABLEGIT.assets/image-20241114094109359.png)

Todo correcto



3. **Crea una rama feature-index. Añade el siguiente código dentro de la section class about, añade los cambios y crea un commit. Sube los cambios al remoto.**

   Creo la rama: ![image-20241114094831093](./TAREAENTREGABLEGIT.assets/image-20241114094831093.png)

   ![image-20241114094853548](./TAREAENTREGABLEGIT.assets/image-20241114094853548.png)

   Hago el commit:

   ![image-20241114095100122](./TAREAENTREGABLEGIT.assets/image-20241114095100122.png)

   Subo los cambios al remoto, hago un push y compruebo desde el remoto que se ha subido: 

   ![image-20241114095238607](./TAREAENTREGABLEGIT.assets/image-20241114095238607.png)

   

4. **En el repositorio local, fusiona la rama feature-index en la rama main .**

   Fusiono la rama en main:

   ![image-20241114095407908](./TAREAENTREGABLEGIT.assets/image-20241114095407908.png) 

   Hago un push para subir los nuevos cambios al remoto

   

5. **Edita el fichero contacto.html . Borra unas líneas. Muestra los ficheros con cambios pendientes y las diferencias. Añade los cambios y haz un commit.**

   Borré esta linea:     

   ```bash
     <button type="submit">Enviar</button> 
   ```

   Que es el botón de enviar

   Fichero con cambios pendientes y sus diferencias:

   ![image-20241114100302899](./TAREAENTREGABLEGIT.assets/image-20241114100302899.png)

   Añado los cambios y hago un commit:

   ![image-20241114100345989](./TAREAENTREGABLEGIT.assets/image-20241114100345989.png)

   

6. **Te das cuenta del error. Deshaz el commit anterior. Captura el estado actual del repositorio.** 

   Para deshacer el commit, doy click en el commit y doy a reverse commit.

   ![image-20241114100658714](./TAREAENTREGABLEGIT.assets/image-20241114100658714.png)

   

7. **Crea una rama feature-mapa . Incluye este código en el archivo contacto.html . Añade los cambios. Realiza un commit. Sube los cambios al remoto. Muestra en el remoto los cambios del archivo contacto.html en la rama feature-mapa.**

   Creo la rama y me cambio a ella

![image-20241115083819366](./TAREAENTREGABLEGIT.assets/image-20241115083819366.png)

![image-20241115083848081](./TAREAENTREGABLEGIT.assets/image-20241115083848081.png)

Incluyo el código en el archivo contacto.html, añado los cambios, y realizo commit

![image-20241115084017688](./TAREAENTREGABLEGIT.assets/image-20241115084017688.png)

Hago un push para sincronizarlo con el repositorio remoto y compruebo que se ha realizado en la nueva rama:

![image-20241115084157548](./TAREAENTREGABLEGIT.assets/image-20241115084157548.png)

Muestro los cambios en el remoto del archivo contacto.html:

![image-20241115084308285](./TAREAENTREGABLEGIT.assets/image-20241115084308285.png)



8. **En GitHub, en la rama main , fusiona la rama feature-mapa . Baja los cambios del remoto a local. Deja los dos repositorios sincronizados.**

Para fusionar las dos ramas en GitHub, creo una pullrequest, desde la rama main, que es a la cual le quiero fusionar la rama feature-mapa

![image-20241115084900085](./TAREAENTREGABLEGIT.assets/image-20241115084900085.png)

Una vez tengo ya el pull request, le doy a merge pull request para fusionar ambas ramas:

![image-20241115084936908](./TAREAENTREGABLEGIT.assets/image-20241115084936908.png)

Le doy a confirmar la fusión:

![image-20241115085028986](./TAREAENTREGABLEGIT.assets/image-20241115085028986.png)

Todo correcto:

![image-20241115085050818](./TAREAENTREGABLEGIT.assets/image-20241115085050818.png)

Hago un pull desde Sourcetree para traerme los cambios del remoto al local: ![image-20241115085217608](./TAREAENTREGABLEGIT.assets/image-20241115085217608.png)

Listo:

![image-20241115085238750](./TAREAENTREGABLEGIT.assets/image-20241115085238750.png)





### Conflictos

1. **Crea una rama hotfix-js . Cámbiate a ella. Añade este código en el fichero script.js . Confirma el cambio y haz un commit. (Fíjate en los números de línea...)**

   Creo la rama:

   ![image-20241115085346724](./TAREAENTREGABLEGIT.assets/image-20241115085346724.png)

   ![image-20241115085424963](./TAREAENTREGABLEGIT.assets/image-20241115085424963.png)

   Añado el código en el fichero script.js en las líneas 24-27

   ![image-20241115085554027](./TAREAENTREGABLEGIT.assets/image-20241115085554027.png)

   Hago commit:

   ![image-20241115085643255](./TAREAENTREGABLEGIT.assets/image-20241115085643255.png)

   

2. **Vuelve a la rama main . En el fichero script.js en las mismas líneas que en la cuestión anterior, añade el código siguiente. Confirma el cambio y haz un commit.**

   Vuelvo a la rama main y modifico las mismas líneas que hice en la otra rama:

   ![image-20241115085825723](./TAREAENTREGABLEGIT.assets/image-20241115085825723.png)

   Hago commit:

   ![image-20241115085910434](./TAREAENTREGABLEGIT.assets/image-20241115085910434.png)

   

3. **Fusiona la rama hotfix-js en main . Debe producirse un conflicto. Resuélvelo. Cuando termines la resolución del conflicto sube los cambios al remoto - Deja los repositorios sincronizados -**

​	Fusiono hotfix-js en main para producir un conflicto:

![image-20241115090049913](./TAREAENTREGABLEGIT.assets/image-20241115090049913.png)

Se ha producido un conflicto, doy click derecho en el archivo y selecciono "Resolve conflict":

![image-20241115090207804](./TAREAENTREGABLEGIT.assets/image-20241115090207804.png)

Resuelvo los cambios del conflicto mediante la herramienta gráfica de Sourcetree y subo los cambios al remoto:

![image-20241115090401048](./TAREAENTREGABLEGIT.assets/image-20241115090401048.png)

Hago un push y compruebo en el remoto si han quedado sincronizados:

![image-20241115090451982](./TAREAENTREGABLEGIT.assets/image-20241115090451982.png)

Todo correcto, tanto el repositorio local como el remoto, quedan sincronizados





###  Subida de documentación

Incluyo en la carpeta `docs`:

- Fichero markdown
- Carpeta con imágenes
- PDF

