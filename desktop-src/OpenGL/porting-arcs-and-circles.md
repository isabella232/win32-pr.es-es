---
title: Trasladar arcos y círculos
description: Con OpenGL, los arcos y los círculos rellenos se dibujan con las mismas llamadas que los arcos y círculos sin rellenar. En la tabla siguiente se enumeran las funciones de arco y círculo de la contabilidad de IRIS y sus funciones de OpenGL (GLU) equivalentes.
ms.assetid: b3458192-9cb6-4376-8136-45467584d3d4
keywords:
- Migración de la contabilidad de IRIS, arcos
- portabilidad de IRIS GL, arcos
- trasladar a OpenGL desde IRIS GL, arcos
- Exportación de OpenGL desde IRIS GL, arcos
- funciones de dibujo, arcos
- Migración de la contabilidad de IRIS, círculos
- portabilidad de IRIS GL, círculos
- trasladar a OpenGL desde IRIS GL, círculos
- Exportación de OpenGL desde IRIS GL, círculos
- dibujar funciones, círculos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce17546ce17f24adf80641549d8843a473c8754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419127"
---
# <a name="porting-arcs-and-circles"></a>Trasladar arcos y círculos

Con OpenGL, los arcos y los círculos rellenos se dibujan con las mismas llamadas que los arcos y círculos sin rellenar. En la tabla siguiente se enumeran las funciones de arco y círculo de la contabilidad de IRIS y sus funciones de OpenGL (GLU) equivalentes.



| Función de GL de IRIS | Función OpenGL                          | Significado                 |
|------------------|------------------------------------------|-------------------------|
| **arcarcf**      | [**gluPartialDisk**](glupartialdisk.md) | Dibuja un arco.           |
| **circcircf**    | [**gluDisk**](gludisk.md)               | Dibuja un círculo o un disco. |



 

Puede hacer algunas cosas con los arcos de OpenGL y los círculos que no se pueden realizar con la contabilidad de IRIS. OpenGL llama a arcos y círculos, discos y discos parciales, respectivamente.

Al migrar arcos y círculos, tenga en cuenta los siguientes puntos sobre OpenGL:

-   Los ángulos se miden en grados y no en décimas de grado.
-   El ángulo inicial se mide desde el eje y positivo y no desde el eje x.
-   El ángulo de barrido es ahora en lugar de las agujas del reloj.

??

 

 




