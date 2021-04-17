---
title: Conversión de colores y coincidencia de color
description: El proceso de conversión de colores de un espacio de colores a otro se denomina conversión de color.
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- Sistema de color de Windows (WCS), conversión de color
- WCS (sistema de color de Windows), conversión de color
- Administración del color de imagen, conversión de color
- Administración del color, conversión de color
- colores, conversión de color
- conversión de color
- Sistema de color de Windows (WCS), coincidencia de color
- WCS (sistema de colores de Windows), coincidencia de color
- Administración del color de imagen, coincidencia de color
- Administración del color, coincidencia de color
- colores, coincidencia de color
- coincidencia de color
- Sistema de color de Windows (WCS), asignación de colores
- WCS (sistema de colores de Windows), asignación de colores
- Administración del color de imagen, asignación de colores
- Administración del color, asignación de colores
- colores, asignación de colores
- asignación de colores
- punto blanco
- colorants
- corrección gamma
- espectro
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74de95238472f58d49c5033a601c6d5458773c8
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105721130"
---
# <a name="color-conversion-and-color-matching"></a><span data-ttu-id="d02ee-125">Conversión de colores y coincidencia de color</span><span class="sxs-lookup"><span data-stu-id="d02ee-125">Color Conversion and Color Matching</span></span>

<span data-ttu-id="d02ee-126">El proceso de conversión de colores de un [espacio de colores](c.md) a otro se denomina conversión de *color*.</span><span class="sxs-lookup"><span data-stu-id="d02ee-126">The process of converting colors from one [color space](c.md) to another is called *color conversion*.</span></span> <span data-ttu-id="d02ee-127">Todos los colores de un espacio de colores son fijos en relación con el [punto blanco](w.md)del espacio de colores.</span><span class="sxs-lookup"><span data-stu-id="d02ee-127">All colors in a color space are fixed relative to the color space's [white point](w.md).</span></span> <span data-ttu-id="d02ee-128">Dado que el punto blanco de un espacio de colores varía de un dispositivo a otro, un color convertido debe coincidir con su color visualmente más cercano en el espacio de colores de destino.</span><span class="sxs-lookup"><span data-stu-id="d02ee-128">Since the white point of a color space varies from device to device, a converted color must then be matched to its visually closest color in the destination color space.</span></span> <span data-ttu-id="d02ee-129">Este proceso se denomina *asignación de colores*.</span><span class="sxs-lookup"><span data-stu-id="d02ee-129">This process is called *color mapping*.</span></span>

<span data-ttu-id="d02ee-130">Por ejemplo, si tiene una imagen digital que ha creado en la pantalla, puede que esté en un espacio de colores RGB dependiente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d02ee-130">For example, if you have a digital image that you created on your display, it may be in a device-dependent RGB color space.</span></span> <span data-ttu-id="d02ee-131">Si desea imprimirlo en una impresora, debe convertirse en el espacio de colores de la impresora.</span><span class="sxs-lookup"><span data-stu-id="d02ee-131">If you want to print it on a printer, it must be converted to the printer's color space.</span></span> <span data-ttu-id="d02ee-132">Dado que es probable que la impresora use un espacio de colores CMYK dependiente del dispositivo, todos los valores RGB se deben convertir a CYMK.</span><span class="sxs-lookup"><span data-stu-id="d02ee-132">Since the printer probably uses a device-dependent CMYK color space, all RGB values must be converted to CYMK.</span></span> <span data-ttu-id="d02ee-133">Esta es la [conversión de color](c.md).</span><span class="sxs-lookup"><span data-stu-id="d02ee-133">This is [color conversion](c.md).</span></span> <span data-ttu-id="d02ee-134">Una vez que los valores se especifican en términos del espacio CYMK, tienen que coincidir con el color más cercano que puede producir la impresora.</span><span class="sxs-lookup"><span data-stu-id="d02ee-134">Once the values are specified in terms of the CYMK space, they need to be matched to the closest color that the printer can produce.</span></span> <span data-ttu-id="d02ee-135">Esto se denomina asignación de colores o [coincidencia de color](c.md).</span><span class="sxs-lookup"><span data-stu-id="d02ee-135">This is called color mapping or [color matching](c.md).</span></span>

<span data-ttu-id="d02ee-136">Tanto la conversión de color como la asignación de colores deben tener en cuenta varios factores específicos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d02ee-136">Both color conversion and color mapping must take into account a number of device-specific factors.</span></span> <span data-ttu-id="d02ee-137">Por ejemplo, los bloques de creación de las imágenes de pantalla son píxeles.</span><span class="sxs-lookup"><span data-stu-id="d02ee-137">For instance, the building blocks of screen images are pixels.</span></span> <span data-ttu-id="d02ee-138">Cada píxel tiene un número de bits establecido para almacenar su valor de índice de color o color.</span><span class="sxs-lookup"><span data-stu-id="d02ee-138">Each pixel has a set number of bits to store its color or color index value.</span></span> <span data-ttu-id="d02ee-139">El número de bits por píxel depende del tipo de adaptador de pantalla y de pantalla que se use, y del modo en el que se establece el adaptador.</span><span class="sxs-lookup"><span data-stu-id="d02ee-139">The number of bits per pixel depends on the type of display and display adapter being used, and the mode to which that the adapter is set.</span></span> <span data-ttu-id="d02ee-140">La mayoría de los tipos de impresora utiliza diferentes [Colorants](c.md) e imprime en determinadas resoluciones.</span><span class="sxs-lookup"><span data-stu-id="d02ee-140">Most every printer type uses different [colorants](c.md) and prints at particular resolutions.</span></span>

<span data-ttu-id="d02ee-141">Además, las características de tono físico de un dispositivo suelen ser diferentes en distintos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d02ee-141">In addition, the physical tone characteristics of a device are often different on different devices.</span></span> <span data-ttu-id="d02ee-142">Por ejemplo, cuando los monitores de equipo generan colores, pueden aparecer diferentes de lo que si se hubieran producido en una imprenta.</span><span class="sxs-lookup"><span data-stu-id="d02ee-142">For instance, when colors are produced by computer monitors, they can appear different than they would if they were produced on a printing press.</span></span> <span data-ttu-id="d02ee-143">Un factor de corrección, denominado *corrección Gamma*, se usa con frecuencia para compensar tales diferencias.</span><span class="sxs-lookup"><span data-stu-id="d02ee-143">A correction factor, called *gamma correction*, is frequently used to compensate for such differences.</span></span>

<span data-ttu-id="d02ee-144">El resultado de estos factores dependientes del dispositivo es que cada dispositivo de color tiene un conjunto determinado de colores que puede generar.</span><span class="sxs-lookup"><span data-stu-id="d02ee-144">The result of these device-dependent factors is that each color device has a particular set of colors that it can produce.</span></span> <span data-ttu-id="d02ee-145">Este conjunto de colores se conoce como su *gama*.</span><span class="sxs-lookup"><span data-stu-id="d02ee-145">This color set is known as its *gamut*.</span></span> <span data-ttu-id="d02ee-146">Para realizar la conversión de colores y la asignación de colores, los colores de una imagen se deben convertir del espacio de colores y la gama del dispositivo de origen en el espacio de colores del dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="d02ee-146">To perform color conversion and color mapping, the colors in an image must be converted from the color space and gamut of the source device into the color space of the destination device.</span></span> <span data-ttu-id="d02ee-147">Después, se asocian a la gama del dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="d02ee-147">They are then matched into the gamut of the destination device.</span></span>

 

 




