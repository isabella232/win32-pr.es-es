---
title: Variables de estado de OpenGL
description: En los temas siguientes se enumeran los nombres de las variables de estado que se pueden consultar
ms.assetid: f4bc4ec1-a529-4b9e-84af-94caa0ef7131
keywords:
- Variables de estado de OpenGL
- variables de estado, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36dee51ba7726277832d94eaf336d03d3c579189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665652"
---
# <a name="opengl-state-variables"></a>Variables de estado de OpenGL

En los temas siguientes se enumeran los nombres de las variables de estado que se pueden consultar:

-   [**Variables de estado para los valores actuales y los datos asociados**](state-variables-for-current-values-and-associated-data.md)
-   [**Variables de estado de transformación**](transformation-state-variables.md)
-   [**Colorear variables de estado**](coloring-state-variables.md)
-   [**Variables de estado de iluminación**](lighting-state-variables.md)
-   [**Variables de estado de rasterización**](rasterization-state-variables.md)
-   [**Variables de estado de texturización**](texturing-state-variables.md)
-   [**Operaciones de píxeles**](pixel-operations.md)
-   [**Variables de estado del control fotogramas**](framebuffer-control-state-variables.md)
-   [**Variables de estado de píxeles**](pixel-state-variables.md)
-   [**Variables de estado del evaluador**](evaluator-state-variables.md)
-   [**Variables de estado de sugerencia**](hint-state-variables.md)
-   [**Variables de estado dependiente de la implementación**](implementation-dependent-state-variables.md)
-   [**Variables de estado de Pixel-Depth dependiente de la implementación**](implementation-dependent-pixel-depth-state-variables.md)
-   [**Variables de estado misceláneas**](miscellaneous-state-variables.md)

Para cada variable, en el tema se muestra una descripción, un grupo de atributos, un valor inicial o mínimo y la función [**glGet \***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) sugerida que se va a usar para obtenerlo.

Las variables de estado que puede obtener con [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md)o [**glGetDoublev**](glgetdoublev.md) se enumeran solo con uno de estos functionsthe, que es más adecuado para el tipo de datos que se va a devolver. No se pueden obtener estas variables de estado mediante [**glIsEnabled**](glisenabled.md). Sin embargo, puede obtener las variables de estado para las que **glIsEnabled** aparece como la función de consulta con **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv** y **glGetDoublev**. Puede obtener las variables de estado para las que cualquier otra función aparece como la función de consulta solo mediante esa función. Si no aparece ningún grupo de atributos, la variable no pertenece a ningún grupo. Todas las variables de estado que puede consultar, excepto las que dependen de la implementación, tienen valores iniciales. Para determinar el valor inicial de una variable para la que no aparece ningún valor inicial, vea la referencia de la variable o el

*Manual de referencia de OpenGL*.

 

 




