# Caso 4: Comparación de negocios inmobiliarios disímiles

## El caso

Tres socios evalúan negocios inmobiliarios que no son directamente comparables (distinto tipo, distinta ubicación, distinta escala). Conversan informalmente, por ejemplo en una cena, y necesitan que lo discutido quede estructurado: qué se comparó, qué opinó cada uno, qué quedó pendiente. Una interfaz resume todo lo conversado y permite comparar los negocios lado a lado con los criterios que surgieron de la charla.

## Lo que necesito que me preguntes antes de escribir

- ¿Qué tan disímiles son los negocios? Ejemplo: ¿es comparar un departamento en pozo vs un terreno vs un local comercial? ¿O son del mismo tipo pero en mercados distintos?
- ¿Qué criterios usan los socios para comparar? (rentabilidad, riesgo, plazo de retorno, liquidez, ubicación, monto de inversión)
- ¿La "cena informal" es literal? ¿Se graba el audio, se toman notas, se mandan audios de WhatsApp después?
- ¿Qué existe hoy? ¿Una planilla, un grupo de WhatsApp, nada?
- ¿Qué decisión toman al final? ¿Invertir en uno, en varios, descartar?
- ¿Hay un ejemplo real (anonimizado) que pueda usarse?
- Números: cuántos negocios evalúan por mes, cuánto tarda hoy llegar a una decisión

## El ángulo interesante

Lo que hace este caso distinto de los otros es que la fuente de datos es una conversación informal entre personas, no documentos. El asistente tiene que:
1. Capturar lo que se dijo (transcripción)
2. Extraer los negocios mencionados y los criterios de evaluación que surgieron
3. Armar una vista comparativa que no existía antes de la conversación
4. Preservar quién dijo qué (para que no se pierdan las objeciones o los entusiasmos individuales)

## Notas para el diagrama

Pensar en: conversación desestructurada → extracción → tabla/interfaz comparativa con atribución por socio. El contraste visual entre el "antes" (charla informal) y el "después" (comparativo estructurado) es el gancho.
