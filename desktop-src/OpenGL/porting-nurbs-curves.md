---
title: Trasladar curvas de NURBS
description: Las funciones de OpenGL para dibujar curvas NURBS son muy similares a las funciones de contabilidad de IRIS. Se especifican las secuencias de nudos y los puntos de control mediante una función gluNurbsCurve, que debe estar contenida dentro de un par gluBeginCurve/gluEndCurve.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- Migración de la contabilidad de IRIS, curvas de NURBS
- trasladar de IRIS GL, curvas de NURBS
- trasladar a OpenGL desde IRIS GL, curvas de NURBS
- Exportación de OpenGL desde IRIS GL, curvas de NURBS
- Curvas NURBS
- curvas
- Migración de la contabilidad de IRIS, curvas
- trasladar de IRIS GL, curvas
- trasladar a OpenGL desde IRIS GL, curvas
- Exportación de OpenGL de IRIS GL, curvas
- NURBS (no uniforme, B-spline racional)
- B-spline racional no uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f539e466ce8ade17d135c9369e1f641831792e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418878"
---
# <a name="porting-nurbs-curves"></a>Trasladar curvas de NURBS

Las funciones de OpenGL para dibujar curvas NURBS son muy similares a las funciones de contabilidad de IRIS. Se especifican las secuencias de nudos y los puntos de control mediante una función [**gluNurbsCurve**](glunurbscurve.md) , que debe estar dentro de un par gluEndCurve de [**gluBeginCurve**](glubegincurve.md)  /  [](gluendcurve.md) .

En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para dibujar curvas NURBS y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS | Función OpenGL                        | Significado                     |
|------------------|----------------------------------------|-----------------------------|
| **bgncurve**     | [**gluBeginCurve**](glubegincurve.md) | Comienza una definición de curva.  |
| **nurbscurve**   | [**gluNurbsCurve**](glunurbscurve.md) | Especifica los atributos de la curva. |
| **endcurve**     | [**gluEndCurve**](gluendcurve.md)     | Finaliza una definición de curva.    |



 

Asocie coordenadas de posición, textura y color presentando cada una de ellas como un **gluNurbsCurve** independiente dentro del par Begin/end. No puede hacer más de una llamada a **gluNurbsCurve** para cada parte de los datos de color, posición y textura dentro de un solo par **gluBeginCurve/gluEndCurve** . Debe hacer exactamente una llamada para describir la posición de la curva (una descripción de \_ MAP1 de vértice \_ \_ 3 o \_ GL \_ MAP1 \_ ). Cuando se llama a **gluEndCurve**, la curva se Tesela en segmentos de línea y, a continuación, se representa.

En la tabla siguiente se enumeran los tipos de curva IRIS GL y OpenGL NURBS.



| Tipo de GL de IRIS | Tipo de OpenGL                  | Significado                                 |
|--------------|------------------------------|-----------------------------------------|
| N \_ V3D       | \_ \_ Vértice \_ 3 de GL MAP1          | Curva polinómica.                       |
| N \_ V3DR      | \_ \_ Vértice \_ 4 de GL MAP1          | Curva racional.                         |
|              | GL \_ MAP1 \_ Texture \_ coordenadas\_\* | Los puntos de control son coordenadas de textura. |
|              | GL \_ MAP1 \_ normal             | Los puntos de control son normales.             |



 

Para obtener más información sobre los tipos de evaluador disponibles, vea [**glMap1**](glmap1.md).

??

 

 




