# Guía práctica: chatbot de WhatsApp para consultas de inscripción registral

Esta guía está orientada a profesionales de arquitectura que desean automatizar la atención inicial sobre trámites de inscripción registral mediante un asistente conversacional en WhatsApp.

## 1) Alcance inicial recomendado

Empiece con un MVP acotado para reducir errores:

- Consultas informativas (requisitos, costos, plazos, oficinas, horarios).
- Prevalidación básica de documentos según tipo de trámite.
- Derivación a atención humana para casos complejos.

No automatice decisiones legales ni dictámenes técnicos en la primera fase.

## 2) Flujos mínimos que debe cubrir

1. **Identificación del trámite**
   - Nueva inscripción.
   - Rectificación / actualización.
   - Levantamiento de observaciones.

2. **Perfil del solicitante**
   - Persona natural / jurídica.
   - Titular / apoderado / profesional representante.

3. **Requisitos personalizados**
   - Lista de documentos obligatorios.
   - Formatos y vigencias.
   - Tasas y forma de pago.

4. **Estado de expediente**
   - Consulta por número de expediente.
   - Mensaje de estado en lenguaje claro.

5. **Derivación humana**
   - Cuando el bot detecte ambigüedad, documentos faltantes o consultas jurídicas.

## 3) Diseño conversacional para WhatsApp

Buenas prácticas:

- Mensajes breves y en pasos.
- Opciones por botones/listas para reducir errores de escritura.
- Confirmaciones antes de registrar datos sensibles.
- Explicación en dos niveles: "resumen" y "detalle".

Ejemplo de inicio:

> Hola, soy el asistente de Inscripción Registral.  
> Puedo ayudarte con requisitos, costos, plazos y estado de expediente.  
> ¿Qué deseas hacer hoy?

## 4) Arquitectura recomendada

- **Canal**: WhatsApp Business API.
- **Motor conversacional**: gestor de flujos + clasificación de intención.
- **Base de conocimiento**: fichas oficiales por trámite, versionadas.
- **Reglas de negocio**: validaciones de costos/plazos/requisitos (sin depender solo de IA generativa).
- **Escalamiento**: bandeja para operador humano con historial resumido.

## 5) Datos y cumplimiento

Mínimos obligatorios:

- Política de privacidad visible.
- Consentimiento para tratamiento de datos personales cuando corresponda.
- Registro de auditoría (quién consultó, cuándo y qué se respondió).
- Retención y eliminación de datos según normativa local.

## 6) Métricas para evaluar éxito

- Tasa de resolución sin operador.
- Tiempo promedio de respuesta.
- Porcentaje de conversaciones derivadas.
- Satisfacción del usuario (CSAT simple de 1–5).
- Preguntas no respondidas (para mejorar contenido).

## 7) Plan de implementación en 6 semanas

- **Semana 1**: levantar normativas, requisitos y preguntas frecuentes reales.
- **Semana 2**: diseñar flujos y árbol de decisión de 3 trámites prioritarios.
- **Semana 3-4**: implementar bot en WhatsApp, validaciones y panel básico.
- **Semana 5**: piloto con usuarios internos + ajuste de mensajes.
- **Semana 6**: salida controlada a vecinos y monitoreo diario.

## 8) Recomendaciones para su perfil (arquitectura)

Como arquitecto, puede aportar alto valor en:

- Estandarizar checklist documental por tipología de proyecto.
- Convertir observaciones frecuentes en respuestas guiadas.
- Definir criterios de prevalidación técnica (sin sustituir revisión oficial).

## 9) Riesgos comunes a evitar

- Publicar requisitos desactualizados.
- Prometer plazos sin validar capacidad operativa.
- No incluir derivación a humano para excepciones.
- Usar respuestas generativas sin control de fuentes.

## 10) Próximo paso sugerido

Construya una **matriz por trámite** con 5 columnas:

1. Tipo de trámite.
2. Requisitos obligatorios.
3. Causales de observación frecuentes.
4. Mensaje estándar de orientación.
5. Área responsable para escalar.

Con esa matriz puede crear un MVP funcional en pocas semanas y con menor riesgo operativo.
