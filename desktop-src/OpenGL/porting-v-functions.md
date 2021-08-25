---
title: Porting v Functions
description: En IRIS GL, se usan variaciones en la función v para especificar vértices. La función OpenGL equivalente es glVertex Below son ejemplos de glVertex.
ms.assetid: b4ac0c41-983a-4387-a69f-530c9094dc33
keywords:
- Porte de IRIS GL, vértices
- porte desde IRIS GL, vértices
- porte a OpenGL desde IRIS GL, vértices
- Porte de OpenGL desde IRIS GL, vértices
- funciones de dibujo, vértices
- vértices, porte desde IRIS GL
- Porte de IRIS GL, funciones v
- porte de funciones GL,v de IRIS
- porte a OpenGL desde IRIS GL,v functions
- Porte de OpenGL desde IRIS GL, funciones v
- funciones de dibujo, funciones v
- Funciones de v
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e84fd5eb036afaf5291902ab00f91f3b155f7507d8fce7135dc8030323c1a05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888075"
---
# <a name="porting-v-functions"></a>Porting v Functions

En IRIS GL, se usan variaciones en la **función v** para especificar vértices. La función OpenGL equivalente es [glVertex:](glvertex-functions.md)a continuación se muestran ejemplos de **glVertex**.

``` syntax
glVertex2[d|f|i|s][v]( x, y ); 
glVertex3[d|f|i|s][v]( x, y, z); 
glVertex4[d|f|i|s][v]( x, y, z, w);
```

La **función glVertex** toma sufijos del mismo modo que otras llamadas OpenGL. Las versiones vectoriales de la llamada toman matrices del tamaño adecuado como argumentos. En la versión 2D, z=0 y w=1. En la versión 3D, w=1.

 

 




