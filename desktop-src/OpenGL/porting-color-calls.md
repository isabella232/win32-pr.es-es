---
title: Trasladar llamadas de color
description: En la tabla siguiente se enumeran las funciones de color de GL de IRIS y sus funciones de OpenGL equivalentes.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- Puerto de GL de IRIS, color
- portabilidad de IRIS GL, color
- trasladar a OpenGL desde IRIS GL, color
- Exportación de OpenGL desde IRIS GL, color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856b9f9d0a62b866ac1c9981d9fbb716cf243341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773999"
---
# <a name="porting-color-calls"></a>Trasladar llamadas de color

En la tabla siguiente se enumeran las funciones de color de GL de IRIS y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS                  | Función OpenGL                                                                                                                               | Significado                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **c**                             | [glColor](glcolor-functions.md)                                                                                                              | Establece el color RGB.                                      |
| **color**                         | [glIndex](glindex-functions.md)                                                                                                              | Establece el índice de color.                                |
| **GetColor**                      | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ índice actual de contabilidad \_ )                                               | Devuelve el índice de color actual.                     |
| **getmcolor**                     |                                                                                                                                               | Obtiene una copia de los valores RGB para una entrada de mapa de color. |
| **gRGBcolor**                     | **glGet**( \_ color actual de GL \_ )                                                                                                               | Obtiene los valores de color RGB actuales.                   |
| **mapcolor**                      |                                                                                                                                               |                                                      |
| **RGBcolor**                      | **glColor**                                                                                                                                   | Establece el color RGB.                                      |
| **writemask**                     | [**glIndexMask**](glindexmask.md)                                                                                                            | Establece la máscara de color del modo de índice de color.                |
| **wmpackRGBwritemask**<br/> | [**glColorMask**](glcolormask.md)                                                                                                            | Establece la máscara del modo de color RGB.                        |
| **getwritemask**                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL \_ color \_ WRITEMASK)**glGet**(GL \_ index \_ WRITEMASK)<br/> | Obtiene la máscara de color.                                 |
| **gRGBmask**                      | **glGet**(GL \_ color \_ WRITEMASK)                                                                                                             | Obtiene la máscara de color.                                 |
| **zwritemask**                    | [**glDepthMask**](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> Tenga cuidado al sustituir **zwritemask** por [**glDepthMask**](gldepthmask.md); **glDepthMask** toma un argumento booleano, mientras que **zwritemask** toma un campo de bits.

 

Si desea usar varias asignaciones de color, debe usar las funciones de mapa de colores de Windows adecuadas. Por lo tanto, **Multimap**, **onemap**, **getcmmode**, **setmap** y **GetMap** no tienen equivalentes de OpenGL.

 

 





