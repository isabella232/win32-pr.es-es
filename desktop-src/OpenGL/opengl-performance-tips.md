---
title: Sugerencias de rendimiento de OpenGL
description: Sugerencias de rendimiento de OpenGL
ms.assetid: f85bf725-1361-49b9-894c-c803b2dead60
keywords:
- OpenGL, sugerencias de rendimiento
- OpenGL, procedimientos recomendados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e5b6fa33f8d6841d0fd47d1a655ef99facc84e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776129"
---
# <a name="opengl-performance-tips"></a>Sugerencias de rendimiento de OpenGL

Estas prácticas de programación optimizan el rendimiento de la aplicación:

-   Use [**glColorMaterial**](glcolormaterial.md) cuando solo se modifique rápidamente una propiedad de material única (en cada vértice, por ejemplo). Use [**glMaterial**](glmaterial-functions.md) para realizar cambios poco frecuentes o cuando se cambie rápidamente más de una propiedad de material.
-   Use [**glLoadIdentity**](glloadidentity.md) para inicializar una matriz, en lugar de cargar su propia copia de la matriz de identidad.
-   Use llamadas de matriz específicas como [**glRotate**](glrotate.md), [**glTranslate**](gltranslate.md)y [**glScale**](glscale.md), en lugar de crear sus propias matrices de escalado, traslación y rotación, y llamar a [**glMultMatrix**](glmultmatrix.md).
-   Use [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md) para guardar y restaurar los valores de estado. Use las funciones de consulta solo cuando la aplicación requiera los valores de estado para sus propios cálculos.
-   Use listas de visualización para encapsular los cambios de estado que pueden consumir mucha memoria. Por ejemplo, coloque todas las llamadas a [**glTexImage**](glteximage1d.md) necesarias para especificar por completo una textura (y quizás también las llamadas [**glTexParameter**](gltexparameter-functions.md), [**glPixelStore**](glpixelstore-functions.md)y [**glPixelTransfer**](glpixeltransfer.md) asociadas) en una sola lista de visualización. Llame a esta lista de visualización para seleccionar la textura.
-   Use mostrar listas para encapsular las llamadas de representación de objetos rígidas que se dibujarán repetidamente.
-   Para minimizar el ancho de banda de red en entornos cliente/servidor, use evaluadores incluso para las teselaciones de superficie simples.
-   Si es posible, para evitar la sobrecarga de la normalización de contabilidad \_ , proporcione normales de longitud unitaria. Dado que [**glScale**](glscale.md) casi siempre requiere la habilitación del \_ normalizado de contabilidad, evite el uso de **glScale** al realizar la iluminación.
-   Si no es necesario el sombreado suave, establezca [**glShadeModel**](glshademodel.md) en GL \_ Flat.
-   Use una única llamada a [**glClear**](glclear.md) por fotograma, si es posible. No use **glClear** para borrar pequeñas subregiones de los búferes. Úselo solo para borrar el búfer completamente o casi por completo.
-   Para dibujar varios triángulos independientes, use una sola llamada, en lugar de varias llamadas a [**glBegin**](glbegin.md) ( \_ triángulos de contabilidad) o una llamada a **glBegin** (libro de contabilidad \_ ). Igual

    Para dibujar un solo triángulo, utilice \_ TRIángulos de contabilidad en lugar de un polígono de contabilidad \_ .

    Use una sola llamada a [**glBegin**](glbegin.md) (GL \_ cuádruples) en lugar de llamar a **glBegin** (GL \_ Polygon) varias veces.

    Use una única llamada a [**glBegin**](glbegin.md) ( \_ líneas de contabilidad) para dibujar varios segmentos de línea independientes, en lugar de llamar varias veces a **glBegin** (líneas de contabilidad \_ ).

-   En general, use las formas de vector de comandos para pasar datos calculados previamente y use las formas escalares de comandos para pasar valores que se calculan cerca de la hora de la llamada.
-   Evite realizar cambios en el modo redundante, como establecer el color en el mismo valor entre cada vértice de un polígono con sombra plana.
-   Al dibujar o copiar imágenes, deshabilite la rasterización y las operaciones por fragmento para optimizar los recursos. OpenGL puede aplicar texturas a imágenes de píxeles.

 

 




