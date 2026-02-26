# DOCUMENTACIÓN DEL PROYECTO - HACKATON / 2º ASIR

> **NOTA PARA EL ALUMNO:** Este documento contiene el contenido textual necesario para rellenar tu entregable PDF. Debes copiar y pegar estas secciones en tu procesador de textos (Word/Google Docs), asegurándote de aplicar el formato de **Normativa APA** (Fuentes tipo Times New Roman 12 o Arial 11, interlineado 1.5, márgenes de 2.54 cm). No olvides generar el índice y la lista de figuras automáticamente.

---

## PORTADA (Sugerida)

**Título del Proyecto:** Despliegue de Infraestructura de Inteligencia Artificial Soberana y Agentes Especializados en Entornos Locales
**Módulo:** Proyecto de Administración de Sistemas Informáticos en Red
**Autor:** Alejandro Pascual Ramos
**Curso:** 2º ASIR
**Fecha:** [Fecha Actual]

---

## 1. DOCUMENTACIÓN DE PROYECTO (3 ptos)

### 1.1 Entrega y consecución de anteproyecto

El presente proyecto nace de la necesidad de democratizar el acceso a herramientas de Inteligencia Artificial (IA) avanzada sin depender de proveedores de nube externos, garantizando así la privacidad de los datos y la soberanía tecnológica.

El anteproyecto planteó el despliegue de una infraestructura completa de IA Generativa en hardware de consumo (PC con GPU NVIDIA RTX), abarcando desde la instalación de motores de inferencia (Ollama) hasta la creación de modelos personalizados mediante técnicas de Fine-Tuning (Axolotl) y su optimización mediante Cuantización (llama.cpp).

Se ha logrado con éxito la consecución de todos los objetivos planteados:
1.  **Infraestructura Base:** Servidor Windows 11 optimizado para IA.
2.  **Agentes Inteligentes:** Despliegue de asistentes de codificación (OpenCode) y propósito general.
3.  **Especialización:** Entrenamiento de un modelo "Chef-Bot" capaz de generar recetas a partir de ingredientes.
4.  **Optimización:** Reducción del tamaño de modelos (4-bit) para duplicar la velocidad de inferencia.
5.  **Acceso Remoto:** Gestión segura del sistema mediante SSH y Escritorio Remoto.

### 1.2 Cumplimiento de la Normativa APA

> *[Instrucción: Asegúrate de que tu documento final tenga un Índice de Contenidos, Índice de Figuras y que las citas bibliográficas sigan el formato (Autor, Año).]*

### 1.3 Calidad

La documentación se ha elaborado siguiendo estándares técnicos profesionales, utilizando terminología precisa del sector (Cuantización Q4_K_M, LoRA, GGUF, Inferencia) y estructurando la información de manera lógica y secuencial para facilitar su replicabilidad.

### 1.4 Bibliografía

*   **Ollama.** (2024). *Get up and running with large language models*. Recuperado de https://ollama.com/
*   **Microsoft.** (2024). *Phi-3 Cookbook*. Recuperado de https://github.com/microsoft/Phi-3Cookbook
*   **Gerganov, G.** (2024). *llama.cpp: Inference of LLaMA model in pure C/C++*. Recuperado de https://github.com/ggerganov/llama.cpp
*   **OpenAccess AI Collective.** (2024). *Axolotl: A comprehensive tool for LLM fine-tuning*. GitHub Repository.
*   **NVIDIA.** (2024). *CUDA Toolkit Documentation*.

### 1.5 Conclusiones y futuras mejoras

**Conclusiones:**
El proyecto demuestra que es totalmente viable ejecutar cargas de trabajo de IA complejas en hardware doméstico moderno. La **cuantización** ha demostrado ser crítica, permitiendo que modelos como Phi-3-mini ejecuten a **87 tokens/segundo** en versión de 4 bits, frente a los 49 tokens/segundo de la versión original, sin una pérdida perceptible de calidad en tareas de razonamiento lógico y creatividad. Además, el Fine-Tuning con adaptadores LoRA permite personalizar modelos con recursos limitados, abriendo la puerta a asistentes especializados para PYMES.

**Futuras Mejoras:**
1.  **Implementación de RAG (Retrieval-Augmented Generation):** Conectar los modelos a una base de conocimiento documental local (PDFs, Wikis) para que respondan con información actualizada.
2.  **Orquestación de Agentes:** Utilizar frameworks como CrewAI para que múltiples modelos especializados (uno programador, otro escritor) colaboren en tareas complejas.
3.  **Interfaz de Voz:** Integrar Whisper (OpenAI) para permitir la interacción por voz con el servidor.

### 1.6 Anexos

Se adjuntan al proyecto los siguientes manuales técnicos desarrollados:
1.  **Manual de Agentes IA:** Instalación de Ollama y OpenCode.
2.  **Manual de Fine-Tuning:** Creación del "Chef-Bot" con Axolotl.
3.  **Manual de Cuantización:** Conversión de modelos a GGUF con llama.cpp.
4.  **Comparativa de Modelos:** Benchmark de rendimiento entre Gemma, DeepSeek y Qwen.
5.  **Manual de Conexión Remota:** Configuración de SSH y RDP.

---

## 2. PRESENTACIÓN (1 pto)

### 2.1 Guion de Diapositivas (Sugerencia)

*   **Diapositiva 1: Título.** "IA Soberana: Despliegue y Entrenamiento Local". Nombre del alumno.
*   **Diapositiva 2: El Problema.** Dependencia de la nube, privacidad de datos, costes recurrentes, latencia.
*   **Diapositiva 3: La Solución.** Servidor Local con GPU NVIDIA. Software Open Source (Ollama, Axolotl).
*   **Diapositiva 4: Arquitectura Técnica.** Windows 11 + WSL2. Flujo: Dataset -> Fine-Tuning (LoRA) -> Fusión -> Cuantización (GGUF).
*   **Diapositiva 5: Resultados (Demo).** Mostrar captura del "Chef-Bot" creando una receta y la comparativa de velocidad (87 vs 49 tk/s).
*   **Diapositiva 6: Conclusiones.** Viabilidad, Eficiencia Energética, Privacidad Total.

### 2.2 Exposición (Ideas clave para hablar)

*   "Buenos días. Mi proyecto trata sobre cómo traer la potencia de ChatGPT a nuestro propio ordenador, sin compartir datos con nadie."
*   "He utilizado una tarjeta gráfica de consumo (RTX 4060 Ti) para entrenar a una IA y enseñarle a cocinar usando un dataset propio."
*   "Lo más interesante ha sido el proceso de 'cuantización', donde comprimimos el 'cerebro' de la IA para que piense el doble de rápido ocupando menos memoria."
*   "Todo el sistema se puede administrar remotamente, permitiendo tener el servidor en un armario y usarlo desde el portátil o el móvil."

### 2.3 Simulaciones

*   **En vivo:** Se mostrará una conexión SSH al servidor y se ejecutará el comando `ollama run chef-bot` para pedirle una receta en tiempo real, demostrando la velocidad de respuesta.
*   **Alternativa (Vídeo):** Un vídeo grabado de la pantalla dividida: a la izquierda el monitor de recursos (GPU al 100%) y a la derecha la IA generando texto.

---

## 3. DEFENSA (1 pto)

> *[Recordatorios para el alumno]*
*   **Asistencia y puntualidad:** Llega 15 minutos antes. Revisa que el proyector funcione con tu equipo.
*   **Distribución grupal:** (Si es individual, ignora esto. Si es grupo, asegura que cada uno hable el mismo tiempo).
*   **Plazo:** Asegúrate de subir este PDF antes de la hora límite en la plataforma.

---

## 4. RESULTADOS DE APRENDIZAJE (5 ptos)

### 4.1 Abstract (Inglés profesional - Nivel B2)

**Title:** Local Deployment and Fine-Tuning of AI Agents for Specialized Tasks

**Abstract:**
This project focuses on the implementation and deployment of local Artificial Intelligence agents using open-source Large Language Models (LLMs). The primary objective is to establish a secure, private, and efficient AI environment on consumer-grade hardware (Windows 11 with NVIDIA GPUs), eliminating the dependency on external cloud providers. Key activities include the configuration of Ollama for model inference, the setup of OpenCode for AI-assisted development, and the Fine-Tuning of base models (such as Phi-3) using Axolotl to create specialized agents like a "Chef-Bot". Furthermore, the project demonstrates the efficiency of 4-bit quantization techniques (GGUF format), achieving inference speeds of over 87 tokens per second. Integrated remote access solutions (SSH, RDP) ensure flexible infrastructure management. This approach validates the "Sovereign AI" model, ensuring data privacy and operational sustainability in line with modern green computing practices.

### 4.2 Objetivos Generales

#### Itinerario personal para la empleabilidad II (RA3)
*   **Innovación y Modernización (Sovereign AI):**
    *   Se ha identificado el modelo de "IA Soberana" como un vector de innovación crítico. Al internalizar la capacidad de procesamiento de IA, las organizaciones evitan la fuga de propiedad intelectual.
    *   Este proyecto capacita al alumno en roles emergentes como "AI Engineer" o "LLM Ops", perfiles de alta demanda que requieren conocimientos híbridos entre administración de sistemas (Linux/Windows, Redes) y Ciencia de Datos.

#### Sostenibilidad aplicada al sistema productivo (RA3)
*   **Eficiencia Energética (Green AI):**
    *   La aplicación de técnicas de **cuantización (Q4_K_M)** permite reducir el consumo de memoria VRAM y la potencia de cálculo necesaria. Ejecutar un modelo optimizado consume significativamente menos energía que consultar repetidamente grandes modelos en centros de datos remotos.
    *   **Reutilización de Hardware:** Se demuestra que no es necesario adquirir hardware empresarial (H100/A100) para tareas de inferencia y ajuste fino ligero, promoviendo la economía circular al dar una segunda vida productiva a tarjetas gráficas "gamer".

### 4.3 Descripción Técnica: Instalación y Herramientas

#### Administración de sistemas operativos (RA2, RA3)
*   **Monitorización y Eficiencia (RA2):**
    *   Uso exhaustivo de `nvidia-smi` y Administrador de Tareas para balancear la carga de trabajo entre la CPU y la GPU durante el entrenamiento con Axolotl.
    *   Identificación de cuellos de botella (ej. temperatura de la GPU, paginación de RAM).
*   **Automatización (RA3):**
    *   Desarrollo de scripts en PowerShell y Bash para automatizar el flujo de trabajo: `Clonado de Repo -> Creación de Venv -> Instalación de Dependencias -> Conversión a GGUF`.
    *   Configuración de variables de entorno (PATH, CUDA_HOME) para el correcto funcionamiento de las librerías de Deep Learning.

#### Herramientas utilizadas y aspectos de seguridad (RA6, RA7)
*   **Stack Tecnológico:**
    *   **Inferencia:** Ollama (Go), llama.cpp (C++).
    *   **Entrenamiento:** Axolotl (Python, PyTorch), PEFT (LoRA).
    *   **Gestión:** Git, Hugging Face CLI.
*   **Seguridad y Alta Disponibilidad (RA6):**
    *   Implementación de servicios locales que funcionan *offline*. El sistema sigue operando incluso si se corta la conexión a internet, garantizando disponibilidad 24/7.
    *   Virtualización de entornos de desarrollo (Python venv) para evitar conflictos que degraden el sistema.
*   **Protección de Datos (RA7):**
    *   **Privacidad:** Todos los datasets (ej. recetas) y las interacciones residen en el disco local cifrado.
    *   **Control de Red:** Configuración del Firewall de Windows para restringir el acceso al puerto de la API de Ollama (11434) solo a IPs de confianza o localhost.

### 4.4 Implantación de aplicaciones web y Servicios de Red

#### Implantación de aplicaciones web (RA3, RA5)
*   **Despliegue:**
    *   Se ha levantado un servidor de inferencia local que expone una API RESTful compatible con OpenAI.
    *   Integración con interfaces gráficas como LM Studio y extensiones de VS Code (OpenCode) que actúan como clientes web/locales consumiendo esta API.
*   **Multiplataforma:**
    *   Los modelos en formato GGUF generados son universales y pueden ser ejecutados en Windows, Linux (servidores) y macOS (como se demostró en la comparativa de rendimiento), asegurando la portabilidad de la solución.

#### Servicios de red e Internet (RA4, RA6)
*   **Acceso Remoto Seguro:**
    *   **SSH (Puerto 22):** Configuración de autenticación mediante clave pública/privada (sin contraseña) para administración segura desde terminales Linux/Móviles.
    *   **RDP (Puerto 3389):** Habilitación de Escritorio Remoto para gestión visual de herramientas como LM Studio.
    *   **TeamViewer:** Solución de respaldo para acceso desde redes externas sin necesidad de abrir puertos en el router (CG-NAT).

### 4.5 Presentación de Software y Manual de Usuario

#### Digitalización (RA5)
*   El proyecto digitaliza el conocimiento experto (en este caso, culinario) transformándolo en un activo digital interactivo (el modelo "Chef-Bot"). Se evalúa la importancia de proteger este activo mediante copias de seguridad locales y control de versiones de los pesos del modelo.

#### Manual de Usuario (Módulo Optativo II)
*   Se ha elaborado una suite documental completa que guía al usuario final:
    *   **Paso 1:** Instalación de prerrequisitos (Drivers NVIDIA, Python).
    *   **Paso 2:** Uso de comandos simples (`ollama run`) para interactuar con la IA.
    *   **Paso 3:** Guía avanzada para usuarios técnicos sobre cómo re-entrenar el modelo con nuevos datos usando el script `train.bat` configurado.
