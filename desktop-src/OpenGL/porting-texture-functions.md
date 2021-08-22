---
title: Porte de funciones de textura
description: Porte de funciones de textura
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- Porte de IRIS GL, textura
- porting from IRIS GL,texture
- porte a OpenGL desde IRIS GL, textura
- Porte de OpenGL desde IRIS GL, textura
- textura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17cd79aaf8e7e5b90d0f171ddcec4b49b6d15b3615ccc1f5e44a04b3e16fae9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339245"
---
# <a name="porting-texture-functions"></a>Porte de funciones de textura

Al porte las funciones de textura de IRIS GL a OpenGL, tenga en cuenta los siguientes puntos:

-   OpenGL no mantiene tablas de texturas; solo usa textura 1D y textura 2D. Para reutilizar las texturas del código GL de IRIS, pónlas en una lista de visualización.
-   OpenGL no genera automáticamente mapas mip. Si usa mipmaps, primero debe llamar a la función [**gluBuild2DMipmaps.**](glubuild2dmipmaps.md)
-   En OpenGL, usa [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) para activar y desactivar las funcionalidades de texturing.
-   En OpenGL, el tamaño de textura está más regulado que en IRIS GL. El tamaño de una textura OpenGL debe ser:

    2 *n* + 2 *b*

    donde *n* es un entero y *b* es:

    -   0, si la textura no tiene borde
    -   1, si la textura tiene un píxel de borde (las texturas OpenGL pueden tener bordes de 1 píxel).

En la tabla siguiente se enumeran las funciones de textura DE IRIS GL y sus equivalentes generales de OpenGL.



| Función GL de IRIS | Función OpenGL                                                                                                                                                                                                                                                       | Significado                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **textdef2d**    | [**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/>                                                                                                           | Especifica una imagen de textura 2D.                                                              |
| **textbind**     | **glTexImage2DglTexParameter**<br/> **gluBuild2DMipmaps**<br/>                                                                                                                                                                                            | Selecciona una función de textura.                                                                 |
| **tevdef**       | [**glTexEnv**](gltexenv-functions.md)                                                                                                                                                                                                                                | Define un entorno de asignación de texturas.                                                      |
| **tevbind**      | **glTexEnv**[**glTexImage1D**](glteximage1d.md)<br/>                                                                                                                                                                                                           | Selecciona un entorno de textura.                                                              |
| **t2**           | [**glTexCoord**](gltexcoord-functions.md)                                                                                                                                                                                                                            | Establece las coordenadas de textura actuales.                                                       |
| **texgen**       | [**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)<br/> [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/> [**gluScaleImage**](gluscaleimage.md)<br/> | Controla la generación de coordenadas de textura. Escala una imagen a un tamaño arbitrario.<br/> |



 

Para obtener más información sobre el texto, vea la *Guía de programación de OpenGL*.

En este tema se incluye información sobre lo siguiente.

-   [Traducción de tevdef](translating-tevdef.md)
-   [Traducción de la definición de texas](translating-texdef.md)
-   [Traducción de texgen](translating-texgen.md)

 

 





