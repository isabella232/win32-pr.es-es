---
title: Rasterizar
description: Rasterizar es el proceso por el que una primitiva se convierte en una imagen bidimensional.
ms.assetid: 8d4e3033-2afe-4526-8862-799c45ea9a6a
keywords:
- Canalización de procesamiento de OpenGL, rasterización
- rasterización de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8192f8fdd919c14be4bd47688abf911b363e13f2e8ca9606f1943eb2956378ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776885"
---
# <a name="rasterizing"></a>Rasterizar

*Rasterizar* es el proceso por el que una primitiva se convierte en una imagen bidimensional. Cada punto de esta imagen contiene información como los datos de color, profundidad y textura. Un punto y su información asociada se denominan *fragmentos*. La posición de trama actual, como se especifica con [**glRasterPos, \***](glrasterpos-functions.md)se usa de varias maneras durante esta fase para dibujar píxeles y mapas de bits. Surgen diferentes problemas al rasterizar puntos, segmentos de línea y polígonos. Además, es necesario rasterizar los rectángulos de píxeles y los mapas de bits.

Con OpenGL puede controlar la rasterización mediante las siguientes funciones:

-   Primitivas. Controlar cómo se rasterizan las primitivas mediante funciones que determinan dimensiones y patrones detippla: [**glPointSize**](glpointsize.md), [**glLineWidth,**](gllinewidth.md) [**glLineStipple**](gllinestipple.md)y [**glPolygonStipple.**](glpolygonstipple.md) Controlar cómo se rasterizan las caras frontal y posterior de los polígonos con [**glCullFace,**](glcullface.md) [**glFrontFace**](glfrontface.md)y [**glPolygonMode.**](glpolygonmode.md)
-   Píxeles. Varias funciones controlan los modos de transferencia y almacenamiento de píxeles. La función [ * *glPixelStore \** _](glpixelstore-functions.md) controla la codificación de píxeles en la memoria del cliente y [_*glPixelTransfer \**_](glpixeltransfer.md) y [_*glPixelMap \**_](glpixelmap.md) controlan cómo se procesan los píxeles antes de colocarse en el búfer de fotogramas. Especifique un rectángulo de píxeles [con _ *glDrawPixels;* *](gldrawpixels.md)controle su rasterización con [**glPixelZoom.**](glpixelzoom.md)
-   Bits. Los mapas de bits son rectángulos de ceros y otros que especifican un patrón determinado de fragmentos que se van a generar. Cada uno de estos fragmentos tiene los mismos datos asociados. La [**función glBitmap**](glbitmap.md) especifica un mapa de bits.
-   Memoria de textura. Cuando el texturing está habilitado, texturing asigna una parte de una imagen de textura especificada a cada primitiva. Esta asignación se realiza mediante el color de la imagen de textura en la ubicación indicada por las coordenadas de textura de un fragmento para modificar el color RGBA del fragmento. Especifique una imagen de textura [**con glTexImage2D**](glteximage2d.md) o [**glTexImage1D.**](glteximage1d.md) Las [ * *funciones \* glTexParameter* _](gltexparameter-functions.md) y [_ *glTexEnv \** *](gltexenv-functions.md) controlan cómo se interpretan y aplican los valores de textura a un fragmento.
-   Niebla. Para combinar un color rojo con el color posterior a la texturación de un fragmento rasterizado, use un factor de combinación que dependa de la distancia entre el punto de los ojos y el fragmento. Use [**glFog \* para**](glfog.md) especificar el color de color y el factor de mezcla.

 

 




