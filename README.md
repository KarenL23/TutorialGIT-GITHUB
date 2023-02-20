# TutorialGIT
## ¿Como añadir un repositorio a GIT?
Para empezar nos dirigimos a la carpeta de documentos en donde tenemos el archivo que deseamos subir y le damos clic derecho y seleccionamos abrir con GIT BASH:

![image](https://user-images.githubusercontent.com/124689720/220139383-21789627-dacb-45fe-8190-89254d47b622.png)

Al seleccionar esta opcion aparecera la consola de comandos, donde debe aparecer la ruta en donde se encuentra el archivo y el nombre de esta forma:

![image](https://user-images.githubusercontent.com/124689720/220139803-bc51faaa-a496-4081-a97a-46c6af705de9.png)

Ya en la consola vamos a ingresar el siguiente comando para iniciar el proceso de subir el repositorio:
```
git init 
```
![image](https://user-images.githubusercontent.com/124689720/220141805-59ea1a40-ba90-456e-ac5f-385cedaea265.png)

Despues ingresaremos el comando GIT REMOTE ADD ORIGIN y entre comillas la url en formato SSH del repositorio creado en GITHUB de la siguiente forma:
```
git remote add origin "URL repo"
```
copiamos el link:

![image](https://user-images.githubusercontent.com/124689720/220143219-d38d9446-69ce-40a5-ab43-99323c49335e.png)

lo pegamos en el comando:

![image](https://user-images.githubusercontent.com/124689720/220143909-78ecfffb-003f-4219-8358-2b57905b7772.png)

luego revisaremos el estatus del proceso con el comando:
```
git status
```
nos debe salir los documentos que estan dentro de la carpeta en rojo:

![image](https://user-images.githubusercontent.com/124689720/220144386-86fef32b-4dd9-47ce-b138-994e4c9e273f.png)

Para descargar el contenido README del repositorio creado en GITHUB utilizamos (es importante para que no nos genere error):
```
git fetch origin main
```
Luego usamos el siguiente comando para actualizar la versión del repositorio donde se encuentra el archivo README que se descargo en el paso anterior:
```
git pull origin main
```
Revisamos nuevamente el estatus con git status y posteriormente usamos el siguiente comando para añadir el proyecto al staging area (area de ensayo)
```
git add .
```
Verificamos nuevamente el estatus y en esta ocasion deben salir los archivos en color verde:
![image](https://user-images.githubusercontent.com/124689720/220146850-5e61e2d4-b677-4566-a3e0-ced98d90bd65.png)
A continuacion utilizamos el siguiente comando para comentar los cambios realizados:
```
git commit -m "Fist Commit"
```
Y para cargar los documentos al repositorio de GITHUB usamos: 
```
git push -u origin main
```
y asi finalizamos el proceso.

## Para editar cambios ##
Utilizamos los mismos pasos excepto:
*** git add (al inicio) ***
se escribirian los comandos de la siguiente forma 
```
git fetch origin main
git pull origin main 
git add .
git comit -m "edicion"
git push 
```
