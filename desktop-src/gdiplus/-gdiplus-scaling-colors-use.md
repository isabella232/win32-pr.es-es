---
description: Una transformación de escalado multiplica uno o varios de los cuatro componentes de color por un número. En la tabla siguiente se proporcionan las entradas de la matriz de colores que representan el escalado.
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: Escalado de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370155306f7b1a177358d7cf28d329ebb0d75f8c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104279718"
---
# <a name="scaling-colors"></a><span data-ttu-id="1f929-104">Escalado de colores</span><span class="sxs-lookup"><span data-stu-id="1f929-104">Scaling Colors</span></span>

<span data-ttu-id="1f929-105">Una transformación de escalado multiplica uno o varios de los cuatro componentes de color por un número.</span><span class="sxs-lookup"><span data-stu-id="1f929-105">A scaling transformation multiplies one or more of the four color components by a number.</span></span> <span data-ttu-id="1f929-106">En la tabla siguiente se proporcionan las entradas de la matriz de colores que representan el escalado.</span><span class="sxs-lookup"><span data-stu-id="1f929-106">The color matrix entries that represent scaling are given in the following table.</span></span>



| <span data-ttu-id="1f929-107">Componente que se va a escalar</span><span class="sxs-lookup"><span data-stu-id="1f929-107">Component to be scaled</span></span> | <span data-ttu-id="1f929-108">Entrada de matriz</span><span class="sxs-lookup"><span data-stu-id="1f929-108">Matrix entry</span></span> |
|------------------------|--------------|
| <span data-ttu-id="1f929-109">Rojo</span><span class="sxs-lookup"><span data-stu-id="1f929-109">Red</span></span>                    | <span data-ttu-id="1f929-110">\[0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="1f929-110">\[0\]\[0\]</span></span>   |
| <span data-ttu-id="1f929-111">Verde</span><span class="sxs-lookup"><span data-stu-id="1f929-111">Green</span></span>                  | <span data-ttu-id="1f929-112">\[1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="1f929-112">\[1\]\[1\]</span></span>   |
| <span data-ttu-id="1f929-113">Azul</span><span class="sxs-lookup"><span data-stu-id="1f929-113">Blue</span></span>                   | <span data-ttu-id="1f929-114">\[2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="1f929-114">\[2\]\[2\]</span></span>   |
| <span data-ttu-id="1f929-115">Alpha</span><span class="sxs-lookup"><span data-stu-id="1f929-115">Alpha</span></span>                  | <span data-ttu-id="1f929-116">\[3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="1f929-116">\[3\]\[3\]</span></span>   |



 

<span data-ttu-id="1f929-117">En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo ColorBars2.bmp.</span><span class="sxs-lookup"><span data-stu-id="1f929-117">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="1f929-118">A continuación, el código escala el componente azul de cada píxel de la imagen en un factor de 2.</span><span class="sxs-lookup"><span data-stu-id="1f929-118">Then the code scales the blue component of each pixel in the image by a factor of 2.</span></span> <span data-ttu-id="1f929-119">La imagen original se dibuja junto con la imagen transformada.</span><span class="sxs-lookup"><span data-stu-id="1f929-119">The original image is drawn alongside the transformed image.</span></span>


```
Image            image(L"ColorBars2.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 2.0f, 0.0f, 0.0f,
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



<span data-ttu-id="1f929-120">En la ilustración siguiente se muestra la imagen original a la izquierda y la imagen escalada a la derecha.</span><span class="sxs-lookup"><span data-stu-id="1f929-120">The following illustration shows the original image on the left and the scaled image on the right.</span></span>

![Muestra cuatro barras coloreadas y, a continuación, las mismas barras con distintos colores.](images/colortrans3.png)

<span data-ttu-id="1f929-122">En la tabla siguiente se muestran los vectores de color de las cuatro barras antes y después del ajuste de escala azul.</span><span class="sxs-lookup"><span data-stu-id="1f929-122">The following table shows the color vectors for the four bars before and after the blue scaling.</span></span> <span data-ttu-id="1f929-123">Tenga en cuenta que el componente azul de la cuarta barra de colores pasó de 0,8 a 0,6.</span><span class="sxs-lookup"><span data-stu-id="1f929-123">Note that the blue component in the fourth color bar went from 0.8 to 0.6.</span></span> <span data-ttu-id="1f929-124">Esto se debe a que GDI+ solo conserva la parte fraccionaria del resultado.</span><span class="sxs-lookup"><span data-stu-id="1f929-124">That is because GDI+ retains only the fractional part of the result.</span></span> <span data-ttu-id="1f929-125">Por ejemplo, (2) (0,8) = 1,6 y la parte fraccionaria de 1,6 es 0,6.</span><span class="sxs-lookup"><span data-stu-id="1f929-125">For example, (2)(0.8) = 1.6, and the fractional part of 1.6 is 0.6.</span></span> <span data-ttu-id="1f929-126">Conservar solo la parte fraccionaria garantiza que el resultado siempre se encuentra en el intervalo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="1f929-126">Retaining only the fractional part ensures that the result is always in the interval \[0, 1\].</span></span>



| <span data-ttu-id="1f929-127">Original</span><span class="sxs-lookup"><span data-stu-id="1f929-127">Original</span></span>           | <span data-ttu-id="1f929-128">Escalar</span><span class="sxs-lookup"><span data-stu-id="1f929-128">Scaled</span></span>             |
|--------------------|--------------------|
| <span data-ttu-id="1f929-129">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-129">(0.4, 0.4, 0.4, 1)</span></span> | <span data-ttu-id="1f929-130">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-130">(0.4, 0.4, 0.8, 1)</span></span> |
| <span data-ttu-id="1f929-131">(0.4, 0.2, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-131">(0.4, 0.2, 0.2, 1)</span></span> | <span data-ttu-id="1f929-132">(0.4, 0.2, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-132">(0.4, 0.2, 0.4, 1)</span></span> |
| <span data-ttu-id="1f929-133">(0.2, 0.4, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-133">(0.2, 0.4, 0.2, 1)</span></span> | <span data-ttu-id="1f929-134">(0.2, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-134">(0.2, 0.4, 0.4, 1)</span></span> |
| <span data-ttu-id="1f929-135">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-135">(0.4, 0.4, 0.8, 1)</span></span> | <span data-ttu-id="1f929-136">(0.4, 0.4, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-136">(0.4, 0.4, 0.6, 1)</span></span> |



 

<span data-ttu-id="1f929-137">En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo ColorBars2.bmp.</span><span class="sxs-lookup"><span data-stu-id="1f929-137">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="1f929-138">A continuación, el código escala los componentes rojo, verde y azul de cada píxel de la imagen.</span><span class="sxs-lookup"><span data-stu-id="1f929-138">Then the code scales the red, green, and blue components of each pixel in the image.</span></span> <span data-ttu-id="1f929-139">Los componentes rojos se escalan hacia abajo en un 25 por ciento, los componentes verdes se escalan hacia abajo el 35 por ciento y los componentes azules se escalan hacia abajo el 50 por ciento.</span><span class="sxs-lookup"><span data-stu-id="1f929-139">The red components are scaled down 25 percent, the green components are scaled down 35 percent, and the blue components are scaled down 50 percent.</span></span>


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   0.75f, 0.0f,  0.0f, 0.0f, 0.0f,
   0.0f,  0.65f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.5f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 1.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 0.0f, 1.0f};
   
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



<span data-ttu-id="1f929-140">En la ilustración siguiente se muestra la imagen original a la izquierda y la imagen escalada a la derecha.</span><span class="sxs-lookup"><span data-stu-id="1f929-140">The following illustration shows the original image on the left and the scaled image on the right.</span></span>

![Ilustración en la que se muestran cuatro barras coloreadas y, a continuación, las barras con distintos colores](images/colortrans4.png)

<span data-ttu-id="1f929-142">En la tabla siguiente se muestran los vectores de color de las cuatro barras antes y después del ajuste de escala rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="1f929-142">The following table shows the color vectors for the four bars before and after the red, green and blue scaling.</span></span>



| <span data-ttu-id="1f929-143">Original</span><span class="sxs-lookup"><span data-stu-id="1f929-143">Original</span></span>           | <span data-ttu-id="1f929-144">Escalar</span><span class="sxs-lookup"><span data-stu-id="1f929-144">Scaled</span></span>               |
|--------------------|----------------------|
| <span data-ttu-id="1f929-145">(0.6, 0.6, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-145">(0.6, 0.6, 0.6, 1)</span></span> | <span data-ttu-id="1f929-146">(0.45, 0.39, 0.3, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-146">(0.45, 0.39, 0.3, 1)</span></span> |
| <span data-ttu-id="1f929-147">(0, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-147">(0, 1, 1, 1)</span></span>       | <span data-ttu-id="1f929-148">(0, 0.65, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-148">(0, 0.65, 0.5, 1)</span></span>    |
| <span data-ttu-id="1f929-149">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-149">(1, 1, 0, 1)</span></span>       | <span data-ttu-id="1f929-150">(0.75, 0.65, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-150">(0.75, 0.65, 0, 1)</span></span>   |
| <span data-ttu-id="1f929-151">(1, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-151">(1, 0, 1, 1)</span></span>       | <span data-ttu-id="1f929-152">(0.75, 0, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="1f929-152">(0.75, 0, 0.5, 1)</span></span>    |



 

 

 



