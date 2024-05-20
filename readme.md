# Configuración del Entorno Virtual

Este documento explica cómo configurar un entorno virtual para tu proyecto, activarlo, instalar las dependencias necesarias y desactivarlo al finalizar. Utilizaremos un script en Bash para automatizar el proceso.

## Requisitos Previos

- Python 3
- `pip3` (administrador de paquetes para Python 3)

## Configuración del Entorno Virtual

Sigue estos pasos para configurar tu entorno virtual:

1. **Clona el repositorio o descarga el proyecto.**
2. **Navega al directorio del proyecto.**
3. **Asegúrate de que tienes un archivo `requirements.txt` con las dependencias necesarias.**
4. **Ejecuta el script de configuración**:

    ```bash
    chmod +x setup_env.sh
    ./setup_env.sh
    ```

   Este script realiza las siguientes tareas:
   - Instala `virtualenv` si no está ya instalado.
   - Crea un entorno virtual llamado `.venv`.
   - Activa el entorno virtual.
   - Instala `ipykernel` y las dependencias listadas en `requirements.txt`.
   - Desactiva el entorno virtual al finalizar.

## Activar el Entorno Virtual

Para activar el entorno virtual, utiliza el siguiente comando:

- En sistemas Unix/Linux y macOS:

    ```bash
    source .venv/bin/activate
    ```

- En sistemas Windows:

    ```cmd
    .venv\Scripts\activate
    ```

Después de activar el entorno virtual, deberías ver el nombre del entorno virtual (`.venv`) en tu línea de comandos, indicando que estás trabajando dentro del entorno virtual.

## Desactivar el Entorno Virtual

Para desactivar el entorno virtual, simplemente utiliza el comando:

```bash
deactivate
```
Este comando restablece tu terminal a su estado original, desactivando el entorno virtual.

## Notas Adicionales
- Asegúrate de tener el archivo requirements.txt en el directorio del proyecto con todas las dependencias necesarias.
- El script está diseñado para continuar con la instalación de las dependencias incluso si una de ellas falla. Si esto ocurre, verás un mensaje de error específico para la dependencia que falló, pero el script continuará instalando las siguientes dependencias.

