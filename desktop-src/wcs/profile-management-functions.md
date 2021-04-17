---
title: Funciones de administración de perfiles
description: Funciones de administración de perfiles
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Sistema de color de Windows (WCS), funciones
- WCS (sistema de colores de Windows), funciones
- Administración del color de imagen, funciones
- Administración del color, funciones
- colores, funciones
- Referencia WCS, funciones
- referencia de las funciones WCS,
- Sistema de color de Windows (WCS), perfiles
- WCS (sistema de colores de Windows), perfiles
- Administración del color de imagen, perfiles
- Administración del color, perfiles
- colores, perfiles
- Referencia WCS, perfiles
- referencia de WCS, perfiles
- Administración de perfiles
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0e80e300532b20148eef6d9dc362438b6714a3
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "105721172"
---
# <a name="profile-management-functions"></a><span data-ttu-id="7470a-118">Funciones de administración de perfiles</span><span class="sxs-lookup"><span data-stu-id="7470a-118">Profile Management Functions</span></span>

## <a name="profile-management-functions"></a><span data-ttu-id="7470a-119">Funciones de administración de perfiles</span><span class="sxs-lookup"><span data-stu-id="7470a-119">Profile Management Functions</span></span>

<span data-ttu-id="7470a-120">Las siguientes funciones de API son útiles en la administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="7470a-120">The following API functions are useful in profile management.</span></span>



| <span data-ttu-id="7470a-121">Función</span><span class="sxs-lookup"><span data-stu-id="7470a-121">Function</span></span>                                                                               | <span data-ttu-id="7470a-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7470a-122">Description</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7470a-123">**AssociateColorProfileWithDeviceW**</span><span class="sxs-lookup"><span data-stu-id="7470a-123">**AssociateColorProfileWithDeviceW**</span></span>](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | <span data-ttu-id="7470a-124">Asocia un perfil de color especificado a un dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="7470a-124">Associates a specified color profile with a specified device.</span></span>                                                              |
| <span data-ttu-id="7470a-125">[**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew)</span><span class="sxs-lookup"><span data-stu-id="7470a-125">[**CreateProfileFromLogColorSpaceW**]((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew)</span></span> | <span data-ttu-id="7470a-126">Convierte un espacio de [colores](c.md) lógico en un [Perfil de dispositivo](d.md).</span><span class="sxs-lookup"><span data-stu-id="7470a-126">Converts a logical [color space](c.md) to a [device profile](d.md).</span></span> |
| [<span data-ttu-id="7470a-127">**DisassociateColorProfileFromDeviceW**</span><span class="sxs-lookup"><span data-stu-id="7470a-127">**DisassociateColorProfileFromDeviceW**</span></span>](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | <span data-ttu-id="7470a-128">Desasocia un perfil de color especificado con un dispositivo especificado en un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="7470a-128">Disassociates a specified color profile with a specified device on a specified computer.</span></span> |
| [<span data-ttu-id="7470a-129">**EnumColorProfilesW**</span><span class="sxs-lookup"><span data-stu-id="7470a-129">**EnumColorProfilesW**</span></span>](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | <span data-ttu-id="7470a-130">Enumera todos los perfiles que cumplen los criterios de enumeración especificados.</span><span class="sxs-lookup"><span data-stu-id="7470a-130">Enumerates all the profiles satisfying the given enumeration criteria.</span></span> |
| [<span data-ttu-id="7470a-131">**GetColorDirectoryW**</span><span class="sxs-lookup"><span data-stu-id="7470a-131">**GetColorDirectoryW**</span></span>](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | <span data-ttu-id="7470a-132">Recupera la ruta de acceso del directorio de COLOR de Windows en un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="7470a-132">Retrieves the path of the Windows COLOR directory on a specified machine.</span></span> |
| [<span data-ttu-id="7470a-133">**GetDeviceGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="7470a-133">**GetDeviceGammaRamp**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | <span data-ttu-id="7470a-134">Obtiene la rampa gamma de los paneles de presentación de colores directos.</span><span class="sxs-lookup"><span data-stu-id="7470a-134">Gets the gamma ramp from direct color display boards.</span></span>                                                                                                |
| [<span data-ttu-id="7470a-135">**GetStandardColorSpaceProfileW**</span><span class="sxs-lookup"><span data-stu-id="7470a-135">**GetStandardColorSpaceProfileW**</span></span>](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | <span data-ttu-id="7470a-136">Recupera el perfil de color registrado para el espacio de [colores](c.md)estándar especificado.</span><span class="sxs-lookup"><span data-stu-id="7470a-136">Retrieves the color profile registered for the specified standard [color space](c.md).</span></span> |
| [<span data-ttu-id="7470a-137">**InstallColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="7470a-137">**InstallColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-installcolorprofilew) | <span data-ttu-id="7470a-138">Instala un perfil determinado para su uso en un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="7470a-138">Installs a given profile for use on a specified machine.</span></span> <span data-ttu-id="7470a-139">El perfil también se copia en el directorio de COLOR.</span><span class="sxs-lookup"><span data-stu-id="7470a-139">The profile is also copied to the COLOR directory.</span></span> |
| [<span data-ttu-id="7470a-140">**RegisterCMMW**</span><span class="sxs-lookup"><span data-stu-id="7470a-140">**RegisterCMMW**</span></span>](/windows/win32/api/icm/nf-icm-registercmmw) | <span data-ttu-id="7470a-141">Asocia un valor de identificación especificado a la biblioteca de vínculos dinámicos del módulo de administración de color (CMM DLL) especificada.</span><span class="sxs-lookup"><span data-stu-id="7470a-141">Associates a specified identification value with the specified color management module dynamic link library (CMM DLL).</span></span> <span data-ttu-id="7470a-142">Cuando este identificador aparece en un perfil de color, Windows puede localizar la CMM correspondiente para crear una transformación.</span><span class="sxs-lookup"><span data-stu-id="7470a-142">When this ID appears in a color profile, Windows can then locate the corresponding CMM so as to create a transform.</span></span> |
| [<span data-ttu-id="7470a-143">**SetDeviceGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="7470a-143">**SetDeviceGammaRamp**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | <span data-ttu-id="7470a-144">Establece la rampa gamma en los paneles de presentación de color directo.</span><span class="sxs-lookup"><span data-stu-id="7470a-144">Sets the gamma ramp on direct color display boards.</span></span>                                                                                                  |
| [<span data-ttu-id="7470a-145">**SetStandardColorSpaceProfileW**</span><span class="sxs-lookup"><span data-stu-id="7470a-145">**SetStandardColorSpaceProfileW**</span></span>](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | <span data-ttu-id="7470a-146">Registra un perfil especificado para un [espacio de colores](c.md)estándar determinado.</span><span class="sxs-lookup"><span data-stu-id="7470a-146">Registers a specified profile for a given standard [color space](c.md).</span></span> <span data-ttu-id="7470a-147">El perfil se puede consultar mediante [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew).</span><span class="sxs-lookup"><span data-stu-id="7470a-147">The profile can be queried using [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew).</span></span> |
| [<span data-ttu-id="7470a-148">**UninstallColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="7470a-148">**UninstallColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | <span data-ttu-id="7470a-149">Quita un perfil de color especificado de un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="7470a-149">Removes a specified color profile from a specified computer.</span></span> <span data-ttu-id="7470a-150">Los archivos asociados se eliminan opcionalmente del sistema.</span><span class="sxs-lookup"><span data-stu-id="7470a-150">Associated files are optionally deleted from the system.</span></span> |
| [<span data-ttu-id="7470a-151">**UnregisterCMMW**</span><span class="sxs-lookup"><span data-stu-id="7470a-151">**UnregisterCMMW**</span></span>](/windows/win32/api/icm/nf-icm-unregistercmmw) | <span data-ttu-id="7470a-152">Anula la Asociación de un valor de identificador especificado de una biblioteca de vínculos dinámicos (DLL CMM) determinada del módulo de administración del color.</span><span class="sxs-lookup"><span data-stu-id="7470a-152">Dissociates a specified ID value from a given color management module dynamic-link library (CMM DLL).</span></span> |
| [<span data-ttu-id="7470a-153">**WcsAssociateColorProfileWithDevice**</span><span class="sxs-lookup"><span data-stu-id="7470a-153">**WcsAssociateColorProfileWithDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | <span data-ttu-id="7470a-154">Asocia un perfil de color WCS especificado a un dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="7470a-154">Associates a specified WCS color profile with a specified device.</span></span>                                                                                    |
| [<span data-ttu-id="7470a-155">**WcsCreateIccProfile**</span><span class="sxs-lookup"><span data-stu-id="7470a-155">**WcsCreateIccProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | <span data-ttu-id="7470a-156">Convierte un perfil WCS en un perfil ICC.</span><span class="sxs-lookup"><span data-stu-id="7470a-156">Converts a WCS profile into an ICC profile.</span></span>                                                                                                          |
| [<span data-ttu-id="7470a-157">**WcsDisassociateColorProfileFromDevice**</span><span class="sxs-lookup"><span data-stu-id="7470a-157">**WcsDisassociateColorProfileFromDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | <span data-ttu-id="7470a-158">Desasocia un perfil de color WCS especificado con un dispositivo especificado en un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="7470a-158">Disassociates a specified WCS color profile with a specified device on a specified computer.</span></span>                                                         |
| [<span data-ttu-id="7470a-159">**WcsEnumColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="7470a-159">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | <span data-ttu-id="7470a-160">Enumera todos los perfiles de color que cumplen los criterios de enumeración en el ámbito de administración de perfiles especificado.</span><span class="sxs-lookup"><span data-stu-id="7470a-160">Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.</span></span>                                       |
| [<span data-ttu-id="7470a-161">**WcsEnumColorProfilesSize**</span><span class="sxs-lookup"><span data-stu-id="7470a-161">**WcsEnumColorProfilesSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | <span data-ttu-id="7470a-162">Devuelve el tamaño, en bytes, del búfer requerido por la función [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) para enumerar los perfiles de color.</span><span class="sxs-lookup"><span data-stu-id="7470a-162">Returns the size, in bytes, of the buffer required by the [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) function to enumerate color profiles.</span></span> |
| [<span data-ttu-id="7470a-163">**WcsGetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="7470a-163">**WcsGetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | <span data-ttu-id="7470a-164">Recupera el perfil de color predeterminado para un dispositivo o el valor predeterminado independiente del dispositivo si no se especifica el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7470a-164">Retrieves the default color profile for a device, or the device-independent default if the device is not specified.</span></span>                                  |
| [<span data-ttu-id="7470a-165">**WcsGetDefaultColorProfileSize**</span><span class="sxs-lookup"><span data-stu-id="7470a-165">**WcsGetDefaultColorProfileSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | <span data-ttu-id="7470a-166">Devuelve el tamaño, en bytes, del nombre de Perfil de color predeterminado para un dispositivo, incluido el terminador **null** .</span><span class="sxs-lookup"><span data-stu-id="7470a-166">Returns the size, in bytes, of the default color profile name for a device, including the **NULL** terminator.</span></span>                                       |
| [<span data-ttu-id="7470a-167">**WcsGetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="7470a-167">**WcsGetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | <span data-ttu-id="7470a-168">Recupera el intento de representación predeterminado en el ámbito de administración de perfiles especificado.</span><span class="sxs-lookup"><span data-stu-id="7470a-168">Retrieves the default rendering intent in the specified profile management scope.</span></span>                                                                    |
| [<span data-ttu-id="7470a-169">**WcsGetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="7470a-169">**WcsGetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | <span data-ttu-id="7470a-170">Determina si el usuario ha elegido utilizar una lista de asociaciones de perfil por usuario para el dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="7470a-170">Determines whether the user has chosen to use a per-user profile association list for the specified device.</span></span>                                          |
| [<span data-ttu-id="7470a-171">**WcsOpenColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="7470a-171">**WcsOpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | <span data-ttu-id="7470a-172">Crea un identificador para un perfil de color especificado.</span><span class="sxs-lookup"><span data-stu-id="7470a-172">Creates a handle to a specified color profile.</span></span>                                                                                                       |
| [<span data-ttu-id="7470a-173">**WcsSetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="7470a-173">**WcsSetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | <span data-ttu-id="7470a-174">Establece el nombre de Perfil de color predeterminado del tipo de perfil especificado en el ámbito de administración de perfiles especificado.</span><span class="sxs-lookup"><span data-stu-id="7470a-174">Sets the default color profile name of the specified profile type in the specified profile management scope.</span></span>                                         |
| [<span data-ttu-id="7470a-175">**WcsSetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="7470a-175">**WcsSetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | <span data-ttu-id="7470a-176">Establece la intención de representación predeterminada en el ámbito de administración de perfiles especificado.</span><span class="sxs-lookup"><span data-stu-id="7470a-176">Sets the default rendering intent in the specified profile management scope.</span></span>                                                                         |
| [<span data-ttu-id="7470a-177">**WcsSetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="7470a-177">**WcsSetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | <span data-ttu-id="7470a-178">Permite al usuario especificar si se va a usar una lista de asociaciones de perfil por usuario para el dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="7470a-178">Allows the user to specify whether to use a per-user profile association list for the specified device.</span></span>                                              |



 

## <a name="profile-consumption-functions"></a><span data-ttu-id="7470a-179">Funciones de consumo de perfiles</span><span class="sxs-lookup"><span data-stu-id="7470a-179">Profile Consumption Functions</span></span>

<span data-ttu-id="7470a-180">Las API de consumo de perfiles son las API de ICM2 que usan perfiles XML de ICC o WCS, identificadores de perfil o representación del Intent como parámetros, y un conjunto de nuevas API para la compatibilidad del perfil WCS con el código de administración del color de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7470a-180">The profile consumption APIs are those APIs in ICM2 that take ICC or WCS XML profiles, profile handles, or rendering intents as parameters, and a set of new APIs for WCS profile support for application color management code.</span></span>

 

## <a name="profiles-and-profile-management-functions"></a><span data-ttu-id="7470a-181">Perfiles y funciones de administración de perfiles</span><span class="sxs-lookup"><span data-stu-id="7470a-181">Profiles and Profile Management Functions</span></span>

<span data-ttu-id="7470a-182">El flujo de trabajo de administración de perfiles se basa en las API de ICM2 existentes que se han ampliado para proporcionar funcionalidad adicional para revisar el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7470a-182">The profile management workflow is based on existing ICM2 APIs that are augmented to provide additional functionality for revising application code.</span></span>

<span data-ttu-id="7470a-183">Los perfiles contienen información que utilizan los algoritmos de procesamiento de color para traducir el color entre diferentes espacios de color.</span><span class="sxs-lookup"><span data-stu-id="7470a-183">Profiles contain information used by color processing algorithms to translate color between different color spaces.</span></span> <span data-ttu-id="7470a-184">La administración de perfiles proporciona una manera de consultar y especificar qué perfiles se usan en diferentes fases por el modelo de procesamiento de color para administrar la salida de color de varios dispositivos periféricos con distintas características de color.</span><span class="sxs-lookup"><span data-stu-id="7470a-184">Profile management provides a way to query and specify which profiles get used at different stages by the color processing model to manage color output of various peripheral devices with diverse color characteristics.</span></span>

<span data-ttu-id="7470a-185">La administración de perfiles proporciona el siguiente conjunto de funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="7470a-185">Profile management provides the following set of functionalities:</span></span>

 

1. <span data-ttu-id="7470a-186">Instalar perfiles de color para su uso en el sistema.</span><span class="sxs-lookup"><span data-stu-id="7470a-186">Installing color profiles for use in the system.</span></span>

 

2. <span data-ttu-id="7470a-187">Asociación de uno o varios perfiles de color instalados con un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="7470a-187">Associating one or more installed color profiles with any particular device.</span></span>

 

3. <span data-ttu-id="7470a-188">Elegir un perfil de color predeterminado de un tipo determinado entre los perfiles disponibles para su uso en una fase determinada de procesamiento de color.</span><span class="sxs-lookup"><span data-stu-id="7470a-188">Choosing a default color profile of a particular type among the profiles available for use in a particular stage of color processing.</span></span> <span data-ttu-id="7470a-189">Esto podría ser para un dispositivo entre los perfiles asociados a él o entre los perfiles instalados en el sistema y no específicos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7470a-189">This could be for a device among the profiles associated with it, or among the profiles installed in the system and not device specific.</span></span>

 

4. <span data-ttu-id="7470a-190">Enumerar los perfiles de color que cumplen determinados criterios entre los perfiles instalados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="7470a-190">Enumerating color profiles that satisfy particular criteria among the profiles installed in the system.</span></span>

<span data-ttu-id="7470a-191">Las extensiones de nombre de archivo del perfil WCS son ". CDMP" para DMPs, ". Camp" para los nombres y ". GMMP" para GMMPs.</span><span class="sxs-lookup"><span data-stu-id="7470a-191">The WCS profile filename extensions are ".cdmp" for DMPs, ".camp" for CAMPs, and ".gmmp" for GMMPs.</span></span>

 

<span data-ttu-id="7470a-192">**Administración de perfiles por usuario y habilitación de la ejecución en el contexto LUA**</span><span class="sxs-lookup"><span data-stu-id="7470a-192">**Per-user profile management and enabling execution in LUA context**</span></span>

<span data-ttu-id="7470a-193">El objetivo del diseño descrito en el documento actual es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="7470a-193">The goal of the design described in the current document is as follows:</span></span>

 

1. <span data-ttu-id="7470a-194">La implementación de ICM2 heredada no proporciona compatibilidad con la administración de perfiles por usuario.</span><span class="sxs-lookup"><span data-stu-id="7470a-194">Legacy ICM2 implementation does not provide support for per-user profile management.</span></span> <span data-ttu-id="7470a-195">Los distintos usuarios no pueden tener su propia configuración de perfil.</span><span class="sxs-lookup"><span data-stu-id="7470a-195">Different users cannot have their own profile settings.</span></span> <span data-ttu-id="7470a-196">En vista, la infraestructura de administración de perfiles WCS permite a los usuarios configurar opciones de perfil individuales para la mayoría de las funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="7470a-196">In Vista, the WCS profile management infrastructure enables users to configure individual profile settings for most functionalities.</span></span>

 

2. <span data-ttu-id="7470a-197">Todas las API de administración de perfiles de ICM2 heredadas modifican la configuración de todo el sistema y requieren privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="7470a-197">All legacy ICM2 profile management APIs modify settings system-wide and require administrative privileges.</span></span> <span data-ttu-id="7470a-198">En Windows Vista, todos los usuarios se ejecutan en la configuración de cuenta de usuario con privilegios mínimos (LUA) la mayoría de las veces, y los administradores pueden elevar los privilegios de forma selectiva para ejecutar aplicaciones que modifican la configuración de todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="7470a-198">In Windows Vista, all users run in Least-privileged User Account (LUA) settings most of the time, and administrators can elevate privilege selectively to run applications that modify system-wide settings.</span></span> <span data-ttu-id="7470a-199">En la administración de perfiles WCS, todas las configuraciones de perfil por usuario se pueden configurar en el contexto LUA.</span><span class="sxs-lookup"><span data-stu-id="7470a-199">In WCS profile management, all per-user profile settings are configurable in LUA context.</span></span> <span data-ttu-id="7470a-200">Las aplicaciones de administración de perfiles se pueden ejecutar como configuraciones de LUA, lo que aumenta el ámbito de uso y garantiza que la seguridad del sistema no se ve comprometida.</span><span class="sxs-lookup"><span data-stu-id="7470a-200">Profile management applications can run as LUA settings, increasing their scope of use and ensuring that security of the system is not compromised.</span></span>

<span data-ttu-id="7470a-201">La administración de perfiles en vista proporciona las siguientes mejoras en la infraestructura de ICM2 heredada:</span><span class="sxs-lookup"><span data-stu-id="7470a-201">Profile management in Vista provides the following enhancements over legacy ICM2 infrastructure:</span></span>

 

1. <span data-ttu-id="7470a-202">Habilita la Asociación de perfiles con los dispositivos, la configuración de perfil predeterminada y la enumeración de perfiles en el ámbito por usuario y todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="7470a-202">It enables profile association with devices, default profile settings, and enumeration of profiles in both per-user and system-wide scope.</span></span>

 

2. <span data-ttu-id="7470a-203">La instalación de un perfil permanece en todo el sistema y requiere privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="7470a-203">Installing a profile remains system wide and requires administrator privileges.</span></span> <span data-ttu-id="7470a-204">Esto es coherente con la instalación del perfil durante la instalación del dispositivo porque la instalación del dispositivo es todo el sistema y requiere privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="7470a-204">This is consistent with profile installation during device installation because device installation is system wide and requires administrative privileges.</span></span>

 

<span data-ttu-id="7470a-205">El hecho de que los dispositivos se puedan instalar desde el contexto LUA es específico de lo que se admite para esa clase de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7470a-205">Whether devices can be installed from LUA context is particular to what is supported for that class of device.</span></span> <span data-ttu-id="7470a-206">Por ejemplo, en vista, es posible realizar la instalación de la impresora desde el contexto de LUA si el usuario tiene derechos para copiar archivos en el almacén de controladores mediante un administrador de dominio mediante directivas de almacén de controladores.</span><span class="sxs-lookup"><span data-stu-id="7470a-206">For example, in Vista, it is possible to do printer installation from LUA context if the user has been granted rights to copy files into the driver store by a domain administrator using driver store policies.</span></span> <span data-ttu-id="7470a-207">La infraestructura de administración de perfiles de color no tiene que hacer nada especial en este sentido, ya que la instalación se produce en el contexto del administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="7470a-207">Color profile management infrastructure doesn't need to do anything special in this regard since the installation happens in spooler context.</span></span>

 

3. <span data-ttu-id="7470a-208">La modificación de la configuración de perfil en el ámbito por usuario se puede realizar en el contexto LUA; las modificaciones en todo el sistema requieren privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="7470a-208">Modifying profile settings in per-user scope can be done in LUA context; system-wide modifications required administrative privileges.</span></span> <span data-ttu-id="7470a-209">Las operaciones de administración de perfiles que requieren la lectura de la información de configuración se pueden realizar en el contexto LUA para configuraciones por usuario y para todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="7470a-209">Profile management operations that require reading configuration information can be done in LUA context for both per-user and system-wide settings.</span></span>

<span data-ttu-id="7470a-210">Ámbito de administración de perfiles indica el ámbito de las operaciones realizadas; por usuario o en todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="7470a-210">Profile management scope indicates the scope of the operations performed; either per-user or system wide.</span></span>

<span data-ttu-id="7470a-211">Para cada operación, se indica si se puede hacer desde el contexto LUA.</span><span class="sxs-lookup"><span data-stu-id="7470a-211">For each operation, it is indicated whether it can be done from LUA context.</span></span> <span data-ttu-id="7470a-212">Si una operación no se puede realizar en el contexto LUA, la API de administración de perfiles correspondiente devuelve un error con acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="7470a-212">If an operation cannot be performed in LUA context, the corresponding profile management API returns failure with access denied.</span></span> <span data-ttu-id="7470a-213">Las aplicaciones que usan la API, como el panel de control de administración del color, pueden permitir que el usuario eleve el contexto administrativo (mediante OTS o la interfaz de usuario de consentimiento) y, después, llama a la API desde el contexto elevado para que la operación se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="7470a-213">Applications using the API, such as Color Management Control Panel, can enable the user to elevate to administrative context (using OTS or Consent UI), and then call the API from the elevated context so that the operation will succeed.</span></span>



<span data-ttu-id="7470a-214">Operación</span><span class="sxs-lookup"><span data-stu-id="7470a-214">Operation</span></span>

<span data-ttu-id="7470a-215">Ámbito de administración de perfiles</span><span class="sxs-lookup"><span data-stu-id="7470a-215">Profile Management Scope</span></span>

<span data-ttu-id="7470a-216">Condición previa</span><span class="sxs-lookup"><span data-stu-id="7470a-216">Pre-condition</span></span>

<span data-ttu-id="7470a-217">Condición posterior</span><span class="sxs-lookup"><span data-stu-id="7470a-217">Post-condition</span></span>

<span data-ttu-id="7470a-218">Ejecutable en contexto LUA</span><span class="sxs-lookup"><span data-stu-id="7470a-218">Executable in LUA context</span></span>

<span data-ttu-id="7470a-219">$ {ROWSPAN2} $Install perfil $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7470a-219">${ROWSPAN2}$Install profile${REMOVE}$</span></span>  

<span data-ttu-id="7470a-220">En todo el sistema</span><span class="sxs-lookup"><span data-stu-id="7470a-220">System wide</span></span>

<span data-ttu-id="7470a-221">Perfil copiado, instalado en el sistema y disponible para su uso.</span><span class="sxs-lookup"><span data-stu-id="7470a-221">Profile copied, installed into the system, and available for use.</span></span> <span data-ttu-id="7470a-222">El perfil es Enumerable en el ámbito de todo el sistema y del usuario actual para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="7470a-222">Profile is enumerable in system-wide and current-user scope for all users.</span></span>

<span data-ttu-id="7470a-223">Durante la instalación del controlador de dispositivo, regido por las directivas de instalación del controlador.</span><span class="sxs-lookup"><span data-stu-id="7470a-223">During device driver installation, governed by driver installation policies.</span></span> <span data-ttu-id="7470a-224">De lo contrario, no.</span><span class="sxs-lookup"><span data-stu-id="7470a-224">No, otherwise.</span></span>

<span data-ttu-id="7470a-225">Usuario actual</span><span class="sxs-lookup"><span data-stu-id="7470a-225">Current user</span></span>

<span data-ttu-id="7470a-226">No compatible</span><span class="sxs-lookup"><span data-stu-id="7470a-226">Not supported</span></span>

<span data-ttu-id="7470a-227">$ {ROWSPAN2} $Uninstall perfil $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7470a-227">${ROWSPAN2}$Uninstall profile${REMOVE}$</span></span>  

<span data-ttu-id="7470a-228">En todo el sistema</span><span class="sxs-lookup"><span data-stu-id="7470a-228">System wide</span></span>

<span data-ttu-id="7470a-229">El perfil está instalado en el sistema</span><span class="sxs-lookup"><span data-stu-id="7470a-229">Profile is installed in the system</span></span>

<span data-ttu-id="7470a-230">Perfil desinstalado del sistema y, opcionalmente, eliminado del almacén de perfiles.</span><span class="sxs-lookup"><span data-stu-id="7470a-230">Profile uninstalled from the system and optionally deleted from the profile store.</span></span> <span data-ttu-id="7470a-231">El perfil ya no está disponible para su uso y no se puede enumerar en ningún ámbito.</span><span class="sxs-lookup"><span data-stu-id="7470a-231">Profile is no longer available for use and is not enumerable in any scope.</span></span>

<span data-ttu-id="7470a-232">No</span><span class="sxs-lookup"><span data-stu-id="7470a-232">No</span></span>

<span data-ttu-id="7470a-233">Usuario actual</span><span class="sxs-lookup"><span data-stu-id="7470a-233">Current user</span></span>

<span data-ttu-id="7470a-234">No compatible</span><span class="sxs-lookup"><span data-stu-id="7470a-234">Not supported</span></span>

<span data-ttu-id="7470a-235">$ {ROWSPAN2} $Associate perfil con el dispositivo $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7470a-235">${ROWSPAN2}$Associate profile with device${REMOVE}$</span></span>  

<span data-ttu-id="7470a-236">En todo el sistema</span><span class="sxs-lookup"><span data-stu-id="7470a-236">System wide</span></span>

<span data-ttu-id="7470a-237">El perfil está instalado y es de tipo ICC o CDMP</span><span class="sxs-lookup"><span data-stu-id="7470a-237">Profile is installed and is of type ICC or CDMP</span></span>

<span data-ttu-id="7470a-238">El perfil está disponible para su uso con el dispositivo por parte de todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="7470a-238">Profile is available for use with the device by all users.</span></span> <span data-ttu-id="7470a-239">Es Enumerable, en el ámbito de todo el sistema y también en el ámbito de usuario actual para todos los usuarios, como está asociado con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7470a-239">It is enumerable, in system-wide scope and also current-user scope for all users, as associated with the device.</span></span>

<span data-ttu-id="7470a-240">No</span><span class="sxs-lookup"><span data-stu-id="7470a-240">No</span></span>

<span data-ttu-id="7470a-241">Usuario actual</span><span class="sxs-lookup"><span data-stu-id="7470a-241">Current user</span></span>

<span data-ttu-id="7470a-242">El perfil está instalado.</span><span class="sxs-lookup"><span data-stu-id="7470a-242">Profile is installed.</span></span> <span data-ttu-id="7470a-243">No importa si el perfil ya está asociado al dispositivo en el ámbito de todo el sistema y es de tipo ICC o CDMP.</span><span class="sxs-lookup"><span data-stu-id="7470a-243">It does not matter whether the profile is already associated to the device in system-wide scope and is of type ICC or CDMP.</span></span>

<span data-ttu-id="7470a-244">El perfil está disponible para su uso con el dispositivo por el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="7470a-244">Profile is available for use with the device by current user.</span></span> <span data-ttu-id="7470a-245">Solo se Enumerable en el ámbito del usuario actual (a menos que también haya una asociación de todo el sistema) como está asociado con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7470a-245">It is enumerable only in current-user scope (unless there is a system-wide association as well) as associated with the device.</span></span>

<span data-ttu-id="7470a-246">Sí</span><span class="sxs-lookup"><span data-stu-id="7470a-246">Yes</span></span>

<span data-ttu-id="7470a-247">$ {ROWSPAN2} $Disassociate perfil del dispositivo $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7470a-247">${ROWSPAN2}$Disassociate profile from device${REMOVE}$</span></span>  

<span data-ttu-id="7470a-248">En todo el sistema</span><span class="sxs-lookup"><span data-stu-id="7470a-248">System wide</span></span>

<span data-ttu-id="7470a-249">El perfil está asociado con el dispositivo en el ámbito de todo el sistema y es de tipo ICC o CDMP</span><span class="sxs-lookup"><span data-stu-id="7470a-249">Profile is associated with the device in system-wide scope and is of type ICC or CDMP</span></span>

<span data-ttu-id="7470a-250">El perfil ya no está disponible para su uso (excepto para los usuarios que tienen esta asociación en su ámbito de usuario actual).</span><span class="sxs-lookup"><span data-stu-id="7470a-250">Profile is no longer available for use (except for users who have this association in their current-user scope as well).</span></span> <span data-ttu-id="7470a-251">No es Enumerable en el ámbito de todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="7470a-251">It is not enumerable in system-wide scope.</span></span> <span data-ttu-id="7470a-252">Sin embargo, podría ser Enumerable en el ámbito del usuario actual para un usuario que tenga esta asociación en su ámbito.</span><span class="sxs-lookup"><span data-stu-id="7470a-252">It could be enumerable in current-user scope though, for a user who has this association in its scope.</span></span>

<span data-ttu-id="7470a-253">No</span><span class="sxs-lookup"><span data-stu-id="7470a-253">No</span></span>

<span data-ttu-id="7470a-254">Usuario actual</span><span class="sxs-lookup"><span data-stu-id="7470a-254">Current user</span></span>

<span data-ttu-id="7470a-255">El perfil está asociado con el dispositivo en el ámbito del usuario actual (independientemente de si está asociado en el ámbito de todo el sistema) y es de tipo ICC o CDMP.</span><span class="sxs-lookup"><span data-stu-id="7470a-255">Profile is associated with the device in current-user scope (irrespective of whether it is associated in system-wide scope) and is of type ICC or CDMP.</span></span>

<span data-ttu-id="7470a-256">El perfil ya no está disponible para su uso, o Enumerable como asociado al dispositivo, por parte del usuario actual (a menos que también esté asociado en el ámbito de todo el sistema al dispositivo).</span><span class="sxs-lookup"><span data-stu-id="7470a-256">Profile is no longer available for use, or enumerable as associated to the device, by current user (unless it is also associated in system-wide scope to the device).</span></span>

<span data-ttu-id="7470a-257">Sí</span><span class="sxs-lookup"><span data-stu-id="7470a-257">Yes</span></span>

<span data-ttu-id="7470a-258">$ {ROWSPAN2} $Set perfil para un tipo (DMP o ICC) como valor predeterminado para un dispositivo $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7470a-258">${ROWSPAN2}$Set profile for a type (DMP or ICC) as default for a device${REMOVE}$</span></span>  

<span data-ttu-id="7470a-259">En todo el sistema</span><span class="sxs-lookup"><span data-stu-id="7470a-259">System wide</span></span>

<span data-ttu-id="7470a-260">El perfil es de tipo ICC o CDMP</span><span class="sxs-lookup"><span data-stu-id="7470a-260">Profile is of type ICC or CDMP</span></span>

<span data-ttu-id="7470a-261">De forma predeterminada, el perfil se usa para el tipo determinado con el dispositivo, para todos los usuarios excepto para aquellos que han invalidado esta configuración en su ámbito de usuario actual.</span><span class="sxs-lookup"><span data-stu-id="7470a-261">The profile is used by default, for the particular type with the device, for all users except for those who have overridden this setting in their current-user scope.</span></span> <span data-ttu-id="7470a-262">(El perfil se instala y se asocia al sistema del dispositivo de ancho, si aún no es el caso).</span><span class="sxs-lookup"><span data-stu-id="7470a-262">(The profile is installed and associated to the device system wide, if that is not already the case.)</span></span>

<span data-ttu-id="7470a-263">No</span><span class="sxs-lookup"><span data-stu-id="7470a-263">No</span></span>

<span data-ttu-id="7470a-264">Usuario actual</span><span class="sxs-lookup"><span data-stu-id="7470a-264">Current user</span></span>

<span data-ttu-id="7470a-265">El perfil es de tipo ICC o CDMP</span><span class="sxs-lookup"><span data-stu-id="7470a-265">Profile is of type ICC or CDMP</span></span>

<span data-ttu-id="7470a-266">De forma predeterminada, el perfil se usa para el tipo determinado con el dispositivo en caso de usuario actual, con independencia del valor predeterminado para todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="7470a-266">The profile is used by default for the particular type with the device in case of current user, irrespective of the system-wide default for this.</span></span> <span data-ttu-id="7470a-267">(El perfil se instala y se asocia al dispositivo para el usuario actual, si aún no es el caso).</span><span class="sxs-lookup"><span data-stu-id="7470a-267">(The profile is installed and associated to the device for current user, if that is not already the case.)</span></span>

<span data-ttu-id="7470a-268">Sí, si el perfil ya está instalado</span><span class="sxs-lookup"><span data-stu-id="7470a-268">Yes, if the profile is already installed</span></span>

<span data-ttu-id="7470a-269">$ {ROWSPAN2} $Set perfil para un tipo (ICC, DMP, CAMP, GMMP) y combinación de subtipo como valor predeterminado global $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7470a-269">${ROWSPAN2}$Set profile for a type (ICC, DMP, CAMP, GMMP) and subtype combination as global default${REMOVE}$</span></span>  

<span data-ttu-id="7470a-270">En todo el sistema</span><span class="sxs-lookup"><span data-stu-id="7470a-270">System wide</span></span>

<span data-ttu-id="7470a-271">Solo los perfiles ICC y CDMP se pueden asociar a los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7470a-271">Only ICC and CDMP profiles can be associated with devices.</span></span>

<span data-ttu-id="7470a-272">El perfil se utiliza de forma predeterminada para el tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="7470a-272">The profile is used by default for the particular type.</span></span> <span data-ttu-id="7470a-273">Los usuarios pueden invalidar esta configuración en el ámbito del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="7470a-273">Users can override this setting in the current-user scope.</span></span> <span data-ttu-id="7470a-274">(El perfil está instalado, si aún no es el caso).</span><span class="sxs-lookup"><span data-stu-id="7470a-274">(The profile is installed, if that is not already the case.)</span></span>

<span data-ttu-id="7470a-275">No</span><span class="sxs-lookup"><span data-stu-id="7470a-275">No</span></span>

<span data-ttu-id="7470a-276">Usuario actual</span><span class="sxs-lookup"><span data-stu-id="7470a-276">Current user</span></span>

<span data-ttu-id="7470a-277">Solo los perfiles ICC y CDMP se pueden asociar a los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7470a-277">Only ICC and CDMP profiles can be associated with devices.</span></span>

<span data-ttu-id="7470a-278">El perfil se utiliza de forma predeterminada para el tipo concreto para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="7470a-278">The profile is used by default for the particular type for current user.</span></span> <span data-ttu-id="7470a-279">(El perfil está instalado, si aún no es el caso).</span><span class="sxs-lookup"><span data-stu-id="7470a-279">(The profile is installed, if that is not already the case.)</span></span>

<span data-ttu-id="7470a-280">Sí, si el perfil ya está instalado.</span><span class="sxs-lookup"><span data-stu-id="7470a-280">Yes, if the profile is already installed.</span></span>

<span data-ttu-id="7470a-281">$ {ROWSPAN2} $Erase la invalidación del usuario actual para una configuración de perfil predeterminada determinada, de modo que el valor predeterminado del sistema se usa siempre (como reserva), incluso para el ámbito del usuario actual. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7470a-281">${ROWSPAN2}$Erase the current-user override for a particular default profile setting, so that the system default always gets used (as fallback) even for current-user scope.${REMOVE}$</span></span>  

<span data-ttu-id="7470a-282">En todo el sistema</span><span class="sxs-lookup"><span data-stu-id="7470a-282">System wide</span></span>

<span data-ttu-id="7470a-283">No aplicable</span><span class="sxs-lookup"><span data-stu-id="7470a-283">Not applicable</span></span>

<span data-ttu-id="7470a-284">Usuario actual</span><span class="sxs-lookup"><span data-stu-id="7470a-284">Current user</span></span>

<span data-ttu-id="7470a-285">Incluso en el caso de las consultas de usuario actual en la configuración de perfil predeterminada, se devuelve la configuración de todo el sistema para su uso.</span><span class="sxs-lookup"><span data-stu-id="7470a-285">Even for current-user queries on default profile settings, system-wide settings are returned for use.</span></span>

<span data-ttu-id="7470a-286">Sí</span><span class="sxs-lookup"><span data-stu-id="7470a-286">Yes</span></span>

<span data-ttu-id="7470a-287">$ {ROWSPAN2} $Enumerate perfiles instalados que satisfacen criterios determinados (como clase de dispositivo, clase de perfil, etc.) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7470a-287">${ROWSPAN2}$Enumerate installed profiles satisfying particular criteria (like device class, profile class, etc.)${REMOVE}$</span></span>  

<span data-ttu-id="7470a-288">En todo el sistema</span><span class="sxs-lookup"><span data-stu-id="7470a-288">System wide</span></span>

<span data-ttu-id="7470a-289">Solo los perfiles ICC y CDMP se pueden asociar y enumerar para dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7470a-289">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="7470a-290">Los perfiles que se instalan y cumplen los criterios especificados en el ámbito de todo el sistema se enumeran.</span><span class="sxs-lookup"><span data-stu-id="7470a-290">Profiles that are installed and satisfy the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="7470a-291">Sí</span><span class="sxs-lookup"><span data-stu-id="7470a-291">Yes</span></span>

<span data-ttu-id="7470a-292">Usuario actual</span><span class="sxs-lookup"><span data-stu-id="7470a-292">Current user</span></span>

<span data-ttu-id="7470a-293">Solo los perfiles ICC y CDMP se pueden asociar con dispositivos y, por tanto, se enumeran para dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7470a-293">Only ICC and CDMP profiles can be associated with devices and thus enumerated for devices.</span></span>

<span data-ttu-id="7470a-294">Los perfiles que se instalan y cumplen los criterios especificados en el ámbito de todo el sistema se enumeran.</span><span class="sxs-lookup"><span data-stu-id="7470a-294">Profiles which are installed and satisfy the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="7470a-295">Sí</span><span class="sxs-lookup"><span data-stu-id="7470a-295">Yes</span></span>

<span data-ttu-id="7470a-296">$ {ROWSPAN2} $Enumerate perfiles asociados a un dispositivo determinado que satisfacen determinados criterios, como la clase de dispositivo y la clase de perfil $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7470a-296">${ROWSPAN2}$Enumerate profiles associated with a particular device satisfying particular criteria, such as device class, and profile class${REMOVE}$</span></span>  

<span data-ttu-id="7470a-297">En todo el sistema</span><span class="sxs-lookup"><span data-stu-id="7470a-297">System wide</span></span>

<span data-ttu-id="7470a-298">Solo los perfiles ICC y CDMP se pueden asociar y enumerar para dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7470a-298">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="7470a-299">Los perfiles que están asociados al dispositivo en el ámbito de todo el sistema y cumplen los criterios especificados en el ámbito de todo el sistema se enumeran.</span><span class="sxs-lookup"><span data-stu-id="7470a-299">Profiles that are associated with the device in system-wide scope and satisfies the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="7470a-300">Sí</span><span class="sxs-lookup"><span data-stu-id="7470a-300">Yes</span></span>

<span data-ttu-id="7470a-301">Usuario actual</span><span class="sxs-lookup"><span data-stu-id="7470a-301">Current user</span></span>

<span data-ttu-id="7470a-302">Solo los perfiles ICC y CDMP se pueden asociar y enumerar para dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7470a-302">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="7470a-303">Los perfiles que están disponibles como asociados al dispositivo en el ámbito del usuario actual, que incluye las asociaciones de todo el sistema y cumplen los criterios especificados en el ámbito del usuario actual, se enumeran.</span><span class="sxs-lookup"><span data-stu-id="7470a-303">Profiles that are available as associated with the device in current-user scope, which includes the system-wide associations and satisfies the specified criteria in current-user scope are enumerated.</span></span>

<span data-ttu-id="7470a-304">Sí</span><span class="sxs-lookup"><span data-stu-id="7470a-304">Yes</span></span>



 

<span data-ttu-id="7470a-305">Los tipos de Perfil de color válidos los proporciona la enumeración COLORPROFILETYPE.</span><span class="sxs-lookup"><span data-stu-id="7470a-305">The valid color profile types are provided by the COLORPROFILETYPE enumeration.</span></span>

<span data-ttu-id="7470a-306">Los subtipos de Perfil de color válidos los proporciona la enumeración COLORPROFILESUBTYPE.</span><span class="sxs-lookup"><span data-stu-id="7470a-306">The valid color profile subtypes are provided by the COLORPROFILESUBTYPE enumeration.</span></span>

<span data-ttu-id="7470a-307">En la tabla siguiente se muestran las combinaciones válidas de tipo de perfil/subtipo.</span><span class="sxs-lookup"><span data-stu-id="7470a-307">The valid profile type/subtype combinations are shown in the following table.</span></span>



<span data-ttu-id="7470a-308">COLORPROFILETYPE </span><span class="sxs-lookup"><span data-stu-id="7470a-308">COLORPROFILETYPE</span></span>

<span data-ttu-id="7470a-309">COLORPROFILESUBTYPE válido</span><span class="sxs-lookup"><span data-stu-id="7470a-309">Valid COLORPROFILESUBTYPE</span></span>

<span data-ttu-id="7470a-310">Notas</span><span class="sxs-lookup"><span data-stu-id="7470a-310">Notes</span></span>

<span data-ttu-id="7470a-311">Valor predeterminado del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7470a-311">Device Default</span></span>

<span data-ttu-id="7470a-312">Valor predeterminado global</span><span class="sxs-lookup"><span data-stu-id="7470a-312">Global Default</span></span>

<span data-ttu-id="7470a-313">Uso previsto</span><span class="sxs-lookup"><span data-stu-id="7470a-313">Intended Use</span></span>

<span data-ttu-id="7470a-314">Uso previsto</span><span class="sxs-lookup"><span data-stu-id="7470a-314">Intended Use</span></span>

<span data-ttu-id="7470a-315">ICC de CPT \_</span><span class="sxs-lookup"><span data-stu-id="7470a-315">CPT\_ICC</span></span>

<span data-ttu-id="7470a-316">CPST \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="7470a-316">CPST\_NONE</span></span>

<span data-ttu-id="7470a-317">Obtiene o establece el perfil ICC predeterminado asociado a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7470a-317">Get/Set default ICC profile associated with a device</span></span>

<span data-ttu-id="7470a-318">CPST \_ RGBWorkingSpace o CPST \_ CustomWorkingSpace</span><span class="sxs-lookup"><span data-stu-id="7470a-318">CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace</span></span>

<span data-ttu-id="7470a-319">Obtiene o establece el perfil de ICC como perfil de espacio de trabajo global RGB o personalizado.</span><span class="sxs-lookup"><span data-stu-id="7470a-319">Get/Set ICC profile as global RGB or custom working space profile.</span></span> <span data-ttu-id="7470a-320">Vea la Nota.</span><span class="sxs-lookup"><span data-stu-id="7470a-320">See Note.</span></span>

<span data-ttu-id="7470a-321">COLORPROFILETYPE CPT \_ ICC y CPT \_ DMP son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="7470a-321">The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive.</span></span> <span data-ttu-id="7470a-322">El perfil de color predeterminado que establezca para un espacio de trabajo determinado (RGB o personalizado) puede ser un perfil ICC o un perfil DMP, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="7470a-322">The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.</span></span>

<span data-ttu-id="7470a-323">DMP de CPT \_</span><span class="sxs-lookup"><span data-stu-id="7470a-323">CPT\_DMP</span></span>

<span data-ttu-id="7470a-324">CPST \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="7470a-324">CPST\_NONE</span></span>

<span data-ttu-id="7470a-325">Obtiene o establece el perfil de DMP predeterminado asociado a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7470a-325">Get/Set default DMP profile associated with a device</span></span>

<span data-ttu-id="7470a-326">CPST \_ RGBWorkingSpace o CPST \_ CustomWorkingSpace</span><span class="sxs-lookup"><span data-stu-id="7470a-326">CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace</span></span>

<span data-ttu-id="7470a-327">Obtiene o establece el perfil de DMP como perfil de espacio de trabajo global RGB o personalizado.</span><span class="sxs-lookup"><span data-stu-id="7470a-327">Get/Set DMP profile as global RGB or custom working space profile.</span></span> <span data-ttu-id="7470a-328">Vea la Nota.</span><span class="sxs-lookup"><span data-stu-id="7470a-328">See Note.</span></span>

<span data-ttu-id="7470a-329">COLORPROFILETYPE CPT \_ ICC y CPT \_ DMP son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="7470a-329">The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive.</span></span> <span data-ttu-id="7470a-330">El perfil de color predeterminado que establezca para un espacio de trabajo determinado (RGB o personalizado) puede ser un perfil ICC o un perfil DMP, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="7470a-330">The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.</span></span>



 

> [!Note]  
> <span data-ttu-id="7470a-331">Cuando se llama a WcsSetDefaultColorProfile para establecer un perfil de DMP como perfil predeterminado para el espacio de trabajo de RGB o un espacio de trabajo personalizado, solo es válido un perfil DMP de tipo RGBVirtualDevice, LCD o CRT.</span><span class="sxs-lookup"><span data-stu-id="7470a-331">When WcsSetDefaultColorProfile is called to set a DMP profile as the default profile for the RGB working space or a custom working space, only a DMP profile that is of type RGBVirtualDevice, LCD, or CRT is valid.</span></span>
>
>  
>
> <span data-ttu-id="7470a-332">Cuando se llama a WcsSetDefaultColorProfile para establecer un perfil de ICC como perfil predeterminado para el espacio de trabajo RGB o un espacio de trabajo personalizado, solo un perfil de ICC cuya clase es "Space" o "DISP" y cuyo espacio de colores es "RGB" es válido.</span><span class="sxs-lookup"><span data-stu-id="7470a-332">When WcsSetDefaultColorProfile is called to set an ICC profile as the default profile for the RGB working space or a custom working space, only an ICC profile whose class is "spac" or "disp," and whose color space is "RGB" is valid.</span></span>

 

<span data-ttu-id="7470a-333">La arquitectura está diseñada según los requisitos de las operaciones que se mencionan en las enumeraciones y las tablas anteriores.</span><span class="sxs-lookup"><span data-stu-id="7470a-333">The architecture is designed according to the requirements of the operations as mentioned in the enumerations and tables above.</span></span>

### <a name="profile-management-public-api-layer"></a><span data-ttu-id="7470a-334">Nivel de API pública de administración de perfiles</span><span class="sxs-lookup"><span data-stu-id="7470a-334">Profile management public API layer</span></span>

<span data-ttu-id="7470a-335">Dado que el ámbito de administración de perfiles no es compatible con las API de ICM2 heredadas, se requiere un nuevo conjunto de API de administración de perfiles WCS que defina el ámbito de administración de perfiles como usuario amplio o del sistema actual.</span><span class="sxs-lookup"><span data-stu-id="7470a-335">Because profile management scope is not supported by legacy ICM2 APIs, a new set of WCS profile management APIs is required that defines profile management scope as system wide or current user.</span></span> <span data-ttu-id="7470a-336">?</span><span class="sxs-lookup"><span data-stu-id="7470a-336">?</span></span> <span data-ttu-id="7470a-337">Las API de ICM2 heredadas siguen siendo compatibles con la compatibilidad con versiones anteriores y funcionan en el ámbito de administración de perfiles que está implícito para la llamada.</span><span class="sxs-lookup"><span data-stu-id="7470a-337">Legacy ICM2 APIs continue to be supported for backward compatibility, and work on profile management scope that is implicit for the call.</span></span> <span data-ttu-id="7470a-338">¿o ICM2 API que funcionan en el ámbito del usuario actual?</span><span class="sxs-lookup"><span data-stu-id="7470a-338">o ICM2 APIs that work on current-user scope ?</span></span> <span data-ttu-id="7470a-339">Esto es para las operaciones que son compatibles con el ámbito de usuario actual y del sistema en la administración de perfiles WCS.</span><span class="sxs-lookup"><span data-stu-id="7470a-339">This is for operations that are supported for both system wide and current-user scope in WCS profile management.</span></span> <span data-ttu-id="7470a-340">Las API de ICM2 heredadas llaman a las nuevas API WCS con el ámbito de administración de perfiles como usuario actual.</span><span class="sxs-lookup"><span data-stu-id="7470a-340">Legacy ICM2 APIs call on new WCS APIs with profile management scope as current user.</span></span> <span data-ttu-id="7470a-341">Esto tiene sentido desde la perspectiva del usuario, ya que permite la configuración por usuario de las aplicaciones heredadas y también la ejecución de la mayoría de las operaciones en el contexto LUA.</span><span class="sxs-lookup"><span data-stu-id="7470a-341">This makes sense from user perspective because this enables per-user settings from legacy applications and also executing most of the operations in LUA context.</span></span> <span data-ttu-id="7470a-342">¿o ICM2 API que funcionan en el ámbito de todo el sistema?</span><span class="sxs-lookup"><span data-stu-id="7470a-342">o ICM2 APIs that work on system-wide scope ?</span></span> <span data-ttu-id="7470a-343">Esto es para las operaciones (instalar perfiles y desinstalar perfiles) que solo admiten el ámbito de todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="7470a-343">This is for operations (install profiles and uninstall profiles) that support only system-wide scope.</span></span> <span data-ttu-id="7470a-344">No se crean nuevas API de administración de perfiles WCS y se pueden modificar las API existentes.</span><span class="sxs-lookup"><span data-stu-id="7470a-344">No new WCS profile management APIs are created and existing APIs can be modified.</span></span>

<span data-ttu-id="7470a-345">Las implementaciones subyacentes de las operaciones de administración de perfiles funcionan en las entidades de datos de configuración siguientes para crear el contexto de los algoritmos de procesamiento de colores con el fin de proporcionar funcionalidades de administración del color.</span><span class="sxs-lookup"><span data-stu-id="7470a-345">The underlying implementations of the profile management operations work on the following configuration data entities to create the context for color processing algorithms to provide color management functionalities.</span></span> <span data-ttu-id="7470a-346">Son valores específicos del dispositivo o globales (independientes del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="7470a-346">They are either device specific or global (device independent) settings.</span></span> <span data-ttu-id="7470a-347">o datos de configuración específicos del dispositivo:?</span><span class="sxs-lookup"><span data-stu-id="7470a-347">o Device specific configuration data: ?</span></span> <span data-ttu-id="7470a-348">Lista de perfiles asociados a un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="7470a-348">List of profiles associated with a particular device.</span></span> <span data-ttu-id="7470a-349">?</span><span class="sxs-lookup"><span data-stu-id="7470a-349">?</span></span> <span data-ttu-id="7470a-350">Perfil predeterminado para distintos tipos de perfiles asociados con un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7470a-350">Default profile for different profile types associated with a device.</span></span> <span data-ttu-id="7470a-351">?</span><span class="sxs-lookup"><span data-stu-id="7470a-351">?</span></span> <span data-ttu-id="7470a-352">Modo de coincidencia de perfiles que se usa para la enumeración.</span><span class="sxs-lookup"><span data-stu-id="7470a-352">Matching mode of profiles used for enumeration.</span></span> <span data-ttu-id="7470a-353">o datos de configuración global:?</span><span class="sxs-lookup"><span data-stu-id="7470a-353">o Global configuration data: ?</span></span> <span data-ttu-id="7470a-354">Lista de perfiles instalados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="7470a-354">List of profiles installed in the system.</span></span> <span data-ttu-id="7470a-355">?</span><span class="sxs-lookup"><span data-stu-id="7470a-355">?</span></span> <span data-ttu-id="7470a-356">Perfil predeterminado global para distintos tipos de perfiles.</span><span class="sxs-lookup"><span data-stu-id="7470a-356">Global default profile for different profile types.</span></span> <span data-ttu-id="7470a-357">?</span><span class="sxs-lookup"><span data-stu-id="7470a-357">?</span></span> <span data-ttu-id="7470a-358">Las implementaciones subyacentes del almacenamiento de datos de configuración se aplican en el ámbito de almacenamiento para los datos de configuración (ya sean independientes del dispositivo o específicos del dispositivo), que puede ser todo el sistema o el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="7470a-358">The underlying implementations of configuration data storage take in storage scope for configuration data (either device independent or device specific), which can be either system wide or current user.</span></span> <span data-ttu-id="7470a-359">Esto es diferente del ámbito de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="7470a-359">This is different from profile management scope.</span></span> <span data-ttu-id="7470a-360">Una operación con el ámbito de administración de perfiles de usuario actual puede producir una lectura desde un ámbito de almacenamiento de todo el sistema si la configuración de usuario actual para esa operación no está presente.</span><span class="sxs-lookup"><span data-stu-id="7470a-360">An operation with current-user profile management scope can cause a read from a system-wide storage scope if the current-user setting for that operation is not present.</span></span> <span data-ttu-id="7470a-361">?</span><span class="sxs-lookup"><span data-stu-id="7470a-361">?</span></span> <span data-ttu-id="7470a-362">El nivel de API ICM2/WCS llama a esta capa de almacenamiento para obtener y establecer datos con el ámbito de almacenamiento adecuado.</span><span class="sxs-lookup"><span data-stu-id="7470a-362">The ICM2/WCS API layer calls in this storage layer for getting and setting data with appropriate storage scope.</span></span> <span data-ttu-id="7470a-363">La capa de almacenamiento es transparente para el ámbito de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="7470a-363">The storage layer is transparent to profile management scope.</span></span> <span data-ttu-id="7470a-364">La lógica para combinar datos de ámbitos de almacenamiento de usuario actual y de todo el sistema para crear o actualizar una configuración de acuerdo con el ámbito de administración de perfiles especificado por el llamador de la API.</span><span class="sxs-lookup"><span data-stu-id="7470a-364">The logic for combining data from current-user and system-wide storage scopes to create or update a configuration according to the profile management scope specified by the API caller.</span></span> <span data-ttu-id="7470a-365">Esta lógica está presente en el nivel de API ICM2/WCS.</span><span class="sxs-lookup"><span data-stu-id="7470a-365">This logic is present in the ICM2/WCS API layer.</span></span>

### <a name="device-specific-storage-layer"></a><span data-ttu-id="7470a-366">Capa de almacenamiento específica del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7470a-366">Device-specific storage layer</span></span>

<span data-ttu-id="7470a-367">El almacenamiento de diferentes clases de dispositivos como imprimir, capturar o mostrar puede ser diferente entre sí.</span><span class="sxs-lookup"><span data-stu-id="7470a-367">The storage for different classes of devices like print, capture or display could be different from each other.</span></span> <span data-ttu-id="7470a-368">Por ejemplo, los datos de configuración de un dispositivo de impresión deben almacenarse mediante las API de impresión estándar, como SetPrinterDataEx y GetPrinterDataEx, para permitir la copia de perfiles y la configuración que se va a transferir a un equipo cliente durante la conexión de punto e impresión.</span><span class="sxs-lookup"><span data-stu-id="7470a-368">For example, configuration data for a print device must be stored using standard print APIs, such as SetPrinterDataEx and GetPrinterDataEx, to enable the profiles to be copied and settings to be transferred to a client machine during Point-and-Print connection.</span></span> <span data-ttu-id="7470a-369">?</span><span class="sxs-lookup"><span data-stu-id="7470a-369">?</span></span> <span data-ttu-id="7470a-370">Esta capa exporta la funcionalidad para abrir el almacén, obtener datos, establecer datos y cerrar el almacén mediante interfaces predefinidas comunes para que la capa de almacenamiento de la configuración de la administración de perfiles pueda llamarlos a la vez que se almacenan los datos para ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7470a-370">This layer exports functionality to open store, get data, set data and close store using common pre-defined interfaces so that the profile management configuration storage layer can call into them while being transparent to the way the data gets stored for that device.</span></span>

<span data-ttu-id="7470a-371">El diagrama siguiente muestra esta arquitectura.</span><span class="sxs-lookup"><span data-stu-id="7470a-371">The following diagram illustrates this architecture.</span></span>



<span data-ttu-id="7470a-372">Nivel de API pública de administración de perfiles</span><span class="sxs-lookup"><span data-stu-id="7470a-372">Profile Management Public API Layer</span></span>

<span data-ttu-id="7470a-373">$ {ROWSPAN2} $Legacy API de ICM2 para las operaciones que solo admiten el ámbito de administración de perfiles de todo el sistema en vista (instalar, desinstalar y obtener directorio de color).</span><span class="sxs-lookup"><span data-stu-id="7470a-373">${ROWSPAN2}$Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista (install, uninstall, and get color directory).</span></span> <span data-ttu-id="7470a-374">Llaman a la capa de almacenamiento de configuración con el ámbito de almacenamiento adecuado. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7470a-374">They call the configuration storage layer with appropriate storage scope.${REMOVE}$</span></span>  

<span data-ttu-id="7470a-375">Legacy ICM2 API para las operaciones que admiten el ámbito de administración de perfiles de usuario actual y todo el sistema en vista (todas las operaciones distintas de install, uninstall y Get color Directory).</span><span class="sxs-lookup"><span data-stu-id="7470a-375">Legacy ICM2 API for operations that support both system-wide and current-user profile management scope in Vista (all operations other than install, uninstall, and get color directory).</span></span> <span data-ttu-id="7470a-376">Funcionan implícitamente en el ámbito del usuario actual y llaman a la nueva API WCS con el ámbito de administración de perfiles como usuario actual.</span><span class="sxs-lookup"><span data-stu-id="7470a-376">They implicitly work on current-user scope, and call into new WCS API with profile management scope as current user.</span></span>

<span data-ttu-id="7470a-377">Nueva API WCS con compatibilidad con el ámbito de administración de perfiles de usuario actual y en todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="7470a-377">New WCS API with system-wide and current-user profile management scope support.</span></span> <span data-ttu-id="7470a-378">Llaman a la capa de almacenamiento de configuración con el ámbito de almacenamiento adecuado.</span><span class="sxs-lookup"><span data-stu-id="7470a-378">They call the configuration storage layer with appropriate storage scope.</span></span>



 



<span data-ttu-id="7470a-379">Capa de almacenamiento de configuración de administración de perfiles</span><span class="sxs-lookup"><span data-stu-id="7470a-379">Profile Management Configuration Storage Layer</span></span>

<span data-ttu-id="7470a-380">Rutinas de configuración global independientes del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7470a-380">Device-independent global configuration routines</span></span>

<span data-ttu-id="7470a-381">Rutinas de configuración específicas del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7470a-381">Device-specific configuration routines</span></span>

<span data-ttu-id="7470a-382">$ {ROWSPAN3} $Profile la instalación y la administración de configuración de perfil predeterminada independiente del dispositivo, que se admite en el ámbito de almacenamiento de usuario actual y en todo el sistema. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7470a-382">${ROWSPAN3}$Profile installation and device-independent default profile settings management, supported in system-wide and current-user storage scope.${REMOVE}$</span></span>  

<span data-ttu-id="7470a-383">Asociación de dispositivos y administración de configuración de perfil predeterminada específica del dispositivo, que se admite en el ámbito de almacenamiento de usuario actual y en todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="7470a-383">Device association and device-specific default profile settings management, supported in system-wide and current-user storage scope.</span></span>

<span data-ttu-id="7470a-384">Device-Specific capa de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="7470a-384">Device-Specific Storage layer</span></span>

<span data-ttu-id="7470a-385">Imprimir almacenamiento específico</span><span class="sxs-lookup"><span data-stu-id="7470a-385">Print specific storage</span></span>

<span data-ttu-id="7470a-386">Mostrar almacenamiento específico</span><span class="sxs-lookup"><span data-stu-id="7470a-386">Display specific storage</span></span>

<span data-ttu-id="7470a-387">Capturar almacenamiento específico</span><span class="sxs-lookup"><span data-stu-id="7470a-387">Capture specific storage</span></span>



 

<span data-ttu-id="7470a-388">Las API de ICM2 heredadas para las operaciones que solo admiten el ámbito de administración de perfiles de todo el sistema en vista no tienen ningún cambio de comportamiento.</span><span class="sxs-lookup"><span data-stu-id="7470a-388">Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista have no changes in behavior.</span></span> <span data-ttu-id="7470a-389">Las operaciones de instalación y desinstalación se encuentran en esta categoría.</span><span class="sxs-lookup"><span data-stu-id="7470a-389">Install and uninstall operations fall in this category.</span></span>

<span data-ttu-id="7470a-390">Las API de ICM2 heredadas para las operaciones que admiten el ámbito de administración de perfiles de usuario actual y todo el sistema tienen su comportamiento cambiado para consultar y configurar las opciones de usuario actual.</span><span class="sxs-lookup"><span data-stu-id="7470a-390">Legacy ICM2 APIs for operations that support both system-wide and current-user profile management scope have their behavior changed to query and configure current-user settings.</span></span> <span data-ttu-id="7470a-391">Todas las operaciones que no sean instalar y desinstalar se encuentran en esta categoría.</span><span class="sxs-lookup"><span data-stu-id="7470a-391">All operations other than install and uninstall fall in this category.</span></span>

 

 




