# Sprint 0 – Definición del Producto

## Descripción del problema y su solución software

### Problemática
Actualmente, Global MVM lleva a cabo su proceso de negociación con clientes de manera manual, lo que implica una inversión significativa de tiempo para entender las necesidades del prospecto, revisar proyectos anteriores y construir propuestas desde cero. Esto limita la agilidad comercial y la escalabilidad de su operación.

### Solución software propuesta
Desarrollaremos una aplicación web que integre un chatbot conversacional, accesible directamente mediante un link, sin necesidad de descargar apps externas.

Este agente conversacional tendrá como objetivo guiar al cliente mediante preguntas clave para identificar su sector, necesidad y el tipo de solución que espera.

Una vez recopilada la información, el sistema construirá un `prompt` que será enviado a la*API de DeepSeek, la cual buscará entre documentos históricos (PDFs con proyectos anteriores) y generará una propuesta personalizada. Esta incluirá:

-  Un caso similar encontrado  
-  Descripción del desafío resuelto  
-  Solución aplicada  
-  Resultados obtenidos  
-  Una cotización aproximada  

Todo el proceso estará integrado en la web y permitirá a Global MVM automatizar su etapa de precalificación comercial, con respuestas rápidas, precisas y basadas en evidencia.

---

##  Personas y roles del proyecto

| Nombre              | Correo institucional         | Rol dentro del proyecto |
|---------------------|------------------------------|--------------------------|
| Nombre              | nombre1@eafit.edu.co         | Sin asignar              |
| Nombre              | nombre2@eafit.edu.co         | Sin asignar              |
| Nombre              | nombre3@eafit.edu.co         | Sin asignar              |
| Nombre              | nombre4@eafit.edu.co         | Sin asignar              |
| **Vladlen Shatunov**| vshatunov@eafit.edu.co       | **Tester**               |

---

##  Público objetivo y contexto

###  Usuarios principales

- Clientes potenciales de Global MVM que acceden a la plataforma mediante un link web.  
- El equipo comercial de Global MVM, que puede usar las propuestas generadas para continuar el proceso de venta.

###  Contexto técnico

- El chatbot conversacional estará embebido en una página web (tecnología aún por definir, como Streamlit, Typebot o similar).
- El usuario final (cliente) interactuará exclusivamente desde la web.
- Las respuestas recolectadas se estructurarán automáticamente.
- La búsqueda de casos similares se realizará mediante la API de DeepSeek, utilizando los documentos históricos (PDFs) previamente procesados.
- El backend se desarrollará en Python.

---

##  Descripción del proceso de interacción

###  Flujo del usuario

1. El cliente accede al chatbot desde un enlace web.  
2. El bot guía la conversación preguntando por:  
   - Sector o industria del cliente  
   - Problema que desea resolver  
   - Tipo de solución que espera  
3. El sistema estructura esta información.  
4. Se construye un prompt que se envía a DeepSeek junto con los documentos PDF.  
5. DeepSeek responde con una propuesta basada en un caso similar.  
6. El bot presenta esta propuesta al usuario en la conversación.

---

##  Glosario de términos

| Término               | Definición                                                                 |
|-----------------------|----------------------------------------------------------------------------|
| **Chatbot**           | Sistema conversacional que guía al cliente mediante texto en la web.       |
| **Web embebida**      | Página accesible desde un navegador, sin apps externas.                    |
| **DeepSeek API**      | Servicio de IA para búsqueda semántica y generación de texto.              |
| **Prompt**            | Instrucción que se le pasa a DeepSeek para generar una respuesta.          |
| **PDF**               | Documento donde se almacenan proyectos anteriores de Global MVM.           |
| **Backend**           | Parte del sistema que controla la lógica y conexión con APIs.              |
| **Cotización estimada** | Valor aproximado calculado con base en un proyecto anterior similar.     |
| **Agente conversacional** | Chatbot guiado que interpreta respuestas del usuario y da soluciones.  |
