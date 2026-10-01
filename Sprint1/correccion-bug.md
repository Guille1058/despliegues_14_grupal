# Reporte de Corrección de Bug - Sprint 1

## 1. Descripción del Bug
Al revisar la página principal (index.html), se identificó un problema de visibilidad en el botón principal de la sección Hero ("Empezar ahora"). El texto del botón no se mostraba en pantalla debido a un fallo de contraste de color.

## 2. Diagnóstico
Utilizando las herramientas de desarrollador del navegador (Inspect / F12), se inspeccionó el elemento <button class="btn btn-primary">. Se observó que en styles.css la regla CSS asignaba la misma variable de color tanto al fondo como al texto:

.btn-primary {
  background-color: var(--color-primary);
  color: var(--color-primary);
}

## 3. Solución Aplicada
Se modificó el archivo styles.css cambiando el valor del texto a blanco para solucionar el contraste:

.btn-primary {
  background-color: var(--color-primary);
  color: #ffffff;
}

## 4. Verificación
Se recargó la página en el navegador y se comprobó que el texto "Empezar ahora" vuelve a ser perfectamente legible en blanco sobre el botón verde.