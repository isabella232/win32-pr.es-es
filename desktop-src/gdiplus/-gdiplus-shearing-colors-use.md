---
description: La cizallación aumenta o disminuye un componente de color en una cantidad proporcional a otro componente de color.
ms.assetid: 12f83f35-33f1-4ac9-b45d-f8700e54053a
title: Distorsionar colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d632fded9f2b4d1e4682ae9f8ffbfedee85a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156177"
---
# <a name="shearing-colors"></a><span data-ttu-id="fb668-103">Distorsionar colores</span><span class="sxs-lookup"><span data-stu-id="fb668-103">Shearing Colors</span></span>

<span data-ttu-id="fb668-104">La cizallación aumenta o disminuye un componente de color en una cantidad proporcional a otro componente de color.</span><span class="sxs-lookup"><span data-stu-id="fb668-104">Shearing increases or decreases a color component by an amount proportional to another color component.</span></span> <span data-ttu-id="fb668-105">Por ejemplo, considere la transformación en la que el componente rojo aumenta en una mitad el valor del componente azul.</span><span class="sxs-lookup"><span data-stu-id="fb668-105">For example, consider the transformation where the red component is increased by one half the value of the blue component.</span></span> <span data-ttu-id="fb668-106">En este tipo de transformación, el color (0,2, 0,5, 1) se convertiría en (0,7, 0,5, 1).</span><span class="sxs-lookup"><span data-stu-id="fb668-106">Under such a transformation, the color (0.2, 0.5, 1) would become (0.7, 0.5, 1).</span></span> <span data-ttu-id="fb668-107">El nuevo componente rojo es 0,2 + (1/2) (1) = 0,7.</span><span class="sxs-lookup"><span data-stu-id="fb668-107">The new red component is 0.2 + (1/2)(1) = 0.7.</span></span>

<span data-ttu-id="fb668-108">En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo ColorBars4.bmp.</span><span class="sxs-lookup"><span data-stu-id="fb668-108">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars4.bmp.</span></span> <span data-ttu-id="fb668-109">A continuación, el código aplica la transformación de recorte que se describe en el párrafo anterior a cada píxel de la imagen.</span><span class="sxs-lookup"><span data-stu-id="fb668-109">Then the code applies the shearing transformation described in the preceding paragraph to each pixel in the image.</span></span>


```
Image            image(L"ColorBars4.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.5f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="fb668-110">En la ilustración siguiente se muestra la imagen original de la izquierda y la imagen distorsionada a la derecha.</span><span class="sxs-lookup"><span data-stu-id="fb668-110">The following illustration shows the original image on the left and the sheared image on the right.</span></span>

![Ilustración que muestra cuatro barras coloreadas y, a continuación, las mismas barras con distintos colores](images/colortrans6.png)

<span data-ttu-id="fb668-112">En la tabla siguiente se muestran los vectores de color para las cuatro barras antes y después de la transformación de recorte.</span><span class="sxs-lookup"><span data-stu-id="fb668-112">The following table shows the color vectors for the four bars before and after the shearing transformation.</span></span>



| <span data-ttu-id="fb668-113">Original</span><span class="sxs-lookup"><span data-stu-id="fb668-113">Original</span></span>           | <span data-ttu-id="fb668-114">Distorsionado</span><span class="sxs-lookup"><span data-stu-id="fb668-114">Sheared</span></span>            |
|--------------------|--------------------|
| <span data-ttu-id="fb668-115">(0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="fb668-115">(0, 0, 1, 1)</span></span>       | <span data-ttu-id="fb668-116">(0.5, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="fb668-116">(0.5, 0, 1, 1)</span></span>     |
| <span data-ttu-id="fb668-117">(0.5, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="fb668-117">(0.5, 1, 0.5, 1)</span></span>   | <span data-ttu-id="fb668-118">(0.75, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="fb668-118">(0.75, 1, 0.5, 1)</span></span>  |
| <span data-ttu-id="fb668-119">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="fb668-119">(1, 1, 0, 1)</span></span>       | <span data-ttu-id="fb668-120">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="fb668-120">(1, 1, 0, 1)</span></span>       |
| <span data-ttu-id="fb668-121">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="fb668-121">(0.4, 0.4, 0.4, 1)</span></span> | <span data-ttu-id="fb668-122">(0.6, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="fb668-122">(0.6, 0.4, 0.4, 1)</span></span> |



 

 

 



