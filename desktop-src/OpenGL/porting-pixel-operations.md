---
title: Porting Pixel Operations
description: Porting Pixel Operations
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- Porte de IRIS GL, píxeles
- porting from IRIS GL,pixels
- porte a OpenGL desde IRIS GL, píxeles
- Porte de OpenGL desde IRIS GL, píxeles
- pixels,porting de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fd484efa031bd12af59cb729c8fa20b68fe88e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074000"
---
# <a name="porting-pixel-operations"></a>Porting Pixel Operations

Al portear código que implica operaciones de píxeles, tenga en cuenta los siguientes puntos:

-   Las operaciones de píxel lógico no se aplican a los búferes de color RGBA. Para obtener más información, [**vea glLogicOp**](gllogicop.md).
-   En general, IRIS GL usa el formato ABGR para píxeles, mientras que OpenGL usa RGBA. Puede cambiar el formato con [**glPixelStore.**](glpixelstore-functions.md)
-   Al **portear funciones lrectwrite,** tenga cuidado de tener en cuenta dónde está escribiendo **lrectwrite** (por ejemplo, podría estar escribiendo en el búfer de profundidad).

OpenGL proporciona cierta flexibilidad adicional en las operaciones de píxeles. En la tabla siguiente se enumeran las funciones GL de IRIS para las operaciones de píxeles y sus funciones OpenGL equivalentes.



| Función IRIS GL                                   | Función OpenGL                                                                           | Significado                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| **lrectread,** **rectread,****readRGB**<br/> | [**glReadPixels**](glreadpixels.md)                                                      | Lee un bloque de píxeles del búfer de fotogramas.                           |
| **lrectwrite**, **rectwrite**                      | [**glDrawPixels**](gldrawpixels.md)                                                      | Escribe un bloque de píxeles en el búfer de fotogramas.                            |
| **rectcopy**                                       | [**glCopyPixels**](glcopypixels.md)                                                      | Copia píxeles en el búfer de fotogramas.                                       |
| **rectzoom**                                       | [**glPixelZoom**](glpixelzoom.md)                                                        | Especifica los factores de zoom de píxeles **para glDrawPixels** **y glCopyPixels.** |
| **cmov**                                           | [glRasterPos](glrasterpos-functions.md)                                                  | Especifica la posición de trama para las operaciones de píxeles.                         |
| **origen de lectura**                                     | [**glReadBuffer**](glreadbuffer.md)                                                      | Selecciona un origen de búfer de color para píxeles.                               |
| **modemode**                                        | [**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md) | Establece los modos de almacenamiento de píxeles. Establecer modos de transferencia de píxeles.                      |
| **logicop**                                        | [**glLogicOp**](gllogicop.md)                                                            | Especifica una operación lógica para escrituras de píxeles.                         |
|                                                    | [**glEnable**](glenable.md) ( GL \_ LOGIC \_ OP )                                            | Activa las operaciones lógicas de píxeles.                                        |



 

Para obtener una lista completa de las posibles operaciones lógicas, [**vea glLogicOp**](gllogicop.md).

En este ejemplo de código de IRIS GL se muestra una escritura típica de píxeles:

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

 

 





