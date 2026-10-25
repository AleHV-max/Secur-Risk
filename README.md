# AuditSec Executive

**Technology Risk & Incident Assurance Dashboard** es un panel ejecutivo de archivo único para simular escenarios de riesgo tecnológico, revisar controles y generar un dictamen imprimible.

## Funcionalidades

- Datos editables de la organización auditada, período de evaluación y auditor líder.
- Tres escenarios corporativos con severidad, coste de inactividad por hora, multa potencial, riesgo de 0 a 100 y referencias a marcos de control:
  - Exposición de credenciales y llaves cloud — ISO 27001 A.9 y NIST CSF PR.AC.
  - Ransomware en sistemas críticos — NIST CSF DE.CM y CIS Control 10.
  - Brecha de datos de clientes y fuga por API — GDPR y regulador financiero.
- Cuatro controles seleccionables para cada escenario, con coste, mitigación y tags de estándares.
- Cálculo ilustrativo de riesgo residual, ahorro estimado por mitigación, inversión de controles, ROSI y cobertura indicativa de cumplimiento.
- Matriz de riesgo 5×5 dibujada en Canvas que compara el riesgo inherente y el residual según los controles elegidos.
- Conclusiones y recomendaciones automáticas, dictamen imprimible mediante **Exportar Dictamen de Auditoría** e historial local con fecha y hora.

## Ejecución local

1. Descarga el proyecto o abre la carpeta del repositorio.
2. Abre `index.html` directamente en un navegador moderno.
3. Completa los datos de auditoría, selecciona un escenario y marca los controles que tengan evidencia.
4. Pulsa **Evaluar escenario** para guardar y revisar la evaluación. Pulsa **Exportar Dictamen de Auditoría** y selecciona guardar como PDF en el diálogo de impresión.

No requiere dependencias, compilación, servidor ni backend. El historial se almacena únicamente en el `localStorage` de ese navegador y puede borrarse desde el panel.

## Modelo de estimación y limitaciones

Las cifras son parámetros didácticos configurados en `index.html`, no datos observados de una organización ni asesoría financiera o legal. Para hacer comparables los escenarios, la exposición se estima como 24 horas de inactividad multiplicadas por el coste horario, más la multa regulatoria potencial. El ahorro se aproxima como exposición multiplicada por los puntos porcentuales de mitigación seleccionados; el ROSI se calcula como `(ahorro estimado − inversión en controles) / inversión en controles`. Sin inversión seleccionada, el ROSI aparece como no disponible.

La puntuación 5×5 es una representación visual normalizada del riesgo de 0 a 100, no un cálculo independiente de probabilidad e impacto. El nivel de cumplimiento refleja la proporción de controles seleccionados y no acredita conformidad con un estándar. Validar todas las estimaciones, la evidencia de controles, la aplicabilidad regulatoria y los supuestos con profesionales antes de tomar decisiones.

## Despliegue en GitHub Pages

El repositorio publica el sitio directamente desde la raíz de la rama `main`. No se requiere proceso de compilación.

**Sitio publicado:** [Abrir AuditSec Executive en GitHub Pages](https://alehv-max.github.io/Secur-Risk/)
