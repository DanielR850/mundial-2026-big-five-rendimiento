# ⚽ Big Five y rendimiento en el Mundial 2026

Dashboard interactivo en Power BI para explorar si existe una relación entre la presencia de futbolistas de las cinco grandes ligas europeas y el rendimiento de sus selecciones en el Mundial 2026.

> **Pregunta del proyecto:** ¿Las selecciones con una mayor proporción de jugadores pertenecientes a clubes de la Premier League, Bundesliga, LaLiga, Ligue 1 y Serie A tienden a llegar más lejos en el torneo?

El proyecto está terminado. El reporte contiene dos páginas: **Big Five Impact**, con comparaciones por fase, liga, selección y club; y **Team & Player Explorer**, para filtrar y consultar selecciones y jugadores.

## Enfoque

La hipótesis se explora relacionando, para cada selección, la proporción de integrantes de su plantilla que juega en clubes de las cinco ligas estudiadas con la fase más avanzada alcanzada en el torneo. La fase es un indicador ordinal de rendimiento; las métricas individuales (valor de mercado, partidos internacionales y goles) sirven como contexto adicional para explorar los registros disponibles.

El análisis es observacional. Puede mostrar una asociación en estos datos, pero no demuestra que jugar en una Big Five cause un mejor resultado. El avance de una selección depende de muchos factores y la comparación de proporciones a nivel de selección no debe interpretarse como una conclusión sobre el rendimiento individual de cada jugador.

## Contenido del repositorio

```text

├── Futbol dashboard - Report View.pbix   # Reporte interactivo de Power BI
├── Report_View_Definition/               # Definición editable de las dos páginas y sus visuales
├── data/
│   └── Libro1_normalizado_v2.xlsx         # Libro de datos incluido para reproducir/actualizar el análisis
├── Tema_BigFive.json                     # Tema visual
└── README.md
```

El Excel contiene cuatro hojas de datos:

| Hoja | Contenido |
| --- | --- |
| `Hoja1` | Selecciones, código FIFA, grupo y confederación |
| `Hoja2` | Fase alcanzada y orden de fase por selección |
| `Hoja3` | Jugadores, selección, posición, club y métricas disponibles |
| `Hoja4` | Catálogo de clubes de las cinco ligas, liga, país y temporada |

Los datos de clubes y jugadores se obtuvieron de un repositorio de GitHub dedicado al Mundial 2026. La información de las selecciones participantes y las fases alcanzadas se recopiló con apoyo de ChatGPT y se organizó para el análisis.

## Cómo abrir el reporte

1. Descarga o clona el repositorio.
2. Abre `Futbol dashboard - Report View.pbix` con Power BI Desktop.
3. Si Power BI solicita la ubicación del libro, selecciona `data/Libro1_normalizado_v2.xlsx` y actualiza las consultas.
4. Revisa las páginas **Big Five Impact** y **Team & Player Explorer** y utiliza los segmentadores para explorar el conjunto.

La definición bajo `Report_View_Definition` documenta los visuales del reporte. Para editar el modelo de datos y las medidas, utiliza el PBIX en Power BI Desktop. Al mover el repositorio a otra computadora, puede ser necesario volver a seleccionar la ruta del Excel en Power Query.

## Tecnologías

- Microsoft Power BI Desktop
- Power Query
- DAX
- Microsoft Excel

## Preparación de datos

Se normalizaron nombres de clubes para hacer coincidir la tabla de jugadores con el catálogo de clubes Big Five. Esto permite clasificar a los jugadores por liga de forma consistente y reduce asociaciones perdidas o incorrectas derivadas de alias y variantes ortográficas.

El catálogo de clubes cubre solo las cinco ligas definidas para este estudio. Por ello, un jugador sin coincidencia en dicho catálogo no debe asumirse como jugador sin club ni como perteneciente a una liga específica: significa que no forma parte del universo de clubes Big Five clasificado por esta tabla.

## Alcance y límites

- El análisis se limita a las selecciones, jugadores, resultados y clubes presentes en el libro versionado en el repositorio.
- La fase alcanzada resume el resultado del equipo y no mide por sí sola todos los aspectos de su rendimiento.
- Los valores de mercado, goles y partidos internacionales son los incluidos en la versión del libro que acompaña al repositorio.
- Los resultados pueden cambiar si se actualizan las plantillas, el catálogo de clubes o la información del torneo.
- La relación observada no implica causalidad.

## Evidencia

La página **Big Five Impact** del PBIX muestra la vista general del dashboard: métricas de participación, evolución por fase y comparaciones por liga, clubes y selecciones. La captura de esa pantalla también está incluida en la ficha del proyecto de Notion.




