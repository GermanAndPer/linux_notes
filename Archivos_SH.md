# 🛠️ Manual para Crear y Ejecutar Archivos `.sh`

Los archivos `.sh` son scripts escritos en **Shell** (generalmente Bash), que permiten automatizar tareas en sistemas Unix/Linux. Este manual te guiará paso a paso para crearlos, configurar permisos correctamente y ejecutarlos sin problemas.

---

## 📁 1. Crear el Archivo

El siguiente comando ayuda a crear un archivo:

```bash
#!/bin/bash
touch mi_script.sh
```

## ✍️ 2. Escribir el Scrip
Puedes escribir el contenido del archivo de la mejor manera que consideres. O Con el comando `ECHO`  y `>` en linux. Ej.:
```bash
#!/bin/bash
echo '
touch "31_.ipynb"
touch "32_.ipynb"
touch "33_.ipynb"
touch "34_.ipynb" 
' > mi_script.sh    #Este Script crea varios archivos Jupyter Notebooks
```
## 🔐 3. Asignar Permisos de Ejecución
Para que el sistema te permita ejecutar el archivo, necesitas otorgar permisos con el siguiente comando:
```bash
chmod +x mi_script.sh
```
Esto añade el permiso de ejecución al propietario del archivo.

📌 Si será usado por varios usuarios o en entornos colaborativos, la siguiente variación para permitir la ejecución a otros.
```bash
chmod 755 mi_script.sh
```
## 🚀 4. Ejecutar el Script
Hay varias formas de ejecutar el archivo, dependiendo de cómo desees usarlo:

```bash
./mi_script.sh       # Ejecuta el script en el shell actual
bash mi_script.sh    # Ejecuta explícitamente con Bash
sh mi_script.sh      # Ejecuta con el shell básico        
```
⚠️ Si usas `./`, asegúrate de estar en el mismo directorio o usar la ruta completa.

## ✅ Buenas Prácticas
- Usa comentarios (#) para explicar cada paso del script.
- Evita usar comandos absolutos innecesarios que limiten la portabilidad.
- Valida entradas para evitar errores o ejecuciones inseguras.
- Agrupa funciones reutilizables en un solo script base.
- Prueba en entornos seguros (como contenedores o máquinas virtuales) antes de usar en producción.

## 📦 Recomendaciones Extra
- Usa `#!/usr/bin/env` bash para hacer el script más portable entre sistemas.
- Versiona tus scripts en Git para mantener historial y mejoras.
- Documenta cada script en tu README con propósito, variables y casos de uso.
