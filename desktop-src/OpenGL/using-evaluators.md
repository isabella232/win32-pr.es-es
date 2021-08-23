---
title: Uso de evaluadores
description: Uso de evaluadores
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, evaluadores
- evaluadores OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4bb6808ad1898b0c98906a543291c700ee61257a35befa8886789f3f8b7e31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553495"
---
# <a name="using-evaluators"></a>Uso de evaluadores

Las funciones del evaluador OpenGL permiten usar una asignación polinómica para generar vértices, normales, coordenadas de textura y colores. Estos valores calculados se pasan a la canalización de procesamiento como si se hubieran especificado directamente. Las funciones de evaluador también son la base de las funciones DE LABS (B-Spline no uniformes), que permiten definir curvas y superficies, como se describe en Biblioteca de la utilidad [OpenGL](opengl-utility-library.md).

El primer paso para usar evaluadores es definir la asignación polinómica unidimensional o bidimensional adecuada mediante [**glMap \***](glmap1.md). A continuación, puede especificar y evaluar los valores de dominio para este mapa de una de estas dos maneras:

-   Defina una serie de valores de dominio espaciados uniformemente que se asignarán mediante [**glMapGrid**](glmapgrid-functions.md) y, a continuación, evalúe un subconjunto rectangular de esa cuadrícula [**con glEvalMesh**](glevalmesh-functions.md). Un único punto de la cuadrícula se puede evaluar mediante [**glEvalPoint**](glevalpoint.md).
-   Especifique explícitamente un valor de dominio deseado como argumento, que evalúa los mapas en ese valor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de evaluadores](evaluators-reference.md)
</dt> </dl>

 

 




