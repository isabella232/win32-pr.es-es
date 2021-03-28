---
description: El modo de interpolación de un objeto gráfico influye en la forma en que Windows GDI+ escala (estira y reduce) las imágenes.
ms.assetid: 3aeead47-78da-4ab3-9126-2fbe9e341e48
title: Usar el modo de interpolación para controlar la calidad de la imagen durante el ajuste de escala
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a829f2edf2f341f50bee771d909f7c4eef98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984426"
---
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a><span data-ttu-id="92fec-103">Usar el modo de interpolación para controlar la calidad de la imagen durante el ajuste de escala</span><span class="sxs-lookup"><span data-stu-id="92fec-103">Using Interpolation Mode to Control Image Quality During Scaling</span></span>

<span data-ttu-id="92fec-104">El modo de interpolación de un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) influye en la forma en que Windows GDI+ escala (estira y reduce) las imágenes.</span><span class="sxs-lookup"><span data-stu-id="92fec-104">The interpolation mode of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object influences the way Windows GDI+ scales (stretches and shrinks) images.</span></span> <span data-ttu-id="92fec-105">La enumeración [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) en Gdiplusenums. h define varios modos de interpolación, algunos de los cuales se muestran en la lista siguiente:</span><span class="sxs-lookup"><span data-stu-id="92fec-105">The [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) enumeration in Gdiplusenums.h defines several interpolation modes, some of which are shown in the following list:</span></span>

-   <span data-ttu-id="92fec-106">InterpolationModeNearestNeighbor</span><span class="sxs-lookup"><span data-stu-id="92fec-106">InterpolationModeNearestNeighbor</span></span>
-   <span data-ttu-id="92fec-107">InterpolationModeBilinear</span><span class="sxs-lookup"><span data-stu-id="92fec-107">InterpolationModeBilinear</span></span>
-   <span data-ttu-id="92fec-108">InterpolationModeHighQualityBilinear</span><span class="sxs-lookup"><span data-stu-id="92fec-108">InterpolationModeHighQualityBilinear</span></span>
-   <span data-ttu-id="92fec-109">InterpolationModeBicubic</span><span class="sxs-lookup"><span data-stu-id="92fec-109">InterpolationModeBicubic</span></span>
-   <span data-ttu-id="92fec-110">InterpolationModeHighQualityBicubic</span><span class="sxs-lookup"><span data-stu-id="92fec-110">InterpolationModeHighQualityBicubic</span></span>

<span data-ttu-id="92fec-111">Para ajustar una imagen, cada píxel de la imagen original debe estar asignado a un grupo de píxeles de la imagen más grande.</span><span class="sxs-lookup"><span data-stu-id="92fec-111">To stretch an image, each pixel in the original image must be mapped to a group of pixels in the larger image.</span></span> <span data-ttu-id="92fec-112">Para reducir una imagen, los grupos de píxeles de la imagen original deben estar asignados a píxeles individuales de la imagen más pequeña.</span><span class="sxs-lookup"><span data-stu-id="92fec-112">To shrink an image, groups of pixels in the original image must be mapped to single pixels in the smaller image.</span></span> <span data-ttu-id="92fec-113">La eficacia de los algoritmos que realizan estas asignaciones determina la calidad de una imagen escalada.</span><span class="sxs-lookup"><span data-stu-id="92fec-113">The effectiveness of the algorithms that perform these mappings determines the quality of a scaled image.</span></span> <span data-ttu-id="92fec-114">Los algoritmos que generan imágenes escaladas de mayor calidad suelen requerir más tiempo de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="92fec-114">Algorithms that produce higher-quality scaled images tend to require more processing time.</span></span> <span data-ttu-id="92fec-115">En la lista anterior, InterpolationModeNearestNeighbor es el modo de menor calidad y InterpolationModeHighQualityBicubic es el modo de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="92fec-115">In the preceding list, InterpolationModeNearestNeighbor is the lowest-quality mode and InterpolationModeHighQualityBicubic is the highest-quality mode.</span></span>

<span data-ttu-id="92fec-116">Para establecer el modo de interpolación, pase uno de los miembros de la enumeración [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) al método **SetInterpolationMode** de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="92fec-116">To set the interpolation mode, pass one of the members of the [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) enumeration to the **SetInterpolationMode** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

<span data-ttu-id="92fec-117">En el ejemplo siguiente se dibuja una imagen y, a continuación, se reduce la imagen con tres modos de interpolación diferentes:</span><span class="sxs-lookup"><span data-stu-id="92fec-117">The following example draws an image and then shrinks the image with three different interpolation modes:</span></span>


```
Image image(L"GrapeBunch.bmp");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Draw the image with no shrinking or stretching.
graphics.DrawImage(
   &image,
   Rect(10, 10, width, height),  // destination rectangle  
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using low-quality interpolation. 
graphics.SetInterpolationMode(InterpolationModeNearestNeighbor);
graphics.DrawImage(
   &image,
   Rect(10, 250, 0.6*width, 0.6*height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using medium-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBilinear);
graphics.DrawImage(
   &image,
   Rect(150, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using high-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBicubic);
graphics.DrawImage(
   &image,
   Rect(290, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
```



<span data-ttu-id="92fec-118">En la ilustración siguiente se muestra la imagen original y las tres imágenes más pequeñas.</span><span class="sxs-lookup"><span data-stu-id="92fec-118">The following illustration shows the original image and the three smaller images.</span></span>

![Ilustración en la que se muestra una imagen original grande y las tres imágenes más pequeñas de calidad variable](images/grapes1.png)

 

 



