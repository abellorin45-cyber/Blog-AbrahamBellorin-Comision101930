Contexto

En un entorno administrativo dedicado a la gestión de facturación y control de información financiera, se trabajaba diariamente con planillas de Excel que contenían datos de clientes, importes, impuestos y márgenes de ganancia. Cada registro requería calcular automáticamente valores como el IVA, la alícuota correspondiente y la ganancia obtenida sobre cada operación.

Inicialmente, estos cálculos se realizaban de forma manual o mediante fórmulas copiadas fila por fila, lo que consumía tiempo y aumentaba la probabilidad de errores cuando se incorporaban nuevos registros.

Problema

El principal desafío consistía en automatizar los cálculos utilizando columnas derivadas dentro de una tabla de Excel, evitando que los usuarios tuvieran que copiar fórmulas manualmente cada vez que se agregaban nuevas filas.

Durante la implementación surgieron varios inconvenientes:

Las fórmulas no siempre se extendían automáticamente al insertar nuevos registros.
Algunos cálculos utilizaban referencias absolutas e impedían que las fórmulas funcionaran correctamente en todas las filas.
Existía el riesgo de modificar accidentalmente una fórmula, generando diferencias entre registros.
La actualización de impuestos o porcentajes obligaba a modificar múltiples fórmulas de manera manual.

Como consecuencia, la información podía presentar inconsistencias y requería una revisión constante antes de generar reportes.

Acciones

Para solucionar el problema se implementó una estrategia de automatización basada en las funcionalidades de Excel.

Las principales acciones fueron:

Conversión del rango de datos en una Tabla de Excel, permitiendo que las fórmulas se propagaran automáticamente al agregar nuevas filas.
Implementación de columnas derivadas para calcular:
IVA.
Alícuota aplicada.
Ganancia.
Reemplazo de referencias tradicionales por referencias estructuradas, facilitando la lectura y mantenimiento de las fórmulas.
Validación de resultados mediante casos de prueba con distintos valores de entrada.
Documentación de cada modificación utilizando un repositorio Git.
Post-Mortem Constructivo

Después de finalizar la implementación se realizó un análisis para identificar qué funcionó correctamente y qué aspectos podían mejorarse.

¿Qué salió bien?

Se eliminó la necesidad de copiar fórmulas manualmente.
Se redujeron significativamente los errores de cálculo.
La planilla quedó preparada para crecer sin requerir modificaciones adicionales.
Los usuarios obtuvieron resultados consistentes independientemente de la cantidad de registros.

¿Qué podría haberse hecho mejor?

Definir desde el inicio una estructura estandarizada para las tablas.
Documentar previamente las reglas de negocio de cada cálculo.
Incorporar validaciones automáticas antes de comenzar a cargar datos reales.

Acciones preventivas implementadas

Mantener todas las bases de datos como Tablas de Excel.
Centralizar los porcentajes utilizados para facilitar futuras modificaciones.
Documentar cada cambio importante mediante commits descriptivos.
Realizar pruebas con datos de ejemplo antes de liberar cambios.
Aprendizajes

Este desafío permitió comprender que la automatización en Excel no depende únicamente de escribir fórmulas, sino también de diseñar correctamente la estructura de los datos.

Entre los principales aprendizajes se destacan:

Las Tablas de Excel facilitan enormemente la automatización de procesos repetitivos.
Las columnas derivadas reducen errores humanos y mejoran la consistencia de la información.
El uso de referencias estructuradas hace que las fórmulas sean más legibles y fáciles de mantener.
Documentar cambios mediante un sistema de control de versiones permite reconstruir el historial del proyecto y comprender la evolución de la solución.
Un pequeño esfuerzo inicial en diseño evita muchas horas de corrección y mantenimiento en el futuro.

Reflexión sobre la aplicación de feedback radicalmente sincero

Durante el desarrollo de esta automatización apliqué el enfoque de feedback radicalmente sincero al evaluar tanto los errores del proceso como las decisiones tomadas. En lugar de buscar responsables, me concentré en identificar las causas reales de los inconvenientes, como el uso de fórmulas manuales y la falta de una estructura estandarizada. A partir de esas observaciones, implementé mejoras concretas, como el uso de Tablas de Excel, columnas derivadas y referencias estructuradas.
Esta forma de analizar el trabajo permitió transformar los errores en oportunidades de aprendizaje, fortalecer la solución implementada y establecer buenas prácticas para futuros proyectos.

Uso de Control de Versiones

Durante el desarrollo se registraron los cambios utilizando Git para mantener trazabilidad de las mejoras implementadas.
