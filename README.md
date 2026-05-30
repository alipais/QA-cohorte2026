# QA-cohorte2026
README — Cypress QA Automation (Aprendizaje) 🚀🧪
Descripción

Repositorio para guardar ejemplos, ejercicios y buenas prácticas de Cypress orientadas a QA Automation. 🎯
Objetivo: aprender conceptos relevantes, crear tests reproducibles y montar una base para proyectos de automatización. 📚
Contenido del repositorio

/cypress
/e2e — tests end-to-end organizados por feature 🧭
/fixtures — datos de prueba (JSON) 📄
/support — comandos personalizados y configuración global 🛠️
/plugins — plugins y hooks de Cypress 🔌
/scripts — scripts útiles (ej.: inicialización, reportes) ⚙️
/reports — resultados generados (Allure, mochawesome, etc.) 📊
/docs — notas, guías rápidas y checklist de QA 🗂️
package.json — dependencias y comandos 📦
Requisitos

Node.js >= 18 🟢
npm o yarn 🧶
Chrome / navegador compatible (o configurar Cypress headless) 🌐
Instalación rápida

Clonar el repositorio: git clone ⤵️
Instalar dependencias: npm install — o — yarn install ⚡
Comandos útiles (npm scripts)

npm run cypress:open — abre la UI de Cypress interactiva 🖥️
npm run cypress:run — ejecuta tests en modo headless ▶️
npm run test:ci — ejecuciones configuradas para CI (headless + reporter) 🔁
npm run lint — chequeo de linter (si aplica) 🔍
Estructura recomendada de tests

Nombre de archivo: feature.spec.js (ej.: login.spec.js) 📝
Cada spec debe:
Tener un propósito claro (describe) 🎯
Incluir setup/teardown en hooks (before, beforeEach, afterEach) 🔁
Usar fixtures para datos reutilizables 🧩
Evitar dependencias entre tests (tests idempotentes) 🚫🔗
Añadir ids de test o data-testid en el HTML para selectores estables 🔎
Buenas prácticas

Seleccionar elementos por atributos (data-cy, data-test, data-testid). 🏷️
Mantener tests rápidos: mocks/stubs para dependencias externas cuando sea apropiado. ⚡
Usar Page Objects o funciones de ayuda para encapsular acciones repetitivas. 📚
Evitar esperas fijas; preferir comandos de espera implícitos y assertions. ⏱️✅
Ejecutar en CI en cada PR; mantener flakiness < 2% mediante revisión. 🔁🛡️
Versionar y documentar los cambios en tests. 🧾
Integración con CI

Ejemplo (GitHub Actions): workflow que instala dependencias, ejecuta npm run cypress:run y sube reportes/artifacts. 🧰📦
Recomendación: ejecutar en contenedor con navegador o usar cypress-io/github-action. 🐳
Reportes y debugging

Integrar mochawesome o Allure para reportes legibles. 📑
Grabar videos/screenshots en fallos (configurable en cypress.config). 🎥📸
Logs y comandos personalizados en support/ para facilitar debugging. 🪵🔧
Checklist antes de merge

 Tests verdes en local y en CI ✅
 Reporte adjunto (si aplica) 📎
 No usar selectores frágiles 🔍
 Datos sensíbles no incluidos en fixtures 🔒
 Revisado por al menos 1 teammate 👥
Ejemplos y recursos

/docs/quick-start.md — guía rápida de cómo añadir un nuevo test ⚡
/docs/selectors.md — convención de selectores (data-cy) 🏷️
/docs/ci-setup.md — ejemplo de workflow para GitHub Actions ⚙️
Contribuir

Abrir PR indicando el propósito y agregar tests cuando corresponda. ➕
Mantener código legible y documentado. ✍️
Seguir convenciones del repo. 📏
Licencia

LICENSE (agregar licencia deseada, ej.: MIT) 📜
