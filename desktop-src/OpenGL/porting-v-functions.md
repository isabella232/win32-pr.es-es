---
title: Portabilidad de funciones de v
description: En IRIS GL, se usan variaciones en la función v para especificar vértices. La función de OpenGL equivalente se glVertex a continuación son ejemplos de glVertex.
ms.assetid: b4ac0c41-983a-4387-a69f-530c9094dc33
keywords:
- Migración de la contabilidad de IRIS, vértices
- trasladar de IRIS GL, vértices
- trasladar a OpenGL desde IRIS GL, vértices
- Exportación de OpenGL desde IRIS GL, vértices
- dibujar funciones, vértices
- vértices, portabilidad de IRIS GL
- Migración de GL de IRIS, funciones de v
- trasladar de IRIS GL, funciones de v
- trasladar a OpenGL desde IRIS GL, funciones de v
- Exportación de OpenGL desde IRIS GL, funciones de v
- funciones de dibujo, funciones de v
- funciones de v
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd5e40915f891817606ac8517c0b3b980b436be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356958"
---
# <a name="porting-v-functions"></a>Portabilidad de funciones de v

En IRIS GL, se usan variaciones en la función **v** para especificar vértices. La función de OpenGL equivalente es [glVertex](glvertex-functions.md): a continuación se muestran ejemplos de **glVertex**.

``` syntax
glVertex2[d|f|i|s][v]( x, y ); 
glVertex3[d|f|i|s][v]( x, y, z); 
glVertex4[d|f|i|s][v]( x, y, z, w);
```

La función **glVertex** toma los sufijos de la misma manera que otras llamadas OpenGL. Las versiones de vector de la llamada toman matrices del tamaño adecuado como argumentos. En la versión 2-D, z = 0 y w = 1. En la versión 3D, w = 1.

 

 




