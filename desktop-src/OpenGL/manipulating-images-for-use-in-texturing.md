---
title: Manipular imágenes para utilizarlas en la texturización
description: La biblioteca de utilidades OpenGL (GLU) proporciona escalado de imágenes y funciones mipmapping automáticas para simplificar la especificación de las imágenes de textura.
ms.assetid: 20edf665-1fed-4761-b8b1-beee02c78b0d
keywords:
- Utilidad OpenGL (GLU), escalado de imágenes
- GLU (utilidad OpenGL), escalado de imágenes
- Utilidad OpenGL (GLU), mipmapping automática
- GLU (utilidad OpenGL), mipmapping automática
- Utilidad OpenGL (GLU), imágenes de textura
- GLU (utilidad OpenGL), imágenes de textura
- Biblioteca GLU, imágenes de textura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16726493bbcb6e0116e4c158e470029f34f5b652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356980"
---
# <a name="manipulating-images-for-use-in-texturing"></a>Manipular imágenes para utilizarlas en la texturización

La biblioteca de utilidades OpenGL (GLU) proporciona escalado de imágenes y funciones mipmapping automáticas para simplificar la especificación de las imágenes de textura. La función [**gluScaleImage**](gluscaleimage.md) escala una imagen especificada a un tamaño de textura aceptado; puede pasar la imagen resultante a OpenGL como textura. Las funciones automáticas de mipmapping, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) y [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), crean imágenes de textura de mipmapped a partir de una imagen especificada y las pasan a [**glTexImage1D**](glteximage1d.md) y [**glTexImage2D**](glteximage2d.md), respectivamente.

 

 




