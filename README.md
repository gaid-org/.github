# GAID – Product Requirements Document (Beta)

## 1. Visión del Producto

**¿Qué es GAID?**  
GAID es una plataforma de personalización cultural que recomienda eventos, lugares y actividades para hacer en tu ciudad —empezando por Buenos Aires— de forma hiperpersonalizada, simple y atractiva.

**Problema que resuelve**  
- Dificultad para encontrar planes alineados con los intereses reales de las personas.  
- Tiempo perdido buscando, guardando y recordando actividades.  
- Estrés generado por la saturación de información dispersa en múltiples plataformas.  

**¿Por qué ahora?**  
En la era de la hiperinformación, GAID actúa como un filtro inteligente que reduce el ruido y muestra solo aquello que verdaderamente interesa, promoviendo experiencias más felices, espontáneas y relevantes.

---

## 2. Objetivos del Pre-lanzamiento

- Validar que las personas regresen al menos 2 veces a la app.
- Confirmar que resuelve el problema de guardar y recordar eventos/lugares de interés.
- Testear la hipótesis de que una interfaz clara y personalizada reduce tiempo y estrés al planear qué hacer.

---

## 3. Usuario Objetivo

- Jóvenes de entre 16 y 40 años.
- Personas que viven o frecuentan la Ciudad de Buenos Aires.
- Buscan salir, hacer planes culturales, descubrir gastronomía y experiencias.

---

## 4. Features – MVP

- [x] Login con Google (via Supabase).
- [ ] Exploración sin login (modo visitante con funcionalidades limitadas).
- [x] Cards de eventos/lugares con info visual.
- [x] Sistema de Likes (me interesa).
- [x] Guardado en perfil (con recordatorio).
- [ ] Recordatorio por email / WhatsApp.
- [ ] Compartir eventos con tarjetas visuales.
- [x] Filtro por ubicación, precio, categoría, etiquetas.
- [ ] Recomendaciones por perfil (MBTI/intereses).
- [ ] Perfil básico con historial de guardados.
- [ ] Capa social: seguir amigos/influencers culturales.

---

## 5. Lógica Técnica

**Stack**  
- Frontend: `Next.js`  
- Backend: `Supabase` (auth + almacenamiento)  
- Infraestructura: `Cloudflare` (hosting del proyecto)

**Datos del usuario**  
- Likes (me interesa)  
- Eventos guardados  
- Preferencias (tags)  
- Historial de eventos vistos  
- Perfil público (en el futuro)

---

## 6. Base de Datos

**Eventos/Lugares**
- `nombre`  
- `descripción`  
- `categoría`  
- `tags` / `keywords`  
- `fecha` y `hora`  
- `precio`  
- `link externo`  
- `mapa` / `ubicación`  
- `link de compra` (opcional)

**Notas**
- Requiere sistema de tags para match con perfiles.
- Eventualmente se usará una LLM para mejorar la personalización.
<!-- TODO: definir estructura de personalización con LLM -->

---

## 7. Roadmap – Abril

- [x] Login con Google
- [ ] Modo exploración sin login
- [x] Cards con info básica y botones de interacción
- [x] Guardado en perfil
- [ ] Recordatorio por email o WhatsApp
- [ ] Testeo cerrado con usuarios reales
- [ ] Feedback directo (observación + entrevistas)

---

## 8. Feedback & Iteración

**Primera fase:**  
- Testeo cerrado con personas conocidas (contacto directo).
- Seguimiento manual del uso y sensaciones.

**Cómo se traducen en mejoras:**  
- TBD (por definir) – se propondrán iteraciones a partir de patrones detectados.

<!-- TODO: definir herramienta para trackear feedback y cambios (Notion, Linear, Trello, etc.) -->

---

## 9. Modelo de Negocio (Exploratorio)

- Seguimiento de influencers culturales con perfiles públicos.
- Sistema de referidos (por link o actividad compartida).
- Monetización por parte de marcas que buscan presencia en la plataforma (activaciones, pauta, etc.).
<!-- TODO: detallar monetización y estrategia de partnerships -->

---

## 10. Bonus Track – Ideas futuras

- Feed de planes recomendados por personas que seguís.
- Integración con calendarios personales.
- IA generadora de planes personalizados (tipo “sorprendeme hoy”).
- Modo colaborativo para armar un plan con amigos.

---

_Hecho con amor por Martina y equipo GAID._
