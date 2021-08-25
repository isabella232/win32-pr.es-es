---
title: Porte de llamadas de color
description: En la tabla siguiente se enumeran las funciones de color IRIS GL y sus funciones OpenGL equivalentes.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- Porte de IRIS GL, color
- porting from IRIS GL,color
- porte a OpenGL desde IRIS GL, color
- Porte de OpenGL desde IRIS GL, color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e15774f66964c11527955b57651e69db26f6f3d3704d114fdfa4de9a0d5b97c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777055"
---
# <a name="porting-color-calls"></a>Porte de llamadas de color

En la tabla siguiente se enumeran las funciones de color IRIS GL y sus funciones OpenGL equivalentes.



| Función GL de IRIS                  | Función OpenGL                                                                                                                               | Significado                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **c**                             | [glColor](glcolor-functions.md)                                                                                                              | Establece el color RGB.                                      |
| **color**                         | [glIndex](glindex-functions.md)                                                                                                              | Establece el índice de color.                                |
| **getcolor**                      | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ CURRENT \_ INDEX )                                               | Devuelve el índice de color actual.                     |
| **getmcolor**                     |                                                                                                                                               | Obtiene una copia de los valores RGB de una entrada de mapa de colores. |
| **gRGBcolor**                     | **glGet**( GL \_ CURRENT \_ COLOR )                                                                                                               | Obtiene los valores de color RGB actuales.                   |
| **mapcolor**                      |                                                                                                                                               |                                                      |
| **Rgbcolor**                      | **glColor**                                                                                                                                   | Establece el color RGB.                                      |
| **writemask**                     | [**glIndexMask**](glindexmask.md)                                                                                                            | Establece la máscara de color del modo de índice de color.                |
| **wmpackRGBwritemask**<br/> | [**glColorMask**](glcolormask.md)                                                                                                            | Establece la máscara de modo de color RGB.                        |
| **getwritemask**                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ COLOR \_ WRITEMASK )**glGet**( GL \_ INDEX \_ WRITEMASK )<br/> | Obtiene la máscara de color.                                 |
| **máscara gRGB**                      | **glGet**( GL \_ COLOR \_ WRITEMASK )                                                                                                             | Obtiene la máscara de color.                                 |
| **zwritemask**                    | [**glDepthMask**](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> Tenga cuidado al reemplazar **zwritemask** por [**glDepthMask**](gldepthmask.md); **glDepthMask toma** un argumento booleano, mientras que **zwritemask** toma un campo de bits.

 

Si desea usar varias asignaciones de colores, debe usar las funciones de mapa de colores Windows de colores adecuadas. Por lo **tanto, multimap**, **onemap**, **getcmmode,** **setmap** y **getmap** no tienen equivalentes openGL.

 

 





