---
title: Usar curvas y superficies de NURBS
description: Las funciones no uniformes de la spline B (NURBS) proporcionan descripciones generales y eficaces de curvas y superficies en dos y tres dimensiones, convirtiendo las curvas y las superficies en evaluadores de OpenGL.
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- Utilidad OpenGL (GLU), B-spline racional no uniforme (NURBS)
- GLU (utilidad OpenGL), B-spline racional no uniforme (NURBS)
- OpenGL B-spline no uniforme (NURBS)
- NURBS (no uniforme, B-spline racional) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f85e9a2045c417007c34d714ae6635ebfaf1180
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356903"
---
# <a name="using-nurbs-curves-and-surfaces"></a>Usar curvas y superficies de NURBS

Las funciones no uniformes de la spline B (NURBS) proporcionan descripciones generales y eficaces de curvas y superficies en dos y tres dimensiones, convirtiendo las curvas y las superficies en evaluadores de OpenGL. Las funciones de NURBS pueden representar geometría en muchos sistemas de diseño mecánico asistidos por PC. Pueden representar curvas y superficies en una variedad de estilos, y pueden controlar automáticamente la subdivisión adaptable que tessellates el dominio en triángulos más pequeños en regiones de bordes de gran curvatura y de siluetas cercanos. Las funciones de NURBS se dividen en las siguientes categorías.

Para administrar un objeto NURBS, use:

-   [**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (crear un objeto NURBS)
-   [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (elimina un objeto NURBS)
-   [*gluNurbsCallback*](glunurbs.md) (establece una función de control de errores)

Para especificar las curvas deseadas, use:

-   [**gluBeginCurve**](glubegincurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndCurve**](gluendcurve.md)

Para especificar las superficies deseadas, use:

-   [**gluBeginSurface**](glubeginsurface.md)
-   [**gluNurbsSurface**](glunurbssurface.md)
-   [**gluEndSurface**](gluendsurface.md)

También puede especificar una región de recorte, que define un subconjunto del dominio de la superficie de NURBS que se va a evaluar para que pueda crear superficies que tengan límites suaves o que contengan huecos.

Para especificar la región de recorte, use:

-   [**gluBeginTrim**](glubegintrim.md)
-   [**gluPwlCurve**](glupwlcurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndTrim**](gluendtrim.md)

Al igual que con los objetos quadric, puede controlar cómo se representan las curvas y curvas de NURBS. Puede determinar:

-   Si se va a descartar una curva o superficie cuyo control polyhedron se encuentre fuera de la ventanilla actual.
-   La longitud máxima (en píxeles) de los bordes de polígonos que se usan para representar curvas y superficies.
-   Si va a tomar la matriz de proyección, la matriz de MODELVIEW y la ventanilla del servidor OpenGL o proporcionarlas explícitamente con [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).

Use [**gluNurbsProperty**](glunurbsproperty.md) para establecer estas propiedades o use los valores predeterminados. Puede consultar un objeto NURBS sobre su estilo de representación con [**gluGetNurbsProperty**](glugetnurbsproperty.md).

 

 




