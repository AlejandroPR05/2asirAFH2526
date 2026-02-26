# Documentación del Entregable - Hackaton / Proyecto ASIR

Este documento contiene la información necesaria para completar los apartados de "Resultados de Aprendizaje" y "Descripción Técnica" del entregable, basado en los proyectos de Agentes de IA Locales, Fine-Tuning y Conexión Remota encontrados en el repositorio.

---

## 1. Resultados de Aprendizaje

### Abstract (Inglés profesional)

**Title:** Local Deployment and Fine-Tuning of AI Agents for Specialized Tasks

**Abstract:**
This project focuses on the implementation and deployment of local Artificial Intelligence agents using open-source Large Language Models (LLMs). The primary objective is to establish a secure, private, and efficient AI environment on consumer-grade hardware (Windows 11 with NVIDIA GPUs), eliminating the dependency on external cloud providers. Key activities include the configuration of Ollama for model inference, the setup of OpenCode for AI-assisted development, and the Fine-Tuning of base models (such as Phi-3) using Axolotl to create specialized agents like a "Chef-Bot". Furthermore, the project integrates remote access solutions (SSH, RDP) to manage the infrastructure efficiently. This approach demonstrates the viability of sovereign AI systems that ensure data privacy and operational sustainability, aligning with modern cybersecurity standards and green computing practices.

### Objetivos Generales

#### Itinerario personal para la empleabilidad II (RA3)
*   **Innovación y Modernización:** Se ha identificado el concepto de "Sovereign AI" (IA Soberana) como una innovación clave para modernizar el sector productivo. Al desplegar modelos locales, las empresas pueden integrar inteligencia artificial en sus procesos sin exponer datos sensibles a terceros, fomentando un modelo de negocio más autónomo y seguro.
*   **Bienestar Social:** La democratización del acceso a LLMs potentes mediante hardware de consumo permite que pequeñas empresas y desarrolladores individuales accedan a herramientas avanzadas, reduciendo la brecha tecnológica y mejorando la competitividad del tejido empresarial local.

#### Sostenibilidad aplicada al sistema productivo (RA3)
*   **Eficiencia Energética (Green AI):** Se aplican criterios de sostenibilidad mediante el uso de técnicas de **cuantización** (modelos de 4 bits). Esto reduce drásticamente el consumo de memoria VRAM y la potencia de cálculo necesaria, permitiendo ejecutar modelos complejos en hardware doméstico (reutilización de equipos existentes) en lugar de depender de grandes centros de datos con alto consumo energético.
*   **Economía Circular:** El proyecto promueve la reutilización de hardware "gamer" (GPUs RTX 30/40) para tareas de investigación e inferencia de IA, extendiendo la vida útil de los equipos y evitando la generación prematura de residuos electrónicos.

---

## 2. Descripción Técnica

### Instalación, herramientas de desarrollo utilizadas

#### Administración de sistemas operativos (RA2, RA3)
*   **RA2. Administración de Procesos:**
    *   Monitorización activa del rendimiento del sistema (CPU, RAM, VRAM) utilizando el Administrador de Tareas de Windows y herramientas de línea de comandos como `nvidia-smi` para asegurar que la carga de los modelos no sature la GPU.
    *   Gestión de procesos en segundo plano para el servidor de inferencia Ollama.
*   **RA3. Automatización de Tareas:**
    *   Uso de **PowerShell** para la configuración del entorno.
    *   Creación de scripts para la instalación automatizada de dependencias (`pip install`, `npm install`).
    *   Gestión de entornos virtuales de Python (`venv`) para aislar las librerías del proyecto y evitar conflictos.

#### Herramientas utilizadas y aspectos de seguridad

*   **Herramientas de Desarrollo:**
    *   **Lenguajes:** Python (entrenamiento/inferencia), Node.js (OpenCode).
    *   **Frameworks/Librerías:** Axolotl (Fine-Tuning), llama.cpp (Conversión GGUF), Ollama (Inferencia).
    *   **Control de Versiones:** Git (clonación de repositorios y gestión de cambios).
    *   **IDE:** VS Code con extensiones de IA local.

*   **Seguridad y alta disponibilidad (RA6, RA7):**
    *   **RA6. Alta Disponibilidad y Virtualización:**
        *   Implementación de servicios que se ejecutan localmente, garantizando la disponibilidad incluso sin conexión a internet (offline-first).
        *   Uso de entornos aislados (Virtual Environments) para asegurar la estabilidad de las aplicaciones.
    *   **RA7. Seguridad y Protección de Datos:**
        *   **Privacidad por Diseño:** Todos los datos (datasets de entrenamiento, prompts, respuestas) se procesan y almacenan localmente. Nada se envía a la nube.
        *   **Cumplimiento Normativo:** Al no existir transferencia de datos a terceros, se simplifica el cumplimiento del RGPD.
        *   **Control de Acceso:** Configuración de Firewall de Windows para gestionar el tráfico en el puerto 11434 (API de Ollama) y uso de claves SSH para el acceso remoto seguro.

### Implantación de aplicaciones web

*   **RA3. Implementación:**
    *   Despliegue de interfaces web para interactuar con los modelos (Open WebUI o similar).
    *   Integración de bases de datos locales (archivos JSONL para datasets) con la lógica de entrenamiento en Python.
*   **RA5. Despliegue y Publicación:**
    *   Configuración del servidor local Ollama para exponer una API compatible con OpenAI.
    *   Documentación técnica detallada en formato HTML/PDF para facilitar la replicabilidad del despliegue.
*   **Multiplataforma:**
    *   Las soluciones implementadas son accesibles desde diferentes sistemas operativos (Windows, Linux, Android) gracias al uso de protocolos estándar (HTTP, SSH) y herramientas web responsivas.

### Servicios de red e Internet

*   **RA4. Instalación y Configuración:**
    *   **Servicio Web (API):** Configuración del servidor Ollama en el puerto `11434`.
    *   **SSH (Secure Shell):** Instalación y configuración de OpenSSH Server en Windows/Linux para administración remota segura (Puerto 22).
    *   **RDP (Remote Desktop Protocol):** Habilitación de Escritorio Remoto para gestión gráfica (Puerto 3389).
*   **RA6. Supervisión:**
    *   Verificación de la conectividad y disponibilidad de los servicios mediante pruebas de conexión (`curl`, `ssh`, `ping`).
    *   Diagnóstico de problemas de red y configuración de reglas de firewall para permitir el tráfico legítimo.

---

## 3. Presentación de Software

### Digitalización aplicada a los sectores productivos (RA5)
*   **Protección del Dato en la Economía Digital:**
    *   El proyecto aborda el desafío crítico de la soberanía de datos. En un entorno globalizado donde la fuga de información es un riesgo constante, el despliegue de **IA Local** asegura que la propiedad intelectual y los datos confidenciales nunca salgan de la infraestructura de la organización.
    *   Se definen sistemas de seguridad a nivel de equipo (cifrado de disco, usuarios locales) y a nivel de red (VPN, SSH tunelizado) para proteger los activos digitales.

### Manual de usuario (Módulo Profesional Optativo II)
*   **Documentación Elaborada:**
    *   Se han creado manuales paso a paso detallados que incluyen:
        1.  **Manual de Agentes IA Local:** Guía de instalación de Ollama y OpenCode en Windows 11.
        2.  **Manual de Creación de LLM (Fine-Tuning):** Guía técnica sobre cómo entrenar un modelo personalizado ("Chef-Bot") usando Axolotl.
        3.  **Manual de Conexión Remota:** Instrucciones para SSH, RDP y TeamViewer.
    *   Estos manuales utilizan un lenguaje claro, capturas de pantalla explicativas y bloques de código para facilitar la comprensión y ejecución por parte del usuario final.
