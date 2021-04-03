---
title: Trasladar operaciones de píxeles
description: Trasladar operaciones de píxeles
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- Puerto de GL de IRIS, píxeles
- trasladar de IRIS GL, píxeles
- portabilidad a OpenGL desde IRIS GL, píxeles
- Exportación de OpenGL de IRIS GL, píxeles
- píxeles, portabilidad de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fd484efa031bd12af59cb729c8fa20b68fe88e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778043"
---
# <a name="porting-pixel-operations"></a>Trasladar operaciones de píxeles

Al trasladar código que implique operaciones en píxeles, tenga en cuenta los puntos siguientes:

-   Las operaciones de píxeles lógicos no se aplican a los búferes de color RGBA. Para obtener más información, vea [**glLogicOp**](gllogicop.md).
-   En general, IRIS GL usa el formato ABGR para píxeles, mientras que OpenGL usa RGBA. Puede cambiar el formato con [**glPixelStore**](glpixelstore-functions.md).
-   Al migrar funciones de **lrectwrite** , tenga cuidado de tener en cuenta dónde se escribe **lrectwrite** (por ejemplo, podría estar escribiendo en el búfer de profundidad).

OpenGL proporciona una flexibilidad adicional en las operaciones de píxeles. En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para las operaciones de píxeles y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS                                   | Función OpenGL                                                                           | Significado                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| **lrectread**, **rectread**,**readRGB**<br/> | [**glReadPixels**](glreadpixels.md)                                                      | Lee un bloque de píxeles de fotogramas.                           |
| **lrectwrite**, **rectwrite**                      | [**glDrawPixels**](gldrawpixels.md)                                                      | Escribe un bloque de píxeles en el fotogramas.                            |
| **rectcopy**                                       | [**glCopyPixels**](glcopypixels.md)                                                      | Copia píxeles en el fotogramas.                                       |
| **rectzoom**                                       | [**glPixelZoom**](glpixelzoom.md)                                                        | Especifica los factores de zoom de píxel para **glDrawPixels** y **glCopyPixels**. |
| **cmov**                                           | [glRasterPos](glrasterpos-functions.md)                                                  | Especifica la posición de trama para las operaciones de píxeles.                         |
| **readsource**                                     | [**glReadBuffer**](glreadbuffer.md)                                                      | Selecciona un origen de búfer de color para los píxeles.                               |
| **pixmode**                                        | [**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md) | Establece modos de almacenamiento en píxeles. Establecer modos de transferencia de píxeles.                      |
| **logicop**                                        | [**glLogicOp**](gllogicop.md)                                                            | Especifica una operación lógica para escrituras de píxeles.                         |
|                                                    | [**glEnable**](glenable.md) ( \_ OP Logical \_ )                                            | Activa las operaciones de lógica de píxeles.                                        |



 

Para obtener una lista completa de las operaciones lógicas posibles, vea [**glLogicOp**](gllogicop.md).

Este ejemplo de código de GL de IRIS muestra una escritura de píxel típica:

``` syntax
unsigned long *packedRaster; 
.. 
packedRaster[k] = 0x00000000; 
.. 
lrectwrite(0, 0, xSize, ySize, packedRaster);
```

El código anterior tiene este aspecto cuando se traduce a OpenGL:

``` syntax
glRasterPos2i( 0, 0); 
glDrawPixels( xSize + 1, ySize + 1, GL_RGBA, GL_UNSIGNED_BYTE, packedRaster);
```

 

 





