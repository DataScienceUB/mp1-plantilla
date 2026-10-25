# SPECS · Cuadro de mando BiciBCN

> **Qué construimos.** Lo escribe el equipo; el agente lo lee pero no lo edita.
> Las indicaciones entre `<!-- -->` son de la plantilla: borradlas cuando escribáis cada sección.

## 1. Objetivo

<!--
Una o dos frases: para quién es el cuadro de mando y qué decisiones le ayuda a tomar.
Pista: no es "ver datos", es decidir algo concreto. ¿Qué decidirá Jordi Puig cada lunes?
-->

## 2. Usuarios y preguntas

<!--
- Usuario: quién lo usa, cuándo y qué sabe (¿es técnico? ¿cuánto tiempo tiene?).
- Preguntas: las del encargo, numeradas (P1, P2…) y concretadas. Cada pantalla del cuadro
  de mando responderá a una de ellas.
-->

## 3. Entradas

<!--
Los ficheros de data/raw/ y los problemas de calidad que encontréis con notebooks/exploracion.ipynb.
Sed concretos: cuántas filas, qué columna, qué valor raro y cuántas veces aparece.
Hito de la sesión 4: al menos seis problemas documentados.

Ejemplo de fila:
| `viajes.csv` (N filas) | Un viaje de la muestra del 5 % | N `viaje_id` repetidos; … |
-->

| Fichero | Una fila es | Problemas encontrados |
| --- | --- | --- |
| | | |

## 4. Salidas

<!--
Qué genera el pipeline en data/processed/ y qué muestra la app.
Como mínimo, las tres tablas del contrato de AGENTS.md §3. Añadid las columnas derivadas
o tablas extra que necesitéis para las métricas (p. ej. fecha, hora, laborable…).
-->

## 5. Requisitos

<!--
Reglas numeradas (R1, R2…), cada una verificable y sin ambigüedad. Separadlas en bloques.
Cada problema de la sección 3 debería tener un requisito que diga qué se hace con él.

Ejemplos de forma:
- R1. Un viaje aparece una sola vez: si un viaje_id se repite, se conserva una fila.
- R7. Viajes por día laborable = viajes estimados en días laborables / número de días laborables. Laborable = …
-->

**Datos**

**Métricas**

**Cuadro de mando**

## 6. Criterios de aceptación

<!--
Cada criterio (CA1, CA2…) dice qué requisito verifica y cómo se comprueba con una cifra o un hecho
concreto. Cada uno tendrá al menos un test en tests/acceptance/ marcado con
@pytest.mark.criterio("CA…"). scripts/trazabilidad.py lee los CA de esta sección.

Dos tipos útiles:
- Con los datos reales: "CA1 (R1). Tras limpiar, ningún viaje_id se repite."
- Con un ejemplo pequeño calculado a mano: "CA5 (R7). Con 3 viajes laborables en 2 días laborables,
  los viajes por día laborable son 30."

Lo que no se pueda testear (p. ej. si un gráfico se entiende) indicad cómo se verifica.
-->

## 7. Fuera de alcance

<!-- Lo que no vais a hacer, para que nadie (ni el agente) lo haga. -->

## 8. Preguntas abiertas

<!-- Dudas pendientes de decidir. Cuando se decidan, pasan a "Decisiones". -->

## 9. Decisiones

<!--
Una línea por decisión: fecha · qué se decide · requisitos afectados · por qué (con cifras si las hay).
Ejemplo:
- 2026-10-20 · Se conserva la primera aparición de cada viaje duplicado · R1 · Son copias exactas (N filas).
-->
