---
title: Porte de líneas
description: La portar código GL de IRIS que dibuja líneas es bastante sencilla, aunque debe tener en cuenta las diferencias en la forma en que OpenGL se enfrenta. En la tabla siguiente se enumeran las funciones GL de IRIS para dibujar líneas y sus funciones OpenGL equivalentes.
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- Porte de IRIS GL, líneas
- porting from IRIS GL,lines
- porting to OpenGL from IRIS GL,lines
- Porte de OpenGL desde IRIS GL, líneas
- funciones de dibujo, líneas
- lines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8b0dd0e254380e65171acef1a536038532a370da85ffaa361e8555f77457424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776965"
---
# <a name="porting-lines"></a>Porte de líneas

La portar código GL de IRIS que dibuja líneas es bastante sencilla, aunque debe tener en cuenta las diferencias en la forma en que OpenGL se enfrenta. En la tabla siguiente se enumeran las funciones GL de IRIS para dibujar líneas y sus funciones OpenGL equivalentes.



| Función IRIS GL                               | Función OpenGL                                                                                         | Significado                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **bgnclosedline**,**endclosedline**<br/> | [**glBegin**](glbegin.md) ( GL \_ LINE LOOP ) \_ [**glEnd**](glend.md)<br/>                          | Dibuja una línea cerrada.                                                                                                                         |
| **bgnline**                                    | [**glBegin**](glbegin.md) ( GL \_ LINE \_ STRIP )                                                          | Dibuja segmentos de línea.                                                                                                                         |
| **linewidth**                                  | [**glLineWidth**](gllinewidth.md)                                                                      | Establece el ancho de línea.                                                                                                                             |
| **getlwidth**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ LINE \_ WIDTH )            | Devuelve el ancho de línea actual.                                                                                                                  |
| **deflinestyle**,**setlinestyle**<br/>   | [**glLineStipple**](gllinestipple.md)                                                                  | Especifica un patrón detipplado de línea.                                                                                                            |
| **lsrepeat**                                   | argumento factor de **glLineStipple**                                                                    | Establece un factor de repetición para el estilo de línea.                                                                                                     |
| **getlstyle**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ LINE \_ STIPPLE \_ PATTERN ) | Devuelve el patrón de stipple de línea.                                                                                                                |
| **getlsrepeat**                                | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ LINE \_ STIPPLE \_ REPEAT )  | Devuelve el factor repeat.                                                                                                                       |
| **linesmooth**, **smoothline**                 | [**glEnable**](glenable.md) ( GL \_ LINE \_ SMOOTH )                                                       | Activa el suavizado de contorno de línea (para obtener más información sobre el suavizado de contorno, vea [Porting Antialiasing Functions [Porting Antialiasing Functions]).](porting-antialiasing-functions.md) |



 

OpenGL no usa tablas para timos de línea; solo mantiene un patrón de información sobre líneas. Puede usar [**glPushAttrib y**](glpushattrib.md) [**glPopAttrib**](glpopattrib.md) para cambiar entre diferentes patrones detippla.

OpenGL no admite funciones de estilo de línea de IRIS GL anteriores (como **draw,** **lsbackup,** **getlsbackup,** entre otras).

Para obtener información sobre cómo dibujar líneas con suavizado de contorno, [vea Porting Antialiasing Functions](porting-antialiasing-functions.md).

??

 

 





