---
title: Trasladar líneas
description: Trasladar el código de GL de IRIS que dibuja las líneas es bastante sencillo, aunque debe tener en cuenta las diferencias en la forma en que se puntea en OpenGL. En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para dibujar líneas y sus funciones de OpenGL equivalentes.
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- Puertos de GL de IRIS, líneas
- trasladar de IRIS GL, líneas
- trasladar a OpenGL desde el GL de IRIS, líneas
- Exportación de OpenGL desde IRIS GL, líneas
- dibujar funciones, líneas
- lines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c97593d0230d6830cf3d3ce8fa2c13466e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269166"
---
# <a name="porting-lines"></a>Trasladar líneas

Trasladar el código de GL de IRIS que dibuja las líneas es bastante sencillo, aunque debe tener en cuenta las diferencias en la forma en que se puntea en OpenGL. En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para dibujar líneas y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS                               | Función OpenGL                                                                                         | Significado                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **bgnclosedline**,**endclosedline**<br/> | [**glBegin**](glbegin.md) (bucle de línea de contabilidad \_ \_ )[**glEnd**](glend.md)<br/>                          | Dibuja una línea cerrada.                                                                                                                         |
| **bgnline**                                    | [**glBegin**](glbegin.md) (franja de línea de contabilidad \_ \_ )                                                          | Dibuja segmentos de línea.                                                                                                                         |
| **linewidth**                                  | [**glLineWidth**](gllinewidth.md)                                                                      | Establece el ancho de línea.                                                                                                                             |
| **getlwidth**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (ancho de línea de contabilidad \_ \_ )            | Devuelve el ancho de línea actual.                                                                                                                  |
| **deflinestyle**,**setlinestyle**<br/>   | [**glLineStipple**](gllinestipple.md)                                                                  | Especifica un patrón punteado de línea.                                                                                                            |
| **lsrepeat**                                   | argumento factor de **glLineStipple**                                                                    | Establece un factor de repetición para el estilo de línea.                                                                                                     |
| **getlstyle**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ \_ patrón punteado de línea de contabilidad \_ ) | Devuelve el patrón punteado de línea.                                                                                                                |
| **getlsrepeat**                                | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (repetición de línea de contabilidad \_ \_ punteada \_ )  | Devuelve el factor de repetición.                                                                                                                       |
| **linesmooth**, **smoothline**                 | [**glEnable**](glenable.md) (línea de contabilidad \_ \_ suave)                                                       | Activa el suavizado de contorno de línea (para obtener más información sobre el suavizado de contorno, consulte [portabilidad de las funciones de suavizado](porting-antialiasing-functions.md)de contorno). |



 

OpenGL no utiliza tablas para las líneas punteadas; mantiene solo un patrón de línea-punteado. Puede usar [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md) para cambiar entre distintos patrones de punteado.

OpenGL no admite las funciones de estilo de línea de la contabilidad de IRIS anterior (como **Draw**, **LSBackup**, **getlsbackup**, etc.).

Para obtener información sobre cómo dibujar líneas con suavizado de contorno, consulte [portabilidad de las funciones de suavizado de contorno](porting-antialiasing-functions.md).

??

 

 





