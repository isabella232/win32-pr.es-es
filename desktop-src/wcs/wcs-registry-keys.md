---
title: Claves del Registro de WCS
description: WCS utiliza las claves del registro para indicar que se han producido determinados eventos de Perfil de color. Las aplicaciones deben consultar estas claves del registro para el estado actualizado del perfil de color del sistema.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Sistema de color de Windows (WCS), claves del registro
- WCS (sistema de colores de Windows), claves del registro
- Administración del color de imagen, claves del registro
- Administración del color, claves del registro
- colores, claves del registro
- Referencia WCS, claves del registro
- referencia de las claves del registro de WCS
- Sistema de color de Windows (WCS), registro
- WCS (sistema de colores de Windows), registro
- Administración del color de imagen, registro
- Administración del color, registro
- colores, registro
- Referencia WCS, registro
- referencia de WCS, registro
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a1c0072d9a00fe0cff4a4dbe57af839f65731b
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "105721170"
---
# <a name="wcs-registry-keys"></a><span data-ttu-id="d4cb5-118">Claves del Registro de WCS</span><span class="sxs-lookup"><span data-stu-id="d4cb5-118">WCS Registry Keys</span></span>

<span data-ttu-id="d4cb5-119">WCS utiliza las claves del registro para indicar que se han producido determinados eventos de Perfil de color.</span><span class="sxs-lookup"><span data-stu-id="d4cb5-119">WCS uses registry keys to signal that certain color profile events have occurred.</span></span> <span data-ttu-id="d4cb5-120">Las aplicaciones deben consultar estas claves del registro para el estado actualizado del perfil de color del sistema.</span><span class="sxs-lookup"><span data-stu-id="d4cb5-120">Apps should query these registry keys for updated system color profile state.</span></span>

## <a name="active-color-profile-changed"></a><span data-ttu-id="d4cb5-121">Perfil de color activo cambiado</span><span class="sxs-lookup"><span data-stu-id="d4cb5-121">Active color profile changed</span></span>

<span data-ttu-id="d4cb5-122">Las aplicaciones pueden querer responder a los eventos de cambio de Perfil de color de un dispositivo de supervisión. Esto garantiza que siempre tienen información de color precisa para su destino, incluso si el usuario u otra aplicación ha cambiado el perfil activo para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4cb5-122">Apps may want to respond to color profile change events for a monitor device; this ensures that they always have accurate color information for their target, even if the user or another app has changed the active profile for the device.</span></span>

### <a name="desktop-applications"></a><span data-ttu-id="d4cb5-123">Aplicaciones de escritorio</span><span class="sxs-lookup"><span data-stu-id="d4cb5-123">Desktop applications</span></span>

<span data-ttu-id="d4cb5-124">Las aplicaciones de escritorio deben escuchar los cambios en el registro para determinar cuándo ha cambiado una asociación de Perfil de color mediante [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span><span class="sxs-lookup"><span data-stu-id="d4cb5-124">Desktop apps should listen for changes to the registry to determine when a color profile associations has changed using [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span></span> <span data-ttu-id="d4cb5-125">Una aplicación debe registrarse tanto para los cambios de Asociación de perfil por usuario como para los cambios en todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="d4cb5-125">An app should register both for per-user profile association changes, and for system-wide changes.</span></span>

<span data-ttu-id="d4cb5-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) debe inicializarse con un HKEY proporcionado por [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa).</span><span class="sxs-lookup"><span data-stu-id="d4cb5-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) should be initialized with an HKEY provided by [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa).</span></span> <span data-ttu-id="d4cb5-127">**RegOpenKeyEx** se debe inicializar con las siguientes ubicaciones de árbol del registro:</span><span class="sxs-lookup"><span data-stu-id="d4cb5-127">**RegOpenKeyEx** should be initialized using the following registry tree locations:</span></span>



|                                  |                                                                                                                                                    |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4cb5-128">Asociaciones de perfil por usuario</span><span class="sxs-lookup"><span data-stu-id="d4cb5-128">Per-user profile associations</span></span>    | <span data-ttu-id="d4cb5-129">**HKEY \_ Current \_ User software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ICM \\ ProfileAssociations \\ Display \\ {4d36e96e-E325-11ce-bfc1-08002be10318}**</span><span class="sxs-lookup"><span data-stu-id="d4cb5-129">**HKEY\_CURRENT\_USER SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ProfileAssociations\\Display\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span> |
| <span data-ttu-id="d4cb5-130">Asociaciones de perfil en todo el sistema</span><span class="sxs-lookup"><span data-stu-id="d4cb5-130">System-wide profile associations</span></span> | <span data-ttu-id="d4cb5-131">**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ Class \\ {4d36e96e-E325-11ce-bfc1-08002be10318}**</span><span class="sxs-lookup"><span data-stu-id="d4cb5-131">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Class\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span>                                        |



 

<span data-ttu-id="d4cb5-132">Cuando se notifica a la aplicación de un cambio de clave del registro, primero debe consultar si se usan asociaciones por usuario o para todo el sistema llamando a [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span><span class="sxs-lookup"><span data-stu-id="d4cb5-132">When the app is notified of a registry key change, it should first query whether per-user or system-wide associations are being used by calling [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span></span> <span data-ttu-id="d4cb5-133">A continuación, debe llamar a [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) con el valor de ámbito de administración de perfiles de WCS adecuado para obtener el nuevo perfil de color activo para el monitor. [**\_ \_ \_**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)</span><span class="sxs-lookup"><span data-stu-id="d4cb5-133">It should then call [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) with the right [**WCS\_PROFILE\_MANAGEMENT\_SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) value to obtain the new active color profile for the monitor.</span></span> <span data-ttu-id="d4cb5-134">Tenga en cuenta que no todos los cambios en las claves del registro se corresponden con un cambio real en el perfil de color activo actualmente. el deberá de la aplicación comprueba si el perfil devuelto por **WcsGetDefaultColorProfile** ha cambiado realmente.</span><span class="sxs-lookup"><span data-stu-id="d4cb5-134">Note that not all registry key changes will correspond to an actual change in the currently active color profile; the app mush check whether the profile returned by **WcsGetDefaultColorProfile** has actually changed.</span></span>

### <a name="universal-windows-uwp-apps"></a><span data-ttu-id="d4cb5-135">Aplicaciones de Windows universal (UWP)</span><span class="sxs-lookup"><span data-stu-id="d4cb5-135">Universal Windows (UWP) apps</span></span>

<span data-ttu-id="d4cb5-136">Las aplicaciones universales de Windows no tienen acceso a las claves del registro anteriores.</span><span class="sxs-lookup"><span data-stu-id="d4cb5-136">Universal Windows Apps do not have access to the above registry keys.</span></span> <span data-ttu-id="d4cb5-137">En su lugar, deben registrar un controlador para el evento [**DisplayInformation. ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) .</span><span class="sxs-lookup"><span data-stu-id="d4cb5-137">Instead, they should register a handler for the [**DisplayInformation.ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) event.</span></span> <span data-ttu-id="d4cb5-138">Este evento se desencadena cuando cambia el perfil de color activo para el monitor en el que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d4cb5-138">This event fires whenever the active color profile for the monitor on which the application is running has changed.</span></span> <span data-ttu-id="d4cb5-139">ColorProfileChanged tiene en cuenta si se usan asociaciones de perfil por usuario o por todo el sistema. Esta información se abstrae de las aplicaciones para UWP.</span><span class="sxs-lookup"><span data-stu-id="d4cb5-139">ColorProfileChanged takes into account whether per-user or system-wide profile associations are being used; this information is abstracted from UWP apps.</span></span>

<span data-ttu-id="d4cb5-140">Al responder al evento ColorProfileChanged, la aplicación debe consultar el perfil activo actualmente mediante [**DisplayInformation. GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span><span class="sxs-lookup"><span data-stu-id="d4cb5-140">When responding to the ColorProfileChanged event, the app should query the currently active profile using [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span></span>

 

 