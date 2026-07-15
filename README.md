# Validación de cursos TALMA — Recurrencia mensual

Herramienta interna de Gestión del Entrenamiento para validar, mes a mes, que el personal
con cursos por vencer (pasivo) ya tenga la matrícula del año en **Talma Aprende**.

## Uso

1. Abrir la página (GitHub Pages) o el archivo `index.html` con doble clic en Chrome/Edge.
2. Cargar el **pasivo del mes** (hoja `Export`) y el **reporte global de Talma Aprende** (hoja `Sheet1`).
3. Verificar el año de vigencia, elegir el mes y presionar **Cruzar información**.
4. Revisar los indicadores, filtrar **Sin matricular** y **Exportar Excel**
   (hojas: Resumen, Cruce, Pendientes, Revisar_Mapeo, Mapeo_Cursos).

## Privacidad

Todo el procesamiento ocurre en el navegador de quien la usa. Los archivos con datos del
personal **no se suben a ningún servidor**: este repositorio solo contiene la página.

## Reglas del cruce

- Filtra cursos del año seleccionado y descarta los marcados como *obsoleto*.
- Traduce el nombre corto del pasivo al nombre largo de Talma Aprende (tabla `MAPEO` en `index.html`).
- `SEGURIDAD EN RAMPA - WINGO` se valida contra la versión PAX u OT según el cargo.
- Cargos que contienen **PAX** quedan excluidos de: SMS - Wingo, Factores Humanos - Wingo, ER101 y ER 201.
- `SERVICIO AL PASAJERO - JETSMART` está excluido del control.
- Cursos sin mapeo salen como **REVISAR MAPEO** (nunca se dan por no matriculados).

## Mantenimiento

Si aparece un curso nuevo en el pasivo, agregarlo a la tabla `MAPEO` al inicio de `index.html`
(está comentada con instrucciones) y subir el archivo actualizado.
