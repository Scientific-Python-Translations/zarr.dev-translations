---
title: Actualización de diseño del protocolo Zarr v3
date: 2019-06-19
categories: especificaciones zarr
layout: home
author_profile: false
sidebar:
  title: Contenido
  nav: sidebar
---

Hoy he reunido algunas [diapositivas que resumen el estado actual del trabajo exploratorio sobre la especificación del protocolo Zarr v3] (https://zarr-developers.github.io/slides/v3-update-20190619.html). El propósito de este blog es compartir esas diapositivas más ampliamente y proporcionar un contexto que explique por qué se comenzó a trabajar en una especificación v3.

## ¿Por qué trabajar en una especificación v3?

La [especificación actual (v2) de Zarr] (https://zarr.readthedocs.io/en/stable/spec/v2.html) se implementa en varias bibliotecas de software y es un protocolo estable y sólido que se utiliza en producción en varias comunidades científicas diferentes. Si necesita almacenar y calcular en paralelo con datos similares a matrices, es una buena solución. Entonces, ¿por qué empezar a pensar en una nueva versión del protocolo?

### Lenguaje-agnóstico

Una razón es que el protocolo v2 está algo centrado en Python e incluye algunas características que no son sencillas de implementar en otros lenguajes. This has meant that implementations do not all
support the same feature set. Sería bueno tener una especificación de protocolo v3 mínima que pudiera implementarse completamente en cualquier lenguaje, de modo que todas las implementaciones tengan paridad en torno a un conjunto de características principales.

### Unifying Zarr and N5

Otra razón es que nos gustaría fusionar los esfuerzos de desarrollo entre las comunidades Zarr y N5, por lo que un objetivo de la especificación v3 es unificar los dos enfoques y proporcionar un objetivo de implementación común.

### Extensibilidad

Una tercera razón es que varios grupos diferentes han comenzado a experimentar y extender el protocolo Zarr de maneras interesantes, pero no siempre es claro cómo extender el protocolo v2 para admitir nuevas funciones. Sería bueno si la especificación v3 proporcionara una variedad de puntos de extensión y mecanismos de extensión claros.

### Almacenamiento en la nube

Finalmente, si bien la especificación v2 se puede utilizar de manera muy efectiva con sistemas de almacenamiento distribuido como Amazon S3 o Google Cloud Storage, hay espacio para mejoras, particularmente en lo que respecta a cómo se almacenan y organizan los metadatos.

## Actualización de diseño Zarr v3

Si está interesado en saber más sobre el estado actual del trabajo en la especificación v3, eche un vistazo a las [diapositivas de actualización del diseño v3] (https://zarr-developers.github.io/slides/v3-update-20190619.html). Las diapositivas usan reveal.js y tienen navegación horizontal y vertical; si no lo has visto antes, navega primero hacia abajo siempre que puedas, antes de navegar hacia la derecha.

Como menciono en las diapositivas, la especificación v3 actual es solo un borrador, destinado a ilustrar algunas ideas y posibles soluciones, pero todo está sujeto a discusión. Entonces, si tiene algún comentario o idea, comuníquese con nosotros, cualquiera es bienvenido a participar.

----

Publicación escrita por [Alistair Miles](https://github.com/alimanfoo).
