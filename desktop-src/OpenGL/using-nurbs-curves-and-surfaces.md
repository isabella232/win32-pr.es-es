---
title: Uso de curvas y superficies DE LABS
description: Las funciones no uniformes de B-Spline lógica (SPLINEBS) proporcionan descripciones generales y eficaces de curvas y superficies en dos y tres dimensiones, lo que convierte las curvas y superficies en evaluadores OpenGL.
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- OpenGL Utility (GLU), Non-Uniform Rational B-Spline (SPLINEBS)
- GLU (utilidad OpenGL), spline B no uniforme lógica (SPLINEBS)
- OpenGL no uniforme de B-Spline lógica (SPLINEBS)
- SPLINEBS (spline B no uniforme lógica) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1b366571be7a9210576e78540c77970667aca2f37ec8a092de07edb97493d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932775"
---
# <a name="using-nurbs-curves-and-surfaces"></a>Uso de curvas y superficies DE LABS

Las funciones no uniformes de B-Spline lógica (SPLINEBS) proporcionan descripciones generales y eficaces de curvas y superficies en dos y tres dimensiones, lo que convierte las curvas y superficies en evaluadores OpenGL. Las funciones DESEMPBS pueden representar la geometría en muchos sistemas de diseño mecánico asistidos por pc. Pueden representar curvas y superficies en una variedad de estilos, y pueden controlar automáticamente la subdivisión adaptable que tesola el dominio en triángulos más pequeños en regiones de alta curva y bordes cercanos. Las funciones DE LABS se divide en las siguientes categorías.

Para administrar un objeto DEBS, use:

-   [**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (crear un objeto DESANBS)
-   [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (elimina un objeto RGBBS)
-   [*gluNurbsCallback*](glunurbs.md) (establece una función de control de errores)

Para especificar las curvas deseadas, use:

-   [**gluBeginCurve**](glubegincurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndCurve**](gluendcurve.md)

Para especificar las superficies deseadas, use:

-   [**gluBeginSurface**](glubeginsurface.md)
-   [**gluNurbsSurface**](glunurbssurface.md)
-   [**gluEndSurface**](gluendsurface.md)

También puede especificar una región de recorte, que define un subconjunto del dominio de superficie DE LABS que se va a evaluar para que pueda crear superficies que tengan límites suavizados o que contengan huecos.

Para especificar la región de recorte, use:

-   [**gluBeginTrim**](glubegintrim.md)
-   [**gluPwlCurve**](glupwlcurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndTrim**](gluendtrim.md)

Al igual que con los objetos cuádigos, puede controlar cómo se representan las curvas y las superficies DE LABS. Puede determinar:

-   Si se va a descartar una curva o superficie cuyo polihedrón de control se encuentra fuera de la ventanilla actual.
-   Longitud máxima (en píxeles) de los bordes de polígonos usados para representar curvas y superficies.
-   Si va a tomar la matriz de proyección, la matriz modelview y la ventanilla desde el servidor OpenGL o suministrarlos explícitamente [**con gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).

Use [**gluNurbsProperty para**](glunurbsproperty.md) establecer estas propiedades o use los valores predeterminados. Puede consultar un objeto LINQBS sobre su estilo de representación [**con gluGetNurbsProperty**](glugetnurbsproperty.md).

 

 




