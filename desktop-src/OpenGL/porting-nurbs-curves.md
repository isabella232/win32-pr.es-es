---
title: Porte de curvas DE LABS DE PORTE
description: Las funciones De OpenGL para dibujar curvas DE COLOR SON muy similares a las funciones GL de IRIS. Puede especificar secuencias de contención y puntos de control mediante una función gluNurbsCurve, que debe estar contenida dentro de un par gluBeginCurve/gluEndCurve.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- Porte de IRIS GL, curvas DE COLORYBS
- porte de curvas IRIS GL,GLBS
- porte a OpenGL desde IRIS GL, curvas DE IRISBS
- Porte de OpenGL desde iris gl,curvas DE IRISBS
- Curvas DE LAS CURVAS DE LAS CURVAS DE COLOR
- curvas
- Porte de IRIS GL, curvas
- porte desde IRIS GL, curvas
- porte a OpenGL desde IRIS GL, curvas
- Porte de OpenGL desde IRIS GL, curvas
- SPLINEBS (B-spline no uniforme)
- Spline B no uniforme lógica (SPLINE) (SPLINEBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9aa43bcc40c2b6a93eb5690abe4265f792a58a2520e579d536a08520ca4f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132404"
---
# <a name="porting-nurbs-curves"></a>Porte de curvas DE LABS DE PORTE

Las funciones De OpenGL para dibujar curvas DE COLOR SON muy similares a las funciones GL de IRIS. Puede especificar secuencias de contención y puntos de control mediante una función [**gluNurbsCurve,**](glunurbscurve.md) que debe estar contenida dentro de un par [**gluBeginCurve**](glubegincurve.md)  /  [**gluEndCurve.**](gluendcurve.md)

En la tabla siguiente se enumeran las funciones GL de IRIS para dibujar curvas DE AMMBS y sus funciones OpenGL equivalentes.



| Función GL de IRIS | Función OpenGL                        | Significado                     |
|------------------|----------------------------------------|-----------------------------|
| **bgncurve**     | [**gluBeginCurve**](glubegincurve.md) | Comienza una definición de curva.  |
| **ybscurve**   | [**gluNurbsCurve**](glunurbscurve.md) | Especifica los atributos de curva. |
| **endcurve**     | [**gluEndCurve**](gluendcurve.md)     | Finaliza una definición de curva.    |



 

Asocie las coordenadas de posición, textura y color mediante la presentación de cada una como **un gluNurbsCurve** independiente dentro del par de inicio y fin. No puede realizar más de una llamada a **gluNurbsCurve** para cada fragmento de datos de color, posición y textura dentro de un único par **gluBeginCurve/gluEndCurve.** Debe realizar exactamente una llamada para describir la posición de la curva (una descripción DE GL \_ MAP1 VERTEX 3 o \_ GL \_ \_ MAP1 VERTEX \_ \_ 4). Cuando se llama **a gluEndCurve**, la curva se tesela en segmentos de línea y, a continuación, se representa.

En la tabla siguiente se enumeran los tipos de curva IRIS GL y OpenGL GLBS.



| Tipo GL de IRIS | Tipo OpenGL                  | Significado                                 |
|--------------|------------------------------|-----------------------------------------|
| N \_ V3D       | GL \_ MAP1 \_ VERTEX \_ 3          | Curva polinómica.                       |
| N \_ V3DR      | GL \_ MAP1 \_ VERTEX \_ 4          | Curva racionalizada.                         |
|              | COORD DE TEXTURA DE GL \_ MAP1 \_ \_\_\* | Los puntos de control son coordenadas de textura. |
|              | GL \_ MAP1 \_ NORMAL             | Los puntos de control son normales.             |



 

Para obtener más información sobre los tipos de evaluador disponibles, [**vea glMap1**](glmap1.md).

??

 

 




