---
title: Trasladar comandos de borrado de pantalla y de búfer
description: OpenGL reemplaza una variedad de funciones claras de la contabilidad de IRIS (como zclear, aclear, sclear, etc.) con una sola función, glClear. Especifique exactamente lo que desea borrar pasando las máscaras a glClear.
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- Migración de la contabilidad de IRIS, borrar funciones
- portabilidad desde IRIS GL, borrar funciones
- trasladar a OpenGL desde IRIS GL, borrar funciones
- Exportación de OpenGL desde IRIS GL, borrar funciones
- borrar funciones
- Migración de la contabilidad de IRIS, comandos de borrado de pantalla
- portabilidad desde IRIS GL, comandos de borrado de pantalla
- trasladar a OpenGL desde IRIS GL, comandos de borrado de pantalla
- Exportación de OpenGL desde IRIS GL, comandos de borrado de pantalla
- comandos de borrado de pantalla
- Migración de la contabilidad de IRIS, comandos de borrado de búfer
- portabilidad desde IRIS GL, comandos de borrado de búfer
- trasladar a OpenGL desde IRIS GL, comandos de borrado de búfer
- Exportación de OpenGL desde IRIS GL, comandos de borrado de búfer
- comandos de borrado de búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53566c9fe14922f3965133cef9e30cbea4548b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665689"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a>Trasladar comandos de borrado de pantalla y de búfer

OpenGL reemplaza una variedad de funciones **claras** de la contabilidad de iris (como **zclear**, **aclear**, **sclear**, etc.) con una sola función, [**glClear**](glclear.md). Especifique exactamente lo que desea borrar pasando las máscaras a **glClear**.

Tenga en cuenta los siguientes puntos al trasladar comandos de pantalla y de búfer:

-   OpenGL mantiene los colores de borrado por separado de los colores de dibujo, con llamadas como [**glClearColor**](glclearcolor.md) y [**glClearIndex**](glclearindex.md). Asegúrese de establecer el color Clear para cada búfer antes de borrarlo.
-   En lugar de usar una de varias llamadas claras con un nombre diferente, ahora se borran varios búferes con una llamada, [**glClear**](glclear.md), y se agrupan las **máscaras de búfer** . Por ejemplo, **czclear** se reemplaza por:

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   IRIS GL hace referencia al punteado de polígono y al color writemask. OpenGL omite el punteado de polígono, pero hace referencia al color writemask. (La función **czclear** omite los dos elementos de polígono y writemask de color).

En la tabla siguiente se enumeran las distintas funciones Clear GL de IRIS con sus funciones de OpenGL equivalentes.



| Llamada de GL de IRIS         | Llamada de OpenGL                                                               | Significado                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| **acbuf**(AC \_ claro) | **glClear**(bit de búfer de la acumulación de GL \_ \_ \_ )                                     | Borre el búfer de acumulación.                    |
|                      | **glClearColor**                                                          | Establezca el color libre de RGBA.                         |
|                      | **glClearIndex**                                                          | Establezca el índice de color claro.                        |
| **clear**            | **glClear**(bit de búfer de color de contabilidad \_ \_ \_ )                                     | Borre el búfer de color.                           |
|                      | **glClearDepth**                                                          | Especifique el valor sin cifrar para el búfer de profundidad.     |
| **zclear**           | **glClear**(bit de búfer de profundidad de contabilidad \_ \_ \_ )                                     | Borre el búfer de profundidad.                           |
| **czclear**          | **glClear**(bit de búfer de \_ \_ \_ \| \_ profundidad \_ \_ del búfer de color de GL)<br/> | Borre el búfer de color y el búfer de profundidad.      |
|                      | **glClearAccum**                                                          | Especifique los valores claros para el búfer de acumulación. |
|                      | **glClearStencil**                                                        | Especifique el valor sin cifrar para el búfer de estarcido.   |
| **sclear**           | **glClear**(bit de búfer de estarcido de GL \_ \_ \_ )                                   | Borrar el búfer de estarcido.                         |



 

Cuando el código de la contabilidad de IRIS usa **gclear** y **sclear**, puede combinarlos en una sola llamada a **glClear** ; puede mejorar el rendimiento del programa.

 

 





