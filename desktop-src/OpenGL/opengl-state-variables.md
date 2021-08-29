---
title: Variables de estado openGL
description: En los temas siguientes se incluyen los nombres de las variables de estado que se pueden consultar.
ms.assetid: f4bc4ec1-a529-4b9e-84af-94caa0ef7131
keywords:
- Variables de estado OpenGL
- variables de estado, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8164cebd065a69f923e908a26bf2ce80357312c73c35f12bc2066c63db91eff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936774"
---
# <a name="opengl-state-variables"></a>Variables de estado openGL

En los temas siguientes se incluyen los nombres de las variables de estado que se pueden consultar:

-   [**Variables de estado para los valores actuales y los datos asociados**](state-variables-for-current-values-and-associated-data.md)
-   [**Variables de estado de la transformación**](transformation-state-variables.md)
-   [**Variables de estado de la opción de coloreado**](coloring-state-variables.md)
-   [**Variables de estado de la opción de iluminación**](lighting-state-variables.md)
-   [**Variables de estado de la rasterización**](rasterization-state-variables.md)
-   [**Variables de estado de la opción de texturas**](texturing-state-variables.md)
-   [**Operaciones de píxeles**](pixel-operations.md)
-   [**Variables de estado del control del buffer de fotogramas**](framebuffer-control-state-variables.md)
-   [**Variables de estado de píxeles**](pixel-state-variables.md)
-   [**Variables de estado del evaluador**](evaluator-state-variables.md)
-   [**Variables de estado de sugerencias**](hint-state-variables.md)
-   [**Variables de estado dependientes de la implementación**](implementation-dependent-state-variables.md)
-   [**Variables de estado de profundidad de píxeles dependientes de la implementación**](implementation-dependent-pixel-depth-state-variables.md)
-   [**Variables de estado varias**](miscellaneous-state-variables.md)

Para cada variable, el tema muestra una descripción, un grupo de atributos, un valor inicial o mínimo, y la función [**glGet \***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) sugerida que se usará para obtenerla.

Las variables de estado que puede obtener mediante [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md)o [**glGetDoublev**](glgetdoublev.md) se enumeran con una sola de estas funciones, la más adecuada para el tipo de datos que se va a devolver. No se pueden obtener estas variables de estado [**mediante glIsEnabled.**](glisenabled.md) Sin embargo, puede obtener variables de estado para las que **glIsEnabled** aparece como la función de consulta **con glGetBooleanv**, **glGetIntegerv**, **glGetFloatv** y **glGetDoublev**. Puede obtener variables de estado para las que cualquier otra función se muestra como función de consulta solo mediante esa función. Si no aparece ningún grupo de atributos, la variable no pertenece a ningún grupo. Todas las variables de estado que se pueden consultar, excepto las que dependen de la implementación, tienen valores iniciales. Para determinar el valor inicial de una variable para la que no se muestra ningún valor inicial, vea la referencia de esa variable o el

*Manual de referencia de OpenGL.*

 

 




