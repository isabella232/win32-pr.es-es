---
title: Porte de llamadas de color
description: En la tabla siguiente se enumeran las funciones de color DE IRIS GL y sus funciones openGL equivalentes.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- Porte de IRIS GL, color
- porting from IRIS GL,color
- porting to OpenGL from IRIS GL,color
- Porte de OpenGL desde IRIS GL, color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856b9f9d0a62b866ac1c9981d9fbb716cf243341
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169201"
---
# <a name="porting-color-calls"></a>Porte de llamadas de color

En la tabla siguiente se enumeran las funciones de color DE IRIS GL y sus funciones openGL equivalentes.



| Función IRIS GL                  | Función OpenGL                                                                                                                               | Significado                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **c**                             | [glColor](glcolor-functions.md)                                                                                                              | Establece el color RGB.                                      |
| **color**                         | [glIndex](glindex-functions.md)                                                                                                              | Establece el índice de color.                                |
| **getcolor**                      | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ CURRENT \_ INDEX )                                               | Devuelve el índice de color actual.                     |
| **getmcolor**                     |                                                                                                                                               | Obtiene una copia de los valores RGB de una entrada de mapa de colores. |
| **gRGBcolor**                     | **glGet**( GL \_ CURRENT \_ COLOR )                                                                                                               | Obtiene los valores de color RGB actuales.                   |
| **mapcolor**                      |                                                                                                                                               |                                                      |
| **Rgbcolor**                      | **glColor**                                                                                                                                   | Establece el color RGB.                                      |
| **máscara de escritura**                     | [**glIndexMask**](glindexmask.md)                                                                                                            | Establece la máscara de color del modo de índice de color.                |
| **wmpackRGBwritemask**<br/> | [**glColorMask**](glcolormask.md)                                                                                                            | Establece la máscara del modo de color RGB.                        |
| **getwritemask**                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ COLOR \_ WRITEMASK )**glGet**( GL \_ INDEX \_ WRITEMASK )<br/> | Obtiene la máscara de color.                                 |
| **máscara gRGB**                      | **glGet**( GL \_ COLOR \_ WRITEMASK )                                                                                                             | Obtiene la máscara de color.                                 |
| **zwritemask**                    | [**glDepthMask**](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> Tenga cuidado al reemplazar **zwritemask** por [**glDepthMask**](gldepthmask.md); **glDepthMask toma** un argumento booleano, mientras que **zwritemask** toma un campo de bits.

 

Si desea usar varios mapas de color, debe usar las funciones de asignación de colores adecuadas Windows mapa de colores. Por lo **tanto, multimap**, **onemap,** **getcmmode,** **setmap** y **getmap** no tienen equivalentes openGL.

 

 





