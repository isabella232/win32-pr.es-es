---
title: Funciones de calibración y caracterización de dispositivos
description: Las siguientes funciones son útiles para escribir herramientas de calibración y caracterización de dispositivos necesarias para instalar y calibrar los dispositivos de pantalla de color, como monitores e impresoras.
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- Sistema de color de Windows (WCS), funciones
- WCS (sistema de colores de Windows), funciones
- Administración del color de imagen, funciones
- Administración del color, funciones
- colores, funciones
- Referencia WCS, funciones
- referencia de las funciones WCS,
- Sistema de color de Windows (WCS), calibración de dispositivos
- WCS (sistema de colores de Windows), calibración de dispositivos
- Administración del color de imagen, calibración de dispositivos
- Administración del color, calibración de dispositivos
- colores, calibración de dispositivos
- Referencia WCS, calibración de dispositivos
- referencia de WCS, calibración de dispositivos
- Sistema de color de Windows (WCS), caracterización
- WCS (sistema de colores de Windows), caracterización
- Administración del color de imagen, caracterización
- Administración del color, caracterización
- colores, caracterización
- Referencia WCS, caracterización
- referencia de WCS, caracterización
- calibración de dispositivos
- curva
- caracterización
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3367bbc6385cc21c8dbff3a88bed685616fb3f29
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105721423"
---
# <a name="device-calibration-and-characterization-functions"></a><span data-ttu-id="a55be-127">Funciones de calibración y caracterización de dispositivos</span><span class="sxs-lookup"><span data-stu-id="a55be-127">Device Calibration and Characterization Functions</span></span>

<span data-ttu-id="a55be-128">Las siguientes funciones son útiles para escribir herramientas de calibración y caracterización de dispositivos necesarias para instalar y calibrar los dispositivos de pantalla de color, como monitores e impresoras.</span><span class="sxs-lookup"><span data-stu-id="a55be-128">The following functions are useful for writing device calibration and characterization tools needed for installing and calibrating color display devices such as monitors and printers.</span></span>



| <span data-ttu-id="a55be-129">Función</span><span class="sxs-lookup"><span data-stu-id="a55be-129">Function</span></span> | <span data-ttu-id="a55be-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a55be-130">Description</span></span> |
|-|-|
| [<span data-ttu-id="a55be-131">**CloseColorProfile**</span><span class="sxs-lookup"><span data-stu-id="a55be-131">**CloseColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-closecolorprofile) | <span data-ttu-id="a55be-132">Cierra un identificador de perfil abierto.</span><span class="sxs-lookup"><span data-stu-id="a55be-132">Closes an open profile handle.</span></span> |
| [<span data-ttu-id="a55be-133">**CreateDeviceLinkProfile**</span><span class="sxs-lookup"><span data-stu-id="a55be-133">**CreateDeviceLinkProfile**</span></span>](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | <span data-ttu-id="a55be-134">Crea un *Perfil de vínculo de dispositivo* de International color Consortium (ICC) a partir de un conjunto de perfiles de color, con las intenciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="a55be-134">Creates an International Color Consortium (ICC) *device link profile* from a set of color profiles, using the specified intents.</span></span> |
| [<span data-ttu-id="a55be-135">**GetColorProfileElement**</span><span class="sxs-lookup"><span data-stu-id="a55be-135">**GetColorProfileElement**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | <span data-ttu-id="a55be-136">Copia datos de un elemento de perfil etiquetado especificado de un perfil de color especificado en un búfer.</span><span class="sxs-lookup"><span data-stu-id="a55be-136">Copies data from a specified tagged profile element of a specified color profile into a buffer.</span></span> |
| [<span data-ttu-id="a55be-137">**GetColorProfileElementTag**</span><span class="sxs-lookup"><span data-stu-id="a55be-137">**GetColorProfileElementTag**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | <span data-ttu-id="a55be-138">Recupera el nombre de etiqueta especificado por *dwIndex* en la tabla de etiquetas de un perfil de color de International color Consortium (ICC) determinado, donde *dwIndex* es un índice basado en uno de la tabla.</span><span class="sxs-lookup"><span data-stu-id="a55be-138">Retrieves the tag name specified by *dwIndex* in the tag table of a given International Color Consortium (ICC) color profile, where *dwIndex* is a one-based index into that table.</span></span> |
| [<span data-ttu-id="a55be-139">**GetColorProfileFromHandle**</span><span class="sxs-lookup"><span data-stu-id="a55be-139">**GetColorProfileFromHandle**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| <span data-ttu-id="a55be-140">Recupera el contenido del perfil de color dado un identificador a un perfil de color abierto.</span><span class="sxs-lookup"><span data-stu-id="a55be-140">Retrieves the color profile contents given a handle to an open color profile.</span></span>     |
| [<span data-ttu-id="a55be-141">**GetColorProfileHeader**</span><span class="sxs-lookup"><span data-stu-id="a55be-141">**GetColorProfileHeader**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | <span data-ttu-id="a55be-142">Recupera o deriva la estructura de encabezado de ICC de un perfil de color ICC o de un perfil XML WCS.</span><span class="sxs-lookup"><span data-stu-id="a55be-142">Retrieves or derives ICC header structure from either ICC color profile or WCS XML profile.</span></span> <span data-ttu-id="a55be-143">Los controladores y las aplicaciones deben suponer que devolver **true** solo indica que se devuelve un encabezado estructurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a55be-143">Drivers and applications should assume returning **TRUE** only indicates that a properly structured header is returned.</span></span> <span data-ttu-id="a55be-144">Cada etiqueta todavía tendrá que validarse de forma independiente mediante las API de ICM2 heredadas o las API de esquemas XML.</span><span class="sxs-lookup"><span data-stu-id="a55be-144">Each tag will still need to be validated independently using either legacy ICM2 APIs or XML schema APIs.</span></span> |
| [<span data-ttu-id="a55be-145">**GetCountColorProfileElements**</span><span class="sxs-lookup"><span data-stu-id="a55be-145">**GetCountColorProfileElements**</span></span>](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | <span data-ttu-id="a55be-146">Recupera el número de elementos etiquetados en un perfil de color determinado.</span><span class="sxs-lookup"><span data-stu-id="a55be-146">Retrieves the number of tagged elements in a given color profile.</span></span> |
| [<span data-ttu-id="a55be-147">**GetPS2ColorRenderingDictionary**</span><span class="sxs-lookup"><span data-stu-id="a55be-147">**GetPS2ColorRenderingDictionary**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | <span data-ttu-id="a55be-148">Recupera el Diccionario de representación del color PostScript de nivel 2 del perfil de color ICC especificado.</span><span class="sxs-lookup"><span data-stu-id="a55be-148">Retrieves the PostScript Level 2 color rendering dictionary from the specified ICC color profile.</span></span> |
| [<span data-ttu-id="a55be-149">**GetPS2ColorRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="a55be-149">**GetPS2ColorRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | <span data-ttu-id="a55be-150">Recupera el [intento de representación](r.md) de color PostScript de nivel 2 de un perfil de color ICC.</span><span class="sxs-lookup"><span data-stu-id="a55be-150">Retrieves the PostScript Level 2 color [rendering intent](r.md) from an ICC color profile.</span></span> |
| [<span data-ttu-id="a55be-151">**GetPS2ColorSpaceArray**</span><span class="sxs-lookup"><span data-stu-id="a55be-151">**GetPS2ColorSpaceArray**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | <span data-ttu-id="a55be-152">Recupera la matriz de [espacio de colores](c.md) PostScript de nivel 2 de un perfil de color ICC.</span><span class="sxs-lookup"><span data-stu-id="a55be-152">Retrieves the PostScript Level 2 [color space](c.md) array from an ICC color profile.</span></span> |
| [<span data-ttu-id="a55be-153">**IsColorProfileTagPresent**</span><span class="sxs-lookup"><span data-stu-id="a55be-153">**IsColorProfileTagPresent**</span></span>](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | <span data-ttu-id="a55be-154">Indica si una etiqueta del consorcio de color internacional (ICC) especificada está presente en el perfil de color especificado.</span><span class="sxs-lookup"><span data-stu-id="a55be-154">Reports whether a specified International Color Consortium (ICC) tag is present in the specified color profile.</span></span> |
| [<span data-ttu-id="a55be-155">**IsColorProfileValid**</span><span class="sxs-lookup"><span data-stu-id="a55be-155">**IsColorProfileValid**</span></span>](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | <span data-ttu-id="a55be-156">Permite determinar si el perfil especificado es un perfil de International color Consortium (ICC) válido o un identificador de perfil del sistema de colores de Windows (WCS) válido que se puede usar para la administración del color.</span><span class="sxs-lookup"><span data-stu-id="a55be-156">Allows you to determine whether the specified profile is a valid International Color Consortium (ICC) profile, or a valid Windows Color System (WCS) profile handle that can be used for color management.</span></span> |
| [<span data-ttu-id="a55be-157">**OpenColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="a55be-157">**OpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-opencolorprofilew) | <span data-ttu-id="a55be-158">Crea un identificador para un perfil de color especificado.</span><span class="sxs-lookup"><span data-stu-id="a55be-158">Creates a handle to a specified color profile.</span></span> <span data-ttu-id="a55be-159">El identificador se puede usar en otras funciones de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="a55be-159">The handle can then be used in other profile management functions.</span></span> |
| [<span data-ttu-id="a55be-160">**SetColorProfileElement**</span><span class="sxs-lookup"><span data-stu-id="a55be-160">**SetColorProfileElement**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | <span data-ttu-id="a55be-161">Establece los datos del elemento para un elemento de perfil etiquetado en un perfil de color de ICC.</span><span class="sxs-lookup"><span data-stu-id="a55be-161">Sets the element data for a tagged profile element in an ICC color profile.</span></span> |
| [<span data-ttu-id="a55be-162">**SetColorProfileElementReference**</span><span class="sxs-lookup"><span data-stu-id="a55be-162">**SetColorProfileElementReference**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | <span data-ttu-id="a55be-163">Crea en un perfil de color ICC especificado una nueva etiqueta que hace referencia a los mismos datos que una etiqueta existente.</span><span class="sxs-lookup"><span data-stu-id="a55be-163">Creates in a specified ICC color profile a new tag that references the same data as an existing tag.</span></span> |
| [<span data-ttu-id="a55be-164">**SetColorProfileElementSize**</span><span class="sxs-lookup"><span data-stu-id="a55be-164">**SetColorProfileElementSize**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | <span data-ttu-id="a55be-165">Establece el tamaño de un elemento etiquetado en un perfil de color de ICC.</span><span class="sxs-lookup"><span data-stu-id="a55be-165">Sets the size of a tagged element in an ICC color profile.</span></span> |
| [<span data-ttu-id="a55be-166">**SetColorProfileHeader**</span><span class="sxs-lookup"><span data-stu-id="a55be-166">**SetColorProfileHeader**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | <span data-ttu-id="a55be-167">Establece los datos de encabezado de un perfil de color ICC especificado.</span><span class="sxs-lookup"><span data-stu-id="a55be-167">Sets the header data in a specified ICC color profile.</span></span> |
| [<span data-ttu-id="a55be-168">**WcsGetCalibrationManagementState**</span><span class="sxs-lookup"><span data-stu-id="a55be-168">**WcsGetCalibrationManagementState**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | <span data-ttu-id="a55be-169">Determina si la administración del sistema del estado de calibración de pantalla está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a55be-169">Determines whether system management of the display calibration state is enabled.</span></span> |
| [<span data-ttu-id="a55be-170">**WcsSetCalibrationManagementState**</span><span class="sxs-lookup"><span data-stu-id="a55be-170">**WcsSetCalibrationManagementState**</span></span>](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | <span data-ttu-id="a55be-171">Determina si la administración del sistema del estado de calibración de pantalla está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a55be-171">Determines whether system management of the display calibration state is enabled.</span></span> |



 

 

 




