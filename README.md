# Lista de comprobacion y resultados de las pruebas de diseño
Seguimiento y documentación: Es decir, no es código, sino información sobre el control de calidad.  Defectos: Deja claro que se enfoca en los problemas.  Pruebas de diseño del formulario de pedido: Especifica el contexto del proyecto.
# 🐛 Gestión de Defectos: Formulario de Pedido (v1)

Este repositorio documenta los defectos encontrados durante las pruebas de diseño del formulario de pedido de la aplicación, específicamente en la "Versión del navegador 1". El objetivo es facilitar el seguimiento y la resolución de estos problemas.

## 📋 Resumen de las Pruebas de Diseño

Se realizaron pruebas exhaustivas sobre el formulario de pedido para asegurar su funcionalidad y diseño. La siguiente tabla resume los hallazgos:

| Descripción de la supervisión | Versión del navegador 1 | Versión del navegador 2 | Enlace al informe de errores | ID JIRA |
| :---------------------------- | :---------------------- | :---------------------- | :-------------------------- | :------ |
| El estado inicial del formulario de pedido: se elige la tarifa "Casual" y los campos "Agregar licencia de conducir" y "Método de pago" están vacíos. | APROBADO | APROBADO | | |
| Requisitos Visibles: El formulario contiene los campos de selección de Tarifa, de Licencia de Conducir y de Método de Pago. | APROBADO | APROBADO | | |
| Ubicación del Botón Final: El botón final de "Reservar" (para confirmar el pedido) está situado correctamente debajo de la sección "Requisitos del pedido" | APROBADO | APROBADO | | |
| **Estado del Botón (Inicial): El botón final "Reservar" está deshabilitado (inactivo) cuando el usuario aún no ha seleccionado la Tarifa, añadido la Licencia y elegido el Método de Pago.** | **NO APROBADO** | APROBADO | [Enlace JIRA-002](https://maira-garcia.atlassian.net/issues/?jql=issueKey%20in%20(MAIRAG-2%2CMAIRAG-3)) | JIRA-002 |
| **Estado del Botón (Listo): El botón final "Reservar" se habilita (activo) automáticamente solo después de que se han completado/seleccionado todos los requisitos obligatorios.** | **NO APROBADO** | APROBADO | [Enlace JIRA-003](https://maira-garcia.atlassian.net/issues/?jql=issueKey%20in%20(MAIRAG-2%2CMAIRAG-3)) | JIRA-003 |
| Acción de Reserva: Al hacer clic en el botón final "Reservar" (habilitado), el sistema inicia el proceso final de pedido y redirige a la pantalla de confirmación/búsqueda de conductor. | APROBADO | APROBADO | | |

## 🐞 Defectos Reportados

Basado en las pruebas, se identificaron los siguientes defectos críticos en la "Versión del navegador 1":

1.  **JIRA-002: El botón 'Reservar' no se deshabilita correctamente al inicio del formulario.**
    * **Descripción:** Al cargar el formulario y seleccionar la tarifa "Casual", el botón "Reservar" debería estar deshabilitado hasta que se llenen los campos obligatorios. Esto no ocurre en la Versión del Navegador 1.
    * **Impacto:** Riesgo de que los usuarios intenten reservar sin completar la información necesaria.
    * **Enlace al Issue en Jira:** [JIRA-002](https://maira-garcia.atlassian.net/issues/?jql=issueKey%20in%20(MAIRAG-2%2CMAIRAG-3))

2.  **JIRA-003: El botón 'Reservar' no se habilita automáticamente tras completar los requisitos.**
    * **Descripción:** Una vez que el usuario ha seleccionado la Tarifa, añadido la Licencia de Conducir y elegido el Método de Pago, el botón "Reservar" debería habilitarse. En la Versión del Navegador 1, esto no sucede.
    * **Impacto:** Impide que los usuarios completen el proceso de reserva de manera fluida.
    * **Enlace al Issue en Jira:** [JIRA-003](https://maira-garcia.atlassian.net/issues/?jql=issueKey%20in%20(MAIRAG-2%2CMAIRAG-3))

## ➡️ Pasos Siguientes

* Los desarrolladores deben revisar y corregir los defectos JIRA-002 y JIRA-003 en la Versión del Navegador 1.
* Una vez implementadas las correcciones, se realizará una **prueba de regresión** para asegurar que los defectos se han resuelto y que no se han introducido nuevos problemas.

## 📂 Evidencia
