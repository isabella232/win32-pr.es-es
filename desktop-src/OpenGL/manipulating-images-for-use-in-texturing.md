---
title: Manipulación de imágenes para su uso en texturing
description: La biblioteca de la utilidad OpenGL (GLU) proporciona funciones de escalado de imágenes y mipmapping automáticas para simplificar la especificación de imágenes de textura.
ms.assetid: 20edf665-1fed-4761-b8b1-beee02c78b0d
keywords:
- Utilidad OpenGL (GLU),escalado de imágenes
- GLU (utilidad OpenGL), escalado de imágenes
- Utilidad OpenGL (GLU), aplicación automática de mipm
- GLU (utilidad OpenGL), aplicación automática de mipm
- Utilidad OpenGL (GLU),imágenes de textura
- GLU (utilidad OpenGL),imágenes de textura
- Biblioteca GLU, imágenes de textura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16726493bbcb6e0116e4c158e470029f34f5b652
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265703"
---
# <a name="manipulating-images-for-use-in-texturing"></a>Manipulación de imágenes para su uso en texturing

La biblioteca de la utilidad OpenGL (GLU) proporciona funciones de escalado de imágenes y mipmapping automáticas para simplificar la especificación de imágenes de textura. La [**función gluScaleImage**](gluscaleimage.md) escala una imagen especificada a un tamaño de textura aceptado; puede pasar la imagen resultante a OpenGL como una textura. Las funciones mipmapping [**automáticas, gluBuild1DMipmaps**](glubuild1dmipmaps.md) y [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), crean imágenes de textura mipmapped a partir de una imagen especificada y las pasan a [**glTexImage1D**](glteximage1d.md) y [**glTexImage2D,**](glteximage2d.md)respectivamente.

 

 




