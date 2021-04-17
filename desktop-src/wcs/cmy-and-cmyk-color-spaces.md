---
title: Espacios de color CMY y CMYK
description: Los espacios de colores CMY y CMYK se suelen usar en la impresión en color. Un espacio de colores CMY usa cian, magenta y amarillo (CMY) como sus colores primarios. Rojo, verde y azul son los colores secundarios.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Sistema de color de Windows (WCS), espacios de colores CMY
- WCS (sistema de colores de Windows), espacios de colores CMY
- Administración del color de imagen, espacios de colores CMY
- Administración del color, espacios de colores CMY
- colores, espacios de colores CMY
- espacios de colores, CMY
- Espacios de colores CMY
- Sistema de color de Windows (WCS), espacios de color CMYK
- WCS (sistema de colores de Windows), espacios de color CMYK
- Administración del color de imagen, espacios de color CMYK
- Administración del color, espacios de CMYKcolor
- colores, espacios de color CMYK
- espacios de colores, CMYK
- Espacios de colores CMYK
- cyan
- magenta
- yellow
- Aguamarina fucsia amarillo (CMY)
- CMY (aguamarina fucsia amarillo)
- Aguamarina fucsia amarillo negro (CMYK)
- CMYK (aguamarina fucsia amarillo negro)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52622c929222eb9027b6272137a8b897210697b6
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105721107"
---
# <a name="cmy-and-cmyk-color-spaces"></a><span data-ttu-id="ec5fd-126">Espacios de color CMY y CMYK</span><span class="sxs-lookup"><span data-stu-id="ec5fd-126">CMY and CMYK Color Spaces</span></span>

<span data-ttu-id="ec5fd-127">Los [espacios de colores](c.md) CMY y CMYK se suelen usar en la impresión en color.</span><span class="sxs-lookup"><span data-stu-id="ec5fd-127">The CMY and CMYK [color spaces](c.md) are often used in color printing.</span></span> <span data-ttu-id="ec5fd-128">Un espacio de colores CMY usa cian, magenta y amarillo (CMY) como sus [colores primarios](p.md).</span><span class="sxs-lookup"><span data-stu-id="ec5fd-128">A CMY color space uses cyan, magenta, and yellow (CMY) as its [primary colors](p.md).</span></span> <span data-ttu-id="ec5fd-129">Rojo, verde y azul son los colores secundarios.</span><span class="sxs-lookup"><span data-stu-id="ec5fd-129">Red, green, and blue are the secondary colors.</span></span>

<span data-ttu-id="ec5fd-130">Las siguientes figuras son representaciones de color del espacio de colores CMY.</span><span class="sxs-lookup"><span data-stu-id="ec5fd-130">The following figures are color representations of the CMY color space.</span></span> <span data-ttu-id="ec5fd-131">El espacio de colores CMY se normaliza.</span><span class="sxs-lookup"><span data-stu-id="ec5fd-131">The CMY color space is normalized.</span></span>

![cubo de espacio de colores CMY en valores máximos](images/cmyclrs1.png)

![cubo de espacio de colores CMY con valores mínimos](images/cmyclrs2.png)

<span data-ttu-id="ec5fd-134">El espacio de colores CMY es sustractivo.</span><span class="sxs-lookup"><span data-stu-id="ec5fd-134">The CMY color space is subtractive.</span></span> <span data-ttu-id="ec5fd-135">Por lo tanto, el blanco está en (0,0, 0,0, 0,0) y el negro está en (1,0, 1,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="ec5fd-135">Therefore, white is at (0.0, 0.0, 0.0) and black is at (1.0, 1.0, 1.0).</span></span> <span data-ttu-id="ec5fd-136">Si empieza con blanco y no resta ningún color, obtendrá blanco.</span><span class="sxs-lookup"><span data-stu-id="ec5fd-136">If you start with white and subtract no colors, you get white.</span></span> <span data-ttu-id="ec5fd-137">Si empieza por blanco y resta todos los colores por igual, obtendrá el color negro.</span><span class="sxs-lookup"><span data-stu-id="ec5fd-137">If you start with white and subtract all colors equally, you get black.</span></span>

<span data-ttu-id="ec5fd-138">El espacio de colores CMYK es una variación del modelo CMY.</span><span class="sxs-lookup"><span data-stu-id="ec5fd-138">The CMYK color space is a variation on the CMY model.</span></span> <span data-ttu-id="ec5fd-139">Agrega negro (aguamarina, fucsia, amarillo y negro).</span><span class="sxs-lookup"><span data-stu-id="ec5fd-139">It adds black (Cyan, Magenta, Yellow, and blacK).</span></span> <span data-ttu-id="ec5fd-140">El espacio de colores CMYK cierra el intervalo entre la teoría y la práctica.</span><span class="sxs-lookup"><span data-stu-id="ec5fd-140">The CMYK color space closes the gap between theory and practice.</span></span> <span data-ttu-id="ec5fd-141">En teoría, no es necesario el componente negro extra.</span><span class="sxs-lookup"><span data-stu-id="ec5fd-141">In theory, the extra black component is not needed.</span></span> <span data-ttu-id="ec5fd-142">Sin embargo, la experiencia con varios tipos de tintas y documentos ha demostrado que cuando se mezclan los componentes iguales de las tintas cian, magenta y amarillo, el resultado suele ser oscuro marrón, no negro.</span><span class="sxs-lookup"><span data-stu-id="ec5fd-142">However, experience with various types of inks and papers has shown that when equal components of cyan, magenta, and yellow inks are mixed, the result is usually a dark brown, not black.</span></span> <span data-ttu-id="ec5fd-143">La adición de una tinta negra a la mezcla soluciona este problema.</span><span class="sxs-lookup"><span data-stu-id="ec5fd-143">Adding black ink to the mix solves this problem.</span></span>

<span data-ttu-id="ec5fd-144">Los espacios de colores CMY y CMYK pueden ser independientes del dispositivo, pero normalmente se usan en referencia a un dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="ec5fd-144">The CMY and CMYK colors spaces can be device independent, but most often they are used in reference to a specific device.</span></span>

 

 




