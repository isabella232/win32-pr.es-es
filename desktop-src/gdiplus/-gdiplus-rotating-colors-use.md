---
description: Es difícil visualizar el giro en un espacio de colores de cuatro dimensiones.
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: Girar colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea322179bd4a46021d181abedd1797d6bdda7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907930"
---
# <a name="rotating-colors"></a><span data-ttu-id="39771-103">Girar colores</span><span class="sxs-lookup"><span data-stu-id="39771-103">Rotating Colors</span></span>

<span data-ttu-id="39771-104">Es difícil visualizar el giro en un espacio de colores de cuatro dimensiones.</span><span class="sxs-lookup"><span data-stu-id="39771-104">Rotation in a four-dimensional color space is difficult to visualize.</span></span> <span data-ttu-id="39771-105">Podemos facilitar la visualización de la rotación al aceptar que se ha corregido uno de los componentes de color.</span><span class="sxs-lookup"><span data-stu-id="39771-105">We can make it easier to visualize rotation by agreeing to keep one of the color components fixed.</span></span> <span data-ttu-id="39771-106">Supongamos que aceptamos mantener el componente alfa fijo en 1 (totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="39771-106">Suppose we agree to keep the alpha component fixed at 1 (fully opaque).</span></span> <span data-ttu-id="39771-107">Después, podemos visualizar un espacio de colores tridimensional con los ejes rojo, verde y azul, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="39771-107">Then we can visualize a three-dimensional color space with red, green, and blue axes as shown in the following illustration.</span></span>

![Ilustración de una vista en perspectiva de un espacio de colores tridimensional con ejes etiquetados como rojo, verde y azul](images/recoloring03.png)

<span data-ttu-id="39771-109">Un color puede considerarse como un punto en un espacio 3D.</span><span class="sxs-lookup"><span data-stu-id="39771-109">A color can be thought of as a point in 3-D space.</span></span> <span data-ttu-id="39771-110">Por ejemplo, el punto (1,0) en el espacio representa el color rojo y el punto (0, 1, 0) en el espacio representa el color verde.</span><span class="sxs-lookup"><span data-stu-id="39771-110">For example, the point (1, 0, 0) in space represents the color red, and the point (0, 1, 0) in space represents the color green.</span></span>

<span data-ttu-id="39771-111">En la ilustración siguiente se muestra lo que significa girar el color (1,0) hasta un ángulo de 60 grados en el plano de Red-Green.</span><span class="sxs-lookup"><span data-stu-id="39771-111">The following illustration shows what it means to rotate the color (1, 0, 0) through an angle of 60 degrees in the Red-Green plane.</span></span> <span data-ttu-id="39771-112">La rotación en un plano paralelo al plano de Red-Green se puede considerar como giro sobre el eje azul.</span><span class="sxs-lookup"><span data-stu-id="39771-112">Rotation in a plane parallel to the Red-Green plane can be thought of as rotation about the blue axis.</span></span>

![Ilustración que muestra el punto (1,0, 0) girado 60 grados a (0,5, 0,866, 0)](images/recoloring04.png)

<span data-ttu-id="39771-114">En la ilustración siguiente se muestra cómo inicializar una matriz de colores para realizar giros sobre cada uno de los tres ejes de coordenadas (rojo, verde, azul).</span><span class="sxs-lookup"><span data-stu-id="39771-114">The following illustration shows how to initialize a color matrix to perform rotations about each of the three coordinate axes (red, green, blue).</span></span>

![Ilustración en la que se muestran las matrices de colores que realizan giros sobre cada uno de los tres ejes de coordenadas](images/recoloring05.png)

<span data-ttu-id="39771-116">En el siguiente ejemplo se toma una imagen de un color (1, 0, 0,6) y se aplica una rotación de 60 grados sobre el eje azul.</span><span class="sxs-lookup"><span data-stu-id="39771-116">The following example takes an image that is all one color (1, 0, 0.6) and applies a 60-degree rotation about the blue axis.</span></span> <span data-ttu-id="39771-117">El ángulo de rotación se barre en un plano paralelo al plano de Red-Green.</span><span class="sxs-lookup"><span data-stu-id="39771-117">The angle of the rotation is swept out in a plane that is parallel to the Red-Green plane.</span></span>


```
Image            image(L"RotationInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
REAL             degrees = 60;
REAL             pi = acos(-1);  // the angle whose cosine is -1.
REAL             r = degrees * pi / 180;  // degrees to radians

ColorMatrix colorMatrix = {
   cos(r),  sin(r), 0.0f, 0.0f, 0.0f,
   -sin(r), cos(r), 0.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   1.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 1.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(130, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="39771-118">En la ilustración siguiente se muestra la imagen original de la izquierda y la imagen girada en color de la derecha.</span><span class="sxs-lookup"><span data-stu-id="39771-118">The following illustration shows the original image on the left and the color-rotated image on the right.</span></span>

![Ilustración en la que se muestran los rectángulos rellenados con la imagen original (rojo violeta) y la imagen girada en color (verde mar)](images/colortrans5.png)

<span data-ttu-id="39771-120">La rotación de color realizada en el ejemplo de código anterior se puede visualizar como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="39771-120">The color rotation performed in the preceding code example can be visualized as follows.</span></span>

![Ilustración que muestra un espacio de colores 3D y el punto (1,0, 0,6) girado 60 grados a (0,5, 0,866, 0,6)](images/recoloring06.png)

 

 



