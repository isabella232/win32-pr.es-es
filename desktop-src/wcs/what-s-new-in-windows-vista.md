---
title: Novedades de Windows Vista
description: La versión 1,0 de administración del color de imagen (ICM) se entregó en Microsoft Windows 95 y proporciona capacidades básicas de administración del color en los contextos de dispositivos de Windows.
ms.assetid: 3079f84c-0d6c-4f87-a041-de86f5f7d99b
keywords:
- Sistema de color de Windows (WCS), Windows Vista
- WCS (sistema de colores de Windows), Windows Vista
- Administración del color de imagen, Windows Vista
- Administración del color, Windows Vista
- colores, Windows Vista
- Sistema de color de Windows (WCS), sistemas operativos
- WCS (sistema de color de Windows), sistemas operativos
- Administración del color de imagen, sistemas operativos
- Administración del color, sistemas operativos
- colores, sistemas operativos
- Administración del color de imagen (ICM)
- ICM (administración del color de imagen)
- Administración del color de Windows Vista
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b889dd0ba3b044f0d0f158bd2364f5c3216ec39
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "105721171"
---
# <a name="whats-new-in-windows-vista"></a><span data-ttu-id="7c108-116">Novedades de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c108-116">What's New in Windows Vista</span></span>

<span data-ttu-id="7c108-117">La versión 1,0 de administración del color de imagen (ICM) se entregó en Microsoft Windows 95 y proporciona capacidades básicas de administración del color en los contextos de dispositivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="7c108-117">Version 1.0 of Image Color Management (ICM) was delivered in Microsoft Windows 95, and provides basic color management capabilities within Windows device contexts.</span></span>

<span data-ttu-id="7c108-118">La versión 2,0 de ICM se entregó en Windows 98, Windows Millennium Edition, Windows 2000 y WindowsXP, e incluye una variedad de funciones nuevas que implementaban la administración del color fuera de los contextos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c108-118">ICM version 2.0 was delivered in Windows 98, Windows Millennium Edition, Windows 2000, and WindowsXP and included a variety of new functions that implemented color management outside of device contexts.</span></span> <span data-ttu-id="7c108-119">Estas nuevas funciones eran adecuadas para los requisitos de administración de color más exigentes y ofrecían a las aplicaciones un mayor control sobre el proceso de administración del color.</span><span class="sxs-lookup"><span data-stu-id="7c108-119">These new functions were suitable for more demanding color management requirements, and gave applications greater control over the color-management process.</span></span>

<span data-ttu-id="7c108-120">Con el lanzamiento de Windows Vista, ICM 2,0 ahora se incluye en el sistema de color de Windows (WCS) 1,0, que agrega más funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="7c108-120">With the release of Windows Vista, ICM 2.0 is now included in Windows Color System (WCS) 1.0, which adds more functionality.</span></span> <span data-ttu-id="7c108-121">En la tabla siguiente se enumeran las nuevas interfaces de programación de aplicaciones (API) que se incluyen en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7c108-121">The following table lists new application programming interfaces (API) that ship in Windows Vista.</span></span>

## <a name="new-api-shipping-in-windows-vista"></a><span data-ttu-id="7c108-122">Nuevo envío de API en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c108-122">New API Shipping in Windows Vista</span></span>



<span data-ttu-id="7c108-123">Enumeraciones</span><span class="sxs-lookup"><span data-stu-id="7c108-123">Enumerations</span></span>

<span data-ttu-id="7c108-124">Nombre de la API</span><span class="sxs-lookup"><span data-stu-id="7c108-124">API Name</span></span>

<span data-ttu-id="7c108-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c108-125">Header</span></span>

<span data-ttu-id="7c108-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c108-126">Library</span></span>

[<span data-ttu-id="7c108-127">**COLORDATATYPE**</span><span class="sxs-lookup"><span data-stu-id="7c108-127">**COLORDATATYPE**</span></span>](/windows/win32/api/icm/ne-icm-colordatatype)

<span data-ttu-id="7c108-128">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-128">icm.h</span></span>

<span data-ttu-id="7c108-129">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-129">mscms.lib</span></span>

[<span data-ttu-id="7c108-130">**COLORPROFILESUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="7c108-130">**COLORPROFILESUBTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colorprofilesubtype)

<span data-ttu-id="7c108-131">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-131">icm.h</span></span>

<span data-ttu-id="7c108-132">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-132">mscms.lib</span></span>

[<span data-ttu-id="7c108-133">**COLORPROFILETYPE**</span><span class="sxs-lookup"><span data-stu-id="7c108-133">**COLORPROFILETYPE**</span></span>](/windows/win32/api/icm/ne-icm-colorprofiletype)

<span data-ttu-id="7c108-134">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-134">icm.h</span></span>

<span data-ttu-id="7c108-135">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-135">mscms.lib</span></span>

[<span data-ttu-id="7c108-136">**\_ámbito de \_ Administración de perfiles WCS \_**</span><span class="sxs-lookup"><span data-stu-id="7c108-136">**WCS\_PROFILE\_MANAGEMENT\_SCOPE**</span></span>](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)

<span data-ttu-id="7c108-137">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-137">icm.h</span></span>

<span data-ttu-id="7c108-138">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-138">mscms.lib</span></span>



 



<span data-ttu-id="7c108-139">Functions</span><span class="sxs-lookup"><span data-stu-id="7c108-139">Functions</span></span>

<span data-ttu-id="7c108-140">Nombre de la API</span><span class="sxs-lookup"><span data-stu-id="7c108-140">API Name</span></span>

<span data-ttu-id="7c108-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c108-141">Header</span></span>

<span data-ttu-id="7c108-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c108-142">Library</span></span>

[<span data-ttu-id="7c108-143">**WcsAssociateColorProfileWithDevice**</span><span class="sxs-lookup"><span data-stu-id="7c108-143">**WcsAssociateColorProfileWithDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

<span data-ttu-id="7c108-144">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-144">icm.h</span></span>

<span data-ttu-id="7c108-145">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-145">mscms.lib</span></span>

[<span data-ttu-id="7c108-146">**WcsCheckColors**</span><span class="sxs-lookup"><span data-stu-id="7c108-146">**WcsCheckColors**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

<span data-ttu-id="7c108-147">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-147">icm.h</span></span>

<span data-ttu-id="7c108-148">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-148">mscms.lib</span></span>

[<span data-ttu-id="7c108-149">**WcsCreateIccProfile**</span><span class="sxs-lookup"><span data-stu-id="7c108-149">**WcsCreateIccProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)

<span data-ttu-id="7c108-150">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-150">icm.h</span></span>

<span data-ttu-id="7c108-151">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-151">mscms.lib</span></span>

[<span data-ttu-id="7c108-152">**WcsDisassociateColorProfileFromDevice**</span><span class="sxs-lookup"><span data-stu-id="7c108-152">**WcsDisassociateColorProfileFromDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice)

<span data-ttu-id="7c108-153">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-153">icm.h</span></span>

<span data-ttu-id="7c108-154">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-154">mscms.lib</span></span>

[<span data-ttu-id="7c108-155">**WcsEnumColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="7c108-155">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)

<span data-ttu-id="7c108-156">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-156">icm.h</span></span>

<span data-ttu-id="7c108-157">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-157">mscms.lib</span></span>

[<span data-ttu-id="7c108-158">**WcsEnumColorProfilesSize**</span><span class="sxs-lookup"><span data-stu-id="7c108-158">**WcsEnumColorProfilesSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)

<span data-ttu-id="7c108-159">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-159">icm.h</span></span>

<span data-ttu-id="7c108-160">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-160">mscms.lib</span></span>

[<span data-ttu-id="7c108-161">**WcsGetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="7c108-161">**WcsGetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)

<span data-ttu-id="7c108-162">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-162">icm.h</span></span>

<span data-ttu-id="7c108-163">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-163">mscms.lib</span></span>

[<span data-ttu-id="7c108-164">**WcsGetDefaultColorProfileSize**</span><span class="sxs-lookup"><span data-stu-id="7c108-164">**WcsGetDefaultColorProfileSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize)

<span data-ttu-id="7c108-165">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-165">icm.h</span></span>

<span data-ttu-id="7c108-166">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-166">mscms.lib</span></span>

[<span data-ttu-id="7c108-167">**WcsGetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="7c108-167">**WcsGetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

<span data-ttu-id="7c108-168">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-168">icm.h</span></span>

<span data-ttu-id="7c108-169">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-169">mscms.lib</span></span>

[<span data-ttu-id="7c108-170">**WcsGetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="7c108-170">**WcsGetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

<span data-ttu-id="7c108-171">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-171">icm.h</span></span>

<span data-ttu-id="7c108-172">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-172">mscms.lib</span></span>

[<span data-ttu-id="7c108-173">**WcsOpenColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="7c108-173">**WcsOpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew)

<span data-ttu-id="7c108-174">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-174">icm.h</span></span>

<span data-ttu-id="7c108-175">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-175">mscms.lib</span></span>

[<span data-ttu-id="7c108-176">**WcsSetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="7c108-176">**WcsSetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile)

<span data-ttu-id="7c108-177">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-177">icm.h</span></span>

<span data-ttu-id="7c108-178">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-178">mscms.lib</span></span>

[<span data-ttu-id="7c108-179">**WcsSetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="7c108-179">**WcsSetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent)

<span data-ttu-id="7c108-180">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-180">icm.h</span></span>

<span data-ttu-id="7c108-181">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-181">mscms.lib</span></span>

[<span data-ttu-id="7c108-182">**WcsSetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="7c108-182">**WcsSetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)

<span data-ttu-id="7c108-183">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-183">icm.h</span></span>

<span data-ttu-id="7c108-184">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-184">mscms.lib</span></span>

[<span data-ttu-id="7c108-185">**WcsTranslateColors**</span><span class="sxs-lookup"><span data-stu-id="7c108-185">**WcsTranslateColors**</span></span>](/windows/win32/api/icm/nf-icm-wcstranslatecolors)

<span data-ttu-id="7c108-186">ICM. h</span><span class="sxs-lookup"><span data-stu-id="7c108-186">icm.h</span></span>

<span data-ttu-id="7c108-187">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="7c108-187">mscms.lib</span></span>



 



<span data-ttu-id="7c108-188">Interfaces y sus funciones</span><span class="sxs-lookup"><span data-stu-id="7c108-188">Interfaces and Their Functions</span></span>

<span data-ttu-id="7c108-189">Nombre de la API</span><span class="sxs-lookup"><span data-stu-id="7c108-189">API Name</span></span>

<span data-ttu-id="7c108-190">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c108-190">Header</span></span>

<span data-ttu-id="7c108-191">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c108-191">Library</span></span>

[<span data-ttu-id="7c108-192">**IDeviceModelPlugin**</span><span class="sxs-lookup"><span data-stu-id="7c108-192">**IDeviceModelPlugin**</span></span>](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)

<span data-ttu-id="7c108-193">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-193">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-194">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-194">N/A</span></span>

[<span data-ttu-id="7c108-195">**IDeviceModelPlugin::ColorimetricToDeviceColors**</span><span class="sxs-lookup"><span data-stu-id="7c108-195">**IDeviceModelPlugin::ColorimetricToDeviceColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolors)

<span data-ttu-id="7c108-196">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-196">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-197">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-197">N/A</span></span>

[<span data-ttu-id="7c108-198">**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**</span><span class="sxs-lookup"><span data-stu-id="7c108-198">**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack)

<span data-ttu-id="7c108-199">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-199">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-200">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-200">N/A</span></span>

[<span data-ttu-id="7c108-201">**IDeviceModelPlugin::D eviceToColorimetricColors**</span><span class="sxs-lookup"><span data-stu-id="7c108-201">**IDeviceModelPlugin::DeviceToColorimetricColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-devicetocolorimetriccolors)

<span data-ttu-id="7c108-202">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-202">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-203">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-203">N/A</span></span>

[<span data-ttu-id="7c108-204">**IDeviceModelPlugin::GetGamutBoundaryMesh**</span><span class="sxs-lookup"><span data-stu-id="7c108-204">**IDeviceModelPlugin::GetGamutBoundaryMesh**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymesh)

<span data-ttu-id="7c108-205">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-205">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-206">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-206">N/A</span></span>

[<span data-ttu-id="7c108-207">**IDeviceModelPlugin::GetGamutBoundaryMeshSize**</span><span class="sxs-lookup"><span data-stu-id="7c108-207">**IDeviceModelPlugin::GetGamutBoundaryMeshSize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymeshsize)

<span data-ttu-id="7c108-208">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-208">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-209">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-209">N/A</span></span>

[<span data-ttu-id="7c108-210">**IDeviceModelPlugin::GetNeutralAxis**</span><span class="sxs-lookup"><span data-stu-id="7c108-210">**IDeviceModelPlugin::GetNeutralAxis**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis)

<span data-ttu-id="7c108-211">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-211">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-212">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-212">N/A</span></span>

[<span data-ttu-id="7c108-213">**IDeviceModelPlugin::GetNeutralAxisSize**</span><span class="sxs-lookup"><span data-stu-id="7c108-213">**IDeviceModelPlugin::GetNeutralAxisSize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxissize)

<span data-ttu-id="7c108-214">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-214">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-215">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-215">N/A</span></span>

[<span data-ttu-id="7c108-216">**IDeviceModelPlugin::GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="7c108-216">**IDeviceModelPlugin::GetNumChannels**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getnumchannels)

<span data-ttu-id="7c108-217">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-217">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-218">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-218">N/A</span></span>

[<span data-ttu-id="7c108-219">**IDeviceModelPlugin::GetPrimarySamples**</span><span class="sxs-lookup"><span data-stu-id="7c108-219">**IDeviceModelPlugin::GetPrimarySamples**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getprimarysamples)

<span data-ttu-id="7c108-220">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-220">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-221">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-221">N/A</span></span>

[<span data-ttu-id="7c108-222">**IDeviceModelPlugin:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="7c108-222">**IDeviceModelPlugin::Initialize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-initialize)

<span data-ttu-id="7c108-223">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-223">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-224">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-224">N/A</span></span>

[<span data-ttu-id="7c108-225">**IDeviceModelPlugin::SetTransformDeviceModelInfo**</span><span class="sxs-lookup"><span data-stu-id="7c108-225">**IDeviceModelPlugin::SetTransformDeviceModelInfo**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-settransformdevicemodelinfo)

<span data-ttu-id="7c108-226">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-226">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-227">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-227">N/A</span></span>

[<span data-ttu-id="7c108-228">**IGamutMapModelPlugin**</span><span class="sxs-lookup"><span data-stu-id="7c108-228">**IGamutMapModelPlugin**</span></span>](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)

<span data-ttu-id="7c108-229">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-229">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-230">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-230">N/A</span></span>

[<span data-ttu-id="7c108-231">**IGamutMapModelPlugin:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="7c108-231">**IGamutMapModelPlugin::Initialize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-initialize)

<span data-ttu-id="7c108-232">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-232">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-233">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-233">N/A</span></span>

[<span data-ttu-id="7c108-234">**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**</span><span class="sxs-lookup"><span data-stu-id="7c108-234">**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-sourcetodestinationappearancecolors)

<span data-ttu-id="7c108-235">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-235">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-236">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-236">N/A</span></span>



 



<span data-ttu-id="7c108-237">Estructuras</span><span class="sxs-lookup"><span data-stu-id="7c108-237">Structures</span></span>

<span data-ttu-id="7c108-238">Nombre de la API</span><span class="sxs-lookup"><span data-stu-id="7c108-238">API Name</span></span>

<span data-ttu-id="7c108-239">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c108-239">Header</span></span>

<span data-ttu-id="7c108-240">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c108-240">Library</span></span>

[<span data-ttu-id="7c108-241">**BlackInformation**</span><span class="sxs-lookup"><span data-stu-id="7c108-241">**BlackInformation**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)

<span data-ttu-id="7c108-242">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-242">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-243">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-243">N/A</span></span>

[<span data-ttu-id="7c108-244">**GamutBoundaryDescription**</span><span class="sxs-lookup"><span data-stu-id="7c108-244">**GamutBoundaryDescription**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutboundarydescription)

<span data-ttu-id="7c108-245">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-245">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-246">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-246">N/A</span></span>

[<span data-ttu-id="7c108-247">**XYZColorF**</span><span class="sxs-lookup"><span data-stu-id="7c108-247">**XYZColorF**</span></span>](https://www.bing.com/search?q=**XYZColorF**)

<span data-ttu-id="7c108-248">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-248">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-249">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-249">N/A</span></span>

[<span data-ttu-id="7c108-250">**JChColorF**</span><span class="sxs-lookup"><span data-stu-id="7c108-250">**JChColorF**</span></span>](https://www.bing.com/search?q=**JChColorF**)

<span data-ttu-id="7c108-251">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-251">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-252">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-252">N/A</span></span>

[<span data-ttu-id="7c108-253">**JabColorF**</span><span class="sxs-lookup"><span data-stu-id="7c108-253">**JabColorF**</span></span>](https://www.bing.com/search?q=**JabColorF**)

<span data-ttu-id="7c108-254">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-254">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-255">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-255">N/A</span></span>

[<span data-ttu-id="7c108-256">**GamutShell**</span><span class="sxs-lookup"><span data-stu-id="7c108-256">**GamutShell**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshell)

<span data-ttu-id="7c108-257">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-257">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-258">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-258">N/A</span></span>

[<span data-ttu-id="7c108-259">**GamutShellTriangle**</span><span class="sxs-lookup"><span data-stu-id="7c108-259">**GamutShellTriangle**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshelltriangle)

<span data-ttu-id="7c108-260">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-260">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-261">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-261">N/A</span></span>

[<span data-ttu-id="7c108-262">**PrimaryJabColors**</span><span class="sxs-lookup"><span data-stu-id="7c108-262">**PrimaryJabColors**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryjabcolors)

<span data-ttu-id="7c108-263">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-263">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-264">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-264">N/A</span></span>

[<span data-ttu-id="7c108-265">**PrimaryXYZColors**</span><span class="sxs-lookup"><span data-stu-id="7c108-265">**PrimaryXYZColors**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryxyzcolors)

<span data-ttu-id="7c108-266">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="7c108-266">WcsPlugIn.h</span></span>

<span data-ttu-id="7c108-267">N/D</span><span class="sxs-lookup"><span data-stu-id="7c108-267">N/A</span></span>



 

 

 