---
description: Una traducción agrega un valor a uno o varios de los cuatro componentes de color. En la tabla siguiente se proporcionan las entradas de la matriz de colores que representan las traducciones.
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: Traducir colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c769a24c02e977c3e32ff913852d4b6b8d54441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559684"
---
# <a name="translating-colors"></a><span data-ttu-id="7c262-104">Traducir colores</span><span class="sxs-lookup"><span data-stu-id="7c262-104">Translating Colors</span></span>

<span data-ttu-id="7c262-105">Una traducción agrega un valor a uno o varios de los cuatro componentes de color.</span><span class="sxs-lookup"><span data-stu-id="7c262-105">A translation adds a value to one or more of the four color components.</span></span> <span data-ttu-id="7c262-106">En la tabla siguiente se proporcionan las entradas de la matriz de colores que representan las traducciones.</span><span class="sxs-lookup"><span data-stu-id="7c262-106">The color matrix entries that represent translations are given in the following table.</span></span>



| <span data-ttu-id="7c262-107">Componente que se va a traducir</span><span class="sxs-lookup"><span data-stu-id="7c262-107">Component to be translated</span></span> | <span data-ttu-id="7c262-108">Entrada de matriz</span><span class="sxs-lookup"><span data-stu-id="7c262-108">Matrix entry</span></span> |
|----------------------------|--------------|
| <span data-ttu-id="7c262-109">Rojo</span><span class="sxs-lookup"><span data-stu-id="7c262-109">Red</span></span>                        | <span data-ttu-id="7c262-110">\[4 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="7c262-110">\[4\]\[0\]</span></span>   |
| <span data-ttu-id="7c262-111">Verde</span><span class="sxs-lookup"><span data-stu-id="7c262-111">Green</span></span>                      | <span data-ttu-id="7c262-112">\[4 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="7c262-112">\[4\]\[1\]</span></span>   |
| <span data-ttu-id="7c262-113">Azul</span><span class="sxs-lookup"><span data-stu-id="7c262-113">Blue</span></span>                       | <span data-ttu-id="7c262-114">\[4 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="7c262-114">\[4\]\[2\]</span></span>   |
| <span data-ttu-id="7c262-115">Alpha</span><span class="sxs-lookup"><span data-stu-id="7c262-115">Alpha</span></span>                      | <span data-ttu-id="7c262-116">\[4 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="7c262-116">\[4\]\[3\]</span></span>   |



 

<span data-ttu-id="7c262-117">En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo ColorBars.bmp.</span><span class="sxs-lookup"><span data-stu-id="7c262-117">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars.bmp.</span></span> <span data-ttu-id="7c262-118">Después, el código agrega 0,75 al componente rojo de cada píxel de la imagen.</span><span class="sxs-lookup"><span data-stu-id="7c262-118">Then the code adds 0.75 to the red component of each pixel in the image.</span></span> <span data-ttu-id="7c262-119">La imagen original se dibuja junto con la imagen transformada.</span><span class="sxs-lookup"><span data-stu-id="7c262-119">The original image is drawn alongside the transformed image.</span></span>


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f,  0.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  1.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 1.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 0.0f, 1.0f, 0.0f,
   0.75f, 0.0f, 0.0f, 0.0f, 1.0f};
   
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



<span data-ttu-id="7c262-120">En la ilustración siguiente se muestra la imagen original de la izquierda y la imagen transformada a la derecha.</span><span class="sxs-lookup"><span data-stu-id="7c262-120">The following illustration shows the original image on the left and the transformed image on the right.</span></span>

![Ilustración que muestra cuatro barras coloreadas y, a continuación, las mismas barras con distintos colores](images/colortrans2.png)

<span data-ttu-id="7c262-122">En la tabla siguiente se enumeran los vectores de color de las cuatro barras antes y después de la traducción roja.</span><span class="sxs-lookup"><span data-stu-id="7c262-122">The following table lists the color vectors for the four bars before and after the red translation.</span></span> <span data-ttu-id="7c262-123">Tenga en cuenta que, dado que el valor máximo de un componente de color es 1, el componente rojo de la segunda fila no cambia.</span><span class="sxs-lookup"><span data-stu-id="7c262-123">Note that because the maximum value for a color component is 1, the red component in the second row does not change.</span></span> <span data-ttu-id="7c262-124">(De igual forma, el valor mínimo de un componente de color es 0).</span><span class="sxs-lookup"><span data-stu-id="7c262-124">(Similarly, the minimum value for a color component is 0.)</span></span>



| <span data-ttu-id="7c262-125">Original</span><span class="sxs-lookup"><span data-stu-id="7c262-125">Original</span></span>           | <span data-ttu-id="7c262-126">Traducidos</span><span class="sxs-lookup"><span data-stu-id="7c262-126">Translated</span></span>      |
|--------------------|-----------------|
| <span data-ttu-id="7c262-127">Negro (0,0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="7c262-127">Black (0, 0, 0, 1)</span></span> | <span data-ttu-id="7c262-128">(0.75, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="7c262-128">(0.75, 0, 0, 1)</span></span> |
| <span data-ttu-id="7c262-129">Rojo (1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="7c262-129">Red (1, 0, 0, 1)</span></span>   | <span data-ttu-id="7c262-130">(1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="7c262-130">(1, 0, 0, 1)</span></span>    |
| <span data-ttu-id="7c262-131">Verde (0, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="7c262-131">Green (0, 1, 0, 1)</span></span> | <span data-ttu-id="7c262-132">(0.75, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="7c262-132">(0.75, 1, 0, 1)</span></span> |
| <span data-ttu-id="7c262-133">Blue (0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="7c262-133">Blue (0, 0, 1, 1)</span></span>  | <span data-ttu-id="7c262-134">(0.75, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="7c262-134">(0.75, 0, 1, 1)</span></span> |



 

 

 



