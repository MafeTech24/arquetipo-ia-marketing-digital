# 🧠 ArquetipoIA — Generador de Buyer Persona con IA

> Mini-Challenge | Curso: Creación de Productos desde Cero con IA | Coderhouse

---

## 📌 Descripción del Proyecto

**ArquetipoIA** es una aplicación web que permite a freelancers y consultores de marketing generar un Arquetipo de Cliente (Buyer Persona) profesional y completo en menos de 5 minutos, respondiendo un formulario guiado de 4 pasos potenciado por Inteligencia Artificial.

### El Problema
Los freelancers y consultores de marketing pierden entre 2 y 4 horas creando manualmente el arquetipo de cliente para cada proyecto nuevo, usando documentos genéricos sin estructura profesional. Esto retrasa el inicio de la estrategia y genera entregables poco convincentes para el cliente.

### La Solución
Una app que genera un Arquetipo de Cliente profesional en minutos, con IA real (Gemini), mediante un wizard guiado de 4 pasos.

---

## 🎯 Blueprint — Definición y Flujo

### User Flow
```
Landing → "Empezar ahora" → Wizard Paso 1 (Perfil) → Paso 2 (Preferencias) 
→ Paso 3 (Hábitos Sociales) → Paso 4 (Factores Psicológicos) 
→ "Generar Arquetipo con IA" → Pantalla de Resultado → Copiar JSON / Nuevo Arquetipo
```

### Funcionalidades Core (Must Have)
- Wizard de 4 pasos con barra de progreso
- Validación de campos obligatorios por paso
- Integración real con API de Google Gemini
- Pantalla de resultado con cards organizadas por sección
- Botón "Copiar JSON" con el resultado completo
- Estado de carga durante la generación con IA

### Estructura de Datos (Mock → Real via Gemini)
```json
{
  "nombre": "Laura Torres",
  "edad": 35,
  "residencia": "Córdoba Capital",
  "ocupacion": "Dueña de salón de belleza",
  "nivel_educativo": "Secundario completo",
  "estado_civil": "Casada",
  "modalidad_laboral": "Independiente",
  "nivel_socioeconomico": "Medio",
  "pasatiempos": "Ver reels, salir con amigas",
  "contenido_digital": "Videos cortos, tutoriales",
  "temas_sociales": "Emprendimiento femenino",
  "que_busca_en_marca": "Confianza y resultados reales",
  "redes": ["Instagram", "Facebook"],
  "frecuencia": "Varias veces al día",
  "influencers": "Emprendedoras locales",
  "ecommerce": "Compra por Instagram",
  "busca_en_servicio": "Simplicidad y rapidez",
  "sentimientos": "Seguridad, orgullo",
  "evita": "Contenido agresivo",
  "valores": "Familia, esfuerzo",
  "miedos": "Perder dinero",
  "deseos": "Que su negocio crezca solo"
}
```

---

## 🛠️ Stack Tecnológico

| Capa | Herramienta |
|------|-------------|
| Generative UI | Lovable |
| AI Code Editor | Antigravity |
| Frontend | React + Vite + TypeScript |
| Estilos | Tailwind CSS + Shadcn UI |
| IA | Google Gemini 2.5 Flash API |
| Deploy | Vercel |
| Control de versiones | GitHub |

---

## 🔧 Fases del Challenge

### Fase 1 — Blueprint (Definición)
Definición del problema, user flow y funcionalidades core antes de tocar ninguna herramienta.

### Fase 2 — Frontend con Generative UI (Lovable)
Generación de toda la interfaz con un único prompt estratégico en Lovable: landing, wizard de 4 pasos y pantalla de resultado con mock data.

### Fase 3 — Lógica Local con AI Editor (Antigravity)
Conexión del botón "Generar Arquetipo con IA" a la API de Google Gemini. Manejo de estados de carga y error. Renderizado del JSON real en la pantalla de resultado.

### Fase 4 — Deploy
Subida del código a GitHub y deploy en Vercel.

---

## 📝 Log de Prompts Clave

### Prompt 1 — Fase de Definición (Claude)
```
Actúa como un Senior Product Manager. Quiero desarrollar una aplicación 
que resuelva el siguiente problema: los freelancers de marketing pierden 
horas creando arquetipos de cliente manualmente. Generá: user flow, 
funcionalidades MVP, estructura JSON y rutas necesarias.
```

### Prompt 2 — Fase de Frontend (Lovable)
```
Construye el frontend completo de una app llamada "ArquetipoIA" usando 
Next.js, Tailwind CSS (instalado via npm, NO CDN) y componentes de Shadcn UI.
Tema oscuro premium. Fondo #0A0A0F. Acentos violeta #7C3AED.
Wizard de 4 pasos: Perfil, Preferencias, Hábitos Sociales, Factores Psicológicos.
Pantalla de resultado con cards glassmorphism y mock data JSON.
```

### Prompt 3 — Fase de Lógica Local (Antigravity)
```
Actúa como Ingeniero Fullstack. Conectá el botón "Generar Arquetipo con IA" 
a la API de Google Gemini (gemini-2.5-flash). Al hacer clic debe tomar todos 
los datos del formulario, enviarlos a Gemini con fetch, mostrar estado de carga 
y navegar a /resultado con la respuesta real. API key en .env como VITE_GEMINI_API_KEY.
```

### System Prompt para Gemini
```
Sos un experto en marketing digital. Con los datos del formulario generá un 
arquetipo de cliente completo. Respondé SOLO con JSON válido, sin markdown, 
sin explicaciones, con estos campos: nombre, edad, residencia, ocupacion, 
nivel_educativo, estado_civil, modalidad_laboral, nivel_socioeconomico, 
pasatiempos, contenido_digital, temas_sociales, que_busca_en_marca, redes, 
frecuencia, influencers, ecommerce, busca_en_servicio, sentimientos, evita, 
valores, miedos, deseos.
```

---

## 🚀 Cómo correr el proyecto localmente

```bash
# Clonar el repositorio
git clone https://github.com/TU_USUARIO/arquetipo-ia-marketing-digital.git

# Instalar dependencias
npm install

# Crear archivo .env con tu API key de Google AI Studio
VITE_GEMINI_API_KEY=tu_api_key_aqui

# Correr en desarrollo
npm run dev
```

> ⚠️ Necesitás una API Key de [Google AI Studio](https://aistudio.google.com/) para que la generación con IA funcione.

---

## 📁 Estructura del Proyecto

```
src/
├── pages/
│   ├── Index.tsx        # Landing page
│   ├── Crear.tsx        # Wizard 4 pasos + integración Gemini
│   └── Resultado.tsx    # Pantalla de resultado con cards
├── components/          # Componentes reutilizables Shadcn UI
├── lib/                 # Utilidades
└── types/               # TypeScript types
```

---

## 🌐 Demo

🔗 **Deploy:** [[Agregar link de Vercel acá](https://arquetipo-ia-marketing-digital.vercel.app/)]

---

## 👩‍💻 Autora

**María Fernanda Moreno — MafeTech**
- Portfolio: [mafetech.vercel.app](https://mafetech.vercel.app)
- LinkedIn: [linkedin.com/in/mafetechdev](https://www.linkedin.com/in/mafetechdev/)
- Showcase: [showcase-de-automatizaciones-y-webs.vercel.app](https://showcase-de-automatizaciones-y-webs.vercel.app)
