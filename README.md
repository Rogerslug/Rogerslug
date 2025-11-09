# ¡Hola! Soy Roger 👋

### Full-Stack Developer | Especialista en IA & RAG (Retrieval-Augmented Generation)

<br>

Soy un programador y estudiante de Informática en la UNAM, apasionado por construir soluciones que viven en la intersección del desarrollo web y la Inteligencia Artificial. Mi objetivo es transformar datos complejos en conocimiento accesible y crear aplicaciones inteligentes que aporten un valor real.

---

### 🔭 Mi Proyecto Destacado

#### **Agente Inteligente Text-to-SQL para Análisis Financiero**

Este es el proyecto más representativo de mis habilidades actuales, donde diseñé un sistema que permite a usuarios no técnicos consultar bases de datos complejas usando lenguaje natural.

*   **Problema:** Dar acceso controlado a analistas para consultar datos de regulación financiera en SQL Server, sin exponer información sensible y sin requerir que escribieran SQL.
*   **Solución:** Un agente que traduce preguntas en español a consultas SQL seguras, las ejecuta, y devuelve un resumen junto con un archivo Excel/CSV.
*   **Impacto:** Se democratizó el acceso a los datos, reduciendo el tiempo de consulta de horas a segundos y manteniendo siempre la seguridad de la información.

**Arquitectura de la Solución:**
```mermaid
%%{init: { "flowchart": { "htmlLabels": false } }}%%
flowchart LR
    subgraph Usuario["👤 Usuario"]
        A[Usuario Final]
    end

    subgraph Interfaz["💬 Interfaz"]
        B[Google Chat API]
    end

    subgraph Aplicacion["🤖 Aplicación del Agente Python"]
        C{Orquestador LangChain/Python}
        D[LLM Text-to-SQL DeepSeek/Llama]
        E[LLM Resumir DeepSeek/Llama]
        F[Generador CSV/Excel]
    end

    subgraph BaseDatos["🔒 Base de Datos Acceso Seguro"]
        G[VPN]
        H[(SQL Server)]
        I[Vistas Seguras]
    end

    A -->|1. Pregunta| B
    B -->|2. Envía| C
    C -->|3. Generar SQL| D
    D -->|4. Devuelve SQL| C
    C -->|5. Ejecuta Query| G
    G --> H --> I
    I -->|6. Devuelve Resultados| C
    C -->|7. Pide Resumen| E
    E -->|8. Devuelve Resumen| C
    C -->|9. Genera Archivo| F
    F -->|10. Archivo| C
    C -->|11. Envía Resumen + Archivo| B
    B -->|12. Muestra Respuesta| A

    style A fill:#e1f5ff
    style B fill:#fff4e1
    style C fill:#e8f5e9
    style D fill:#f3e5f5
    style E fill:#f3e5e9
    style F fill:#e8f5e9
    style G fill:#ffebee
    style H fill:#ffebee
    style I fill:#ffebee
```

---

### 🛠️ Mi Stack Tecnológico

<table>
  <tr>
    <td valign="top" width="50%">
      <strong>Frontend</strong><br>
      <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
      <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
      <img src="https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vue.js&logoColor=4FC08D" />
      <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white" />
      <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
      <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" />
    </td>
    <td valign="top" width="50%">
      <strong>Backend</strong><br>
      <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
      <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
      <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
      <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" />
      <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" />
    </td>
  </tr>
  <tr>
    <td valign="top" width="50%">
      <strong>IA & Bases de Datos</strong><br>
      <img src="https://img.shields.io/badge/LangChain-000000?style=for-the-badge&logo=LangChain&logoColor=white" />
      <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" />
      <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
      <img src="https://img.shields.io/badge/Microsoft_SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white" />
      <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" />
    </td>
    <td valign="top" width="50%">
      <strong>DevOps & Herramientas</strong><br>
      <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
      <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
      <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
      <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white" />
    </td>
  </tr>
</table>

---

### 🌱 Otros Proyectos Relevantes

- **Autonomeals.net (EdTech):** Plataforma de aprendizaje de cocina para niños con un backend en Node.js/TypeScript y frontend en Vue.js. Incluye un agente RAG para mejorar la accesibilidad.
- **Sistema de Recomendación de Alimentos:** Modelo de aprendizaje automático que utiliza técnicas RAG para recomendar recetas basadas en datos nutricionales.
- **Análisis de Sentimientos de Estudiantes:** Creación de un pipeline de datos para evaluar el rendimiento académico mediante reconocimiento facial con DeepFace, MediaPipe y OpenCV.

---

### 📫 Cómo Contactarme

<p align="left">
  <a href="https://www.linkedin.com/in/alan-rogelio-lopez-c-a67559195" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="mailto:rogelio.020496@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail"/>
  </a>
</p>

---

### 📊 Mis Estadísticas de GitHub

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Rogerslug&show_icons=true&theme=radical&rank_icon=github" alt="Estadísticas de GitHub de Roger"/>
  <br>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Rogerslug&layout=compact&theme=radical" alt="Lenguajes más usados por Roger"/>
</p>
