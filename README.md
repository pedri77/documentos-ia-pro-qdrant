# documentos-ia-pro-qdrant
gestion de documentos con IA en Colab-Drive

## 🧩 Descripción general

**Documentos IA PRO** es una aplicación de inteligencia artificial que permite **subir, analizar y consultar documentos PDF** mediante **búsqueda semántica**.

El sistema utiliza:
- **SentenceTransformers** (`all-MiniLM-L6-v2`) para generar embeddings vectoriales.
- **Qdrant** como base de datos vectorial local (persistente en Google Drive).
- **Gradio** como interfaz web segura (con autenticación HTTP básica).
- **Google Colab** como entorno gratuito y reproducible.

🔒 Todo se ejecuta en tu entorno — **sin exponer datos a la nube**.

---

## 🚀 Funcionalidades principales

| 💡 Característica | 🧠 Descripción |
|--------------------|----------------|
| 📥 **Ingesta de PDFs** | Extrae texto por página y lo convierte en vectores semánticos. |
| 🧠 **Modelo IA integrado** | Usa `all-MiniLM-L6-v2` de SentenceTransformers (384 dimensiones). |
| 💾 **Persistencia en Google Drive** | La base de datos Qdrant se guarda localmente. |
| 🔍 **Consulta semántica** | Busca fragmentos relevantes mediante lenguaje natural. |
| 🔐 **Acceso seguro** | Requiere usuario y contraseña para acceder a la interfaz. |
| 🧰 **Autónomo y reproducible** | No requiere claves de API externas. |
| ☁️ **Optimizado para Colab** | Instalación limpia en una sola celda. |

---

## 🏗️ Arquitectura del sistema

```plaintext
Google Colab Notebook
│
├── Gradio (UI web segura)
│   └── Autenticación básica HTTP
│
├── SentenceTransformers
│   └── Modelo "all-MiniLM-L6-v2"
│
├── Qdrant (almacenamiento vectorial local)
│   └── Persistente en Google Drive
│
└── PyMuPDF
    └── Extracción de texto de PDFs


