# RespositorioCursodevops


### DevOps-Foundations This repository contains hands-on exercise for the DevOps Foundations course
## Exercises: 
- git add Readme.md
- git commit -m "added a brief description to README.md"
- git push -u origin add-README
- git pull origin main
- git checkout main
- git merge add-README
- git push
- git branch -d add-README
- git push origin --delete add.README

## RESUMEN PERSONALIZADO PASO A PASO CON COMANDOS Y CONCEPTOS CLAVES
CI/CD + YAML

## 1. CI – Integración Continua

Qué es: Automatiza la integración de cambios de código en un repositorio compartido.

Objetivo: Detectar errores temprano y asegurar que el código nuevo funcione con el existente.

Cómo funciona:

Un desarrollador hace push de cambios.

El sistema CI ejecuta tests automáticos y builds.

Retroalimentación inmediata al equipo.

Beneficio: Problemas se resuelven antes de que se conviertan en errores mayores.

---

## 2. CD – Despliegue/Entrega Continua

Entrega continua: Código listo para despliegue, puede requerir aprobación manual.

Despliegue continuo: Totalmente automatizado; código validado se libera automáticamente a producción.

Ventajas:

Menos intervención manual.

Actualizaciones más rápidas y confiables.

Reducción de errores y riesgos.

Permite liberar actualizaciones pequeñas y frecuentes.

---

## 3. Herramientas comunes CI/CD
Herramienta	Características principales
Jenkins	Open source, flexible, integra casi cualquier herramienta, requiere setup manual.
GitHub Actions	Integrado en GitHub, fácil de usar, mínima configuración, preintegraciones disponibles.
GitLab CI/CD	Integrado en GitLab, potente, incluye revisión de código, monitoreo y despliegue.

Elección depende del ecosistema, experiencia del equipo y necesidades del proyecto.

Muchas herramientas tienen versiones gratuitas o open source.

---

## 4. Beneficios de CI/CD

Automatiza pruebas y despliegues.

Reduce tiempo de entrega al mercado.

Minimiza errores humanos.

Facilita colaboración simultánea en múltiples funcionalidades.

Solo el código probado llega a producción.

Integración con monitoreo para alertas tempranas.

---

## 5. YAML

Qué es: Formato simple y legible para archivos de configuración.

Uso en DevOps: Configuración de pipelines CI/CD.

Estructura:

Clave-valor: nombre: valor

Listas: cada ítem precedido por -

Anidamiento: mediante indentación con espacios

Ventaja: Intuitivo para desarrolladores y no desarrolladores.

---

## 6. GitHub Actions + YAML

Workflows: Archivos YAML que automatizan tareas (build, test, deploy).

Ubicación: Carpeta .github/workflows del repositorio.

Activadores (triggers): Ej. push de código, apertura de pull request.

Jobs: Tareas individuales, que pueden ejecutarse en secuencia o paralelo.

Ejemplo básico:

name: CI
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Run tests
        run: npm test


## Diagrama de flujo

![Diagrama de flujo](https://github.com/AnaJotta/RespositorioCursodevops/blob/main/Diagrama%20de%20flujo.png?raw=true)


---

# Introducción a Docker

Docker es una plataforma que permite crear, ejecutar y gestionar contenedores: entornos ligeros y autónomos que incluyen una aplicación y todas sus dependencias. Esto garantiza que la aplicación funcione igual en cualquier entorno, desde tu computadora hasta servidores en la nube.

## 🧩 Conceptos clave
1️⃣ Imágenes

📦 Paquetes de solo lectura que contienen todo lo necesario para ejecutar una aplicación: código, librerías y dependencias.

📝 Actúan como plantillas para crear contenedores.

🔹 Ejemplo: una imagen con una aplicación en Python y todas sus librerías.

2️⃣ Contenedores

⚙️ Instancias de imágenes que se ejecutan como procesos aislados.

🔄 Son dinámicos: se pueden iniciar, detener y modificar durante su ciclo de vida.

📈 Permiten escalabilidad y consistencia.

3️⃣ Dockerfile

📝 Archivo de texto con instrucciones para construir una imagen.

## 🔧 Define pasos como instalar librerías, copiar código y configurar el entorno.

🖥 Comandos básicos

- docker build – Crea una imagen desde un Dockerfile.

- docker run – Inicia un contenedor desde una imagen.

- docker stop – Detiene un contenedor en ejecución.

- docker ps – Lista todos los contenedores que están corriendo.

## 🌟 Ventajas de Docker

- 🌍 Portabilidad: funciona igual en diferentes entornos.

- ⚡ Ligero y eficiente: consume menos recursos que una máquina virtual y arranca rápidamente.

- ✅ Consistencia: elimina el problema de “funciona en mi máquina”.

- 📊 Escalabilidad: se pueden crear o eliminar contenedores según la demanda de tráfico.
