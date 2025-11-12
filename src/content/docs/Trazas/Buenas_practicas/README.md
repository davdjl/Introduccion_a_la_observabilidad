---
title: "Buenas practicas en trazas"
description: "Se describen las buenas practicas que se tienen que contemplar en la recolección de trazas"
customSlug: "buenas-practicas-en-trazas"
folder: "Observabilidad"
subfolder: "Pilares de la observabilidad"
---
# Buenas practicas
## Correlación de eventos
Para poder llegar a una grafica que integre todo el flujo es importante que la traza y spans estén correlacionados por un identificador único llamado traceID (dependiendo de la plataforma de observabilidad puede cambiar la estructura del nombre) este identificador además de otros elementos es propagado en los headers a cada uno de los elementos del sistema, para comprender como es creado este identificador y los demás elementos podemos revisar la pagina [W3C TraceContext](https://www.w3.org/TR/trace-context/).
## Sampling de datos
Una buena practica en trazas es aplicar una función llamada Sampling, el cual consiste en no recolectar el 100% de los eventos generados en la plataforma, ya que el tamaño de almacenamiento en un ambiente productivo puede llegar a Terabytes e incluso Petabytes de datos. Dependiendo el sampling que se aplique es posible recolectar solo los eventos de errores.
