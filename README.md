# Curso de Jenkins - Pipelines Básicos

Este repositorio contiene una serie de recursos y archivos Jenkinsfiles diseñados para enseñar y practicar el uso de Jenkins, una herramienta de automatización ampliamente utilizada en el desarrollo de software. Aquí encontrarás ejemplos de sintaxis básica, mecanismos de flujo de control, etc.

## Estructura del repositorio

El repositorio se organiza de la siguiente manera:

- **Jenkinsfile-basicoX**: Estos ficheros son una serie de Jenkinsfiles que abarcan los conceptos fundamentales de pipelines y su sintaxis básica. Estos ejemplos te ayudarán a comprender la estructura de un Jenkinsfile y cómo configurar pipelines sencillos para tus proyectos.

## Pipelines incluidos

### Jenkinsfile-basico1

Pipeline declarativo mínimo. Muestra la estructura básica de un Jenkinsfile con `pipeline`, `agent`, `stages`, `stage` y `steps`, ejecutando un simple `echo`.

### Jenkinsfile-basico2

Uso de variables de entorno y credenciales. Enseña cómo declarar variables globales con `environment` y cómo inyectar credenciales de Jenkins con `credentials()`.

### Jenkinsfile-basico3

Uso de parámetros de entrada al lanzar el pipeline. Incluye ejemplos de `string`, `text`, `booleanParam`, `choice` y `password`, y muestra cómo leerlos desde `params`.

### Jenkinsfile-basico4

Uso de aprobaciones manuales con `input`. Muestra una pausa declarativa dentro de una fase y otra pausa creada desde un bloque `script`, incluyendo un ejemplo con `timeout`.

### Jenkinsfile-basico5

Ejemplo de lógica condicional dentro de un bloque `script`. Evalúa la rama de ejecución con `env.BRANCH_NAME` y ejecuta acciones diferentes según su valor.

### Jenkinsfile-basico6

Uso de la directiva `when`. Muestra cómo decidir si una fase debe ejecutarse o saltarse en función de una expresión booleana.

### Jenkinsfile-basico7

Uso de `withEnv`, herramientas configuradas en Jenkins y Maven. Enseña cómo definir variables de entorno temporales y cómo seleccionar instalaciones de herramientas como JDK o Maven.

### Jenkinsfile-basico8

Estructuras de control dentro de bloques `script`. Incluye ejemplos de `if`, `switch`, `for` y `while`, apoyándose en entradas manuales del usuario.

### Jenkinsfile-basico9

Acciones posteriores a la ejecución con `post`. Muestra bloques habituales como `always`, `success`, `failure` y `cleanup`.

### Jenkinsfile-basico10

Ejecución de fases en paralelo con `parallel`. Simula pruebas unitarias, pruebas de integración y análisis estático ejecutándose al mismo tiempo.

### Jenkinsfile-basico11

Gestión de ficheros generados durante el pipeline. Enseña cómo crear un fichero, moverlo entre fases con `stash` y `unstash`, y publicarlo como artefacto con `archiveArtifacts`.

### Jenkinsfile-basico12

Opciones generales y control de ejecución. Incluye `timestamps`, `timeout`, conservación limitada de builds con `buildDiscarder` y reintentos con `retry`.

### Jenkinsfile-basico13

Ejecución periódica mediante `triggers`. Usa `cron` para mostrar cómo programar automáticamente un pipeline.

## ¿Cómo utilizar este repositorio?

1. Clona este repositorio en tu máquina local utilizando el siguiente comando:
```console
git clone https://github.com/jacampano/pipelinesBasicos.git
```
2. Explora las diferentes secciones del repositorio y navega por los archivos Jenkinsfiles proporcionados.

3. Abre los Jenkinsfiles en un editor de texto de tu elección y estudia la sintaxis y configuración utilizada en cada uno de ellos. 

4. Si deseas ejecutar alguno de los Jenkinsfiles, asegúrate de tener una instancia de Jenkins configurada y en funcionamiento. Luego, puedes importar el Jenkinsfile correspondiente en tu proyecto Jenkins y ajustar los parámetros según sea necesario.
