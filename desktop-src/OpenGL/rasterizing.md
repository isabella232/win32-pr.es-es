---
title: Rasterización
description: La rasterización es el proceso por el que se convierte un primitivo en una imagen bidimensional.
ms.assetid: 8d4e3033-2afe-4526-8862-799c45ea9a6a
keywords:
- Canalización de procesamiento de OpenGL, rasterización
- rasterizar OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f0d8e7ece3bead408b8d056356593879edc638c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532026"
---
# <a name="rasterizing"></a>Rasterización

La *rasterización* es el proceso por el que se convierte un primitivo en una imagen bidimensional. Cada punto de esta imagen contiene información como color, profundidad y datos de textura. Un punto y su información asociada se denominan *fragmentos*. La posición de la trama actual, tal y como se especifica con [**glRasterPos \***](glrasterpos-functions.md), se usa de varias maneras en esta fase para dibujar píxeles y mapas de bits. Se producen diferentes problemas al rasterizar puntos, segmentos de línea y polígonos. Además, es necesario rasterizar los rectángulos y los mapas de bits en píxeles.

Con OpenGL, controla la rasterización mediante las siguientes funciones:

-   Primitives. Controla cómo se rasterizan los primitivos mediante las funciones que determinan las dimensiones y los patrones punteados: [**glPointSize**](glpointsize.md), [**glLineWidth**](gllinewidth.md), [**glLineStipple**](gllinestipple.md)y [**glPolygonStipple**](glpolygonstipple.md). Controla cómo se rasterizan las caras frontal y trasera de los polígonos con [**glCullFace**](glcullface.md), [**glFrontFace**](glfrontface.md)y [**glPolygonMode**](glpolygonmode.md).
-   Pixel. Varias funciones controlan el almacenamiento de píxeles y los modos de transferencia. La función [**glPixelStore \***](glpixelstore-functions.md) controla la codificación de píxeles en la memoria del cliente y [**glPixelTransfer \***](glpixeltransfer.md) y [**glPixelMap \***](glpixelmap.md) controlan cómo se procesan los píxeles antes de colocarlos en fotogramas. Especifique un rectángulo de píxeles con [**glDrawPixels**](gldrawpixels.md); Controle su rasterización con [**glPixelZoom**](glpixelzoom.md).
-   Mapas. Los mapas de bits son rectángulos de ceros y unos que especifican un patrón determinado de fragmentos que se van a generar. Cada uno de estos fragmentos tiene los mismos datos asociados. La función [**glBitmap**](glbitmap.md) especifica un mapa de bits.
-   Memoria de textura. Cuando se habilita la texturización, la texturización asigna una parte de una imagen de textura especificada en cada primitiva. Esta asignación se realiza utilizando el color de la imagen de textura en la ubicación indicada por las coordenadas de textura de un fragmento para modificar el color RGBA del fragmento. Especifique una imagen de textura con [**glTexImage2D**](glteximage2d.md) o [**glTexImage1D**](glteximage1d.md). Las [**funciones \* GlTexParameter**](gltexparameter-functions.md) y [**glTexEnv \***](gltexenv-functions.md) controlan cómo se interpretan los valores de textura y se aplican a un fragmento.
-   Luz. Para mezclar un color de niebla con el color posterior a la texturización de un fragmento rasterizado, use un factor de mezcla que dependa de la distancia entre el eyepoint y el fragmento. Use [**glFog \***](glfog.md) para especificar el color de niebla y el factor de mezcla.

 

 




