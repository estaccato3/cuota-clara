# Cuota Clara

Calculadora gratuita en español para estimar una cuota mensual de mantenimiento de automatizaciones en n8n, Make o Zapier.

> **Estado:** MVP experimental. No se ha validado con clientes y no hay ventas verificadas. Los valores iniciales son ejemplos, no recomendaciones de mercado.

## Qué permite hacer

- Estimar horas rutinarias, incidencias, coordinación y una reserva para imprevistos.
- Calcular una cuota orientativa usando el costo interno por hora y el margen bruto objetivo.
- Mostrar costos de herramientas/infraestructura y disponibilidad (SLA) como partidas separadas.
- Comparar las horas estimadas con las horas incluidas en el plan.
- Editar, copiar y descargar un borrador de alcance mensual.

## Uso

Abre [Cuota Clara](https://estaccato3.github.io/cuota-clara/) en un navegador moderno. Para explicar cómo se calcula una cuota, consulta la [guía de mantenimiento de n8n](https://estaccato3.github.io/cuota-clara/guia-mantenimiento-n8n.html). También puedes descargar `index.html` y abrirlo localmente; no requiere instalación, dependencias ni servidor.

## Privacidad

La aplicación funciona en el navegador y no realiza solicitudes a un backend. No pide una cuenta ni claves API y no envía ni guarda las entradas en un servidor.

## Cómo se calcula la estimación

1. Horas base = horas rutinarias + horas estimadas para incidencias + coordinación.
2. Horas con reserva = horas base × (1 + porcentaje de reserva).
3. Costo laboral = horas con reserva × costo interno por hora.
4. Precio laboral objetivo = costo laboral ÷ (1 − margen bruto).
5. La cuota sugerida suma el precio laboral objetivo, costos externos trasladados y la cuota de disponibilidad, redondeando el resultado.

El resultado es una ayuda para planificar, no una garantía de rentabilidad ni una cotización fiscal o legal. Los costos de terceros pueden tratarse de otra manera según el acuerdo comercial; evita contarlos dos veces.

## Publicación en GitHub Pages

El workflow [pages.yml](.github/workflows/pages.yml) despliega el sitio cuando hay cambios en `main` y también puede ejecutarse manualmente. En el repositorio, ve a **Settings → Pages** y selecciona **GitHub Actions** como fuente de despliegue si todavía no está configurada.

## Descubrimiento orgánico

El proyecto incluye un [sitemap XML](sitemap.xml) y un [robots.txt](robots.txt). Estos archivos ayudan a los rastreadores a descubrir las dos páginas públicas, pero no garantizan que los buscadores las indexen o les envíen visitas. Para medir impresiones, clics y consultas, verifica la propiedad `https://estaccato3.github.io/` (o la propiedad de URL correspondiente) en [Google Search Console](https://search.google.com/search-console/about) y envía `sitemap.xml`. Revisa luego el informe de rendimiento; evita interpretar la ausencia de datos iniciales como prueba definitiva de que no existe demanda.

## Próximas validaciones

Antes de añadir funcionalidades, validar con usuarios:
- Qué variables usan realmente para estimar mantenimiento.
- Cómo separan incidencias, mantenimiento preventivo y SLA.
- Si usarían o recomendarían la herramienta.
- Si existe disposición a pagar por funciones premium.

## Licencia

MIT. Consulta [LICENSE](LICENSE).
