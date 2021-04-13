---
title: Usar evaluadores
description: Usar evaluadores
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, evaluadores
- los evaluadores OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1aef70a7a854e16cf4992d9dd44c4931ad4d044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356904"
---
# <a name="using-evaluators"></a>Usar evaluadores

Las funciones del evaluador de OpenGL permiten usar una asignación polinómica para generar vértices, normales, coordenadas de textura y colores. Después, estos valores calculados se pasan a la canalización de procesamiento como si hubieran sido especificados directamente. Las funciones del evaluador también son la base de las funciones de NURBS (no uniforme B-spline racional), que permiten definir curvas y superficies, tal y como se describe en [biblioteca de utilidades de OpenGL](opengl-utility-library.md).

El primer paso en el uso de evaluadores es definir la asignación polinómica de una o dos dimensiones adecuada [**mediante \* glMap**](glmap1.md). Después, puede especificar y evaluar los valores de dominio para esta asignación de una de estas dos maneras:

-   Defina una serie de valores de dominio equidistantemente espaciados que se van a asignar mediante [**glMapGrid**](glmapgrid-functions.md) y, a continuación, evalúe un subconjunto rectangular de esa cuadrícula con [**glEvalMesh**](glevalmesh-functions.md). Se puede evaluar un solo punto de la cuadrícula mediante [**glEvalPoint**](glevalpoint.md).
-   Especifique explícitamente un valor de dominio deseado como argumento, que evalúa las asignaciones en ese valor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de evaluadores](evaluators-reference.md)
</dt> </dl>

 

 




