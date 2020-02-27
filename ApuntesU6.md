# DOCUMENTACIÓN Y CONTROL DE VERSIONES


## INTRODUCCIÓN
### EN ESTA UNIDAD APRENDEREMOS A
 - Identificar diferentes herramientas de generación de documentación.
 - Utilizar diferentes formatos para la documentación.
 - Utilizar herramientas colaborativas para la elaboración y mantenimiento de la documentación.
 - Instalar, configurar y utilizar un sistema de control de versiones.

## DOCUMENTACIÓN CON MARKDOWN
### CABECERAS

### LISTAS SIN ORDEN
### LISTAS CON ORDEN
### FORMATO
### ENLACES
### IMÁGENES
### CITAS
### CÓDIGO FUENTE
### MENCIONES Y REFERENCIAS


## CONTROL DE VERSIONES CON GIT
### INSTALACIÓN DE GIT
```ssh
sudo  apt  install  git
```
### CONFIGURACIÓN DE GIT
```ssh
git  config  --global  user.name   "Nombre y Apellidos"
git  config  --global  user.email  "nombre@mail.com"
```
### INICIAR REPOSITORIO LOCAL
```ssh
git  init
```
  - Es recomendable crear un archivo .gitignore con listado de carpetas y archivos a los que no se realizará seguimiento.
### COMANDOS BÁSICOS
```ssh
git  status
git  add .
git  commit -m  "Mensaje"

```
### CLONAR REPOSITORIO REMOTO
```ssh
git  clone   https://github.com/usuario/repositorio.git
git  clone   git@github.com:usuario/repositorio.git
```
### VINCULAR Y DESVINCULAR REPOSITORIO REMOTO
```ssh
git  remote  -v
git  remote  add  origin  https://github.com/usuario/repositorio.git
git  remote  rm   origin
```
### BAJAR Y SUBIR CONTENIDO A REPOSITORIO REMOTO
```ssh
git  pull  origin  master  // bajar commits
git  push  origin  master  // subir commits
```
### TRABAJO CON RAMAS
```ssh
git  branch    -va        // listado verbose, all (local y remoto)

git  branch    nuevo      // creación de rama
git  checkout  nuevo      // cambiar a dicha rama

git  checkout  -b nuevo   // equivalente a las 2 sentencias anteriores
```
### CHECKOUT
  - El comando checkout de git sirve para cambiar de rama.
```ssh
git  checkout  rama
```

  - También sirve para cambiar de commit dentro de una rama.
```ssh
git  checkout  0f82
```
### ETIQUETAS DE ANOTACIÓN
```ssh
git tag -l                          // Listado
git tag -a v1.0 -m "Version 1.0"    // Añadir etiqueta
git tag -d v1.0                     // Eliminar etiqueta
```
  - Las etiquetas deben enviarse explícitamente al repositorio remoto:
```ssh
git  push  --tags
```