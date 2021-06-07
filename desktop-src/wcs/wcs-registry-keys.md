---
title: Claves del Registro de WCS
description: WCS usa claves del Registro para indicar que se han producido determinados eventos de perfil de color. Las aplicaciones deben consultar estas claves del Registro para obtener el estado actualizado del perfil de color del sistema.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Sistema de colores de Windows (WCS), claves del Registro
- WCS (Sistema de colores de Windows), claves del Registro
- administración de colores de imagen, claves del Registro
- administración de colores, claves del Registro
- colors,registry keys
- Referencia de WCS, claves del Registro
- referencia de WCS,claves del Registro
- Sistema de colores de Windows (WCS), registro
- WCS (Sistema de colores de Windows), registro
- administración de colores de imagen, registro
- administración de colores, registro
- colors,registry
- WCS reference,registry
- referencia de WCS,registry
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058ec839b226e96542604f151f06e2654a4180d5
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444676"
---
# <a name="wcs-registry-keys"></a><span data-ttu-id="356e1-118">Claves del Registro de WCS</span><span class="sxs-lookup"><span data-stu-id="356e1-118">WCS Registry Keys</span></span>

<span data-ttu-id="356e1-119">WCS usa claves del Registro para indicar que se han producido determinados eventos de perfil de color.</span><span class="sxs-lookup"><span data-stu-id="356e1-119">WCS uses registry keys to signal that certain color profile events have occurred.</span></span> <span data-ttu-id="356e1-120">Las aplicaciones deben consultar estas claves del Registro para obtener el estado actualizado del perfil de color del sistema.</span><span class="sxs-lookup"><span data-stu-id="356e1-120">Apps should query these registry keys for updated system color profile state.</span></span>

## <a name="active-color-profile-changed"></a><span data-ttu-id="356e1-121">Cambio del perfil de color activo</span><span class="sxs-lookup"><span data-stu-id="356e1-121">Active color profile changed</span></span>

<span data-ttu-id="356e1-122">Es posible que las aplicaciones quieran responder a eventos de cambio de perfil de color para un dispositivo de supervisión. Esto garantiza que siempre tienen información de color precisa para su destino, incluso si el usuario u otra aplicación ha cambiado el perfil activo para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="356e1-122">Apps may want to respond to color profile change events for a monitor device; this ensures that they always have accurate color information for their target, even if the user or another app has changed the active profile for the device.</span></span>

### <a name="desktop-applications"></a><span data-ttu-id="356e1-123">Aplicaciones de escritorio</span><span class="sxs-lookup"><span data-stu-id="356e1-123">Desktop applications</span></span>

<span data-ttu-id="356e1-124">Las aplicaciones de escritorio deben escuchar los cambios en el Registro para determinar cuándo han cambiado las asociaciones de un perfil de color [**mediante RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span><span class="sxs-lookup"><span data-stu-id="356e1-124">Desktop apps should listen for changes to the registry to determine when a color profile associations has changed using [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span></span> <span data-ttu-id="356e1-125">Una aplicación debe registrarse tanto para los cambios de asociación de perfiles por usuario como para los cambios en todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="356e1-125">An app should register both for per-user profile association changes, and for system-wide changes.</span></span>

<span data-ttu-id="356e1-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) debe inicializarse con un HKEY proporcionado por [**RegOpenKeyEx.**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)</span><span class="sxs-lookup"><span data-stu-id="356e1-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) should be initialized with an HKEY provided by [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa).</span></span> <span data-ttu-id="356e1-127">**RegOpenKeyEx** debe inicializarse con las siguientes ubicaciones de árbol del Registro:</span><span class="sxs-lookup"><span data-stu-id="356e1-127">**RegOpenKeyEx** should be initialized using the following registry tree locations:</span></span>



|    &nbsp;  |  &nbsp;      | 
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="356e1-128">Asociaciones de perfil por usuario</span><span class="sxs-lookup"><span data-stu-id="356e1-128">Per-user profile associations</span></span>    | <span data-ttu-id="356e1-129">**HKEY \_ CURRENT USER SOFTWARE Microsoft Windows NT \_ \\ \\ \\ CurrentVersion \\ ICM \\ ProfileAssociations \\ Display \\ {4d36e96e-e325-11ce-bfc1-08002be10318}**</span><span class="sxs-lookup"><span data-stu-id="356e1-129">**HKEY\_CURRENT\_USER SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ProfileAssociations\\Display\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span> |
| <span data-ttu-id="356e1-130">Asociaciones de perfil de todo el sistema</span><span class="sxs-lookup"><span data-stu-id="356e1-130">System-wide profile associations</span></span> | <span data-ttu-id="356e1-131">**Clase de control HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ CurrentControlSet \\ \\ \\ {4d36e96e-e325-11ce-bfc1-08002be10318}**</span><span class="sxs-lookup"><span data-stu-id="356e1-131">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Class\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span>                                        |



 

<span data-ttu-id="356e1-132">Cuando se notifica a la aplicación un cambio de clave del Registro, primero debe consultar si se usan asociaciones por usuario o para todo el sistema mediante una llamada a [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span><span class="sxs-lookup"><span data-stu-id="356e1-132">When the app is notified of a registry key change, it should first query whether per-user or system-wide associations are being used by calling [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span></span> <span data-ttu-id="356e1-133">A continuación, debe llamar [**a WcsGetDefaultColorProfile con**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) el valor de ÁMBITO DE ADMINISTRACIÓN DE [**\_ \_ PERFILES \_ DE WCS**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) correcto para obtener el nuevo perfil de color activo para el monitor.</span><span class="sxs-lookup"><span data-stu-id="356e1-133">It should then call [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) with the right [**WCS\_PROFILE\_MANAGEMENT\_SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) value to obtain the new active color profile for the monitor.</span></span> <span data-ttu-id="356e1-134">Tenga en cuenta que no todos los cambios de clave del Registro se corresponderán con un cambio real en el perfil de color activo actualmente. la aplicación mush comprueba si el perfil devuelto por **WcsGetDefaultColorProfile** ha cambiado realmente.</span><span class="sxs-lookup"><span data-stu-id="356e1-134">Note that not all registry key changes will correspond to an actual change in the currently active color profile; the app mush check whether the profile returned by **WcsGetDefaultColorProfile** has actually changed.</span></span>

### <a name="universal-windows-uwp-apps"></a><span data-ttu-id="356e1-135">Aplicaciones universales de Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="356e1-135">Universal Windows (UWP) apps</span></span>

<span data-ttu-id="356e1-136">Las aplicaciones universales de Windows no tienen acceso a las claves del Registro anteriores.</span><span class="sxs-lookup"><span data-stu-id="356e1-136">Universal Windows Apps do not have access to the above registry keys.</span></span> <span data-ttu-id="356e1-137">En su lugar, deben registrar un controlador para el [**evento DisplayInformation.ColorProfileChanged.**](/uwp/api/Windows.Graphics.Display.DisplayInformation)</span><span class="sxs-lookup"><span data-stu-id="356e1-137">Instead, they should register a handler for the [**DisplayInformation.ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) event.</span></span> <span data-ttu-id="356e1-138">Este evento se activa cada vez que cambia el perfil de color activo para el monitor en el que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="356e1-138">This event fires whenever the active color profile for the monitor on which the application is running has changed.</span></span> <span data-ttu-id="356e1-139">ColorProfileChanged tiene en cuenta si se usan asociaciones de perfil por usuario o de todo el sistema; esta información se abstrae de las aplicaciones para UWP.</span><span class="sxs-lookup"><span data-stu-id="356e1-139">ColorProfileChanged takes into account whether per-user or system-wide profile associations are being used; this information is abstracted from UWP apps.</span></span>

<span data-ttu-id="356e1-140">Al responder al evento ColorProfileChanged, la aplicación debe consultar el perfil activo actualmente mediante [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span><span class="sxs-lookup"><span data-stu-id="356e1-140">When responding to the ColorProfileChanged event, the app should query the currently active profile using [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span></span>

 

 