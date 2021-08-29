---
title: Porte de arcos y círculos
description: Con OpenGL, los arcos y círculos rellenos se dibujan con las mismas llamadas que los arcos y círculos sin rellenar. En la tabla siguiente se enumeran las funciones de arco y círculo IRIS GL y sus funciones equivalentes de OpenGL (GLU).
ms.assetid: b3458192-9cb6-4376-8136-45467584d3d4
keywords:
- Porte de IRIS GL, arcos
- porting from IRIS GL,arcs
- porte a OpenGL desde IRIS GL,arcs
- Porte de OpenGL desde IRIS GL,arcs
- funciones de dibujo, arcos
- Porte de IRIS GL, círculos
- porting from IRIS GL,circles
- porte a OpenGL desde IRIS GL, círculos
- Porte de OpenGL desde IRIS GL, círculos
- funciones de dibujo, círculos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72298caac6495d39c8a5d6cf7441b3b3664180d9e5396fb22106d9e138019b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936224"
---
# <a name="porting-arcs-and-circles"></a>Porte de arcos y círculos

Con OpenGL, los arcos y círculos rellenos se dibujan con las mismas llamadas que los arcos y círculos sin rellenar. En la tabla siguiente se enumeran las funciones de arco y círculo IRIS GL y sus funciones equivalentes de OpenGL (GLU).



| Función GL de IRIS | Función OpenGL                          | Significado                 |
|------------------|------------------------------------------|-------------------------|
| **arcarcf**      | [**gluPartialDisk**](glupartialdisk.md) | Dibuja un arco.           |
| **circcircf**    | [**gluDisk**](gludisk.md)               | Dibuja un círculo o disco. |



 

Puede hacer algunas cosas con arcos y círculos OpenGL que no puede hacer con IRIS GL. OpenGL llama a arcos y círculos, discos y discos parciales, respectivamente.

Al portear arcos y círculos, tenga en cuenta los siguientes puntos sobre OpenGL:

-   Los ángulos se miden en grados y no en décimas de grados.
-   El ángulo inicial se mide desde el eje Y positivo y no desde el eje X.
-   El ángulo de barrido ahora es en el sentido de las agujas del reloj en lugar de en sentido contrario a las agujas del reloj.

??

 

 




