---
title: Uso de evaluadores
description: Uso de evaluadores
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, evaluadores
- evaluadores OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1aef70a7a854e16cf4992d9dd44c4931ad4d044
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361980"
---
# <a name="using-evaluators"></a>Uso de evaluadores

Las funciones del evaluador OpenGL permiten usar una asignación polinómica para generar vértices, normales, coordenadas de textura y colores. A continuación, estos valores calculados se pasan a la canalización de procesamiento como si se hubieran especificado directamente. Las funciones de evaluador también son la base de las funciones DENOMBS (B-Spline no uniformes racionalizadas), que permiten definir curvas y superficies, tal y como se describe en Biblioteca de la utilidad [OpenGL](opengl-utility-library.md).

El primer paso para usar evaluadores es definir la asignación polinómica unidimensional o bidimensional adecuada mediante [**glMap \***](glmap1.md). A continuación, puede especificar y evaluar los valores de dominio de esta asignación de una de estas dos maneras:

-   Defina una serie de valores de dominio espaciados uniformemente que se asignarán mediante [**glMapGrid**](glmapgrid-functions.md) y, a continuación, evalúe un subconjunto rectangular de esa cuadrícula [**con glEvalMesh**](glevalmesh-functions.md). Un único punto de la cuadrícula se puede evaluar mediante [**glEvalPoint**](glevalpoint.md).
-   Especifique explícitamente un valor de dominio deseado como argumento, que evalúa los mapas en ese valor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de evaluadores](evaluators-reference.md)
</dt> </dl>

 

 




