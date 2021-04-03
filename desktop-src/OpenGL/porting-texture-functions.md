---
title: Trasladar funciones de textura
description: Trasladar funciones de textura
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- Migración de la contabilidad de IRIS, textura
- portabilidad de IRIS GL, textura
- trasladar a OpenGL desde IRIS GL, textura
- Exportación de OpenGL desde IRIS GL, textura
- textura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cba8b105089553084a93f997517d19cf371e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075948"
---
# <a name="porting-texture-functions"></a>Trasladar funciones de textura

Al migrar funciones de textura de GL de IRIS a OpenGL, tenga en cuenta los puntos siguientes:

-   OpenGL no mantiene tablas de texturas; solo usa la textura 1D y la textura 2D. Para reutilizar las texturas del código de GL de IRIS, colóquelas en una lista de visualización.
-   OpenGL no genera automáticamente mapas MIP. Si utiliza mapas MIP, primero debe llamar a la función [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) .
-   En OpenGL, se usa [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) para activar y desactivar las funcionalidades de la texturización.
-   En OpenGL, el tamaño de la textura se regula de forma más estricta que en el GL de IRIS. El tamaño de una textura OpenGL debe ser:

    2 *n* + 2 *b*

    donde *n* es un entero y *b* es:

    -   0, si la textura no tiene borde
    -   1, si la textura tiene un píxel de borde (las texturas OpenGL pueden tener bordes de 1 píxel).

En la tabla siguiente se enumeran las funciones de textura GL de IRIS y sus equivalentes de OpenGL generales.



| Función de GL de IRIS | Función OpenGL                                                                                                                                                                                                                                                       | Significado                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **textdef2d**    | [**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/>                                                                                                           | Especifica una imagen de textura 2D.                                                              |
| **textbind**     | **glTexImage2DglTexParameter**<br/> **gluBuild2DMipmaps**<br/>                                                                                                                                                                                            | Selecciona una función de textura.                                                                 |
| **tevdef**       | [**glTexEnv**](gltexenv-functions.md)                                                                                                                                                                                                                                | Define un entorno de asignación de texturas.                                                      |
| **tevbind**      | **glTexEnv**[**glTexImage1D**](glteximage1d.md)<br/>                                                                                                                                                                                                           | Selecciona un entorno de textura.                                                              |
| **T2**           | [**glTexCoord**](gltexcoord-functions.md)                                                                                                                                                                                                                            | Establece las coordenadas de textura actuales.                                                       |
| **texgen**       | [**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)<br/> [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/> [**gluScaleImage**](gluscaleimage.md)<br/> | Controla la generación de coordenadas de textura. Escala una imagen a un tamaño arbitrario.<br/> |



 

Para obtener más información sobre la texturización, vea la *Guía de programación de OpenGL*.

En este tema se incluye información sobre lo siguiente.

-   [Traducción de tevdef](translating-tevdef.md)
-   [Traducción de texdef](translating-texdef.md)
-   [Traducción de texgen](translating-texgen.md)

 

 





