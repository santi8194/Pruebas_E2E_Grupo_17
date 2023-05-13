# Pruebas VRT Grupo 17

Este repositorio fue creado como parte de la entrega correspondiente a la semana 6 de la asignatura de Pruebas Automatizadas de Software.

## Integrantes del grupo

- Santiago Alvarez Soto
- Camilo Ramírez Restrepo
- Laura Daniela Molina
- Wilmar Julian Puentes

## Resumen actividades:

**1. Implementar la toma de screenshots al interior de las pruebas ya existentes. Tengan en cuenta que el objetivo final de esta fase es realizar comparación de dichos screenshots por lo tanto, los scrennshots se deben tomar después de cada paso ejecutado:**

Se hicieron las modificaciones correspondientes para los 40 escenarios de pruebas, de manera que se tome una captura de pantalla al finalizar cada paso.

Para el caso de Cypress, implementamos la funcionalidad `cy.screenshot()` para tomar screenshots después de cada paso. Puede ver los 20 escenarios modificados en el [siguiente link](https://github.com/santi8194/Pruebas_VRT_Cypress/tree/main/cypress/e2e).

Para el caso de Kraken, creamos un nuevo step para tomar screenshots:

```
When("I take screenshot with name {string}",
      async function (screenName){
  return await this.driver.saveScreenshot (\`screenshots/${screenName}.png\`);
});
```

y dicho step fue llamado luego de finalizar cada paso. Puede ver los 20 escenarios modificados en el [siguiente link](https://github.com/julianpuentesuribe/Pruebas_VRT_Kraken/tree/main/features/web/scenarios).

---

**2. Ejecutar los 40 escenarios modificados en la versión de Ghost actual:**

Se corrieron las pruebas ya existentes con la implementación de screenshots para la versión Ghost 4.44.0 tanto en Cypress como en Kraken. Puede ver los screenshots generados al correr los 20 escenarios en *Cypress* el [siguiente link](https://github.com/santi8194/Pruebas_VRT_Cypress/tree/main/cypress/screenshots). También puede ver los screenshots generados al correr los 20 escenarios en *Kraken* en el [siguiente link](https://github.com/julianpuentesuribe/Pruebas_VRT_Kraken/tree/main/screenshots).

---
**3. Seleccionar 10 escenarios y ejecutelos en la nueva versión instalada preferiblemente pertenecientes a funcionalidades diferentes, para que sean ejecutados en modo de regresión visual a nivel de paso ejecutado.**

Como el equipo tiene mayor afinidad con la herramienta *Cypress* se decidió escoger todos los 10 escenarios en esta herramienta. Los escenarios seleccionados se pueden ver en el [siguiente link](https://github.com/santi8194/Pruebas_VRT_Cypress/tree/main/cypress/e2e_10_scenarios). A dichos escenarios se les hicieron las correciones correspondientes para que pasaran tanto en *Ghost v3.41.1*, como en *Ghost v4.44.0*. 

Se ejecutaron los scripts modificados y se generaron los screenshots por cada paso y por cada versión. Puede ver los screenshots generados en el [siguiente link](https://github.com/santi8194/Pruebas_VRT_Cypress/tree/main/cypress/screenshots_10_scenarios).

---

**4. Construir un reporte HTML mediante un script en el lenguaje de su preferencia, que de forma automática, dadas dos carpetas de ejecución de pruebas, analice los resultados de cada paso y presente: los pasos, los screenshots en ambas versiones y las diferencias visuales.**

---

**5. Si encuentran diferencias visuales,repórtenlas en el sistema de registro de incidencias (una incidencia por diferencia encontrada):**

---


## Escenarios probados con Cypress
Para mantener en un solo lugar los scripts en Cypress de los 20 escenarios de prueba, creamos un repositorio independiente. El README del repositorio explica cómo se pueden ejecutar los scripts correspondientes. [Link repositorio](https://github.com/Molvilada/Pruebas_E2E_Cypress)

## Escenarios probados con Kraken
Para mantener en un solo lugar los scripts en Kraken de los 20 escenarios de prueba, creamos un repositorio independiente. El README del repositorio explica cómo se pueden ejecutar los scripts correspondientes [Link repositorio](https://github.com/Molvilada/Pruebas_E2E_Kraken)

