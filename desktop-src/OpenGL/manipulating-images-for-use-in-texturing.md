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
# <a name="manipulating-images-for-use-in-texturing"></a><span data-ttu-id="71010-110">Manipular imágenes para utilizarlas en la texturización</span><span class="sxs-lookup"><span data-stu-id="71010-110">Manipulating Images for Use in Texturing</span></span>

<span data-ttu-id="71010-111">La biblioteca de utilidades OpenGL (GLU) proporciona escalado de imágenes y funciones mipmapping automáticas para simplificar la especificación de las imágenes de textura.</span><span class="sxs-lookup"><span data-stu-id="71010-111">The OpenGL Utility library (GLU) provides image scaling and automatic mipmapping functions to simplify the specification of texture images.</span></span> <span data-ttu-id="71010-112">La función [**gluScaleImage**](gluscaleimage.md) escala una imagen especificada a un tamaño de textura aceptado; puede pasar la imagen resultante a OpenGL como textura.</span><span class="sxs-lookup"><span data-stu-id="71010-112">The [**gluScaleImage**](gluscaleimage.md) function scales a specified image to an accepted texture size; you can pass the resulting image to OpenGL as a texture.</span></span> <span data-ttu-id="71010-113">Las funciones automáticas de mipmapping, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) y [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), crean imágenes de textura de mipmapped a partir de una imagen especificada y las pasan a [**glTexImage1D**](glteximage1d.md) y [**glTexImage2D**](glteximage2d.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="71010-113">The automatic mipmapping functions, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) and [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), create mipmapped texture images from a specified image and pass them to [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md), respectively.</span></span>

 

 




