# Práctica de Laboratorio: Línea de Comandos y Bash

**Alumno:** Isaac Natanael Esquivel Márquez  
**Institución:** Universidad Autónoma de Zacatecas "Francisco García Salinas"  
**Curso:** Laboratorio / CLI  

---

## Índice de Actividades

1. [Actividad 1: Estructura de Directorios y Archivos](#actividad-1-estructura-de-directorios-y-archivos)
2. [Actividad 2: Creación de Archivos y Contenido](#actividad-2-creación-de-archivos-y-contenido)
3. [Actividad 3: Creación de Alias de Navegación](#actividad-3-creación-de-alias-de-navegación)
4. [Actividad 4: Historial de Comandos](#actividad-4-historial-de-comandos)
5. [Actividad 5: Automatización con Alias y Gestión de Directorios/Archivos](#actividad-5-automatización-con-alias-y-gestión-de-directoriosarchivos)

---

## Actividad 1: Estructura de Directorios y Archivos

### Instrucciones del pizarón:
1. Crear dentro de `Laboratorio-cli` una carpeta `proyectos`.
2. Dentro de `proyectos`, crear las carpetas `web` y `movil`.
3. Dentro de `web`, crear el archivo `index.html` usando `touch`.

### Comandos ejecutados y evidencia:
```bash
cd ~/laboratorio-cli/
mkdir proyectos
cd proyectos/
mkdir web movil
cd web
touch index.html
```

---

## Actividad 2: Creación de Archivos y Contenido

### Instrucciones del pizarón:
1. Dentro de `proyectos/movil`, crear el archivo `notas.txt` (usando `touch` y `nano`).
2. Dentro de `notas.txt`, colocar el texto: `"Aprendemos a crear archivos con touch y nano"`.

### Comandos ejecutados y evidencia:
```bash
cd movil
touch notas.txt
nano notas.txt
```

Contenido dentro de `notas.txt`:
```text
Aprendemos a crear archivos con touch y nano
```

---

## Actividad 3: Creación de Alias de Navegación

### Instrucciones del pizarón:
1. Crear un alias llamado `ir_notas` que abra directamente desde cualquier carpeta el archivo `notas.txt`.

### Comandos y correcciones probadas:
  ```bash
  alias ir_notas='nano laboratorio/proyectos/movil/notas.txt'
  ```

---

## Actividad 4: Historial de Comandos

### Instrucciones del pizarón:
1. Revisar el historial de los últimos 5 comandos y filtrar su contenido para solo mostrar la ejecución de `touch`.
2. Eliminar el historial de comandos (`history -c`).
3. Ejecutar `!!`.
4. Presentar el historial actual.

### Comandos ejecutados y evidencia:
```bash
history 5
history | grep "touch"
history -c
!!
history
```

---

## Actividad 5: Automatización con Alias y Gestión de Directorios/Archivos

### Instrucciones del pizarón:
1. Crear un alias llamado `respaldo` que genere una carpeta con el mismo nombre (`mkdir respaldo`).
2. Ejecutar el alias `respaldo`.
3. Entrar a la carpeta `respaldo` y crear un archivo llamado `log.txt`.
4. Dentro de `log.txt`, colocar la palabra `"OK"` (y posteriormente agregar `"ERROR"`).
5. Crear un alias que genere la palabra `"Error"` dentro del archivo `log.txt` llamado `error` (`alias error='echo "ERROR" >> log.txt'`).
6. Crear un alias llamado `wiper` que elimine el archivo `log.txt` y la carpeta `respaldo` (`alias wiper='rm -rf respaldo'`).

### Comandos ejecutados y evidencia:
```bash
alias respaldo='mkdir respaldo'
respaldo
cd respaldo
touch log.txt
nano log.txt
alias error='echo "ERROR" >> log.txt'
error
nano log.txt
alias wiper='rm log.txt && cd .. && rm -r respaldo'
wiper
```
