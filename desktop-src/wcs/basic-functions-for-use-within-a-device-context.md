---
title: Funciones básicas para usar en un contexto de dispositivo
description: Las siguientes funciones WCS proporcionan funciones de asignación de color básicas dentro de los contextos de dispositivo. Son útiles para todas las aplicaciones que necesitan implementar la administración del color con baja sobrecarga y mínima intervención del usuario.
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- Sistema de color de Windows (WCS), funciones
- WCS (sistema de colores de Windows), funciones
- Administración del color de imagen, funciones
- Administración del color, funciones
- colores, funciones
- Referencia WCS, funciones
- referencia de las funciones WCS,
- Sistema de color de Windows (WCS), contextos de dispositivo
- WCS (sistema de colores de Windows), contextos de dispositivo
- Administración del color de imagen, contextos de dispositivo
- Administración del color, contextos de dispositivo
- colores, contextos de dispositivo
- Referencia WCS, contextos de dispositivo
- referencia de WCS, contextos de dispositivo
- contextos de dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde99ed077af108ddc20c73f86e17bedfe1d4a8c
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "105721167"
---
# <a name="basic-functions-for-use-within-a-device-context"></a><span data-ttu-id="0689a-119">Funciones básicas para usar en un contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="0689a-119">Basic Functions for Use Within a Device Context</span></span>

<span data-ttu-id="0689a-120">Las siguientes funciones WCS proporcionan funciones de [asignación de color](c.md) básicas dentro de los contextos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0689a-120">The following WCS functions deliver basic [color mapping](c.md) capabilities within device contexts.</span></span> <span data-ttu-id="0689a-121">Son útiles para todas las aplicaciones que necesitan implementar la administración del color con baja sobrecarga y mínima intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="0689a-121">They are useful to all applications that need to implement color management with low overhead and minimal user intervention.</span></span>



| <span data-ttu-id="0689a-122">Función</span><span class="sxs-lookup"><span data-stu-id="0689a-122">Function</span></span>                                                           | <span data-ttu-id="0689a-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="0689a-123">Description</span></span>                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0689a-124">**CheckColorsInGamut**</span><span class="sxs-lookup"><span data-stu-id="0689a-124">**CheckColorsInGamut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | <span data-ttu-id="0689a-125">Comprueba si determinados colores se encuentran en la gama de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0689a-125">Checks if given colors are in a device's gamut.</span></span>                                                                                                     |
| [<span data-ttu-id="0689a-126">**ColorCorrectPalette**</span><span class="sxs-lookup"><span data-stu-id="0689a-126">**ColorCorrectPalette**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | <span data-ttu-id="0689a-127">Corrige las entradas de una paleta para un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0689a-127">Corrects the entries in a palette for a device context.</span></span>                                                                                             |
| [<span data-ttu-id="0689a-128">**ColorMatchToTarget**</span><span class="sxs-lookup"><span data-stu-id="0689a-128">**ColorMatchToTarget**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | <span data-ttu-id="0689a-129">Realiza la asignación de colores para fines de vista previa.</span><span class="sxs-lookup"><span data-stu-id="0689a-129">Performs color mapping for preview purposes.</span></span>                                                                                                        |
| [<span data-ttu-id="0689a-130">**CreateColorSpace**</span><span class="sxs-lookup"><span data-stu-id="0689a-130">**CreateColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | <span data-ttu-id="0689a-131">Crea un espacio de colores.</span><span class="sxs-lookup"><span data-stu-id="0689a-131">Creates a color space.</span></span>                                                                                                                              |
| [<span data-ttu-id="0689a-132">**DeleteColorSpace**</span><span class="sxs-lookup"><span data-stu-id="0689a-132">**DeleteColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | <span data-ttu-id="0689a-133">Elimina un espacio de colores.</span><span class="sxs-lookup"><span data-stu-id="0689a-133">Deletes a color space.</span></span>                                                                                                                              |
| [<span data-ttu-id="0689a-134">**EnumICMProfiles**</span><span class="sxs-lookup"><span data-stu-id="0689a-134">**EnumICMProfiles**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | <span data-ttu-id="0689a-135">Enumera los perfiles de color de salida disponibles para un contexto de dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="0689a-135">Enumerates output color profiles available for a given device context.</span></span>                                                                              |
| [<span data-ttu-id="0689a-136">**EnumICMProfilesProcCallback**</span><span class="sxs-lookup"><span data-stu-id="0689a-136">**EnumICMProfilesProcCallback**</span></span>](/windows/desktop/api/Wingdi/) | <span data-ttu-id="0689a-137">Función de devolución de llamada definida por la aplicación para [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).</span><span class="sxs-lookup"><span data-stu-id="0689a-137">Application-defined callback function for [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).</span></span> <span data-ttu-id="0689a-138">La aplicación también define el nombre de esta función.</span><span class="sxs-lookup"><span data-stu-id="0689a-138">The name of this function is also defined by the application.</span></span> |
| [<span data-ttu-id="0689a-139">**GetColorSpace**</span><span class="sxs-lookup"><span data-stu-id="0689a-139">**GetColorSpace**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | <span data-ttu-id="0689a-140">Obtiene el espacio de colores de entrada actual en un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0689a-140">Gets the current input color space in a device context.</span></span> |
| [<span data-ttu-id="0689a-141">**GetICMProfile**</span><span class="sxs-lookup"><span data-stu-id="0689a-141">**GetICMProfile**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | <span data-ttu-id="0689a-142">Obtiene el perfil de color de salida actual de un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0689a-142">Gets the current output color profile of a device context.</span></span>                                                                                          |
| [<span data-ttu-id="0689a-143">**GetLogColorSpace**</span><span class="sxs-lookup"><span data-stu-id="0689a-143">**GetLogColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | <span data-ttu-id="0689a-144">Obtiene la estructura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) de un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0689a-144">Gets the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure of a device context.</span></span>                                                                      |
| [<span data-ttu-id="0689a-145">**SetColorSpace**</span><span class="sxs-lookup"><span data-stu-id="0689a-145">**SetColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | <span data-ttu-id="0689a-146">Establece el espacio de colores de entrada de un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0689a-146">Sets a device context's input color space.</span></span>                                                                                                          |
| [<span data-ttu-id="0689a-147">**SetICMMode**</span><span class="sxs-lookup"><span data-stu-id="0689a-147">**SetICMMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | <span data-ttu-id="0689a-148">Activa o desactiva la administración del color en un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0689a-148">Turns color management on or off in a device context.</span></span>                                                                                               |
| [<span data-ttu-id="0689a-149">**SetICMProfile**</span><span class="sxs-lookup"><span data-stu-id="0689a-149">**SetICMProfile**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | <span data-ttu-id="0689a-150">Establece el perfil de color de salida para un contexto de dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="0689a-150">Sets the output color profile for a given device context.</span></span>                                                                                           |
| [<span data-ttu-id="0689a-151">**WcsEnumColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="0689a-151">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | <span data-ttu-id="0689a-152">Enumera todos los perfiles de color que cumplen los criterios de enumeración en el ámbito de administración de perfiles especificado.</span><span class="sxs-lookup"><span data-stu-id="0689a-152">Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.</span></span>                                      |



 

 

 




