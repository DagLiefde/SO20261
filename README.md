Integrantes:

Tomás Cadavid Martínez
Juan José García Álvarez

A continuación se describe el procedimiento realizado para completar el laboratorio utilizando la terminal de Linux (RedHat).

Punto 2 y 12:
En este punto se completaron los módulos del curso de RedHat desde el módulo 1 hasta el módulo 5, cumpliendo con los contenidos solicitados en la plataforma.
<img width="1314" height="655" alt="modulo5" src="https://github.com/user-attachments/assets/0fd6e08b-93bd-416f-9a03-4802b534e867" />
<img width="1409" height="623" alt="image" src="https://github.com/user-attachments/assets/9110506a-32eb-4b75-95d2-fe073968d0b9" />


Punto 3, 4 y 5:
Se creó la estructura del laboratorio dentro del directorio personal utilizando la terminal de Linux.
Luego se accedió al directorio creado y se verificó su ubicación absoluta.
Finalmente, la ruta fue almacenada dentro del archivo path.txt.
<img width="1366" height="768" alt="p3-4-5" src="https://github.com/user-attachments/assets/140d57cf-9365-4671-b9b2-b4720df65676" />

Punto 6:
Se crearon los directorios requeridos para el laboratorio dentro del proyecto mediante un único comando, permitiendo generar simultáneamente todas las carpetas necesarias.
<img width="1366" height="768" alt="p6" src="https://github.com/user-attachments/assets/38166995-d60d-4c87-91c3-0a71f7ba50e6" />

Punto 7:
Se generaron automáticamente 100 archivos dentro de cada directorio utilizando un ciclo for en Bash, evitando la creación manual de archivos.
También se verificó la correcta creación de los archivos listando su contenido.
<img width="1366" height="768" alt="p7" src="https://github.com/user-attachments/assets/559bc883-eec6-462e-96e3-59acd264132c" />

Punto 8:
Se eliminaron los primeros 10 y los últimos 20 archivos de cada directorio utilizando un ciclo iterativo que permitió realizar la operación de forma automática.
Se verificó la eliminación mostrando los primeros y últimos archivos restantes.
<img width="1366" height="768" alt="p8" src="https://github.com/user-attachments/assets/b2b709e3-9801-43a4-8977-57b70fc6f4ad" />

Punto 9:
Los directorios example, music y photos fueron movidos dentro del directorio projects, organizando la estructura final solicitada.
<img width="1366" height="768" alt="p9" src="https://github.com/user-attachments/assets/b100ff7a-101d-4ce3-9cd3-d2dfd410fc21" />

Punto 10:
Se eliminaron únicamente los archivos contenidos dentro del directorio projects utilizando el modo detallado, almacenando el resultado de la operación dentro del archivo output.txt.
<img width="1366" height="768" alt="p10" src="https://github.com/user-attachments/assets/362123ca-fcb3-45c1-a542-575b02b7d59f" />
<img width="1366" height="768" alt="p10_1" src="https://github.com/user-attachments/assets/5dee503c-b26d-4c0a-9857-83291cc033bb" />

Punto 13: 
Finalmente se verificó el estado del repositorio, se agregaron los archivos al área de preparación y se realizó el commit inicial del laboratorio para posteriormente enviarlo al repositorio remoto en GitHub mediante autenticación.
<img width="1366" height="768" alt="git1" src="https://github.com/user-attachments/assets/01f8f937-6701-42ce-853e-a24f66546e81" />
<img width="1366" height="768" alt="git2" src="https://github.com/user-attachments/assets/fb4f966c-85ec-4b05-abb1-1771150a3699" />
<img width="1366" height="768" alt="git3" src="https://github.com/user-attachments/assets/cc07ace9-ae19-439c-90d3-0665295351a6" />
<img width="1366" height="768" alt="git4" src="https://github.com/user-attachments/assets/8049d335-c18f-496d-a4e9-2009cc781cfc" />

Shortcuts utilizados:
En el desarrollo del laboratorio en la terminal Linux se utilizaron estos atajos de teclado para optimizar la ejecución de comandos:

Tab - Autocompletar comandos y rutas de directorios.
↑ (Flecha arriba) - Recuperar comandos previamente ejecutados.

Ctrl + C - Cancelar la ejecución de un comando en curso.
Ctrl + L - Limpiar la pantalla de la terminal.
Ctrl + A - Mover el cursor al inicio de la línea.
Ctrl + E - Mover el cursor al final de la línea.
Ctrl + Shift + C - Copiar texto desde la terminal.
Ctrl + Shift + V - Pegar texto en la terminal.

Shortcuts utilizados en el editor Nano
Ctrl + O - Guardar archivo.
Enter - Confirmar nombre del archivo.
Ctrl + X - Salir del editor.
Ctrl + K - Cortar línea.

Comandos utilizados so far:

```bash
sudo apt install git

ls
mkdir -p ~/operating-systems-20261/laboratories/lab0
cd operating-systems-20261/laboratories/lab0
pwd
pwd > path.txt
cat path.txt

mkdir example music photos projects

for dir in example music photos projects; do
touch $dir/file{1..100}
done

ls example | head
ls music | head
ls photos | wc -l
ls projects | wc -l

for i in {1..10} {81..100}; do
rm example/file$i music/file$i photos/file$i projects/file$i
done

ls example | wc -l
ls example | head
ls example | tail

mv example music photos projects/
ls
ls projects

rm -v projects/* > laboratories/lab0/output.txt
ls laboratories/lab0/output.txt
nano laboratories/lab0/output.txt

git init
git status
git add .
git commit -m "Commit inicial lab0"
git config --global user.email
git config --global user.name
git remote add origin
git branch -M main
git push -u origin main
```
