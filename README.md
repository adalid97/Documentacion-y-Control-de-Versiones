# DOCUMENTACIÓN Y CONTROL DE VERSIONES

## ÍNDICE

- [INTRODUCCIÓN](#INTRODUCCIÓN)
- [DOCUMENTACIÓN CON MARKDOWN](#DOCUMENTACIÓN-CON-MARKDOWN)
- [CONTROL DE VERSIONES CON GIT](#CONTROL-DE-VERSIONES-CON-GIT)

## INTRODUCCIÓN

### EN ESTA UNIDAD APRENDEREMOS A
 - Identificar diferentes herramientas de generación de documentación.
 - Utilizar diferentes formatos para la documentación.
 - Utilizar herramientas colaborativas para la elaboración y mantenimiento de la documentación.
 - Instalar, configurar y utilizar un sistema de control de versiones.

## DOCUMENTACIÓN CON MARKDOWN

### CABECERAS
```markdown
# Esto es un H1
## Esto es un H2
### Esto es un H3
#### Esto es un H4
##### Esto es un H5
###### Esto es un H6
```

### LISTAS SIN ORDEN
```markdown
* Item 1
* Item 2
 * Item 2a
 * Item 2b
```

### LISTAS CON ORDEN
```markdown
1. Item 1
2. Item 2
3. Item 3
 * Item 3a
 * Item 3b
```
### FORMATO
#### Cursivas

`*Esto es cursiva*`

`_Esto también es cursiva_`

#### Negrita

`**Esto es negrita**`

`__Esto también es negrita__`

#### Tachado
`~~Esto es tachado~~`

### ENLACES
```markdown
https://github.com/adalid97 - GitHub José Ángel Adalid
[GitHub](https://github.com/adalid97)
```
https://github.com/adalid97 - GitHub José Ángel Adalid
[GitHub](https://github.com/adalid97)

### IMÁGENES
```markdown
![GitHub Logo](/images/logo.jpg)
Formato: ![Texto alternativo](url)
```
![GitHub Logo](https://steemitimages.com/640x0/https://camo.githubusercontent.com/7710b43d0476b6f6d4b4b2865e35c108f69991f3/68747470733a2f2f7777772e69636f6e66696e6465722e636f6d2f646174612f69636f6e732f6f637469636f6e732f313032342f6d61726b2d6769746875622d3235362e706e67)

### CITAS
Como dijo Antonio Machado:
> Despacito y buena letra, que el hacer las cosas bien, importa más que el hacerlas.

```markdown
> Despacito y buena letra, que el hacer las cosas bien, importa más que el hacerlas.
```
### CÓDIGO FUENTE
<pre>
```javascript
var s = "Lenguaje javascript. Se realizará coloreado de sintaxis.";
alert(s); 
```

```python
s = "Lenguaje Python. Se realizará coloreado de sintaxis."
print s
```

```
No se indica lenguaje. No se realizará coloreado de sintaxis. 
```
</pre>

```javascript
var s = "Lenguaje javascript. Se realizará coloreado de sintaxis.";
alert(s); 
```

```python
s = "Lenguaje Python. Se realizará coloreado de sintaxis."
print s
```

```
No se indica lenguaje. No se realizará coloreado de sintaxis. 
```

### MENCIONES Y REFERENCIAS
 - Menciones a usuarios: @usuario

 - Referencias a Issues y Pull request: #numero

### TABLAS
<pre>
|HORA| LUNES | MARTES | MIÉRCOLES | JUEVES | VIERNES |
| -- | -- | -- | -- | -- | -- |
|8:15| DWEC | DAW | DWEC | DWEC | EIE |
|9:15| DWEC | EIE | DWEC | DWEC | EIE |
|10:15| DIW | EIE | DWES | DWES | HLC |
|11:15| R | E | CR | E | O |
|11:45| DIW | DIW | DWES | DWES | DIW |
|12:45| DWES | DWES | DIW | DAW | HLC |
|13:45| DWES | DWES | DIW | DAW | HLC |
</pre>

|HORA| LUNES | MARTES | MIÉRCOLES | JUEVES | VIERNES |
| -- | -- | -- | -- | -- | -- |
|8:15| DWEC | DAW | DWEC | DWEC | EIE |
|9:15| DWEC | EIE | DWEC | DWEC | EIE |
|10:15| DIW | EIE | DWES | DWES | HLC |
|11:15| R | E | CR | E | O |
|11:45| DIW | DIW | DWES | DWES | DIW |
|12:45| DWES | DWES | DIW | DAW | HLC |
|13:45| DWES | DWES | DIW | DAW | HLC |

## CONTROL DE VERSIONES CON GIT

### INSTALACIÓN DE GIT
```ssh
sudo  apt  install  git
```
### CONFIGURACIÓN DE GIT
Configurar el nombre que aparece en los commits.
```ssh
git  config  --global  user.name   "Nombre y Apellidos"
```
Configurar Email.
```ssh
git  config  --global  user.email  "nombre@mail.com"
```

### INICIAR REPOSITORIO LOCAL
```ssh
git  init
```
Cargar en el HEAD los cambios realizados.
```ssh
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
Bajar commits
```ssh
git  pull  origin  master
```
Subir commits.
```ssh
git  push  origin  master
```

### TRABAJO CON RAMAS
Crea un branch
```ssh
git branch <nombreBranch>
```
Lista los branches
```ssh
git branch
```

Elimina sin preguntar
```ssh
git branch -D <nombreBranch>
```

### CHECKOUT
El comando checkout nos permite cambiar de rama..
```ssh
git  checkout <nombreBranch>
```

También sirve para cambiar de commit dentro de una rama.
```ssh
git  checkout  0f82
```
### ETIQUETAS DE ANOTACIÓN
```ssh
git tag -l                          // Listado
git tag -a v1.0 -m "Version 1.0"    // Añadir etiqueta
git tag -d v1.0                     // Eliminar etiqueta
```
Las etiquetas deben enviarse explícitamente al repositorio remoto:
```ssh
git  push  --tags
```
