---
description: Puede girar, reflejar y sesgar una imagen especificando los puntos de destino de las esquinas superior izquierda, superior derecha e inferior izquierda de la imagen original.
ms.assetid: 1e982d84-8749-451b-89a8-81440fcee439
title: Girar, reflejar y sesgar imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637cb8be0290d96a164042086e997bc878c0227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001660"
---
# <a name="rotating-reflecting-and-skewing-images"></a><span data-ttu-id="7e46e-103">Girar, reflejar y sesgar imágenes</span><span class="sxs-lookup"><span data-stu-id="7e46e-103">Rotating, Reflecting, and Skewing Images</span></span>

<span data-ttu-id="7e46e-104">Puede girar, reflejar y sesgar una imagen especificando los puntos de destino de las esquinas superior izquierda, superior derecha e inferior izquierda de la imagen original.</span><span class="sxs-lookup"><span data-stu-id="7e46e-104">You can rotate, reflect, and skew an image by specifying destination points for the upper-left, upper-right, and lower-left corners of the original image.</span></span> <span data-ttu-id="7e46e-105">Los tres puntos de destino determinan una transformación afín que asigna la imagen rectangular original a un paralelogramo.</span><span class="sxs-lookup"><span data-stu-id="7e46e-105">The three destination points determine an affine transformation that maps the original rectangular image to a parallelogram.</span></span> <span data-ttu-id="7e46e-106">(La esquina inferior derecha de la imagen original se asigna a la cuarta esquina del paralelogramo, que se calcula a partir de los tres puntos de destino especificados).</span><span class="sxs-lookup"><span data-stu-id="7e46e-106">(The lower-right corner of the original image is mapped to the fourth corner of the parallelogram, which is calculated from the three specified destination points.)</span></span>

<span data-ttu-id="7e46e-107">Por ejemplo, supongamos que la imagen original es un rectángulo con la esquina superior izquierda en (0,0), la esquina superior derecha en (100, 0) y la esquina inferior izquierda en (0, 50).</span><span class="sxs-lookup"><span data-stu-id="7e46e-107">For example, suppose the original image is a rectangle with upper-left corner at (0, 0), upper-right corner at (100, 0), and lower-left corner at (0, 50).</span></span> <span data-ttu-id="7e46e-108">Ahora Supongamos que asignamos esos tres puntos a los puntos de destino como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="7e46e-108">Now suppose we map those three points to destination points as follows.</span></span>



| <span data-ttu-id="7e46e-109">Punto original</span><span class="sxs-lookup"><span data-stu-id="7e46e-109">Original point</span></span>       | <span data-ttu-id="7e46e-110">Punto de destino</span><span class="sxs-lookup"><span data-stu-id="7e46e-110">Destination point</span></span> |
|----------------------|-------------------|
| <span data-ttu-id="7e46e-111">Superior izquierda (0,0)</span><span class="sxs-lookup"><span data-stu-id="7e46e-111">Upper-left (0, 0)</span></span>    | <span data-ttu-id="7e46e-112">(200, 20)</span><span class="sxs-lookup"><span data-stu-id="7e46e-112">(200, 20)</span></span>         |
| <span data-ttu-id="7e46e-113">Superior derecha (100)</span><span class="sxs-lookup"><span data-stu-id="7e46e-113">Upper-right (100, 0)</span></span> | <span data-ttu-id="7e46e-114">(110, 100)</span><span class="sxs-lookup"><span data-stu-id="7e46e-114">(110, 100)</span></span>        |
| <span data-ttu-id="7e46e-115">Inferior izquierda (0, 50)</span><span class="sxs-lookup"><span data-stu-id="7e46e-115">Lower-left (0, 50)</span></span>   | <span data-ttu-id="7e46e-116">(250, 30)</span><span class="sxs-lookup"><span data-stu-id="7e46e-116">(250, 30)</span></span>         |



 

<span data-ttu-id="7e46e-117">En la ilustración siguiente se muestra la imagen original y la imagen asignada al paralelogramo.</span><span class="sxs-lookup"><span data-stu-id="7e46e-117">The following illustration shows the original image and the image mapped to the parallelogram.</span></span> <span data-ttu-id="7e46e-118">La imagen original se ha sesgado, reflejado, girado y traducido.</span><span class="sxs-lookup"><span data-stu-id="7e46e-118">The original image has been skewed, reflected, rotated, and translated.</span></span> <span data-ttu-id="7e46e-119">El eje x a lo largo del borde superior de la imagen original se asigna a la línea que se ejecuta a través de (200, 20) y (110, 100).</span><span class="sxs-lookup"><span data-stu-id="7e46e-119">The x-axis along the top edge of the original image is mapped to the line that runs through (200, 20) and (110, 100).</span></span> <span data-ttu-id="7e46e-120">El eje y a lo largo del borde izquierdo de la imagen original se asigna a la línea que se ejecuta a través de (200, 20) y (250, 30).</span><span class="sxs-lookup"><span data-stu-id="7e46e-120">The y-axis along the left edge of the original image is mapped to the line that runs through (200, 20) and (250, 30).</span></span>

![Ilustración en la que se muestran las franjas en color en el origen de los ejes de coordenadas y las mismas franjas sesgadas y en una ubicación, rotación y tamaño diferentes](images/stripes1.png)

<span data-ttu-id="7e46e-122">En el ejemplo siguiente se generan las imágenes que se muestran en la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="7e46e-122">The following example produces the images shown in the preceding illustration.</span></span>


```
Point destinationPoints[] = {
   Point(200, 20),   // destination for upper-left point of original
   Point(110, 100),  // destination for upper-right point of original
   Point(250, 30)};  // destination for lower-left point of original
Image image(L"Stripes.bmp");
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw the image mapped to the parallelogram.
graphics.DrawImage(&image, destinationPoints, 3); 
```



<span data-ttu-id="7e46e-123">En la ilustración siguiente se muestra una transformación similar que se aplica a una imagen fotográfica.</span><span class="sxs-lookup"><span data-stu-id="7e46e-123">The following illustration shows a similar transformation applied to a photographic image.</span></span>

![Ilustración en la que se muestra la misma foto dos veces; la segunda se revierte, sesga y tiene un tamaño, una rotación y una ubicación diferentes](images/transformedclimber.png)

<span data-ttu-id="7e46e-125">En la ilustración siguiente se muestra una transformación similar que se aplica a un metarchivo.</span><span class="sxs-lookup"><span data-stu-id="7e46e-125">The following illustration shows a similar transformation applied to a metafile.</span></span>

![Ilustración en la que se muestran formas y texto, pero de nuevo, pero se revierten, se sesgan y con una ubicación, una rotación y un tamaño diferentes.](images/transformedmetafile.png)

 

 



