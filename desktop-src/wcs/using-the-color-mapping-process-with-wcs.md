---
title: Uso del proceso de asignación de color con WCS
description: La asignación de colores WCS se basa en los perfiles de dispositivo.
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- Sistema de color de Windows (WCS), asignación de colores
- WCS (sistema de colores de Windows), asignación de colores
- Administración del color de imagen, asignación de colores
- Administración del color, asignación de colores
- colores, asignación de colores
- asignación de colores
- Sistema de color de Windows (WCS), perfiles de dispositivo
- WCS (sistema de colores de Windows), perfiles de dispositivo
- Administración del color de imagen, perfiles de dispositivo
- Administración del color, perfiles de dispositivo
- colores, perfiles de dispositivo
- Sistema de color de Windows (WCS), perfiles
- WCS (sistema de colores de Windows), perfiles
- Administración del color de imagen, perfiles
- Administración del color, perfiles
- colores, perfiles
- perfiles de dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 428b09749f3781def44e56ff6cea0539259d0464
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105721117"
---
# <a name="using-the-color-mapping-process-with-wcs"></a><span data-ttu-id="19c08-120">Uso del proceso de asignación de color con WCS</span><span class="sxs-lookup"><span data-stu-id="19c08-120">Using The Color Mapping Process with WCS</span></span>

<span data-ttu-id="19c08-121">La asignación de colores WCS se basa en los [perfiles de dispositivo](d.md).</span><span class="sxs-lookup"><span data-stu-id="19c08-121">WCS color mapping is based on [device profiles](d.md).</span></span> <span data-ttu-id="19c08-122">Los proporcionan los proveedores de dispositivos de hardware de color y se instalan cuando se instala un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19c08-122">These are supplied by vendors of color hardware devices and installed when a device is installed.</span></span> <span data-ttu-id="19c08-123">Cuando un programa de aplicación utiliza la asignación de colores, WCS accede al perfil de dispositivo de la imagen para obtener la información necesaria para convertir la imagen en los equipos.</span><span class="sxs-lookup"><span data-stu-id="19c08-123">When color mapping is used by an application program, WCS accesses the device profile of the image to get the information needed to convert the image to the PCS.</span></span> <span data-ttu-id="19c08-124">La conversión se realiza mediante la CMM.</span><span class="sxs-lookup"><span data-stu-id="19c08-124">The conversion is done by the CMM.</span></span>

<span data-ttu-id="19c08-125">Un perfil de dispositivo se puede incrustar en la propia imagen.</span><span class="sxs-lookup"><span data-stu-id="19c08-125">A device profile can be embedded into the image itself.</span></span> <span data-ttu-id="19c08-126">Por lo tanto, el perfil del dispositivo viaja con la imagen, incluso a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="19c08-126">So the device profile travels with the image, even across the Internet.</span></span> <span data-ttu-id="19c08-127">Un usuario no necesita el dispositivo de origen para obtener una asignación de color precisa.</span><span class="sxs-lookup"><span data-stu-id="19c08-127">A user does not need the source device to get an accurate color mapping.</span></span> <span data-ttu-id="19c08-128">Si una imagen no tiene un perfil de dispositivo, el espacio sRGB se utiliza como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="19c08-128">If an image does not have a device profile, the sRGB space is used as a default.</span></span> <span data-ttu-id="19c08-129">Para obtener más información, consulte [uso de la administración del color en Internet](using-color-management-on-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="19c08-129">For more details, see [Using Color Management on the Internet](using-color-management-on-the-internet.md).</span></span>

<span data-ttu-id="19c08-130">Tenga en cuenta que las aplicaciones que usan WCS nunca deben insertar el perfil sRGB en una imagen.</span><span class="sxs-lookup"><span data-stu-id="19c08-130">Note that applications which use WCS should never embed the sRGB profile into an image.</span></span> <span data-ttu-id="19c08-131">El espacio de colores sRGB proporciona un espacio de colores estandarizado en todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="19c08-131">The sRGB color space provides a standardized color space that is portable across all devices.</span></span> <span data-ttu-id="19c08-132">Está disponible automáticamente para los usuarios de Windows 98 y versiones posteriores, así como para Windows 2000 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="19c08-132">It is automatically available to users of Windows 98 and later as well as Windows 2000 and later.</span></span> <span data-ttu-id="19c08-133">Por lo tanto, no es necesario viajar con la imagen.</span><span class="sxs-lookup"><span data-stu-id="19c08-133">Therefore, it does not need to travel with the image.</span></span>

<span data-ttu-id="19c08-134">Una vez que los colores de la imagen están en los [equipos](p.md), WCS accede al perfil de dispositivo del dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="19c08-134">After the image colors are in the [PCS](p.md), WCS accesses the device profile of the destination device.</span></span> <span data-ttu-id="19c08-135">Obtiene la CMM para convertir los colores de la imagen de los equipos a la gama del dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="19c08-135">It gets the CMM to convert the image colors from PCS to the gamut of the destination device.</span></span>

<span data-ttu-id="19c08-136">También se puede realizar una asignación de colores más compleja con WCS.</span><span class="sxs-lookup"><span data-stu-id="19c08-136">More complex color mapping can also be done with WCS.</span></span> <span data-ttu-id="19c08-137">Por ejemplo, se puede usar para hacerse una idea del aspecto que tendrá una imagen creada en una pantalla de vídeo cuando se imprima en una impresora láser de alta resolución.</span><span class="sxs-lookup"><span data-stu-id="19c08-137">For example, it can be used to get an idea of what an image created on a video display would look like when printed on a high resolution laser printer.</span></span> <span data-ttu-id="19c08-138">El ejemplo se obtiene más complejo si solo hay una impresora de inyección de tinta estándar en la que se va a obtener una vista previa.</span><span class="sxs-lookup"><span data-stu-id="19c08-138">The example gets more complex if there is only a standard inkjet printer on which to preview it.</span></span> <span data-ttu-id="19c08-139">La imagen se puede convertir desde la gama de la pantalla hasta la gama de la impresora de inyección de tinta.</span><span class="sxs-lookup"><span data-stu-id="19c08-139">The image can be converted from the gamut of the display, into the gamut of the inkjet printer.</span></span> <span data-ttu-id="19c08-140">Desde allí, se puede convertir en la gama de la impresora láser.</span><span class="sxs-lookup"><span data-stu-id="19c08-140">From there it can converted into the gamut of the laser printer.</span></span> <span data-ttu-id="19c08-141">La imagen resultante se puede imprimir en la impresora de inyección de tinta.</span><span class="sxs-lookup"><span data-stu-id="19c08-141">The resulting image can be printed on the inkjet printer.</span></span> <span data-ttu-id="19c08-142">Por supuesto, la imagen tendría una resolución más alta cuando se imprimiera en la impresora láser de color.</span><span class="sxs-lookup"><span data-stu-id="19c08-142">Of course the image would be at a higher resolution when printed on the color laser printer.</span></span> <span data-ttu-id="19c08-143">Sin embargo, los colores de la imagen de prueba que se imprimen en la impresora de inyección de tinta serían una coincidencia aproximada con los colores que imprimiría la impresora láser.</span><span class="sxs-lookup"><span data-stu-id="19c08-143">However, the colors of the proofing image printed on the inkjet printer would be a close match to the colors that the laser printer would print.</span></span>

<span data-ttu-id="19c08-144">La forma en que se realizan las conversiones en el ejemplo consiste en convertir los colores de la imagen de la gama de la pantalla en los equipos.</span><span class="sxs-lookup"><span data-stu-id="19c08-144">The way the conversions in the example are accomplished is to convert the image colors from the display's gamut into the PCS.</span></span> <span data-ttu-id="19c08-145">Una vez convertidos los colores de la imagen en los equipos, el perfil de dispositivo de la impresora de inyección de tinta se utilizaría para transformarlos en la gama de la impresora de inyección de tinta.</span><span class="sxs-lookup"><span data-stu-id="19c08-145">After the image colors are converted into the PCS, the device profile of the inkjet printer would be used to transform them into the gamut of the inkjet printer.</span></span> <span data-ttu-id="19c08-146">A continuación, se utilizaría la transformación gama a PCS para devolver los colores a los equipos.</span><span class="sxs-lookup"><span data-stu-id="19c08-146">Next, the gamut to PCS transform would be used to move the colors back to the PCS.</span></span> <span data-ttu-id="19c08-147">A partir de ahí, el perfil de dispositivo de la impresora láser se usa para convertir los colores de los equipos a la gama de la impresora láser.</span><span class="sxs-lookup"><span data-stu-id="19c08-147">From there, the laser printer's device profile is used to convert the colors from PCS into the gamut of the laser printer.</span></span>

<span data-ttu-id="19c08-148">La capacidad de transformar fácilmente los colores de una gama de dispositivos en los equipos y viceversa permite que los colores de imagen que se destinan a un dispositivo de salida de color se prueben en casi cualquier otro.</span><span class="sxs-lookup"><span data-stu-id="19c08-148">The ability to easily transform colors from a device gamut to the PCS and back again enables image colors intended for one color output device to be proofed on almost any other.</span></span>

<span data-ttu-id="19c08-149">En el ejemplo anterior, la descripción varía del procedimiento real en cierto modo para mayor claridad.</span><span class="sxs-lookup"><span data-stu-id="19c08-149">In the preceding example, the description varies from the actual procedure somewhat for clarity.</span></span> <span data-ttu-id="19c08-150">En realidad, todas las transformaciones mencionadas en el párrafo anterior se concatenarían en una única transformación.</span><span class="sxs-lookup"><span data-stu-id="19c08-150">In reality, all of the transformations mentioned in the preceding paragraph would be concatenated into a single transformation.</span></span>

 

 




