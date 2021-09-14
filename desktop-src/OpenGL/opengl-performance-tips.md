---
title: Rendimiento de OpenGL Sugerencias
description: Rendimiento de OpenGL Sugerencias
ms.assetid: f85bf725-1361-49b9-894c-c803b2dead60
keywords:
- OpenGL, sugerencias de rendimiento
- OpenGL, procedimientos recomendados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e5b6fa33f8d6841d0fd47d1a655ef99facc84e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244880"
---
# <a name="opengl-performance-tips"></a>Rendimiento de OpenGL Sugerencias

Estas prácticas de programación optimizan el rendimiento de la aplicación:

-   Use [**glColorMaterial cuando**](glcolormaterial.md) solo se va a variar rápidamente una sola propiedad de material (por ejemplo, en cada vértice). Use [**glMaterial**](glmaterial-functions.md) para cambios poco frecuentes o cuando se va a modificar rápidamente más de una propiedad de material única.
-   Use [**glLoadIdentity para**](glloadidentity.md) inicializar una matriz, en lugar de cargar su propia copia de la matriz de identidad.
-   Use llamadas de matriz específicas como [**glRotate,**](glrotate.md) [**glTranslate**](gltranslate.md)y [**glScale,**](glscale.md)en lugar de crear sus propias matrices de rotación, traducción y escala y llamar [**a glMultMatrix**](glmultmatrix.md).
-   Use [**glPushAttrib y**](glpushattrib.md) [**glPopAttrib para**](glpopattrib.md) guardar y restaurar valores de estado. Use funciones de consulta solo cuando la aplicación requiera los valores de estado para sus propios cálculos.
-   Use listas para mostrar para encapsular los cambios de estado que consumen mucha memoria. Por ejemplo, coloque todas las llamadas [**glTexImage**](glteximage1d.md) necesarias para especificar completamente una textura (y quizás las llamadas [**glTexParameter**](gltexparameter-functions.md), [**glPixelStore y**](glpixelstore-functions.md) [**glPixelTransfer**](glpixeltransfer.md) asociadas también) en una sola lista de visualización. Llame a esta lista de visualización para seleccionar la textura.
-   Use listas de visualización para encapsular las llamadas de representación de objetos rígidas que se dibujarán repetidamente.
-   Para minimizar el ancho de banda de red en entornos cliente/servidor, use evaluadores incluso para teselaciones de superficie simples.
-   Si es posible, para evitar la sobrecarga de GL \_ NORMALIZE, proporcione normales de longitud de unidad. Dado [**que glScale casi**](glscale.md) siempre requiere habilitar GL \_ NORMALIZE, evite usar **glScale** al realizar la iluminación.
-   Si no es necesario el sombreado suave, establezca [**glShadeModel**](glshademodel.md) en GL \_ FLAT.
-   Use una sola [**llamada glClear**](glclear.md) por fotograma, si es posible. No use **glClear para** borrar subregiones pequeñas de los búferes; úselo solo para borrar el búfer por completo o casi por completo.
-   Para dibujar varios triángulos independientes, use una sola llamada en lugar de varias llamadas a [**glBegin**](glbegin.md) ( GL TRIANGLES ) o una llamada \_ a **glBegin** ( GL \_ POLYGON ). Semejantemente:

    Para dibujar un triángulo único, use GL \_ TRIANGLES en lugar de \_ GL POLYGON.

    Use una sola llamada a [**glBegin**](glbegin.md) (GL QUADS) en lugar de llamar a \_ **glBegin** \_ (GL POLYGON) repetidamente.

    Use una sola llamada a [**glBegin**](glbegin.md) (GL LINES ) para dibujar varios segmentos de línea independientes, en lugar de llamar a \_ **glBegin** (GL \_ LINES ) varias veces.

-   En general, use las formas vectoriales de los comandos para pasar datos precalutados y use las formas escalares de comandos para pasar valores que se calculan cerca del tiempo de llamada.
-   Evite realizar cambios en el modo redundante, como establecer el color en el mismo valor entre cada vértice de un polígono sombreado plano.
-   Al dibujar o copiar imágenes, deshabilite la rasterización y las operaciones por fragmento para optimizar los recursos. OpenGL puede aplicar texturas a imágenes de píxeles.

 

 




