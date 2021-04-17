---
title: Espacios de color HLS
description: Los artistas también usan los espacios de colores HLS. Sus componentes de color son matiz, luminosidad y saturación (croma).
ms.assetid: 8c80d200-c4d0-4233-8f53-a9637dff9ab2
keywords:
- Sistema de color de Windows (WCS), espacios de color HLS
- WCS (sistema de colores de Windows), espacios de color HLS
- Administración del color de imagen, espacios de color HLS
- Administración del color, espacios de color HLS
- colores, espacios de color HLS
- espacios de colores, HLS
- Espacios de color HLS
- altera
- satura
- luminosidad
- saturación cero
- saturación de luminosidad de matiz (HLS)
- HLS (saturación de luminosidad de matiz)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613a62d4a998b51f9bfb22bd7431dd8645a72f3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105721119"
---
# <a name="hls-color-spaces"></a><span data-ttu-id="37059-117">Espacios de color HLS</span><span class="sxs-lookup"><span data-stu-id="37059-117">HLS Color Spaces</span></span>

<span data-ttu-id="37059-118">Los artistas también usan los [espacios de colores](c.md) HLS.</span><span class="sxs-lookup"><span data-stu-id="37059-118">HLS [color spaces](c.md) are also widely used by artists.</span></span> <span data-ttu-id="37059-119">Sus componentes de color son matiz, luminosidad y saturación (croma).</span><span class="sxs-lookup"><span data-stu-id="37059-119">Its color components are hue, lightness, and saturation (chroma).</span></span>

<span data-ttu-id="37059-120">Hue tiene el mismo significado que el modelo HSV, salvo que un ángulo de matiz de 0 corresponde a Blue en este modelo.</span><span class="sxs-lookup"><span data-stu-id="37059-120">Hue has the same meaning as the HSV model, except that a hue angle of 0 corresponds to blue in this model.</span></span> <span data-ttu-id="37059-121">Magenta está en 60, el rojo está en 120.</span><span class="sxs-lookup"><span data-stu-id="37059-121">Magenta is at 60, red is at 120.</span></span> <span data-ttu-id="37059-122">Al igual que con el modelo HSV, los colores complementarios están separados por 180.</span><span class="sxs-lookup"><span data-stu-id="37059-122">As with the HSV model, complementary colors are 180 apart.</span></span>

<span data-ttu-id="37059-123">La luminosidad es la cantidad de blanco o negro en un color.</span><span class="sxs-lookup"><span data-stu-id="37059-123">Lightness is the amount of black or white in a color.</span></span> <span data-ttu-id="37059-124">Aumentar la luminosidad agrega blanco al matiz.</span><span class="sxs-lookup"><span data-stu-id="37059-124">Increasing lightness adds white to the hue.</span></span> <span data-ttu-id="37059-125">Al reducir la luminosidad, se agrega negro al matiz.</span><span class="sxs-lookup"><span data-stu-id="37059-125">Decreasing lightness adds black to the hue.</span></span>

<span data-ttu-id="37059-126">La [saturación](s.md) del modelo HLS es una medida de la "pureza" de un matiz.</span><span class="sxs-lookup"><span data-stu-id="37059-126">[Saturation](s.md) in the HLS model is a measure of the "purity" of a hue.</span></span> <span data-ttu-id="37059-127">A medida que se reduce la saturación, el matiz se vuelve más gris.</span><span class="sxs-lookup"><span data-stu-id="37059-127">As saturation is decreased, the hue becomes more gray.</span></span> <span data-ttu-id="37059-128">Un valor de saturación de cero da como resultado un valor de escala de grises.</span><span class="sxs-lookup"><span data-stu-id="37059-128">A saturation value of zero results in a gray-scale value.</span></span>

<span data-ttu-id="37059-129">La siguiente ilustración es un dibujo de línea del espacio HLS, que es un doble hexcone.</span><span class="sxs-lookup"><span data-stu-id="37059-129">The following figure is a line drawing of HLS space, which is a double hexcone.</span></span> <span data-ttu-id="37059-130">Cualquier sección transversal horizontal del espacio de colores HLS es un hexágono.</span><span class="sxs-lookup"><span data-stu-id="37059-130">Any horizontal cross section of the HLS color space is a hexagon.</span></span> <span data-ttu-id="37059-131">HLS es un espacio de colores normalizado.</span><span class="sxs-lookup"><span data-stu-id="37059-131">HLS is a normalized color space.</span></span> <span data-ttu-id="37059-132">Es decir, los valores de luminosidad y saturación van de 0,0 a 1,0, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="37059-132">That is, the lightness and saturation values range from 0.0 to 1.0 inclusive.</span></span> <span data-ttu-id="37059-133">Hue varía entre 0 y 360, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="37059-133">Hue varies from 0 to 360 inclusive.</span></span>

![espacio de color HLS](images/hlsline.png)

<span data-ttu-id="37059-135">Los espacios de colores HLS pueden ser dependientes del dispositivo o independientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37059-135">HLS color spaces can be device dependent or device independent.</span></span>

 

 




