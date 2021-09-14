---
title: Porte de curvas DE COLORERBS
description: Las funciones de OpenGL para dibujar curvas DE ASEBS son muy similares a las funciones GL de IRIS. Las secuencias de secuencias y los puntos de control se especifican mediante una función gluNurbsCurve, que debe estar dentro de un par gluBeginCurve/gluEndCurve.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- Porte de IRIS GL, curvas DE ASEBS
- porte de curvas IRIS GL,GLBS
- porte a OpenGL desde curvas IRIS GL,GLBS
- Porte de OpenGL desde curvas IRIS GL,GLBS
- Curvas DE CURVAS DE CURVAS
- curvas
- Porte de IRIS GL, curvas
- porting from IRIS GL,curves
- porte a OpenGL desde IRIS GL, curvas
- Porte de OpenGL desde IRIS GL, curvas
- SPLINEBS (spline B no uniforme lógica)
- Spline B no uniforme lógica (SPLINEBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f539e466ce8ade17d135c9369e1f641831792e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074007"
---
# <a name="porting-nurbs-curves"></a>Porte de curvas DE COLORERBS

Las funciones de OpenGL para dibujar curvas DE ASEBS son muy similares a las funciones GL de IRIS. Las secuencias de secuencias y los puntos de control se especifican mediante una función [**gluNurbsCurve,**](glunurbscurve.md) que debe incluirse dentro de un par [**gluBeginCurve**](glubegincurve.md)  /  [**gluEndCurve.**](gluendcurve.md)

En la tabla siguiente se enumeran las funciones GL de IRIS para dibujar curvas DE AMMBS y sus funciones OpenGL equivalentes.



| Función IRIS GL | Función OpenGL                        | Significado                     |
|------------------|----------------------------------------|-----------------------------|
| **bgncurve**     | [**gluBeginCurve**](glubegincurve.md) | Comienza una definición de curva.  |
| **ybscurve**   | [**gluNurbsCurve**](glunurbscurve.md) | Especifica atributos de curva. |
| **endcurve**     | [**gluEndCurve**](gluendcurve.md)     | Finaliza una definición de curva.    |



 

Asocie las coordenadas de posición, textura y color mediante la presentación de cada una como **un gluNurbsCurve** independiente dentro del par inicial y final. No puede realizar más de una llamada a **gluNurbsCurve** para cada fragmento de datos de color, posición y textura dentro de un único par **gluBeginCurve/gluEndCurve.** Debe realizar exactamente una llamada para describir la posición de la curva (una descripción DE GL \_ MAP1 VERTEX 3 o \_ GL \_ \_ MAP1 VERTEX \_ \_ 4). Cuando se llama **a gluEndCurve,** la curva se tesela en segmentos de línea y, a continuación, se representa.

En la tabla siguiente se enumeran los tipos de curva IRIS GL y OpenGL GLBS.



| Tipo GL de IRIS | Tipo OpenGL                  | Significado                                 |
|--------------|------------------------------|-----------------------------------------|
| N \_ V3D       | GL \_ MAP1 \_ VERTEX \_ 3          | Curva polinómica.                       |
| N \_ V3DR      | GL \_ MAP1 \_ VERTEX \_ 4          | Curva racionalizada.                         |
|              | COORD DE TEXTURA DE GL \_ MAP1 \_ \_\_\* | Los puntos de control son coordenadas de textura. |
|              | GL \_ MAP1 \_ NORMAL             | Los puntos de control son normales.             |



 

Para obtener más información sobre los tipos de evaluador disponibles, [**vea glMap1**](glmap1.md).

??

 

 




