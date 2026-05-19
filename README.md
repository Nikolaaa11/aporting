# CEHTA Asamblea 2026 — Iteración PPT

Repo para iterar correcciones sobre la presentación de la Asamblea de Aportantes 2026 de Cehta Capital.

## Archivos

- `CEHTA_Asamblea_2026_v11_corregido.pptx` — versión más reciente (apuntar nuevas iteraciones a partir de aquí)
- `CEHTA_Asamblea_2026_v8_original.pptx` — original sin modificar (referencia)
- `anotaciones/*.jpg` — 18 fotos de la PPT impresa con anotaciones a mano del usuario (Nicolás)

## Instrucciones para agente automatizado

1. Leer todas las imágenes en `anotaciones/` con la herramienta Read.
2. Identificar anotaciones a mano que sean CAMBIOS al texto impreso (tachaduras + reemplazos, números nuevos, palabras agregadas).
3. Comparar con el contenido actual de `CEHTA_Asamblea_2026_v11_corregido.pptx` (extraer texto vía `python -c "from pptx import Presentation; ..."` o desempacando el zip).
4. Aplicar los cambios faltantes editando los XML internos del PPTX (workflow estándar: unzip → editar `ppt/slides/slideN.xml` → rezip preservando estructura).
5. Guardar como nueva versión `CEHTA_Asamblea_2026_v{N+1}_corregido.pptx`.
6. Commitear los cambios con mensaje describiendo qué se modificó.
7. Push.

## Reglas críticas

- **NO cambiar el diseño** de la PPT. Solo correcciones de texto.
- Las NOTAS PERSONALES del usuario ("mostraría a Diego", "ver con Jorge", "??", "what a hell") NO son cambios — son apuntes personales.
- Si una anotación es ambigua, NO aplicar el cambio.
- Mantener consistencia: fecha de asamblea es **27 de mayo de 2026** (miércoles, 10:00 hrs).
- Mantener todas las versiones anteriores; nunca sobreescribir.

## Cambios ya aplicados (v8 → v11)

- Fecha "22 de mayo" → "27 de mayo" en todos los slides
- Portada: "Viernes" → "Miércoles"
- Slide 3 Pilar 01: título → "Compra de empresas con nuevas tecnologías"
- Slide 3 Pilar 02: → "Obtención de subsidios y financiamiento"
- Slide 5: título → "Obtención de subsidios estatales y financiamiento"
- Slide 10: bancos chinos ampliados (Bank of China, ICBC, CMB, SWCB)
- Slide 12: aseguradoras → "SINOSURE · PICC"; bancos → "CMB · SWCB"
- Slide 13 header: "HITO PRIORITARIO 2027" (era 2026)
- Slide 13 Climate Smart: hito → "Exclusividad territorial · Electro-Asset"
- Slide 13 Rho Generación: hito → "Primera planta construida 2027"
- Slide 13 DTE Consulting: hito → "416 viviendas en La Serena · DS49"; sector → "Desarrollo habitacional sustentable · DS49 aprobado"
- Slide 13 Revtech: hito → "Primera planta de plomos construida 2027"; sector → "Cobre, cátodos, residuos mineros y energías renovables"
- Slide 13 Trongkai: hito → "Piloto comercial financiado"
- Slide 15 (Un año de evidencia): "MW en pipeline" → "MW en pipeline R2B"; "Viviendas sociales" → "Viviendas sociales (fuera R2B)"; "Subsidios CORFO" → "Financiamiento CORFO"

## Cambios candidatos (a evaluar/decidir)

- Slide 5: reestructurar para que financiamiento sea protagonista (rediseño visual — NO aplicar sin confirmar)
- Slide 6: rediseñar el flujo Ready-to-Build (rediseño visual — NO aplicar sin confirmar)
- Slide 7/8: añadir slide de gobernanza contable (contadores/auditores/comités)
- Slide 13 Climate Smart: redefinir hito ("Expansión cartera + reporte impacto ESG" tiene "??")
- Slide 13 Evoque: pendiente nuevo hito 2027 (consulta a Jorge / Guillermo Navarrete del usuario)
