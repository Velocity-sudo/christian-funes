# PIPELINE GHL — CHRISTIAN FUNES

> **Documento vivo:** Mapeo de etapas, tags y comunicaciones para GoHighLevel. En construcción a partir de diagramas visuales.

---

## 1. REGISTRO (Lead Entrante)
**Condición / Trigger:** El lead entra por formulario (Ads u Orgánico).
**Tags Aplicables:** `Registro`, `Ads`, `orgánico`

### Comunicación Interna (Slack & Email)
- **0H (Inmediato):** "Llenó form, llámalo tan pronto puedas."
- **1H:** "Llenó form y aún no lo has llamado. Llámalo tan pronto puedas."
- **12H:** "No te olvides de contactar al lead, debe ser hoy mismo."
- **24H:** "Pasó un día y no lo llamaste, la probabilidad de cierre bajó."
- **48H:** "Pasaron 2 días y no lo llamaste, la probabilidad de cierre bajó aún más."
- **72H:** "Pasaron 3 días y no lo llamaste, la probabilidad de cierre bajó aún más, en un día se moverá a inacción."
- **96H:** Se mueve a inacción automáticamente.

### Comunicación Externa (WhatsApp, SMS, Email)
*(Sin comunicación externa programada en esta etapa específica. El objetivo es que Laura llame y la sorpresa de la llamada rápida es clave).*

---

## 2. LLAMADA 1 (Intento 1)
**Condición / Trigger:** Lead movido a etapa "Llamada 1" tras el primer intento fallido.
**Tags Aplicables:** `c1`, `inacción - c1`

### Comunicación Interna (Slack & Email)
- **24H:** "Llámalo 2nd vez."
- **48H:** "Aún no lo has llamado 2nd vez."
- **72H:** "Aún no lo has llamado 2nd vez, se va a ir a inacción."
- **96H:** Se mueve a inacción automáticamente (`inacción - c1`).

### Comunicación Externa (WhatsApp, SMS, Email)
- **WhatsApp / SMS / Email (0H):** "Hola [Nombre], soy Laura del equipo de Christian Funes. Te llamé recién porque vi que querías validar si podías comprar casa con nuestro método. ¿En qué horario te queda mejor que te marque hoy para hacerte 3 preguntas rápidas?"

---

## 3. LLAMADA 2 (Intento 2)
**Condición / Trigger:** Lead movido a etapa "Llamada 2" tras el segundo intento fallido.
**Tags Aplicables:** `c2`, `inacción - c2`

### Comunicación Interna (Slack & Email)
- **24H:** "Llámalo 3era vez."
- **48H:** "Aún no lo has llamado 3era vez."
- **72H:** "Aún no lo has llamado 3era vez, se va a ir a inacción."
- **96H:** Se mueve a inacción automáticamente (`inacción - c2`).

### Comunicación Externa (WhatsApp, SMS, Email)
*(Sin comunicación externa programada en esta etapa. Solo se intenta la llamada).*

---

## 4. LLAMADA 3 (Intento 3)
**Condición / Trigger:** Lead movido a etapa "Llamada 3" tras el tercer intento fallido.
**Tags Aplicables:** `c3`, `inacción - c3`

### Comunicación Interna (Slack & Email)
- **24H:** "Llámalo última vez."
- **48H:** "Aún no lo has llamado última vez."
- **72H:** "Aún no lo has llamado última vez. Se va a ir a inacción."
- **96H:** Se mueve a inacción automáticamente (`inacción - c3`).

### Comunicación Externa (WhatsApp, SMS, Email)
- **WhatsApp / Email (0H) [Break up]:** "Hola [Nombre], soy Laura. Veo que no hemos podido coincidir en estos días. Cerramos tu archivo temporalmente para enfocarnos en las familias que están listas para iniciar el proceso de compra de casa. Si en algún momento decides que es tu turno, guárdate nuestro número y contáctanos cuando quieras retomar. ¡Mucho éxito!"

---

## 5. LLAMADA AGENDADA
**Condición / Trigger:** Contacto avanzó en embudo agendando videollamada.
**Tags Aplicables:** `llamada agendada`, `Ads`, `orgánico`

### Comunicación Interna (Slack & Gmail)
- **0H (Inmediata):** "Agenda automática con X, llámalo ahora para confirmar"
- **-24H (Antes de la cita):** "Mañana tienes agenda automática con X, confírmala"
- **-2H (Antes de la cita):** "En 2 horas tienes llamada con X"
- **-10m (Antes de la cita):** "En 10 minutos tienes llamada con X"

### Comunicación Externa (Omnicanal: WhatsApp, SMS, Email)
- **0H (Inmediata):** "Llamada agendada! por favor ten en cuenta esto [Link/Info]"
- **-24H (Antes de la cita):** "Mañana tenemos una llamada agendada, ten esto presente"
- **-10m (Antes de la cita):** "Cómo quedamos, en 10 min te llamo"

---

## 6. FORMULARIO + ID
**Condición / Trigger:** Lead termina post-llamada, se le envió encuesta y requerimiento de licencia.
**Tags Aplicables:** `formulario`, `inacción - formulario`

### 📋 GHL Custom Form (Automatización de Filtro)
Esta etapa se automatiza enviando un formulario que consolida el filtro de viabilidad y el requerimiento de ID. Si el lead no lo llena, entran las alarmas de seguimiento para hacerlo en llamada manual (Fórmula Híbrida).
**Campos del Formulario a construir:**
1. Rango de precio estimado / Pago mensual ideal.
2. ¿Primera vez comprando o ya tienes casa?
3. Ahorros actuales aproximados (Down payment + Cierre).
4. Estimado de puntaje de crédito (Opciones: Ej. Arriba/Abajo de 570).
5. Tipo de empleo (W2, Self-Employed, Mixto).
6. Estimado de ingresos mensuales o anuales (antes de taxes).
7. Estimado de deudas mensuales (Auto, préstamos, tarjetas de crédito).
8. ¿En cuánto tiempo quieres comprar? (30 días, 1-3 meses, más de 3 meses).
9. **Carga de Archivo (Upload):** Fotografía de Licencia de Conducir / ID.

### Comunicación Interna (Slack & Gmail)
- **0H:** "Se le acaba de enviar el formulario a X, por favor haz seguimiento."
- **24H:** "X aún no envía el formulario, las primeras horas son críticas, hazle seguimiento"
- **48H:** "Aún no el formulario, las primeras horas son críticas, hazle seguimiento"
- **96H (4 Días):** "Se está enfriando el proceso, llama y asegura"
- **7D (1 Semana):** "1 semana y X no ha enviado el formulario, llámalo y actualiza la oportunidad"
- **13D:** "Última oportunidad, mañana el lead pasa a inacción, llámalo ahora"
- **14D:** Automáticamente se mueve a inacción (`inacción - formulario`)

### Comunicación Externa (Omnicanal: WhatsApp, SMS, Email)
- **0H:** "Por favor llena este formulario para que podamos validar que puedes acceder al prestamo para tu casa [Enlace]"
- **24H:** "Aún no recibimos, por favor llena el formulario [Enlace]"
- **48H:** "Aún no llenas el formulario, si necesitas ayuda contáctanos! [Enlace]"
- **72H:** "Aún no recibimos, por favor llena el formulario, ¿sigues interesado?"
- **96H (4 Días):** "Como no recibimos el formulario vamos asumir que ya no estas interesado y daremos prioridad a otras personas."
- **7D (1 Semana):** "Imagino andas ocupado, ¿aún sigues interesado?"

---

## 7. ENVÍO DE DOCUMENTOS
**Condición / Trigger:** El lead pasó el formulario y fue preaprobado, requiere subir W2, taxes, bancarios etc.
**Tags Aplicables:** `documentos`, `inacción - documentos`

### 📋 GHL Custom Form (Portal de Carga de Documentos)
Para evitar documentos regados por email o WhatsApp, automatizaremos el envío mediante un formulario integrado en GHL de "File Upload" vinculado al perfil del cliente.
**Archivos Requeridos a solicitar en el formulario:**
1. **Identificación (Si no se envió antes):** Copia Licencia de Conducir.
2. **Tax Returns (2024 y 2023):** Modos PDF, incluyendo todas las páginas.
3. **Bank Statements (2 meses más recientes):** De donde provendrán los fondos de inversión (todas las páginas).

### Comunicación Interna (Slack & Gmail)
- **0H:** "X está pre aprobado, pendiente que tenga todo lo necesario para enviar documentos"
- **24H:** "X aún no envía documentos, las primeras horas son críticas, hazle seguimiento"
- **48H:** "Aún no envía documentos, las primeras horas son críticas, hazle seguimiento"
- **96H (4 Días):** "Se está enfriando el proceso, llama y asegura"
- **7D (1 Semana):** "1 semana y X no ha enviado documentos, llámalo y actualiza la oportunidad"
- **13D:** "Última oportunidad, mañana el lead pasa a inacción, llámalo ahora"
- **14D:** Automáticamente se mueve a inacción (`inacción - documentos`)

### Comunicación Externa (Omnicanal: WhatsApp, SMS, Email)
- **0H:** "ESTAS PRE APROBADO! solo hace falta un solo paso antes de que podamos conseguir tu prestamo para tu casa, haz esta aplicación [Enlace/Portal]"
- **24H:** "Aún no recibimos, por favor llena la aplicación y envía [Enlace]"
- **48H:** "Aún no vemos reflejados tus documentos, si necesitas ayuda para subirlos, contáctanos!"
- **72H:** "Aún no recibimos, por favor envía la info, ¿sigues interesado?"
- **96H (4 Días):** "Como no recibimos los documentos vamos asumir que ya no estas interesado y daremos prioridad a otras personas."
- **7D (1 Semana):** "Imagino sigues ocupado, ¿aún sigues interesado?"

---

## 8. APLICACIÓN BANCOS (Underwriting)
**Condición / Trigger:** El cliente subió todos sus documentos (taxes, stmts) y enviamos la carpeta a los bancos/lenders finales para la aprobación blindada definitiva.
**Tags Aplicables:** `aplicación`, `inacción - aplicación`

### Comunicación Interna (Slack & Gmail)
- **0H:** "Ya tienes todos los documentos completos, envía la aplicación de X a los bancos"
- **24H:** "Ya deberías tener una razón del banco, por favor actualiza la oportunidad y asegura que el cliente esta enterado"
- **48H:** "Ya recibiste la actualización del banco? actualiza oportunidad y avisa al cliente."
- **96H:** "Ya recibiste la actualización del banco? actualiza oportunidad y avisa al cliente."
- **13D:** "Última oportunidad, mañana el lead pasa a inacción, llámalo ahora"
- **14D:** Automáticamente se mueve a inacción (`inacción - aplicación`)

### Comunicación Externa (Omnicanal: WhatsApp, SMS, Email)
- **0H:** "RECIBIMOS TUS DOCUMENTOS! ya mismo vamos a comenzar a aplicar con los bancos, en menos de 24 horas deberías saber de nosotros"
- *(Por definir mensajes posteriores si se posterga respuesta del banco)*

---

## 9. BÚSQUEDA DE CASA + OFERTA
**Condición / Trigger:** El cliente recibió la aprobación del banco y sale a buscar casa con su Realtor (Poder de 'Cash Buyer').
**Tags Aplicables:** `buscando casa`, `inacción - busqueda - casa`

### Comunicación Interna (Slack & Gmail)
- **0H:** "Cliente entra a etapa de mirar casa, haz seguimiento"
- **1M (Mes):** "Ya llevamos 30 días, qué ha pasado con el cliente"
- **2M (Meses):** "Ya llevamos 60 días, qué ha pasado con el cliente"
- **3M (Meses):** "Ya llevamos 90 días, qué ha pasado con el cliente"
- **4M (Meses):** "Ya llevamos 120 días, qué ha pasado con el cliente"
- **5M:** Pasa a inacción automáticamente.

### Comunicación Externa (Omnicanal: WhatsApp, SMS, Email)
- **0H:** "ESTAS APROBADO POR $XXXXX, este es el siguiente paso"
- **1M (Mes):** "Ya llevamos 30 días, cómo va la búsqueda de casa con tu realtor"
- **2M (Meses):** "Ya llevamos 60 días, cómo va la búsqueda de casa con tu realtor?"
- **3M (Meses):** "Ya llevamos 90 días, recuerda que la carta de aprobación es valida por 2 meses más."
- **4M (Meses):** "Ya llevamos 120 días desde la aprobación, tienes un mes mas, cómo va todo?"
- **5M:** "Como no tomaste acción, habilitaremos el cupo del banco para otro cliente."

---

## 10. CON CONTRATO (Cierre)
**Condición / Trigger:** Cliente encontró la casa y entra bajo contrato (En proceso de escrituración/cierre hipotecario).
**Tags Aplicables:** `contrato`

### Comunicación Interna (Slack & Gmail)
- **0H:** "¡Felicitaciones! lograste llevar a X hasta el resultado final, gracias a ti hoy una familia nueva tiene su propio hogar."

### Comunicación Externa (Omnicanal: WhatsApp, SMS, Email)
- **0H:** "Felicitaciones! la casa que escogiste está bajo contrato, estos son los siguientes pasos."

---

## 11. NO CALIFICA / NO APROBADO (Dead Loss)
**Condición / Trigger:** Cliente no viabilidad financiera actual ni en horizonte cercano.
**Tags Aplicables:** `No aprobado`, `No responde`, `No envio documentos`, `No tiempo`

### Comunicación Interna (Slack & Gmail)
*(Movimiento silencioso, archivo del lead en CRM)*

### Comunicación Externa (Omnicanal: WhatsApp, SMS, Email)
- **Acción:** Pasa a campaña de Nutrición a largo plazo (newsletter, re-educación) para no perder el dato en caso de mejora a futuro.

---

## 12. COACHING APROBACIÓN
**Condición / Trigger:** Cliente demostró interés pero le falta mejorar su puntaje de crédito o estructuración.
**Tags Aplicables:** `coaching`

### Comunicación Interna (Slack & Gmail)
- **0H:** "X entra a coaching, hazle seguimiento y asegurate que pueda cumplir pronto las condiciones para aplicar."
- **1M (Mes):** "X lleva 1 mes en coaching, que ha pasado, actualiza su estado en el pipeline"
- **3M (Meses):** "X lleva 3 meses en coaching, que ha pasado, actualiza su estado en el pipeline"
- **6M (Meses):** "X lleva 6 meses en coaching, que ha pasado, actualiza su estado en el pipeline"

### Comunicación Externa (Omnicanal: WhatsApp, SMS, Email)
- **Acción:** Pasa a campaña de Nutrición enfocada en reparación de crédito, subir ingresos documentados y disciplina financiera.

---

## 13. INACCIÓN
**Condición / Trigger:** Lead que superó los tiempos de gracia/espera en cualquier etapa previa (ej. no mandó form en 14d, no mandó IDs, no buscó casa en 5 meses).
**Tags Aplicables:** Etiqueta heredada según su abandono + Tag global inactivo.

### Comunicación Interna (Slack & Gmail)
- **0H (Al caer a Inacción):** "Esto no puede pasar, es inaceptable, nos cuesta tiempo y dinero, aún puedes contactarlo."

### Comunicación Externa (Omnicanal: WhatsApp, SMS, Email)
- **Acción:** Pasa a campaña de Nutrición (estrategia de reactivación profunda).
