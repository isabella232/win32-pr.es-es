---
description: A partir de Windows Vista, los elementos del panel de control incluidos en Windows reciben un nombre canónico que se puede usar en una llamada API o en una instrucción de línea de comandos para iniciar ese elemento mediante programación.
ms.assetid: A02DFC9F-646D-40d8-901C-7239A820DE2C
title: Nombres canónicos de los elementos del panel de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55fc360b0d3db0f85a057977d1898c59d09d5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000987"
---
# <a name="canonical-names-of-control-panel-items"></a><span data-ttu-id="edbdd-103">Nombres canónicos de los elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="edbdd-103">Canonical Names of Control Panel Items</span></span>

<span data-ttu-id="edbdd-104">A partir de Windows Vista, los elementos del panel de control incluidos en Windows reciben un nombre canónico que se puede usar en una [llamada API o en una instrucción de línea de comandos](executing-control-panel-items.md) para iniciar ese elemento mediante programación.</span><span class="sxs-lookup"><span data-stu-id="edbdd-104">As of Windows Vista, Control Panel items included with Windows are given a canonical name that can be used in an [API call or a command-line instruction](executing-control-panel-items.md) to programmatically launch that item.</span></span> <span data-ttu-id="edbdd-105">A partir de Windows 7 y Windows Server 2008 R2, los nombres canónicos se pueden usar en una directiva de grupo para ocultar determinados elementos del panel de control.</span><span class="sxs-lookup"><span data-stu-id="edbdd-105">As of Windows 7 and Windows Server 2008 R2, canonical names can be used in a group policy to hide specific Control Panel items.</span></span> <span data-ttu-id="edbdd-106">En este tema se proporcionan detalles para cada elemento del panel de control: nombre canónico, GUID, nombre del módulo y las versiones del sistema operativo que reconocen el nombre canónico.</span><span class="sxs-lookup"><span data-stu-id="edbdd-106">This topic provides details for each Control Panel item: canonical name, GUID, module name, and the operating system versions that recognize the canonical name.</span></span>

> [!Note]  
> <span data-ttu-id="edbdd-107">Los nombres canónicos para los elementos del panel de control no se admiten antes de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="edbdd-107">Canonical names for Control Panel items are not supported prior to Windows Vista.</span></span>

 

-   [<span data-ttu-id="edbdd-108">Nombres canónicos del panel de control</span><span class="sxs-lookup"><span data-stu-id="edbdd-108">Control Panel Canonical Names</span></span>](#control-panel-canonical-names)
-   [<span data-ttu-id="edbdd-109">Nombres canónicos del panel de control desusados</span><span class="sxs-lookup"><span data-stu-id="edbdd-109">Deprecated Control Panel Canonical Names</span></span>](#deprecated-control-panel-canonical-names)
-   [<span data-ttu-id="edbdd-110">Usar nombres canónicos en directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="edbdd-110">Using Canonical Names in Group Policy</span></span>](#using-canonical-names-in-local-group-policy)
-   [<span data-ttu-id="edbdd-111">Comentarios:</span><span class="sxs-lookup"><span data-stu-id="edbdd-111">Remarks</span></span>](#remarks)

## <a name="control-panel-canonical-names"></a><span data-ttu-id="edbdd-112">Nombres canónicos del panel de control</span><span class="sxs-lookup"><span data-stu-id="edbdd-112">Control Panel Canonical Names</span></span>

<span data-ttu-id="edbdd-113">Puntos a tener en recordar al trabajar con estos valores:</span><span class="sxs-lookup"><span data-stu-id="edbdd-113">Points to remember when working with these values:</span></span>

-   <span data-ttu-id="edbdd-114">Por definición, los nombres canónicos no cambian en función del idioma del sistema; siempre están en inglés, aunque el idioma del sistema no lo sea.</span><span class="sxs-lookup"><span data-stu-id="edbdd-114">By definition, canonical names do not change based on the system language; they're always in English, even if the system's language is not.</span></span>
-   <span data-ttu-id="edbdd-115">No todos los elementos del panel de control están presentes en todas las variedades de ventanas.</span><span class="sxs-lookup"><span data-stu-id="edbdd-115">Not all Control Panel items are present in all varieties of Windows.</span></span>
-   <span data-ttu-id="edbdd-116">Algunos elementos del panel de control solo aparecen si se detecta el hardware adecuado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="edbdd-116">Some Control Panel items only appear if the right hardware is detected on the system.</span></span>
-   <span data-ttu-id="edbdd-117">Los terceros también pueden agregar elementos del panel de control.</span><span class="sxs-lookup"><span data-stu-id="edbdd-117">Third parties can also add Control Panel items.</span></span> <span data-ttu-id="edbdd-118">Los nombres canónicos que se muestran aquí solo son para los elementos del panel de control que se incluyen con Windows.</span><span class="sxs-lookup"><span data-stu-id="edbdd-118">The canonical names listed here are only for Control Panel items that are included with Windows.</span></span>

<span data-ttu-id="edbdd-119">A continuación se muestran los elementos del panel de control disponibles en Windows 8.1:</span><span class="sxs-lookup"><span data-stu-id="edbdd-119">The following are the Control Panel items available in Windows 8.1:</span></span>

-   [<span data-ttu-id="edbdd-120">Centro de actividades</span><span class="sxs-lookup"><span data-stu-id="edbdd-120">Action Center</span></span>](#action-center)
-   [<span data-ttu-id="edbdd-121">Herramientas administrativas</span><span class="sxs-lookup"><span data-stu-id="edbdd-121">Administrative Tools</span></span>](#administrative-tools)
-   [<span data-ttu-id="edbdd-122">Estaba</span><span class="sxs-lookup"><span data-stu-id="edbdd-122">AutoPlay</span></span>](#autoplay)
-   [<span data-ttu-id="edbdd-123">Dispositivos biométricos</span><span class="sxs-lookup"><span data-stu-id="edbdd-123">Biometric Devices</span></span>](#biometric-devices)
-   [<span data-ttu-id="edbdd-124">Cifrado de unidad BitLocker</span><span class="sxs-lookup"><span data-stu-id="edbdd-124">BitLocker Drive Encryption</span></span>](#bitlocker-drive-encryption)
-   [<span data-ttu-id="edbdd-125">Administración del color</span><span class="sxs-lookup"><span data-stu-id="edbdd-125">Color Management</span></span>](#color-management)
-   [<span data-ttu-id="edbdd-126">Administrador de credenciales</span><span class="sxs-lookup"><span data-stu-id="edbdd-126">Credential Manager</span></span>](#credential-manager)
-   [<span data-ttu-id="edbdd-127">Fecha y hora</span><span class="sxs-lookup"><span data-stu-id="edbdd-127">Date and Time</span></span>](#date-and-time)
-   [<span data-ttu-id="edbdd-128">Programas predeterminados</span><span class="sxs-lookup"><span data-stu-id="edbdd-128">Default Programs</span></span>](#default-programs)
-   [<span data-ttu-id="edbdd-129">Administrador de dispositivos</span><span class="sxs-lookup"><span data-stu-id="edbdd-129">Device Manager</span></span>](#device-manager)
-   [<span data-ttu-id="edbdd-130">Dispositivos e impresoras</span><span class="sxs-lookup"><span data-stu-id="edbdd-130">Devices and Printers</span></span>](#devices-and-printers)
-   [<span data-ttu-id="edbdd-131">Pantalla</span><span class="sxs-lookup"><span data-stu-id="edbdd-131">Display</span></span>](#display)
-   [<span data-ttu-id="edbdd-132">Centro de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="edbdd-132">Ease of Access Center</span></span>](#ease-of-access-center)
-   [<span data-ttu-id="edbdd-133">Protección infantil</span><span class="sxs-lookup"><span data-stu-id="edbdd-133">Family Safety</span></span>](#family-safety)
-   [<span data-ttu-id="edbdd-134">Historial de archivos</span><span class="sxs-lookup"><span data-stu-id="edbdd-134">File History</span></span>](#file-history)
-   [<span data-ttu-id="edbdd-135">Opciones de carpeta</span><span class="sxs-lookup"><span data-stu-id="edbdd-135">Folder Options</span></span>](#folder-options)
-   [<span data-ttu-id="edbdd-136">Fuentes</span><span class="sxs-lookup"><span data-stu-id="edbdd-136">Fonts</span></span>](#fonts)
-   [<span data-ttu-id="edbdd-137">Grupo Hogar</span><span class="sxs-lookup"><span data-stu-id="edbdd-137">HomeGroup</span></span>](#homegroup)
-   [<span data-ttu-id="edbdd-138">Opciones de indización</span><span class="sxs-lookup"><span data-stu-id="edbdd-138">Indexing Options</span></span>](#indexing-options)
-   [<span data-ttu-id="edbdd-139">Infrarrojos</span><span class="sxs-lookup"><span data-stu-id="edbdd-139">Infrared</span></span>](#infrared)
-   [<span data-ttu-id="edbdd-140">Opciones de Internet</span><span class="sxs-lookup"><span data-stu-id="edbdd-140">Internet Options</span></span>](#internet-options)
-   [<span data-ttu-id="edbdd-141">Iniciador iSCSI</span><span class="sxs-lookup"><span data-stu-id="edbdd-141">iSCSI Initiator</span></span>](#iscsi-initiator)
-   [<span data-ttu-id="edbdd-142">Servidor iSNS</span><span class="sxs-lookup"><span data-stu-id="edbdd-142">iSNS Server</span></span>](#isns-server)
-   [<span data-ttu-id="edbdd-143">Teclado</span><span class="sxs-lookup"><span data-stu-id="edbdd-143">Keyboard</span></span>](#keyboard)
-   [<span data-ttu-id="edbdd-144">Configuración de ubicación</span><span class="sxs-lookup"><span data-stu-id="edbdd-144">Location Settings</span></span>](#location-settings)
-   [<span data-ttu-id="edbdd-145">Mouse</span><span class="sxs-lookup"><span data-stu-id="edbdd-145">Mouse</span></span>](#mouse)
-   [<span data-ttu-id="edbdd-146">MPIOConfiguration</span><span class="sxs-lookup"><span data-stu-id="edbdd-146">MPIOConfiguration</span></span>](#mpioconfiguration)
-   [<span data-ttu-id="edbdd-147">Centro de redes y recursos compartidos</span><span class="sxs-lookup"><span data-stu-id="edbdd-147">Network and Sharing Center</span></span>](#network-and-sharing-center)
-   [<span data-ttu-id="edbdd-148">Iconos del área de notificación</span><span class="sxs-lookup"><span data-stu-id="edbdd-148">Notification Area Icons</span></span>](#notification-area-icons)
-   [<span data-ttu-id="edbdd-149">Lápiz y entrada táctil</span><span class="sxs-lookup"><span data-stu-id="edbdd-149">Pen and Touch</span></span>](#pen-and-touch)
-   [<span data-ttu-id="edbdd-150">Personalización</span><span class="sxs-lookup"><span data-stu-id="edbdd-150">Personalization</span></span>](#personalization)
-   [<span data-ttu-id="edbdd-151">Teléfono y módem</span><span class="sxs-lookup"><span data-stu-id="edbdd-151">Phone and Modem</span></span>](#phone-and-modem)
-   [<span data-ttu-id="edbdd-152">Opciones de energía</span><span class="sxs-lookup"><span data-stu-id="edbdd-152">Power Options</span></span>](#power-options)
-   [<span data-ttu-id="edbdd-153">Programas y características</span><span class="sxs-lookup"><span data-stu-id="edbdd-153">Programs and Features</span></span>](#programs-and-features)
-   [<span data-ttu-id="edbdd-154">Recuperación</span><span class="sxs-lookup"><span data-stu-id="edbdd-154">Recovery</span></span>](#recovery)
-   [<span data-ttu-id="edbdd-155">Región</span><span class="sxs-lookup"><span data-stu-id="edbdd-155">Region</span></span>](#region)
-   [<span data-ttu-id="edbdd-156">Conexión de RemoteApp y Escritorio</span><span class="sxs-lookup"><span data-stu-id="edbdd-156">RemoteApp and Desktop Connections</span></span>](#remoteapp-and-desktop-connections)
-   [<span data-ttu-id="edbdd-157">Sonido</span><span class="sxs-lookup"><span data-stu-id="edbdd-157">Sound</span></span>](#sound)
-   [<span data-ttu-id="edbdd-158">Reconocimiento de voz</span><span class="sxs-lookup"><span data-stu-id="edbdd-158">Speech Recognition</span></span>](#speech-recognition)
-   [<span data-ttu-id="edbdd-159">Espacios de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="edbdd-159">Storage Spaces</span></span>](#storage-spaces)
-   [<span data-ttu-id="edbdd-160">Centro de sincronización</span><span class="sxs-lookup"><span data-stu-id="edbdd-160">Sync Center</span></span>](#sync-center)
-   [<span data-ttu-id="edbdd-161">Sistema</span><span class="sxs-lookup"><span data-stu-id="edbdd-161">System</span></span>](#system)
-   [<span data-ttu-id="edbdd-162">Configuración de Tablet PC</span><span class="sxs-lookup"><span data-stu-id="edbdd-162">Tablet PC Settings</span></span>](#tablet-pc-settings)
-   [<span data-ttu-id="edbdd-163">Barra de tareas y navegación</span><span class="sxs-lookup"><span data-stu-id="edbdd-163">Taskbar and Navigation</span></span>](#taskbar-and-navigation)
-   [<span data-ttu-id="edbdd-164">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="edbdd-164">Troubleshooting</span></span>](#troubleshooting)
-   [<span data-ttu-id="edbdd-165">TSAppInstall</span><span class="sxs-lookup"><span data-stu-id="edbdd-165">TSAppInstall</span></span>](#tsappinstall)
-   [<span data-ttu-id="edbdd-166">Cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="edbdd-166">User Accounts</span></span>](#user-accounts)
-   [<span data-ttu-id="edbdd-167">Windows Anytime Upgrade</span><span class="sxs-lookup"><span data-stu-id="edbdd-167">Windows Anytime Upgrade</span></span>](#windows-anytime-upgrade)
-   [<span data-ttu-id="edbdd-168">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="edbdd-168">Windows Defender</span></span>](#windows-defender)
-   [<span data-ttu-id="edbdd-169">Firewall de Windows</span><span class="sxs-lookup"><span data-stu-id="edbdd-169">Windows Firewall</span></span>](#windows-firewall)
-   [<span data-ttu-id="edbdd-170">Centro de movilidad de Windows</span><span class="sxs-lookup"><span data-stu-id="edbdd-170">Windows Mobility Center</span></span>](#windows-mobility-center)
-   [<span data-ttu-id="edbdd-171">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="edbdd-171">Windows To Go</span></span>](#windows-to-go)
-   [<span data-ttu-id="edbdd-172">Windows Update</span><span class="sxs-lookup"><span data-stu-id="edbdd-172">Windows Update</span></span>](#windows-update)
-   [<span data-ttu-id="edbdd-173">Carpetas de trabajo</span><span class="sxs-lookup"><span data-stu-id="edbdd-173">Work Folders</span></span>](#work-folders)

### <a name="action-center"></a><span data-ttu-id="edbdd-174">Centro de actividades</span><span class="sxs-lookup"><span data-stu-id="edbdd-174">Action Center</span></span>

-   <span data-ttu-id="edbdd-175">**Nombre canónico**: Microsoft. ActionCenter</span><span class="sxs-lookup"><span data-stu-id="edbdd-175">**Canonical name**: Microsoft.ActionCenter</span></span>
-   <span data-ttu-id="edbdd-176">**GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}</span><span class="sxs-lookup"><span data-stu-id="edbdd-176">**GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}</span></span>
-   <span data-ttu-id="edbdd-177">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-177">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-178">**Nombre del módulo**: @% SystemRoot% \\ system32 \\ActionCenterCPL.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-178">**Module name**: @%SystemRoot%\\System32\\ActionCenterCPL.dll,-1</span></span>
-   <span data-ttu-id="edbdd-179">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-179">**Pages**</span></span>

    | <span data-ttu-id="edbdd-180">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-180">Page Name</span></span>           | <span data-ttu-id="edbdd-181">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-181">Opens</span></span>                      |
    |---------------------|----------------------------|
    | <span data-ttu-id="edbdd-182">MaintenanceSettings</span><span class="sxs-lookup"><span data-stu-id="edbdd-182">MaintenanceSettings</span></span> | <span data-ttu-id="edbdd-183">Mantenimiento automático</span><span class="sxs-lookup"><span data-stu-id="edbdd-183">Automatic Maintenance</span></span>      |
    | <span data-ttu-id="edbdd-184">pageProblems</span><span class="sxs-lookup"><span data-stu-id="edbdd-184">pageProblems</span></span>        | <span data-ttu-id="edbdd-185">Informes de problemas</span><span class="sxs-lookup"><span data-stu-id="edbdd-185">Problem Reports</span></span>            |
    | <span data-ttu-id="edbdd-186">pageReliabilityView</span><span class="sxs-lookup"><span data-stu-id="edbdd-186">pageReliabilityView</span></span> | <span data-ttu-id="edbdd-187">Monitor de confiabilidad</span><span class="sxs-lookup"><span data-stu-id="edbdd-187">Reliability Monitor</span></span>        |
    | <span data-ttu-id="edbdd-188">pageResponseArchive</span><span class="sxs-lookup"><span data-stu-id="edbdd-188">pageResponseArchive</span></span> | <span data-ttu-id="edbdd-189">Mensajes archivados</span><span class="sxs-lookup"><span data-stu-id="edbdd-189">Archived Messages</span></span>          |
    | <span data-ttu-id="edbdd-190">pageSettings</span><span class="sxs-lookup"><span data-stu-id="edbdd-190">pageSettings</span></span>        | <span data-ttu-id="edbdd-191">Configuración de informes de problemas</span><span class="sxs-lookup"><span data-stu-id="edbdd-191">Problem Reporting Settings</span></span> |

    

     

### <a name="administrative-tools"></a><span data-ttu-id="edbdd-192">Herramientas administrativas</span><span class="sxs-lookup"><span data-stu-id="edbdd-192">Administrative Tools</span></span>

-   <span data-ttu-id="edbdd-193">**Nombre canónico**: Microsoft. AdministrativeTools</span><span class="sxs-lookup"><span data-stu-id="edbdd-193">**Canonical name**: Microsoft.AdministrativeTools</span></span>
-   <span data-ttu-id="edbdd-194">**GUID**: {D20EA4E1-3957-11D2-A40B-0C5020524153}</span><span class="sxs-lookup"><span data-stu-id="edbdd-194">**GUID**: {D20EA4E1-3957-11d2-A40B-0C5020524153}</span></span>
-   <span data-ttu-id="edbdd-195">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-195">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-196">**Nombre del módulo**: @% SystemRoot% \\ system32 \\shell32.dll,-22982</span><span class="sxs-lookup"><span data-stu-id="edbdd-196">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-22982</span></span>

### <a name="autoplay"></a><span data-ttu-id="edbdd-197">Reproducción automática</span><span class="sxs-lookup"><span data-stu-id="edbdd-197">AutoPlay</span></span>

-   <span data-ttu-id="edbdd-198">**Nombre canónico**: Microsoft. hyperplay</span><span class="sxs-lookup"><span data-stu-id="edbdd-198">**Canonical name**: Microsoft.AutoPlay</span></span>
-   <span data-ttu-id="edbdd-199">**GUID**: {9C60DE1E-E5FC-40f4-A487-460851A8D915}</span><span class="sxs-lookup"><span data-stu-id="edbdd-199">**GUID**: {9C60DE1E-E5FC-40f4-A487-460851A8D915}</span></span>
-   <span data-ttu-id="edbdd-200">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-200">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-201">**Nombre del módulo**: @% SystemRoot% \\ system32 \\autoplay.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-201">**Module name**: @%SystemRoot%\\System32\\autoplay.dll,-1</span></span>

### <a name="biometric-devices"></a><span data-ttu-id="edbdd-202">Dispositivos biométricos</span><span class="sxs-lookup"><span data-stu-id="edbdd-202">Biometric Devices</span></span>

-   <span data-ttu-id="edbdd-203">**Nombre canónico**: Microsoft. BiometricDevices</span><span class="sxs-lookup"><span data-stu-id="edbdd-203">**Canonical name**: Microsoft.BiometricDevices</span></span>
-   <span data-ttu-id="edbdd-204">**GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}</span><span class="sxs-lookup"><span data-stu-id="edbdd-204">**GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}</span></span>
-   <span data-ttu-id="edbdd-205">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-205">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-206">**Nombre del módulo**: @% SystemRoot% \\ system32 \\biocpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-206">**Module name**: @%SystemRoot%\\System32\\biocpl.dll,-1</span></span>

### <a name="bitlocker-drive-encryption"></a><span data-ttu-id="edbdd-207">Cifrado BitLocker de unidades</span><span class="sxs-lookup"><span data-stu-id="edbdd-207">BitLocker Drive Encryption</span></span>

-   <span data-ttu-id="edbdd-208">**Nombre canónico**: Microsoft. BitLockerDriveEncryption</span><span class="sxs-lookup"><span data-stu-id="edbdd-208">**Canonical name**: Microsoft.BitLockerDriveEncryption</span></span>
-   <span data-ttu-id="edbdd-209">**GUID**: {D9EF8727-CaC2-4e60-809E-86F80A666C91}</span><span class="sxs-lookup"><span data-stu-id="edbdd-209">**GUID**: {D9EF8727-CAC2-4e60-809E-86F80A666C91}</span></span>
-   <span data-ttu-id="edbdd-210">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-210">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-211">**Nombre del módulo**: @% SystemRoot% \\ system32 \\fvecpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-211">**Module name**: @%SystemRoot%\\System32\\fvecpl.dll,-1</span></span>

### <a name="color-management"></a><span data-ttu-id="edbdd-212">Administración del color</span><span class="sxs-lookup"><span data-stu-id="edbdd-212">Color Management</span></span>

-   <span data-ttu-id="edbdd-213">**Nombre canónico**: Microsoft. ColorManagement</span><span class="sxs-lookup"><span data-stu-id="edbdd-213">**Canonical name**: Microsoft.ColorManagement</span></span>
-   <span data-ttu-id="edbdd-214">**GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}</span><span class="sxs-lookup"><span data-stu-id="edbdd-214">**GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}</span></span>
-   <span data-ttu-id="edbdd-215">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-215">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-216">**Nombre del módulo**: @% SystemRoot% \\ system32 \\colorcpl.exe,-6</span><span class="sxs-lookup"><span data-stu-id="edbdd-216">**Module name**: @%systemroot%\\system32\\colorcpl.exe,-6</span></span>

### <a name="credential-manager"></a><span data-ttu-id="edbdd-217">Administrador de credenciales</span><span class="sxs-lookup"><span data-stu-id="edbdd-217">Credential Manager</span></span>

-   <span data-ttu-id="edbdd-218">**Nombre canónico**: Microsoft. CredentialManager</span><span class="sxs-lookup"><span data-stu-id="edbdd-218">**Canonical name**: Microsoft.CredentialManager</span></span>
-   <span data-ttu-id="edbdd-219">**GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}</span><span class="sxs-lookup"><span data-stu-id="edbdd-219">**GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}</span></span>
-   <span data-ttu-id="edbdd-220">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-220">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-221">**Nombre del módulo**: @% SystemRoot% \\ system32 \\Vault.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-221">**Module name**: @%SystemRoot%\\system32\\Vault.dll,-1</span></span>
-   <span data-ttu-id="edbdd-222">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-222">**Pages**</span></span>

    | <span data-ttu-id="edbdd-223">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-223">Page Name</span></span>                   | <span data-ttu-id="edbdd-224">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-224">Opens</span></span>               |
    |-----------------------------|---------------------|
    | <span data-ttu-id="edbdd-225">? SelectedVault = CredmanVault</span><span class="sxs-lookup"><span data-stu-id="edbdd-225">?SelectedVault=CredmanVault</span></span> | <span data-ttu-id="edbdd-226">Credenciales de Windows</span><span class="sxs-lookup"><span data-stu-id="edbdd-226">Windows Credentials</span></span> |

    

     

### <a name="date-and-time"></a><span data-ttu-id="edbdd-227">Fecha y hora</span><span class="sxs-lookup"><span data-stu-id="edbdd-227">Date and Time</span></span>

-   <span data-ttu-id="edbdd-228">**Nombre canónico**: Microsoft. DateAndTime</span><span class="sxs-lookup"><span data-stu-id="edbdd-228">**Canonical name**: Microsoft.DateAndTime</span></span>
-   <span data-ttu-id="edbdd-229">**GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}</span><span class="sxs-lookup"><span data-stu-id="edbdd-229">**GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}</span></span>
-   <span data-ttu-id="edbdd-230">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-230">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-231">**Nombre del módulo**: @% SystemRoot% \\ system32 \\timedate.cpl,-51</span><span class="sxs-lookup"><span data-stu-id="edbdd-231">**Module name**: @%SystemRoot%\\System32\\timedate.cpl,-51</span></span>
-   <span data-ttu-id="edbdd-232">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-232">**Pages**</span></span>

    | <span data-ttu-id="edbdd-233">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-233">Page Name</span></span> | <span data-ttu-id="edbdd-234">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-234">Opens</span></span>             |
    |-----------|-------------------|
    | <span data-ttu-id="edbdd-235">1</span><span class="sxs-lookup"><span data-stu-id="edbdd-235">1</span></span>         | <span data-ttu-id="edbdd-236">Relojes adicionales</span><span class="sxs-lookup"><span data-stu-id="edbdd-236">Additional Clocks</span></span> |

    

     

### <a name="default-programs"></a><span data-ttu-id="edbdd-237">Programas predeterminados</span><span class="sxs-lookup"><span data-stu-id="edbdd-237">Default Programs</span></span>

-   <span data-ttu-id="edbdd-238">**Nombre canónico**: Microsoft. DefaultPrograms</span><span class="sxs-lookup"><span data-stu-id="edbdd-238">**Canonical name**: Microsoft.DefaultPrograms</span></span>
-   <span data-ttu-id="edbdd-239">**GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}</span><span class="sxs-lookup"><span data-stu-id="edbdd-239">**GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}</span></span>
-   <span data-ttu-id="edbdd-240">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-240">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-241">**Nombre del módulo**: @% SystemRoot% \\ system32 \\sud.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-241">**Module name**: @%SystemRoot%\\System32\\sud.dll,-1</span></span>
-   <span data-ttu-id="edbdd-242">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-242">**Pages**</span></span>

    | <span data-ttu-id="edbdd-243">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-243">Page Name</span></span>          | <span data-ttu-id="edbdd-244">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-244">Opens</span></span>                |
    |--------------------|----------------------|
    | <span data-ttu-id="edbdd-245">pageDefaultProgram</span><span class="sxs-lookup"><span data-stu-id="edbdd-245">pageDefaultProgram</span></span> | <span data-ttu-id="edbdd-246">Establecer programas predeterminados</span><span class="sxs-lookup"><span data-stu-id="edbdd-246">Set Default Programs</span></span> |
    | <span data-ttu-id="edbdd-247">pageFileAssoc</span><span class="sxs-lookup"><span data-stu-id="edbdd-247">pageFileAssoc</span></span>      | <span data-ttu-id="edbdd-248">Establecer asociaciones</span><span class="sxs-lookup"><span data-stu-id="edbdd-248">Set Associations</span></span>     |

    

     

### <a name="device-manager"></a><span data-ttu-id="edbdd-249">Administrador de dispositivos</span><span class="sxs-lookup"><span data-stu-id="edbdd-249">Device Manager</span></span>

-   <span data-ttu-id="edbdd-250">**Nombre canónico**: Microsoft. DeviceManager</span><span class="sxs-lookup"><span data-stu-id="edbdd-250">**Canonical name**: Microsoft.DeviceManager</span></span>
-   <span data-ttu-id="edbdd-251">**GUID**: {74246bfc-4c96-11d0-abef-0020af6b0b7a}</span><span class="sxs-lookup"><span data-stu-id="edbdd-251">**GUID**: {74246bfc-4c96-11d0-abef-0020af6b0b7a}</span></span>
-   <span data-ttu-id="edbdd-252">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-252">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-253">**Nombre del módulo**: @% SystemRoot% \\ system32 \\devmgr.dll,-4</span><span class="sxs-lookup"><span data-stu-id="edbdd-253">**Module name**: @%SystemRoot%\\System32\\devmgr.dll,-4</span></span>

### <a name="devices-and-printers"></a><span data-ttu-id="edbdd-254">Dispositivos e impresoras</span><span class="sxs-lookup"><span data-stu-id="edbdd-254">Devices and Printers</span></span>

-   <span data-ttu-id="edbdd-255">**Nombre canónico**: Microsoft. DevicesAndPrinters</span><span class="sxs-lookup"><span data-stu-id="edbdd-255">**Canonical name**: Microsoft.DevicesAndPrinters</span></span>
-   <span data-ttu-id="edbdd-256">**GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}</span><span class="sxs-lookup"><span data-stu-id="edbdd-256">**GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}</span></span>
-   <span data-ttu-id="edbdd-257">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-257">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-258">**Nombre del módulo**: @% SystemRoot% \\ system32 \\DeviceCenter.dll,-1000</span><span class="sxs-lookup"><span data-stu-id="edbdd-258">**Module name**: @%systemroot%\\system32\\DeviceCenter.dll,-1000</span></span>

### <a name="display"></a><span data-ttu-id="edbdd-259">Pantalla</span><span class="sxs-lookup"><span data-stu-id="edbdd-259">Display</span></span>

-   <span data-ttu-id="edbdd-260">**Nombre canónico**: Microsoft. display</span><span class="sxs-lookup"><span data-stu-id="edbdd-260">**Canonical name**: Microsoft.Display</span></span>
-   <span data-ttu-id="edbdd-261">**GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}</span><span class="sxs-lookup"><span data-stu-id="edbdd-261">**GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}</span></span>
-   <span data-ttu-id="edbdd-262">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-262">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-263">**Nombre del módulo**: @% SystemRoot% \\ system32 \\Display.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-263">**Module name**: @%SystemRoot%\\System32\\Display.dll,-1</span></span>
-   <span data-ttu-id="edbdd-264">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-264">**Pages**</span></span>

    | <span data-ttu-id="edbdd-265">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-265">Page Name</span></span> | <span data-ttu-id="edbdd-266">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-266">Opens</span></span>             |
    |-----------|-------------------|
    | <span data-ttu-id="edbdd-267">Configuración</span><span class="sxs-lookup"><span data-stu-id="edbdd-267">Settings</span></span>  | <span data-ttu-id="edbdd-268">Resolución de pantalla</span><span class="sxs-lookup"><span data-stu-id="edbdd-268">Screen Resolution</span></span> |

    

     

### <a name="ease-of-access-center"></a><span data-ttu-id="edbdd-269">Centro de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="edbdd-269">Ease of Access Center</span></span>

-   <span data-ttu-id="edbdd-270">**Nombre canónico**: Microsoft. EaseOfAccessCenter</span><span class="sxs-lookup"><span data-stu-id="edbdd-270">**Canonical name**: Microsoft.EaseOfAccessCenter</span></span>
-   <span data-ttu-id="edbdd-271">**GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}</span><span class="sxs-lookup"><span data-stu-id="edbdd-271">**GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}</span></span>
-   <span data-ttu-id="edbdd-272">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-272">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-273">**Nombre del módulo**: @% SystemRoot% \\ system32 \\accessibilitycpl.dll,-10</span><span class="sxs-lookup"><span data-stu-id="edbdd-273">**Module name**: @%SystemRoot%\\System32\\accessibilitycpl.dll,-10</span></span>
-   <span data-ttu-id="edbdd-274">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-274">**Pages**</span></span>

    | <span data-ttu-id="edbdd-275">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-275">Page Name</span></span>               | <span data-ttu-id="edbdd-276">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-276">Opens</span></span>                                                               |
    |-------------------------|---------------------------------------------------------------------|
    | <span data-ttu-id="edbdd-277">pageEasierToClick</span><span class="sxs-lookup"><span data-stu-id="edbdd-277">pageEasierToClick</span></span>       | <span data-ttu-id="edbdd-278">Facilitar el uso del mouse</span><span class="sxs-lookup"><span data-stu-id="edbdd-278">Make the mouse easier to use</span></span>                                        |
    | <span data-ttu-id="edbdd-279">pageEasierToSee</span><span class="sxs-lookup"><span data-stu-id="edbdd-279">pageEasierToSee</span></span>         | <span data-ttu-id="edbdd-280">Facilitar la visualización en el equipo</span><span class="sxs-lookup"><span data-stu-id="edbdd-280">Make the computer easier to see</span></span>                                     |
    | <span data-ttu-id="edbdd-281">pageEasierWithSounds</span><span class="sxs-lookup"><span data-stu-id="edbdd-281">pageEasierWithSounds</span></span>    | <span data-ttu-id="edbdd-282">Usar texto o alternativas visuales para los sonidos</span><span class="sxs-lookup"><span data-stu-id="edbdd-282">Use text or visual alternatives for sounds</span></span>                          |
    | <span data-ttu-id="edbdd-283">pageFilterKeysSettings</span><span class="sxs-lookup"><span data-stu-id="edbdd-283">pageFilterKeysSettings</span></span>  | <span data-ttu-id="edbdd-284">Configurar claves de filtro</span><span class="sxs-lookup"><span data-stu-id="edbdd-284">Set up Filter Keys</span></span>                                                  |
    | <span data-ttu-id="edbdd-285">pageKeyboardEasierToUse</span><span class="sxs-lookup"><span data-stu-id="edbdd-285">pageKeyboardEasierToUse</span></span> | <span data-ttu-id="edbdd-286">Facilitar el uso del teclado</span><span class="sxs-lookup"><span data-stu-id="edbdd-286">Make the keyboard easier to use</span></span>                                     |
    | <span data-ttu-id="edbdd-287">pageNoMouseOrKeyboard</span><span class="sxs-lookup"><span data-stu-id="edbdd-287">pageNoMouseOrKeyboard</span></span>   | <span data-ttu-id="edbdd-288">Usar el equipo sin un mouse o teclado</span><span class="sxs-lookup"><span data-stu-id="edbdd-288">Use the computer without a mouse or keyboard</span></span>                        |
    | <span data-ttu-id="edbdd-289">pageNoVisual</span><span class="sxs-lookup"><span data-stu-id="edbdd-289">pageNoVisual</span></span>            | <span data-ttu-id="edbdd-290">Usar el equipo sin pantalla</span><span class="sxs-lookup"><span data-stu-id="edbdd-290">Use the computer without a display</span></span>                                  |
    | <span data-ttu-id="edbdd-291">pageQuestionsCognitive</span><span class="sxs-lookup"><span data-stu-id="edbdd-291">pageQuestionsCognitive</span></span>  | <span data-ttu-id="edbdd-292">Obtener recomendaciones para facilitar el uso del equipo (cognitiva)</span><span class="sxs-lookup"><span data-stu-id="edbdd-292">Get recommendations to make your computer easier to use (cognitive)</span></span> |
    | <span data-ttu-id="edbdd-293">pageQuestionsEyesight</span><span class="sxs-lookup"><span data-stu-id="edbdd-293">pageQuestionsEyesight</span></span>   | <span data-ttu-id="edbdd-294">Obtener recomendaciones para facilitar el uso del equipo (ver)</span><span class="sxs-lookup"><span data-stu-id="edbdd-294">Get recommendations to make your computer easier to use (eyesight)</span></span>  |

    

     

### <a name="family-safety"></a><span data-ttu-id="edbdd-295">Protección infantil</span><span class="sxs-lookup"><span data-stu-id="edbdd-295">Family Safety</span></span>

-   <span data-ttu-id="edbdd-296">**Nombre canónico**: Microsoft. ParentalControls</span><span class="sxs-lookup"><span data-stu-id="edbdd-296">**Canonical name**: Microsoft.ParentalControls</span></span>
-   <span data-ttu-id="edbdd-297">**GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}</span><span class="sxs-lookup"><span data-stu-id="edbdd-297">**GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}</span></span>
-   <span data-ttu-id="edbdd-298">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-298">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-299">**Nombre del módulo**: @% SystemRoot% \\ system32 \\wpccpl.dll,-100</span><span class="sxs-lookup"><span data-stu-id="edbdd-299">**Module name**: @%SystemRoot%\\System32\\wpccpl.dll,-100</span></span>
-   <span data-ttu-id="edbdd-300">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-300">**Pages**</span></span>

    | <span data-ttu-id="edbdd-301">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-301">Page Name</span></span>   | <span data-ttu-id="edbdd-302">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-302">Opens</span></span>                                  |
    |-------------|----------------------------------------|
    | <span data-ttu-id="edbdd-303">pageUserHub</span><span class="sxs-lookup"><span data-stu-id="edbdd-303">pageUserHub</span></span> | <span data-ttu-id="edbdd-304">Elección de un usuario y configuración de la seguridad de la familia</span><span class="sxs-lookup"><span data-stu-id="edbdd-304">Choose a user and set up Family Safety</span></span> |

    

     

### <a name="file-history"></a><span data-ttu-id="edbdd-305">Historial de archivos</span><span class="sxs-lookup"><span data-stu-id="edbdd-305">File History</span></span>

-   <span data-ttu-id="edbdd-306">**Nombre canónico**: Microsoft. FileHistory</span><span class="sxs-lookup"><span data-stu-id="edbdd-306">**Canonical name**: Microsoft.FileHistory</span></span>
-   <span data-ttu-id="edbdd-307">**GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}</span><span class="sxs-lookup"><span data-stu-id="edbdd-307">**GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}</span></span>
-   <span data-ttu-id="edbdd-308">**Sistema operativo compatible**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-308">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-309">**Nombre del módulo**: @% SystemRoot% \\ system32 \\fhcpl.dll,-52</span><span class="sxs-lookup"><span data-stu-id="edbdd-309">**Module name**: @%SystemRoot%\\System32\\fhcpl.dll,-52</span></span>
-   <span data-ttu-id="edbdd-310">El historial de archivos incluye una versión más reciente del elemento de copia de seguridad y restauración, pero el nombre canónico del elemento anterior no se reasigna al historial de archivos.</span><span class="sxs-lookup"><span data-stu-id="edbdd-310">File History includes a newer version of the Backup and Restore item, but that older item's canonical name does not remap to File History.</span></span>

### <a name="folder-options"></a><span data-ttu-id="edbdd-311">Opciones de carpeta</span><span class="sxs-lookup"><span data-stu-id="edbdd-311">Folder Options</span></span>

-   <span data-ttu-id="edbdd-312">**Nombre canónico**: Microsoft. FolderOptions</span><span class="sxs-lookup"><span data-stu-id="edbdd-312">**Canonical name**: Microsoft.FolderOptions</span></span>
-   <span data-ttu-id="edbdd-313">**GUID**: {6DFD7C5C-2451-11D3-A299-00C04F8EF6AF}</span><span class="sxs-lookup"><span data-stu-id="edbdd-313">**GUID**: {6DFD7C5C-2451-11d3-A299-00C04F8EF6AF}</span></span>
-   <span data-ttu-id="edbdd-314">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-314">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-315">**Nombre del módulo**: @% SystemRoot% \\ system32 \\shell32.dll,-22985</span><span class="sxs-lookup"><span data-stu-id="edbdd-315">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-22985</span></span>

### <a name="fonts"></a><span data-ttu-id="edbdd-316">Fuentes</span><span class="sxs-lookup"><span data-stu-id="edbdd-316">Fonts</span></span>

-   <span data-ttu-id="edbdd-317">**Nombre canónico**: Microsoft. Fonts</span><span class="sxs-lookup"><span data-stu-id="edbdd-317">**Canonical name**: Microsoft.Fonts</span></span>
-   <span data-ttu-id="edbdd-318">**GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}</span><span class="sxs-lookup"><span data-stu-id="edbdd-318">**GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}</span></span>
-   <span data-ttu-id="edbdd-319">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-319">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-320">**Nombre del módulo**: @% SystemRoot% \\ system32 \\FontExt.dll,-8007</span><span class="sxs-lookup"><span data-stu-id="edbdd-320">**Module name**: @%SystemRoot%\\System32\\FontExt.dll,-8007</span></span>

### <a name="homegroup"></a><span data-ttu-id="edbdd-321">Grupo Hogar</span><span class="sxs-lookup"><span data-stu-id="edbdd-321">HomeGroup</span></span>

-   <span data-ttu-id="edbdd-322">**Nombre canónico**: Microsoft. Grupo hogar</span><span class="sxs-lookup"><span data-stu-id="edbdd-322">**Canonical name**: Microsoft.HomeGroup</span></span>
-   <span data-ttu-id="edbdd-323">**GUID**: {67CA7650-96E6-4FDD-BB43-A8E774F73A57}</span><span class="sxs-lookup"><span data-stu-id="edbdd-323">**GUID**: {67CA7650-96E6-4FDD-BB43-A8E774F73A57}</span></span>
-   <span data-ttu-id="edbdd-324">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-324">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-325">**Nombre del módulo**: @% SystemRoot% \\ system32 \\hgcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-325">**Module name**: @%SystemRoot%\\System32\\hgcpl.dll,-1</span></span>

### <a name="indexing-options"></a><span data-ttu-id="edbdd-326">Opciones de indización</span><span class="sxs-lookup"><span data-stu-id="edbdd-326">Indexing Options</span></span>

-   <span data-ttu-id="edbdd-327">**Nombre canónico**: Microsoft. IndexingOptions</span><span class="sxs-lookup"><span data-stu-id="edbdd-327">**Canonical name**: Microsoft.IndexingOptions</span></span>
-   <span data-ttu-id="edbdd-328">**GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}</span><span class="sxs-lookup"><span data-stu-id="edbdd-328">**GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}</span></span>
-   <span data-ttu-id="edbdd-329">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-329">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-330">**Nombre del módulo**: @% SystemRoot% \\ system32 \\srchadmin.dll,-601</span><span class="sxs-lookup"><span data-stu-id="edbdd-330">**Module name**: @%SystemRoot%\\System32\\srchadmin.dll,-601</span></span>

### <a name="infrared"></a><span data-ttu-id="edbdd-331">Infrarrojos</span><span class="sxs-lookup"><span data-stu-id="edbdd-331">Infrared</span></span>

-   <span data-ttu-id="edbdd-332">**Nombre canónico**: Microsoft. infrarrojos</span><span class="sxs-lookup"><span data-stu-id="edbdd-332">**Canonical name**: Microsoft.Infrared</span></span>
-   <span data-ttu-id="edbdd-333">**GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span><span class="sxs-lookup"><span data-stu-id="edbdd-333">**GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span></span>
-   <span data-ttu-id="edbdd-334">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-334">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-335">**Nombre del módulo**: @% SystemRoot% \\ system32 \\irprops.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-335">**Module name**: @%SystemRoot%\\System32\\irprops.cpl,-1</span></span>

### <a name="internet-options"></a><span data-ttu-id="edbdd-336">Opciones de Internet</span><span class="sxs-lookup"><span data-stu-id="edbdd-336">Internet Options</span></span>

-   <span data-ttu-id="edbdd-337">**Nombre canónico**: Microsoft. InternetOptions</span><span class="sxs-lookup"><span data-stu-id="edbdd-337">**Canonical name**: Microsoft.InternetOptions</span></span>
-   <span data-ttu-id="edbdd-338">**GUID**: {A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}</span><span class="sxs-lookup"><span data-stu-id="edbdd-338">**GUID**: {A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}</span></span>
-   <span data-ttu-id="edbdd-339">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-339">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-340">**Nombre del módulo**: @C: \\ Windows \\ system32 \\inetcpl.cpl,-4312</span><span class="sxs-lookup"><span data-stu-id="edbdd-340">**Module name**: @C:\\Windows\\System32\\inetcpl.cpl,-4312</span></span>
-   <span data-ttu-id="edbdd-341">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-341">**Pages**</span></span>

    | <span data-ttu-id="edbdd-342">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-342">Page Name</span></span> | <span data-ttu-id="edbdd-343">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-343">Opens</span></span>       |
    |-----------|-------------|
    | <span data-ttu-id="edbdd-344">1</span><span class="sxs-lookup"><span data-stu-id="edbdd-344">1</span></span>         | <span data-ttu-id="edbdd-345">Seguridad</span><span class="sxs-lookup"><span data-stu-id="edbdd-345">Security</span></span>    |
    | <span data-ttu-id="edbdd-346">2</span><span class="sxs-lookup"><span data-stu-id="edbdd-346">2</span></span>         | <span data-ttu-id="edbdd-347">Privacidad</span><span class="sxs-lookup"><span data-stu-id="edbdd-347">Privacy</span></span>     |
    | <span data-ttu-id="edbdd-348">3</span><span class="sxs-lookup"><span data-stu-id="edbdd-348">3</span></span>         | <span data-ttu-id="edbdd-349">Contenido</span><span class="sxs-lookup"><span data-stu-id="edbdd-349">Content</span></span>     |
    | <span data-ttu-id="edbdd-350">4</span><span class="sxs-lookup"><span data-stu-id="edbdd-350">4</span></span>         | <span data-ttu-id="edbdd-351">Conexiones</span><span class="sxs-lookup"><span data-stu-id="edbdd-351">Connections</span></span> |
    | <span data-ttu-id="edbdd-352">5</span><span class="sxs-lookup"><span data-stu-id="edbdd-352">5</span></span>         | <span data-ttu-id="edbdd-353">Programas</span><span class="sxs-lookup"><span data-stu-id="edbdd-353">Programs</span></span>    |
    | <span data-ttu-id="edbdd-354">6</span><span class="sxs-lookup"><span data-stu-id="edbdd-354">6</span></span>         | <span data-ttu-id="edbdd-355">Avanzado</span><span class="sxs-lookup"><span data-stu-id="edbdd-355">Advanced</span></span>    |

    

     

### <a name="iscsi-initiator"></a><span data-ttu-id="edbdd-356">Iniciador iSCSI</span><span class="sxs-lookup"><span data-stu-id="edbdd-356">iSCSI Initiator</span></span>

-   <span data-ttu-id="edbdd-357">**Nombre canónico**: Microsoft. iSCSIInitiator</span><span class="sxs-lookup"><span data-stu-id="edbdd-357">**Canonical name**: Microsoft.iSCSIInitiator</span></span>
-   <span data-ttu-id="edbdd-358">**GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}</span><span class="sxs-lookup"><span data-stu-id="edbdd-358">**GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}</span></span>
-   <span data-ttu-id="edbdd-359">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-359">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-360">**Nombre del módulo**: @% SystemRoot% \\ system32 \\iscsicpl.dll,-5001</span><span class="sxs-lookup"><span data-stu-id="edbdd-360">**Module name**: @%SystemRoot%\\System32\\iscsicpl.dll,-5001</span></span>

### <a name="isns-server"></a><span data-ttu-id="edbdd-361">Servidor iSNS</span><span class="sxs-lookup"><span data-stu-id="edbdd-361">iSNS Server</span></span>

-   <span data-ttu-id="edbdd-362">**Nombre canónico**: Microsoft. iSNSServer</span><span class="sxs-lookup"><span data-stu-id="edbdd-362">**Canonical name**: Microsoft.iSNSServer</span></span>
-   <span data-ttu-id="edbdd-363">**GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}</span><span class="sxs-lookup"><span data-stu-id="edbdd-363">**GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}</span></span>
-   <span data-ttu-id="edbdd-364">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-364">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-365">**Nombre del módulo**: @% SystemRoot% \\ system32 \\isnssrv.dll,-5005</span><span class="sxs-lookup"><span data-stu-id="edbdd-365">**Module name**: @%SystemRoot%\\System32\\isnssrv.dll,-5005</span></span>
-   <span data-ttu-id="edbdd-366">Este elemento del panel de control solo se verá en las versiones de servidor de Windows.</span><span class="sxs-lookup"><span data-stu-id="edbdd-366">This Control Panel item will be seen only in server versions of Windows.</span></span>

### <a name="keyboard"></a><span data-ttu-id="edbdd-367">Keyboard</span><span class="sxs-lookup"><span data-stu-id="edbdd-367">Keyboard</span></span>

-   <span data-ttu-id="edbdd-368">**Nombre canónico**: Microsoft. Keyboard</span><span class="sxs-lookup"><span data-stu-id="edbdd-368">**Canonical name**: Microsoft.Keyboard</span></span>
-   <span data-ttu-id="edbdd-369">**GUID**: {725BE8F7-668E-4C7B-8F90-46BDB0936430}</span><span class="sxs-lookup"><span data-stu-id="edbdd-369">**GUID**: {725BE8F7-668E-4C7B-8F90-46BDB0936430}</span></span>
-   <span data-ttu-id="edbdd-370">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-370">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-371">**Nombre del módulo**: @% SystemRoot% \\ system32 \\main.cpl,-102</span><span class="sxs-lookup"><span data-stu-id="edbdd-371">**Module name**: @%SystemRoot%\\System32\\main.cpl,-102</span></span>

### <a name="location-settings"></a><span data-ttu-id="edbdd-372">Configuración de ubicación</span><span class="sxs-lookup"><span data-stu-id="edbdd-372">Location Settings</span></span>

-   <span data-ttu-id="edbdd-373">**Nombre canónico**: Microsoft. LocationSettings</span><span class="sxs-lookup"><span data-stu-id="edbdd-373">**Canonical name**: Microsoft.LocationSettings</span></span>
-   <span data-ttu-id="edbdd-374">**GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}</span><span class="sxs-lookup"><span data-stu-id="edbdd-374">**GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}</span></span>
-   <span data-ttu-id="edbdd-375">**Sistema operativo compatible**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-375">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-376">**Nombre del módulo**: @% SystemRoot% \\ system32 \\SensorsCpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-376">**Module name**: @%SystemRoot%\\System32\\SensorsCpl.dll,-1</span></span>

### <a name="mouse"></a><span data-ttu-id="edbdd-377">Mouse</span><span class="sxs-lookup"><span data-stu-id="edbdd-377">Mouse</span></span>

-   <span data-ttu-id="edbdd-378">**Nombre canónico**: Microsoft. Mouse</span><span class="sxs-lookup"><span data-stu-id="edbdd-378">**Canonical name**: Microsoft.Mouse</span></span>
-   <span data-ttu-id="edbdd-379">**GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}</span><span class="sxs-lookup"><span data-stu-id="edbdd-379">**GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}</span></span>
-   <span data-ttu-id="edbdd-380">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-380">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-381">**Nombre del módulo**: @% SystemRoot% \\ system32 \\main.cpl,-100</span><span class="sxs-lookup"><span data-stu-id="edbdd-381">**Module name**: @%SystemRoot%\\System32\\main.cpl,-100</span></span>
-   <span data-ttu-id="edbdd-382">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-382">**Pages**</span></span>

    | <span data-ttu-id="edbdd-383">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-383">Page Name</span></span> | <span data-ttu-id="edbdd-384">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-384">Opens</span></span>           |
    |-----------|-----------------|
    | <span data-ttu-id="edbdd-385">1</span><span class="sxs-lookup"><span data-stu-id="edbdd-385">1</span></span>         | <span data-ttu-id="edbdd-386">Punteros</span><span class="sxs-lookup"><span data-stu-id="edbdd-386">Pointers</span></span>        |
    | <span data-ttu-id="edbdd-387">2</span><span class="sxs-lookup"><span data-stu-id="edbdd-387">2</span></span>         | <span data-ttu-id="edbdd-388">Opciones de puntero</span><span class="sxs-lookup"><span data-stu-id="edbdd-388">Pointer Options</span></span> |
    | <span data-ttu-id="edbdd-389">3</span><span class="sxs-lookup"><span data-stu-id="edbdd-389">3</span></span>         | <span data-ttu-id="edbdd-390">Rueda</span><span class="sxs-lookup"><span data-stu-id="edbdd-390">Wheel</span></span>           |
    | <span data-ttu-id="edbdd-391">4</span><span class="sxs-lookup"><span data-stu-id="edbdd-391">4</span></span>         | <span data-ttu-id="edbdd-392">Hardware</span><span class="sxs-lookup"><span data-stu-id="edbdd-392">Hardware</span></span>        |

    

     

### <a name="mpioconfiguration"></a><span data-ttu-id="edbdd-393">MPIOConfiguration</span><span class="sxs-lookup"><span data-stu-id="edbdd-393">MPIOConfiguration</span></span>

-   <span data-ttu-id="edbdd-394">**Nombre canónico**: Microsoft. MPIOConfiguration</span><span class="sxs-lookup"><span data-stu-id="edbdd-394">**Canonical name**: Microsoft.MPIOConfiguration</span></span>
-   <span data-ttu-id="edbdd-395">**GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}</span><span class="sxs-lookup"><span data-stu-id="edbdd-395">**GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}</span></span>
-   <span data-ttu-id="edbdd-396">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-396">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-397">**Nombre del módulo**: @% SystemRoot% \\ system32 \\mpiocpl.dll,-1000</span><span class="sxs-lookup"><span data-stu-id="edbdd-397">**Module name**: @%SystemRoot%\\System32\\mpiocpl.dll,-1000</span></span>
-   <span data-ttu-id="edbdd-398">Este elemento del panel de control solo se verá en las versiones de servidor de Windows.</span><span class="sxs-lookup"><span data-stu-id="edbdd-398">This Control Panel item will be seen only in server versions of Windows.</span></span>

### <a name="network-and-sharing-center"></a><span data-ttu-id="edbdd-399">Centro de redes y recursos compartidos</span><span class="sxs-lookup"><span data-stu-id="edbdd-399">Network and Sharing Center</span></span>

-   <span data-ttu-id="edbdd-400">**Nombre canónico**: Microsoft. NetworkAndSharingCenter</span><span class="sxs-lookup"><span data-stu-id="edbdd-400">**Canonical name**: Microsoft.NetworkAndSharingCenter</span></span>
-   <span data-ttu-id="edbdd-401">**GUID**: {8E908FC9-BECC-40f6-915B-F4CA0E70D03D}</span><span class="sxs-lookup"><span data-stu-id="edbdd-401">**GUID**: {8E908FC9-BECC-40f6-915B-F4CA0E70D03D}</span></span>
-   <span data-ttu-id="edbdd-402">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-402">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-403">**Nombre del módulo**: @% SystemRoot% \\ system32 \\netcenter.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-403">**Module name**: @%SystemRoot%\\System32\\netcenter.dll,-1</span></span>
-   <span data-ttu-id="edbdd-404">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-404">**Pages**</span></span>

    | <span data-ttu-id="edbdd-405">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-405">Page Name</span></span>  | <span data-ttu-id="edbdd-406">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-406">Opens</span></span>                     |
    |------------|---------------------------|
    | <span data-ttu-id="edbdd-407">Avanzado</span><span class="sxs-lookup"><span data-stu-id="edbdd-407">Advanced</span></span>   | <span data-ttu-id="edbdd-408">Configuración de uso compartido avanzado</span><span class="sxs-lookup"><span data-stu-id="edbdd-408">Advanced sharing settings</span></span> |
    | <span data-ttu-id="edbdd-409">ShareMedia</span><span class="sxs-lookup"><span data-stu-id="edbdd-409">ShareMedia</span></span> | <span data-ttu-id="edbdd-410">Opciones de transmisión por secuencias de multimedia</span><span class="sxs-lookup"><span data-stu-id="edbdd-410">Media streaming options</span></span>   |

    

     

### <a name="notification-area-icons"></a><span data-ttu-id="edbdd-411">Iconos del área de notificación</span><span class="sxs-lookup"><span data-stu-id="edbdd-411">Notification Area Icons</span></span>

-   <span data-ttu-id="edbdd-412">**Nombre canónico**: Microsoft. NotificationAreaIcons</span><span class="sxs-lookup"><span data-stu-id="edbdd-412">**Canonical name**: Microsoft.NotificationAreaIcons</span></span>
-   <span data-ttu-id="edbdd-413">**GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}</span><span class="sxs-lookup"><span data-stu-id="edbdd-413">**GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}</span></span>
-   <span data-ttu-id="edbdd-414">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-414">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-415">**Nombre del módulo**: @% SystemRoot% \\ system32 \\taskbarcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-415">**Module name**: @%SystemRoot%\\System32\\taskbarcpl.dll,-1</span></span>

### <a name="pen-and-touch"></a><span data-ttu-id="edbdd-416">Lápiz y entrada táctil</span><span class="sxs-lookup"><span data-stu-id="edbdd-416">Pen and Touch</span></span>

-   <span data-ttu-id="edbdd-417">**Nombre canónico**: Microsoft. PenAndTouch</span><span class="sxs-lookup"><span data-stu-id="edbdd-417">**Canonical name**: Microsoft.PenAndTouch</span></span>
-   <span data-ttu-id="edbdd-418">**GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span><span class="sxs-lookup"><span data-stu-id="edbdd-418">**GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span></span>
-   <span data-ttu-id="edbdd-419">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-419">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-420">**Nombre del módulo**: @% SystemRoot% \\ system32 \\tabletpc.cpl,-10103</span><span class="sxs-lookup"><span data-stu-id="edbdd-420">**Module name**: @%SystemRoot%\\System32\\tabletpc.cpl,-10103</span></span>
-   <span data-ttu-id="edbdd-421">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-421">**Pages**</span></span>

    | <span data-ttu-id="edbdd-422">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-422">Page Name</span></span> | <span data-ttu-id="edbdd-423">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-423">Opens</span></span>       |
    |-----------|-------------|
    | <span data-ttu-id="edbdd-424">1</span><span class="sxs-lookup"><span data-stu-id="edbdd-424">1</span></span>         | <span data-ttu-id="edbdd-425">Gestos</span><span class="sxs-lookup"><span data-stu-id="edbdd-425">Flicks</span></span>      |
    | <span data-ttu-id="edbdd-426">2</span><span class="sxs-lookup"><span data-stu-id="edbdd-426">2</span></span>         | <span data-ttu-id="edbdd-427">Escritura a mano</span><span class="sxs-lookup"><span data-stu-id="edbdd-427">Handwriting</span></span> |

    

     

### <a name="personalization"></a><span data-ttu-id="edbdd-428">Personalización</span><span class="sxs-lookup"><span data-stu-id="edbdd-428">Personalization</span></span>

-   <span data-ttu-id="edbdd-429">**Nombre canónico**: Microsoft. Personalization</span><span class="sxs-lookup"><span data-stu-id="edbdd-429">**Canonical name**: Microsoft.Personalization</span></span>
-   <span data-ttu-id="edbdd-430">**GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}</span><span class="sxs-lookup"><span data-stu-id="edbdd-430">**GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}</span></span>
-   <span data-ttu-id="edbdd-431">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-431">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-432">**Nombre del módulo**: @% SystemRoot% \\ system32 \\themecpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-432">**Module name**: @%SystemRoot%\\System32\\themecpl.dll,-1</span></span>
-   <span data-ttu-id="edbdd-433">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-433">**Pages**</span></span>

    | <span data-ttu-id="edbdd-434">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-434">Page Name</span></span>        | <span data-ttu-id="edbdd-435">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-435">Opens</span></span>                |
    |------------------|----------------------|
    | <span data-ttu-id="edbdd-436">pageColorization</span><span class="sxs-lookup"><span data-stu-id="edbdd-436">pageColorization</span></span> | <span data-ttu-id="edbdd-437">Color y apariencia</span><span class="sxs-lookup"><span data-stu-id="edbdd-437">Color and Appearance</span></span> |
    | <span data-ttu-id="edbdd-438">pageWallpaper</span><span class="sxs-lookup"><span data-stu-id="edbdd-438">pageWallpaper</span></span>    | <span data-ttu-id="edbdd-439">Fondo de escritorio</span><span class="sxs-lookup"><span data-stu-id="edbdd-439">Desktop Background</span></span>   |

    

     

### <a name="phone-and-modem"></a><span data-ttu-id="edbdd-440">Teléfono y módem</span><span class="sxs-lookup"><span data-stu-id="edbdd-440">Phone and Modem</span></span>

-   <span data-ttu-id="edbdd-441">**Nombre canónico**: Microsoft. PhoneAndModem</span><span class="sxs-lookup"><span data-stu-id="edbdd-441">**Canonical name**: Microsoft.PhoneAndModem</span></span>
-   <span data-ttu-id="edbdd-442">**GUID**: {40419485-C444-4567-851A-2DD7BFA1684D}</span><span class="sxs-lookup"><span data-stu-id="edbdd-442">**GUID**: {40419485-C444-4567-851A-2DD7BFA1684D}</span></span>
-   <span data-ttu-id="edbdd-443">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-443">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-444">**Nombre del módulo**: @% SystemRoot% \\ system32 \\telephon.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-444">**Module name**: @%SystemRoot%\\System32\\telephon.cpl,-1</span></span>
-   <span data-ttu-id="edbdd-445">La ventana que este valor inicia se titula "información de ubicación" en versiones de Windows anteriores a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="edbdd-445">The window that this value launches is titled "Location Information" in versions of Windows prior to Windows 8.</span></span> <span data-ttu-id="edbdd-446">La interfaz de usuario del elemento se cambia considerablemente a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="edbdd-446">The item's UI is considerably changed as of Windows 8.</span></span>

### <a name="power-options"></a><span data-ttu-id="edbdd-447">Opciones de energía</span><span class="sxs-lookup"><span data-stu-id="edbdd-447">Power Options</span></span>

-   <span data-ttu-id="edbdd-448">**Nombre canónico**: Microsoft. PowerOptions</span><span class="sxs-lookup"><span data-stu-id="edbdd-448">**Canonical name**: Microsoft.PowerOptions</span></span>
-   <span data-ttu-id="edbdd-449">**GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}</span><span class="sxs-lookup"><span data-stu-id="edbdd-449">**GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}</span></span>
-   <span data-ttu-id="edbdd-450">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-450">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-451">**Nombre del módulo**: @% SystemRoot% \\ system32 \\powercpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-451">**Module name**: @%SystemRoot%\\System32\\powercpl.dll,-1</span></span>
-   <span data-ttu-id="edbdd-452">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-452">**Pages**</span></span>

    | <span data-ttu-id="edbdd-453">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-453">Page Name</span></span>          | <span data-ttu-id="edbdd-454">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-454">Opens</span></span>              |
    |--------------------|--------------------|
    | <span data-ttu-id="edbdd-455">pageGlobalSettings</span><span class="sxs-lookup"><span data-stu-id="edbdd-455">pageGlobalSettings</span></span> | <span data-ttu-id="edbdd-456">Configuración del sistema</span><span class="sxs-lookup"><span data-stu-id="edbdd-456">System Settings</span></span>    |
    | <span data-ttu-id="edbdd-457">pagePlanSettings</span><span class="sxs-lookup"><span data-stu-id="edbdd-457">pagePlanSettings</span></span>   | <span data-ttu-id="edbdd-458">Editar la configuración del plan</span><span class="sxs-lookup"><span data-stu-id="edbdd-458">Edit Plan Settings</span></span> |

    

     

### <a name="programs-and-features"></a><span data-ttu-id="edbdd-459">Programas y características</span><span class="sxs-lookup"><span data-stu-id="edbdd-459">Programs and Features</span></span>

-   <span data-ttu-id="edbdd-460">**Nombre canónico**: Microsoft. ProgramsAndFeatures</span><span class="sxs-lookup"><span data-stu-id="edbdd-460">**Canonical name**: Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="edbdd-461">**GUID**: {7b81be6a-ce2b-4676-a29e-eb907a5126c5}</span><span class="sxs-lookup"><span data-stu-id="edbdd-461">**GUID**: {7b81be6a-ce2b-4676-a29e-eb907a5126c5}</span></span>
-   <span data-ttu-id="edbdd-462">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-462">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-463">**Nombre del módulo**: @% SystemRoot% \\ system32 \\appwiz.cpl,-159</span><span class="sxs-lookup"><span data-stu-id="edbdd-463">**Module name**: @%systemroot%\\system32\\appwiz.cpl,-159</span></span>
-   <span data-ttu-id="edbdd-464">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-464">**Pages**</span></span>

    | <span data-ttu-id="edbdd-465">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-465">Page Name</span></span>                                | <span data-ttu-id="edbdd-466">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-466">Opens</span></span>             |
    |------------------------------------------|-------------------|
    | <span data-ttu-id="edbdd-467">::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD}</span><span class="sxs-lookup"><span data-stu-id="edbdd-467">::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD}</span></span> | <span data-ttu-id="edbdd-468">Actualizaciones instaladas</span><span class="sxs-lookup"><span data-stu-id="edbdd-468">Installed Updates</span></span> |

    

     

### <a name="recovery"></a><span data-ttu-id="edbdd-469">Recuperación</span><span class="sxs-lookup"><span data-stu-id="edbdd-469">Recovery</span></span>

-   <span data-ttu-id="edbdd-470">**Nombre canónico**: Microsoft. Recovery</span><span class="sxs-lookup"><span data-stu-id="edbdd-470">**Canonical name**: Microsoft.Recovery</span></span>
-   <span data-ttu-id="edbdd-471">**GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}</span><span class="sxs-lookup"><span data-stu-id="edbdd-471">**GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}</span></span>
-   <span data-ttu-id="edbdd-472">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-472">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-473">**Nombre del módulo**: @% SystemRoot% \\ system32 \\recovery.dll,-101</span><span class="sxs-lookup"><span data-stu-id="edbdd-473">**Module name**: @%SystemRoot%\\System32\\recovery.dll,-101</span></span>

### <a name="region"></a><span data-ttu-id="edbdd-474">Region</span><span class="sxs-lookup"><span data-stu-id="edbdd-474">Region</span></span>

-   <span data-ttu-id="edbdd-475">**Nombre canónico**: Microsoft. RegionAndLanguage</span><span class="sxs-lookup"><span data-stu-id="edbdd-475">**Canonical name**: Microsoft.RegionAndLanguage</span></span>
-   <span data-ttu-id="edbdd-476">**GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span><span class="sxs-lookup"><span data-stu-id="edbdd-476">**GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span></span>
-   <span data-ttu-id="edbdd-477">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-477">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-478">**Nombre del módulo**: @% SystemRoot% \\ system32 \\intl.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-478">**Module name**: @%SystemRoot%\\System32\\intl.cpl,-1</span></span>
-   <span data-ttu-id="edbdd-479">El elemento de idioma y región que se encuentra en Windows 7 se dividió a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="edbdd-479">The Region and Language item found in Windows 7 was split as of Windows 8.</span></span> <span data-ttu-id="edbdd-480">Microsoft. RegionAndLanguage ahora inicia el elemento region.</span><span class="sxs-lookup"><span data-stu-id="edbdd-480">Microsoft.RegionAndLanguage now launches the Region item.</span></span> <span data-ttu-id="edbdd-481">Para iniciar el elemento de idioma, use [Microsoft. Language](#location-settings).</span><span class="sxs-lookup"><span data-stu-id="edbdd-481">To launch the Language item, use [Microsoft.Language](#location-settings).</span></span>
-   <span data-ttu-id="edbdd-482">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-482">**Pages**</span></span>

    | <span data-ttu-id="edbdd-483">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-483">Page Name</span></span> | <span data-ttu-id="edbdd-484">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-484">Opens</span></span>          |
    |-----------|----------------|
    | <span data-ttu-id="edbdd-485">1</span><span class="sxs-lookup"><span data-stu-id="edbdd-485">1</span></span>         | <span data-ttu-id="edbdd-486">Ubicación</span><span class="sxs-lookup"><span data-stu-id="edbdd-486">Location</span></span>       |
    | <span data-ttu-id="edbdd-487">2</span><span class="sxs-lookup"><span data-stu-id="edbdd-487">2</span></span>         | <span data-ttu-id="edbdd-488">Administrativo</span><span class="sxs-lookup"><span data-stu-id="edbdd-488">Administrative</span></span> |

    

     

### <a name="remoteapp-and-desktop-connections"></a><span data-ttu-id="edbdd-489">Conexión de RemoteApp y Escritorio</span><span class="sxs-lookup"><span data-stu-id="edbdd-489">RemoteApp and Desktop Connections</span></span>

-   <span data-ttu-id="edbdd-490">**Nombre canónico**: Microsoft. RemoteAppAndDesktopConnections</span><span class="sxs-lookup"><span data-stu-id="edbdd-490">**Canonical name**: Microsoft.RemoteAppAndDesktopConnections</span></span>
-   <span data-ttu-id="edbdd-491">**GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}</span><span class="sxs-lookup"><span data-stu-id="edbdd-491">**GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}</span></span>
-   <span data-ttu-id="edbdd-492">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-492">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-493">**Nombre del módulo**: @% SystemRoot% \\ system32 \\tsworkspace.dll,-15300</span><span class="sxs-lookup"><span data-stu-id="edbdd-493">**Module name**: @%SystemRoot%\\System32\\tsworkspace.dll,-15300</span></span>

### <a name="sound"></a><span data-ttu-id="edbdd-494">Sonido</span><span class="sxs-lookup"><span data-stu-id="edbdd-494">Sound</span></span>

-   <span data-ttu-id="edbdd-495">**Nombre canónico**: Microsoft. Sound</span><span class="sxs-lookup"><span data-stu-id="edbdd-495">**Canonical name**: Microsoft.Sound</span></span>
-   <span data-ttu-id="edbdd-496">**GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span><span class="sxs-lookup"><span data-stu-id="edbdd-496">**GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span></span>
-   <span data-ttu-id="edbdd-497">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-497">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-498">**Nombre del módulo**: @% SystemRoot% \\ system32 \\mmsys.cpl,-300</span><span class="sxs-lookup"><span data-stu-id="edbdd-498">**Module name**: @%SystemRoot%\\System32\\mmsys.cpl,-300</span></span>

### <a name="speech-recognition"></a><span data-ttu-id="edbdd-499">Reconocimiento de voz</span><span class="sxs-lookup"><span data-stu-id="edbdd-499">Speech Recognition</span></span>

-   <span data-ttu-id="edbdd-500">**Nombre canónico**: Microsoft. SpeechRecognition</span><span class="sxs-lookup"><span data-stu-id="edbdd-500">**Canonical name**: Microsoft.SpeechRecognition</span></span>
-   <span data-ttu-id="edbdd-501">**GUID**: {58E3C745-D971-4081-9034-86E34B30836A}</span><span class="sxs-lookup"><span data-stu-id="edbdd-501">**GUID**: {58E3C745-D971-4081-9034-86E34B30836A}</span></span>
-   <span data-ttu-id="edbdd-502">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-502">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-503">**Nombre del módulo**: @% SystemRoot% \\ System32 \\ Speech \\ SpeechUX \\speechuxcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-503">**Module name**: @%SystemRoot%\\System32\\Speech\\SpeechUX\\speechuxcpl.dll,-1</span></span>

### <a name="storage-spaces"></a><span data-ttu-id="edbdd-504">Espacios de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="edbdd-504">Storage Spaces</span></span>

-   <span data-ttu-id="edbdd-505">**Nombre canónico**: Microsoft. StorageSpaces</span><span class="sxs-lookup"><span data-stu-id="edbdd-505">**Canonical name**: Microsoft.StorageSpaces</span></span>
-   <span data-ttu-id="edbdd-506">**GUID**: {F942C606-0914-47AB-BE56-1321B8035096}</span><span class="sxs-lookup"><span data-stu-id="edbdd-506">**GUID**: {F942C606-0914-47AB-BE56-1321B8035096}</span></span>
-   <span data-ttu-id="edbdd-507">**Sistema operativo compatible**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-507">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-508">**Nombre del módulo**: @C: \\ Windows \\ system32 \\SpaceControl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-508">**Module name**: @C:\\Windows\\System32\\SpaceControl.dll,-1</span></span>

### <a name="sync-center"></a><span data-ttu-id="edbdd-509">Centro de sincronización</span><span class="sxs-lookup"><span data-stu-id="edbdd-509">Sync Center</span></span>

-   <span data-ttu-id="edbdd-510">**Nombre canónico**: Microsoft. SyncCenter</span><span class="sxs-lookup"><span data-stu-id="edbdd-510">**Canonical name**: Microsoft.SyncCenter</span></span>
-   <span data-ttu-id="edbdd-511">**GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}</span><span class="sxs-lookup"><span data-stu-id="edbdd-511">**GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}</span></span>
-   <span data-ttu-id="edbdd-512">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-512">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-513">**Nombre del módulo**: @% SystemRoot% \\ system32 \\SyncCenter.dll,-3000</span><span class="sxs-lookup"><span data-stu-id="edbdd-513">**Module name**: @%SystemRoot%\\System32\\SyncCenter.dll,-3000</span></span>

### <a name="system"></a><span data-ttu-id="edbdd-514">Sistema</span><span class="sxs-lookup"><span data-stu-id="edbdd-514">System</span></span>

-   <span data-ttu-id="edbdd-515">**Nombre canónico**: Microsoft.SysTEM</span><span class="sxs-lookup"><span data-stu-id="edbdd-515">**Canonical name**: Microsoft.System</span></span>
-   <span data-ttu-id="edbdd-516">**GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}</span><span class="sxs-lookup"><span data-stu-id="edbdd-516">**GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}</span></span>
-   <span data-ttu-id="edbdd-517">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-517">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-518">**Nombre del módulo**: @% SystemRoot% \\ system32 \\systemcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-518">**Module name**: @%SystemRoot%\\System32\\systemcpl.dll,-1</span></span>

### <a name="tablet-pc-settings"></a><span data-ttu-id="edbdd-519">Configuración de Tablet PC</span><span class="sxs-lookup"><span data-stu-id="edbdd-519">Tablet PC Settings</span></span>

-   <span data-ttu-id="edbdd-520">**Nombre canónico**: Microsoft. TabletPCSettings</span><span class="sxs-lookup"><span data-stu-id="edbdd-520">**Canonical name**: Microsoft.TabletPCSettings</span></span>
-   <span data-ttu-id="edbdd-521">**GUID**: {80F3F1D5-Feca-45F3-BC32-752C152E456E}</span><span class="sxs-lookup"><span data-stu-id="edbdd-521">**GUID**: {80F3F1D5-FECA-45F3-BC32-752C152E456E}</span></span>
-   <span data-ttu-id="edbdd-522">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-522">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-523">**Nombre del módulo**: @% SystemRoot% \\ system32 \\tabletpc.cpl,-10100</span><span class="sxs-lookup"><span data-stu-id="edbdd-523">**Module name**: @%SystemRoot%\\System32\\tabletpc.cpl,-10100</span></span>

### <a name="taskbar-and-navigation"></a><span data-ttu-id="edbdd-524">Barra de tareas y navegación</span><span class="sxs-lookup"><span data-stu-id="edbdd-524">Taskbar and Navigation</span></span>

-   <span data-ttu-id="edbdd-525">**Nombre canónico**: Microsoft. Taskbar</span><span class="sxs-lookup"><span data-stu-id="edbdd-525">**Canonical name**: Microsoft.Taskbar</span></span>
-   <span data-ttu-id="edbdd-526">**GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}</span><span class="sxs-lookup"><span data-stu-id="edbdd-526">**GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}</span></span>
-   <span data-ttu-id="edbdd-527">**Sistema operativo compatible**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-527">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-528">**Nombre del módulo**: @% SystemRoot% \\ system32 \\shell32.dll,-32517</span><span class="sxs-lookup"><span data-stu-id="edbdd-528">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-32517</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="edbdd-529">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="edbdd-529">Troubleshooting</span></span>

-   <span data-ttu-id="edbdd-530">**Nombre canónico**: Microsoft. Troubleshooting</span><span class="sxs-lookup"><span data-stu-id="edbdd-530">**Canonical name**: Microsoft.Troubleshooting</span></span>
-   <span data-ttu-id="edbdd-531">**GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}</span><span class="sxs-lookup"><span data-stu-id="edbdd-531">**GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}</span></span>
-   <span data-ttu-id="edbdd-532">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-532">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-533">**Nombre del módulo**: @% SystemRoot% \\ system32 \\DiagCpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-533">**Module name**: @%SystemRoot%\\System32\\DiagCpl.dll,-1</span></span>
-   <span data-ttu-id="edbdd-534">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-534">**Pages**</span></span>

    | <span data-ttu-id="edbdd-535">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-535">Page Name</span></span>   | <span data-ttu-id="edbdd-536">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-536">Opens</span></span>   |
    |-------------|---------|
    | <span data-ttu-id="edbdd-537">HistoryPage</span><span class="sxs-lookup"><span data-stu-id="edbdd-537">HistoryPage</span></span> | <span data-ttu-id="edbdd-538">Historial</span><span class="sxs-lookup"><span data-stu-id="edbdd-538">History</span></span> |

    

     

### <a name="tsappinstall"></a><span data-ttu-id="edbdd-539">TSAppInstall</span><span class="sxs-lookup"><span data-stu-id="edbdd-539">TSAppInstall</span></span>

-   <span data-ttu-id="edbdd-540">**Nombre canónico**: Microsoft. TSAppInstall</span><span class="sxs-lookup"><span data-stu-id="edbdd-540">**Canonical name**: Microsoft.TSAppInstall</span></span>
-   <span data-ttu-id="edbdd-541">**GUID**: {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}</span><span class="sxs-lookup"><span data-stu-id="edbdd-541">**GUID**: {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}</span></span>
-   <span data-ttu-id="edbdd-542">**Sistema operativo compatible**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-542">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-543">**Nombre del módulo**: @% SystemRoot% \\ system32 \\tsappinstall.exe,-2001</span><span class="sxs-lookup"><span data-stu-id="edbdd-543">**Module name**: @%systemroot%\\system32\\tsappinstall.exe,-2001</span></span>

### <a name="user-accounts"></a><span data-ttu-id="edbdd-544">Cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="edbdd-544">User Accounts</span></span>

-   <span data-ttu-id="edbdd-545">**Nombre canónico**: Microsoft. el</span><span class="sxs-lookup"><span data-stu-id="edbdd-545">**Canonical name**: Microsoft.UserAccounts</span></span>
-   <span data-ttu-id="edbdd-546">**GUID**: {60632754-c523-4b62-b45c-4172da012619}</span><span class="sxs-lookup"><span data-stu-id="edbdd-546">**GUID**: {60632754-c523-4b62-b45c-4172da012619}</span></span>
-   <span data-ttu-id="edbdd-547">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-547">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-548">**Nombre del módulo**: @% SystemRoot% \\ system32 \\usercpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-548">**Module name**: @%SystemRoot%\\System32\\usercpl.dll,-1</span></span>

### <a name="windows-anytime-upgrade"></a><span data-ttu-id="edbdd-549">Windows Anytime Upgrade</span><span class="sxs-lookup"><span data-stu-id="edbdd-549">Windows Anytime Upgrade</span></span>

-   <span data-ttu-id="edbdd-550">**Nombre canónico**: Microsoft. WindowsAnytimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="edbdd-550">**Canonical name**: Microsoft.WindowsAnytimeUpgrade</span></span>
-   <span data-ttu-id="edbdd-551">**GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}</span><span class="sxs-lookup"><span data-stu-id="edbdd-551">**GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}</span></span>
-   <span data-ttu-id="edbdd-552">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-552">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-553">**Nombre del módulo**: @ $ (resourceString. \_ SYS \_ mod \_ path),-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-553">**Module name**: @$(resourceString.\_SYS\_MOD\_PATH),-1</span></span>

### <a name="windows-defender"></a><span data-ttu-id="edbdd-554">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="edbdd-554">Windows Defender</span></span>

-   <span data-ttu-id="edbdd-555">**Nombre canónico**: Microsoft. WindowsDefender</span><span class="sxs-lookup"><span data-stu-id="edbdd-555">**Canonical name**: Microsoft.WindowsDefender</span></span>
-   <span data-ttu-id="edbdd-556">**GUID**: {D8559EB9-20C0-410E-Beda-7ED416AECC2A}</span><span class="sxs-lookup"><span data-stu-id="edbdd-556">**GUID**: {D8559EB9-20C0-410E-BEDA-7ED416AECC2A}</span></span>
-   <span data-ttu-id="edbdd-557">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-557">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-558">**Nombre del módulo**: @% programfiles% \\ Windows Defender \\MsMpRes.dll,-104</span><span class="sxs-lookup"><span data-stu-id="edbdd-558">**Module name**: @%ProgramFiles%\\Windows Defender\\MsMpRes.dll,-104</span></span>

### <a name="windows-firewall"></a><span data-ttu-id="edbdd-559">Firewall de Windows</span><span class="sxs-lookup"><span data-stu-id="edbdd-559">Windows Firewall</span></span>

-   <span data-ttu-id="edbdd-560">**Nombre canónico**: Microsoft. firewall</span><span class="sxs-lookup"><span data-stu-id="edbdd-560">**Canonical name**: Microsoft.WindowsFirewall</span></span>
-   <span data-ttu-id="edbdd-561">**GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}</span><span class="sxs-lookup"><span data-stu-id="edbdd-561">**GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}</span></span>
-   <span data-ttu-id="edbdd-562">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-562">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-563">**Nombre del módulo**: @C: \\ Windows \\ system32 \\FirewallControlPanel.dll,-12122</span><span class="sxs-lookup"><span data-stu-id="edbdd-563">**Module name**: @C:\\Windows\\system32\\FirewallControlPanel.dll,-12122</span></span>
-   <span data-ttu-id="edbdd-564">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-564">**Pages**</span></span>

    | <span data-ttu-id="edbdd-565">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-565">Page Name</span></span>         | <span data-ttu-id="edbdd-566">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-566">Opens</span></span>        |
    |-------------------|--------------|
    | <span data-ttu-id="edbdd-567">pageConfigureApps</span><span class="sxs-lookup"><span data-stu-id="edbdd-567">pageConfigureApps</span></span> | <span data-ttu-id="edbdd-568">Aplicaciones permitidas</span><span class="sxs-lookup"><span data-stu-id="edbdd-568">Allowed apps</span></span> |

    

     

### <a name="windows-mobility-center"></a><span data-ttu-id="edbdd-569">Centro de movilidad de Windows</span><span class="sxs-lookup"><span data-stu-id="edbdd-569">Windows Mobility Center</span></span>

-   <span data-ttu-id="edbdd-570">**Nombre canónico**: Microsoft. MobilityCenter</span><span class="sxs-lookup"><span data-stu-id="edbdd-570">**Canonical name**: Microsoft.MobilityCenter</span></span>
-   <span data-ttu-id="edbdd-571">**GUID**: {5ea4f148-308C-46d7-98a9-49041b1dd468}</span><span class="sxs-lookup"><span data-stu-id="edbdd-571">**GUID**: {5ea4f148-308c-46d7-98a9-49041b1dd468}</span></span>
-   <span data-ttu-id="edbdd-572">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-572">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-573">**Nombre del módulo**: @% SystemRoot% \\ system32 \\mblctr.exe,-1002</span><span class="sxs-lookup"><span data-stu-id="edbdd-573">**Module name**: @%SystemRoot%\\system32\\mblctr.exe,-1002</span></span>

### <a name="windows-to-go"></a><span data-ttu-id="edbdd-574">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="edbdd-574">Windows To Go</span></span>

-   <span data-ttu-id="edbdd-575">**Nombre canónico**: Microsoft. PortableWorkspaceCreator</span><span class="sxs-lookup"><span data-stu-id="edbdd-575">**Canonical name**: Microsoft.PortableWorkspaceCreator</span></span>
-   <span data-ttu-id="edbdd-576">**GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}</span><span class="sxs-lookup"><span data-stu-id="edbdd-576">**GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}</span></span>
-   <span data-ttu-id="edbdd-577">**Sistema operativo compatible**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-577">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-578">**Nombre del módulo**: @% SystemRoot% \\ system32 \\pwcreator.exe,-151</span><span class="sxs-lookup"><span data-stu-id="edbdd-578">**Module name**: @%SystemRoot%\\System32\\pwcreator.exe,-151</span></span>

### <a name="windows-update"></a><span data-ttu-id="edbdd-579">Windows Update</span><span class="sxs-lookup"><span data-stu-id="edbdd-579">Windows Update</span></span>

-   <span data-ttu-id="edbdd-580">**Nombre canónico**: Microsoft. windowsupdate</span><span class="sxs-lookup"><span data-stu-id="edbdd-580">**Canonical name**: Microsoft.WindowsUpdate</span></span>
-   <span data-ttu-id="edbdd-581">**GUID**: {36eef7db-88ad-4e81-ad49-0e313f0c35f8}</span><span class="sxs-lookup"><span data-stu-id="edbdd-581">**GUID**: {36eef7db-88ad-4e81-ad49-0e313f0c35f8}</span></span>
-   <span data-ttu-id="edbdd-582">**Sistema operativo compatible**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-582">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-583">**Nombre del módulo**: @% SystemRoot% \\ system32 \\wucltux.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-583">**Module name**: @%SystemRoot%\\system32\\wucltux.dll,-1</span></span>
-   <span data-ttu-id="edbdd-584">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="edbdd-584">**Pages**</span></span>

    | <span data-ttu-id="edbdd-585">Nombre de página</span><span class="sxs-lookup"><span data-stu-id="edbdd-585">Page Name</span></span>         | <span data-ttu-id="edbdd-586">Aperturas</span><span class="sxs-lookup"><span data-stu-id="edbdd-586">Opens</span></span>               |
    |-------------------|---------------------|
    | <span data-ttu-id="edbdd-587">pageSettings</span><span class="sxs-lookup"><span data-stu-id="edbdd-587">pageSettings</span></span>      | <span data-ttu-id="edbdd-588">Cambio de configuración</span><span class="sxs-lookup"><span data-stu-id="edbdd-588">Change settings</span></span>     |
    | <span data-ttu-id="edbdd-589">pageUpdateHistory</span><span class="sxs-lookup"><span data-stu-id="edbdd-589">pageUpdateHistory</span></span> | <span data-ttu-id="edbdd-590">Ver el historial de actualizaciones</span><span class="sxs-lookup"><span data-stu-id="edbdd-590">View update history</span></span> |

    

     

### <a name="work-folders"></a><span data-ttu-id="edbdd-591">Carpetas de trabajo</span><span class="sxs-lookup"><span data-stu-id="edbdd-591">Work Folders</span></span>

-   <span data-ttu-id="edbdd-592">**Nombre canónico**: Microsoft. WorkFolders</span><span class="sxs-lookup"><span data-stu-id="edbdd-592">**Canonical name**: Microsoft.WorkFolders</span></span>
-   <span data-ttu-id="edbdd-593">**GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}</span><span class="sxs-lookup"><span data-stu-id="edbdd-593">**GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}</span></span>
-   <span data-ttu-id="edbdd-594">**So admitido**: Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="edbdd-594">**Supported OS**: Windows 8.1</span></span>
-   <span data-ttu-id="edbdd-595">**Nombre del módulo**: @C: \\ Windows \\ system32 \\WorkfoldersControl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="edbdd-595">**Module name**: @C:\\Windows\\System32\\WorkfoldersControl.dll,-1</span></span>

## <a name="deprecated-control-panel-canonical-names"></a><span data-ttu-id="edbdd-596">Nombres canónicos del panel de control desusados</span><span class="sxs-lookup"><span data-stu-id="edbdd-596">Deprecated Control Panel Canonical Names</span></span>

<span data-ttu-id="edbdd-597">A continuación se muestran nombres canónicos que ya no se usan a partir de Windows 8.1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="edbdd-597">The following are canonical names that are no longer in use as of Windows 8.1 or later.</span></span> <span data-ttu-id="edbdd-598">Algunos se han quitado por completo.</span><span class="sxs-lookup"><span data-stu-id="edbdd-598">Some have been removed altogether.</span></span> <span data-ttu-id="edbdd-599">Otros se han reasignado en estas situaciones:</span><span class="sxs-lookup"><span data-stu-id="edbdd-599">Others have been remapped in these situations:</span></span>

-   <span data-ttu-id="edbdd-600">Se cambia el nombre de un elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="edbdd-600">A Control Panel item is renamed.</span></span> <span data-ttu-id="edbdd-601">Al elemento al que se ha cambiado el nombre se le asigna un nuevo nombre canónico pero mantiene el mismo GUID.</span><span class="sxs-lookup"><span data-stu-id="edbdd-601">The renamed item is given a new canonical name but keeps the same GUID.</span></span> <span data-ttu-id="edbdd-602">En este caso, el antiguo nombre canónico inicia el elemento del panel de control cuyo nombre ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="edbdd-602">In this case, the old canonical name launches the renamed Control Panel item.</span></span> <span data-ttu-id="edbdd-603">Tenga en cuenta que el elemento que se inicia podría no usar la misma interfaz de usuario que la versión anterior de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="edbdd-603">Be aware that the item that's launched might not use the same UI as that item's older version.</span></span>
-   <span data-ttu-id="edbdd-604">La funcionalidad de uno o más elementos del panel de control se mueve o consolida en un nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="edbdd-604">The functionality of one or more Control Panel items is moved or consolidated into a new item.</span></span> <span data-ttu-id="edbdd-605">En este caso, el antiguo nombre canónico se asigna al nuevo elemento del panel de control más adecuado.</span><span class="sxs-lookup"><span data-stu-id="edbdd-605">In this case, the old canonical name maps to the most appropriate new Control Panel item.</span></span>

> [!Note]  
> <span data-ttu-id="edbdd-606">Existen reasignaciones para la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="edbdd-606">Remappings exist for backward compatibility.</span></span> <span data-ttu-id="edbdd-607">No debe utilizar valores en desuso en el código nuevo.</span><span class="sxs-lookup"><span data-stu-id="edbdd-607">You should not use deprecated values in new code.</span></span>

 



| <span data-ttu-id="edbdd-608">Nombre canónico desusado</span><span class="sxs-lookup"><span data-stu-id="edbdd-608">Deprecated canonical name</span></span>                                   | <span data-ttu-id="edbdd-609">Elemento del panel de control</span><span class="sxs-lookup"><span data-stu-id="edbdd-609">Control Panel Item</span></span>                | <span data-ttu-id="edbdd-610">GUID</span><span class="sxs-lookup"><span data-stu-id="edbdd-610">GUID</span></span>                                   | <span data-ttu-id="edbdd-611">Notas</span><span class="sxs-lookup"><span data-stu-id="edbdd-611">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edbdd-612">Microsoft. AddHardware</span><span class="sxs-lookup"><span data-stu-id="edbdd-612">Microsoft.AddHardware</span></span>                                       | <span data-ttu-id="edbdd-613">Agregar hardware</span><span class="sxs-lookup"><span data-stu-id="edbdd-613">Add Hardware</span></span>                      | <span data-ttu-id="edbdd-614">{7A979262-40CE-46ff-AEEE-7884AC3B6136}</span><span class="sxs-lookup"><span data-stu-id="edbdd-614">{7A979262-40CE-46ff-AEEE-7884AC3B6136}</span></span> | <span data-ttu-id="edbdd-615">Se asigna a [Microsoft. DevicesAndPrinters](#devices-and-printers) a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="edbdd-615">Maps to [Microsoft.DevicesAndPrinters](#devices-and-printers) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="edbdd-616">Microsoft. AudioDevicesAndSoundThemes</span><span class="sxs-lookup"><span data-stu-id="edbdd-616">Microsoft.AudioDevicesAndSoundThemes</span></span>                        | <span data-ttu-id="edbdd-617">Sonido</span><span class="sxs-lookup"><span data-stu-id="edbdd-617">Sound</span></span>                             | <span data-ttu-id="edbdd-618">{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span><span class="sxs-lookup"><span data-stu-id="edbdd-618">{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span></span> | <span data-ttu-id="edbdd-619">Se asigna a [Microsoft. Sound](#sound) a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="edbdd-619">Maps to [Microsoft.Sound](#sound) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="edbdd-620">Microsoft. BackupAndRestoreCenter/Microsoft. BackupAndRestore</span><span class="sxs-lookup"><span data-stu-id="edbdd-620">Microsoft.BackupAndRestoreCenter/Microsoft.BackupAndRestore</span></span> | <span data-ttu-id="edbdd-621">Centro de copias de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="edbdd-621">Backup and Restore Center</span></span>         | <span data-ttu-id="edbdd-622">{B98A2BEA-7D42-4558-8BD1-832F41BAC6FD}</span><span class="sxs-lookup"><span data-stu-id="edbdd-622">{B98A2BEA-7D42-4558-8BD1-832F41BAC6FD}</span></span> | <span data-ttu-id="edbdd-623">Microsoft. BackupAndRestoreCenter se asigna a Microsoft. BackupAndRestore en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="edbdd-623">Microsoft.BackupAndRestoreCenter maps to Microsoft.BackupAndRestore in Windows 7.</span></span> <span data-ttu-id="edbdd-624">Ambos se quitan a partir de Windows 8; Use [Microsoft. FileHistory](#file-history) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="edbdd-624">Both are removed as of Windows 8; use [Microsoft.FileHistory](#file-history) instead.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="edbdd-625">Microsoft. CardSpace</span><span class="sxs-lookup"><span data-stu-id="edbdd-625">Microsoft.CardSpace</span></span>                                         | <span data-ttu-id="edbdd-626">Windows CardSpace</span><span class="sxs-lookup"><span data-stu-id="edbdd-626">Windows CardSpace</span></span>                 | <span data-ttu-id="edbdd-627">{78CB147A-98EA-4AA6-B0DF-C8681F69341C}</span><span class="sxs-lookup"><span data-stu-id="edbdd-627">{78CB147A-98EA-4AA6-B0DF-C8681F69341C}</span></span> | <span data-ttu-id="edbdd-628">Se quita a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="edbdd-628">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="edbdd-629">Microsoft. DesktopGadgets</span><span class="sxs-lookup"><span data-stu-id="edbdd-629">Microsoft.DesktopGadgets</span></span>                                    | <span data-ttu-id="edbdd-630">Gadgets de escritorio</span><span class="sxs-lookup"><span data-stu-id="edbdd-630">Desktop Gadgets</span></span>                   | <span data-ttu-id="edbdd-631">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span><span class="sxs-lookup"><span data-stu-id="edbdd-631">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span></span> | <span data-ttu-id="edbdd-632">Se quita a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="edbdd-632">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="edbdd-633">Microsoft. GetProgramsOnline</span><span class="sxs-lookup"><span data-stu-id="edbdd-633">Microsoft.GetProgramsOnline</span></span>                                 | <span data-ttu-id="edbdd-634">Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="edbdd-634">Windows Marketplace</span></span>               | <span data-ttu-id="edbdd-635">{3e7efb4c-faf1-453d-89eb-56026875ef90}</span><span class="sxs-lookup"><span data-stu-id="edbdd-635">{3e7efb4c-faf1-453d-89eb-56026875ef90}</span></span> | <span data-ttu-id="edbdd-636">Se quita a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="edbdd-636">Removed as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="edbdd-637">Microsoft. InfraredOptions</span><span class="sxs-lookup"><span data-stu-id="edbdd-637">Microsoft.InfraredOptions</span></span>                                   | <span data-ttu-id="edbdd-638">Infrarrojos</span><span class="sxs-lookup"><span data-stu-id="edbdd-638">Infrared</span></span>                          | <span data-ttu-id="edbdd-639">{A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span><span class="sxs-lookup"><span data-stu-id="edbdd-639">{A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span></span> | <span data-ttu-id="edbdd-640">Se asigna a [Microsoft. Infrared](#infrared) a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="edbdd-640">Maps to [Microsoft.Infrared](#infrared) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="edbdd-641">Microsoft. Language</span><span class="sxs-lookup"><span data-stu-id="edbdd-641">Microsoft.Language</span></span>                                          | <span data-ttu-id="edbdd-642">Lenguaje</span><span class="sxs-lookup"><span data-stu-id="edbdd-642">Language</span></span>                          | <span data-ttu-id="edbdd-643">{BF782CC9-5A52-4A17-806C-2A894FFEEAC5}</span><span class="sxs-lookup"><span data-stu-id="edbdd-643">{BF782CC9-5A52-4A17-806C-2A894FFEEAC5}</span></span> | <span data-ttu-id="edbdd-644">Se quitó a partir de la versión 1803 de Windows 10</span><span class="sxs-lookup"><span data-stu-id="edbdd-644">Removed as of Windows 10, version 1803</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="edbdd-645">Microsoft. LocationAndOtherSensors</span><span class="sxs-lookup"><span data-stu-id="edbdd-645">Microsoft.LocationAndOtherSensors</span></span>                           | <span data-ttu-id="edbdd-646">Ubicación y otros sensores</span><span class="sxs-lookup"><span data-stu-id="edbdd-646">Location and Other Sensors</span></span>        | <span data-ttu-id="edbdd-647">{E9950154-C418-419e-A90A-20C5287AE24B}</span><span class="sxs-lookup"><span data-stu-id="edbdd-647">{E9950154-C418-419e-A90A-20C5287AE24B}</span></span> | <span data-ttu-id="edbdd-648">Se asigna a [Microsoft. LocationSettings](#infrared) a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="edbdd-648">Maps to [Microsoft.LocationSettings](#infrared) as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="edbdd-649">Microsoft. PenAndInputDevices</span><span class="sxs-lookup"><span data-stu-id="edbdd-649">Microsoft.PenAndInputDevices</span></span>                                | <span data-ttu-id="edbdd-650">Lápiz y dispositivos de entrada</span><span class="sxs-lookup"><span data-stu-id="edbdd-650">Pen and Input Devices</span></span>             | <span data-ttu-id="edbdd-651">{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span><span class="sxs-lookup"><span data-stu-id="edbdd-651">{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span></span> | <span data-ttu-id="edbdd-652">Se asigna a [Microsoft. PenAndTouch](#pen-and-touch) a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="edbdd-652">Maps to [Microsoft.PenAndTouch](#pen-and-touch) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="edbdd-653">Microsoft. PeopleNearMe</span><span class="sxs-lookup"><span data-stu-id="edbdd-653">Microsoft.PeopleNearMe</span></span>                                      | <span data-ttu-id="edbdd-654">People Near Me (Gente que esté cerca)</span><span class="sxs-lookup"><span data-stu-id="edbdd-654">People Near Me</span></span>                    | <span data-ttu-id="edbdd-655">{5224F545-A443-4859-BA23-7B5A95BDC8EF}</span><span class="sxs-lookup"><span data-stu-id="edbdd-655">{5224F545-A443-4859-BA23-7B5A95BDC8EF}</span></span> | <span data-ttu-id="edbdd-656">Se quita a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="edbdd-656">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="edbdd-657">Microsoft. PerformanceInformationAndTools</span><span class="sxs-lookup"><span data-stu-id="edbdd-657">Microsoft.PerformanceInformationAndTools</span></span>                    | <span data-ttu-id="edbdd-658">Información y herramientas de rendimiento</span><span class="sxs-lookup"><span data-stu-id="edbdd-658">Performance Information and Tools</span></span> | <span data-ttu-id="edbdd-659">{78F3955E-3B90-4184-BD14-5397C15F1EFC}</span><span class="sxs-lookup"><span data-stu-id="edbdd-659">{78F3955E-3B90-4184-BD14-5397C15F1EFC}</span></span> | <span data-ttu-id="edbdd-660">Se ha quitado de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="edbdd-660">Removed as of Windows 8.1.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="edbdd-661">Microsoft. PhoneAndModemOptions</span><span class="sxs-lookup"><span data-stu-id="edbdd-661">Microsoft.PhoneAndModemOptions</span></span>                              | <span data-ttu-id="edbdd-662">Teléfono y módem</span><span class="sxs-lookup"><span data-stu-id="edbdd-662">Phone and Modem</span></span>                   | <span data-ttu-id="edbdd-663">{40419485-C444-4567-851A-2DD7BFA1684D}</span><span class="sxs-lookup"><span data-stu-id="edbdd-663">{40419485-C444-4567-851A-2DD7BFA1684D}</span></span> | <span data-ttu-id="edbdd-664">Se asigna a [Microsoft. PhoneAndModem](#phone-and-modem) a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="edbdd-664">Maps to [Microsoft.PhoneAndModem](#phone-and-modem) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="edbdd-665">Microsoft. Printers</span><span class="sxs-lookup"><span data-stu-id="edbdd-665">Microsoft.Printers</span></span>                                          | <span data-ttu-id="edbdd-666">Impresoras</span><span class="sxs-lookup"><span data-stu-id="edbdd-666">Printers</span></span>                          | <span data-ttu-id="edbdd-667">{2227A280-3AEA-1069-A2DE-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="edbdd-667">{2227A280-3AEA-1069-A2DE-08002B30309D}</span></span> | <span data-ttu-id="edbdd-668">Se asigna a [Microsoft. DevicesAndPrinters](#devices-and-printers) a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="edbdd-668">Maps to [Microsoft.DevicesAndPrinters](#devices-and-printers) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="edbdd-669">Microsoft. ProblemReportsAndSolutions</span><span class="sxs-lookup"><span data-stu-id="edbdd-669">Microsoft.ProblemReportsAndSolutions</span></span>                        | <span data-ttu-id="edbdd-670">Informes de problemas y soluciones</span><span class="sxs-lookup"><span data-stu-id="edbdd-670">Problem Reports and Solutions</span></span>     | <span data-ttu-id="edbdd-671">{FCFEECAE-EE1B-4849-AE50-685DCF7717EC}</span><span class="sxs-lookup"><span data-stu-id="edbdd-671">{FCFEECAE-EE1B-4849-AE50-685DCF7717EC}</span></span> | <span data-ttu-id="edbdd-672">Se asigna a [Microsoft. ActionCenter](#action-center) a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="edbdd-672">Maps to [Microsoft.ActionCenter](#action-center) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="edbdd-673">Microsoft. RegionalAndLanguageOptions</span><span class="sxs-lookup"><span data-stu-id="edbdd-673">Microsoft.RegionalAndLanguageOptions</span></span>                        | <span data-ttu-id="edbdd-674">Configuración regional y de idioma</span><span class="sxs-lookup"><span data-stu-id="edbdd-674">Regional and Language Options</span></span>     | <span data-ttu-id="edbdd-675">{62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span><span class="sxs-lookup"><span data-stu-id="edbdd-675">{62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span></span> | <span data-ttu-id="edbdd-676">Se asigna a [Microsoft. RegionAndLanguage](#region) a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="edbdd-676">Maps to [Microsoft.RegionAndLanguage](#region) as of Windows 7.</span></span> <span data-ttu-id="edbdd-677">Tenga en cuenta que, a partir de Windows 8, región e idioma, cada uno de ellos tiene su propio elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="edbdd-677">Note that as of Windows 8, Region and Language were each given their own Control Panel item.</span></span> <span data-ttu-id="edbdd-678">Microsoft. RegionalAndLanguageOptions y Microsoft. RegionAndLanguage actualmente abren el elemento region.</span><span class="sxs-lookup"><span data-stu-id="edbdd-678">Both Microsoft.RegionalAndLanguageOptions and Microsoft.RegionAndLanguage currently open the Region item.</span></span> <span data-ttu-id="edbdd-679">Debe usar [Microsoft. Language](#location-settings) para tener acceso al elemento de idioma.</span><span class="sxs-lookup"><span data-stu-id="edbdd-679">You must use [Microsoft.Language](#location-settings) to access the Language item.</span></span> |
| <span data-ttu-id="edbdd-680">Microsoft. SecurityCenter</span><span class="sxs-lookup"><span data-stu-id="edbdd-680">Microsoft.SecurityCenter</span></span>                                    | <span data-ttu-id="edbdd-681">Centro de seguridad de Windows</span><span class="sxs-lookup"><span data-stu-id="edbdd-681">Windows Security Center</span></span>           | <span data-ttu-id="edbdd-682">{087DA31B-0DD3-4537-8E23-64A18591F88B}</span><span class="sxs-lookup"><span data-stu-id="edbdd-682">{087DA31B-0DD3-4537-8E23-64A18591F88B}</span></span> | <span data-ttu-id="edbdd-683">Se asigna a [Microsoft. ActionCenter](#action-center) a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="edbdd-683">Maps to [Microsoft.ActionCenter](#action-center) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="edbdd-684">Microsoft. SpeechRecognitionOptions</span><span class="sxs-lookup"><span data-stu-id="edbdd-684">Microsoft.SpeechRecognitionOptions</span></span>                          | <span data-ttu-id="edbdd-685">Opciones de reconocimiento de voz</span><span class="sxs-lookup"><span data-stu-id="edbdd-685">Speech Recognition Options</span></span>        | <span data-ttu-id="edbdd-686">{58E3C745-D971-4081-9034-86E34B30836A}</span><span class="sxs-lookup"><span data-stu-id="edbdd-686">{58E3C745-D971-4081-9034-86E34B30836A}</span></span> | <span data-ttu-id="edbdd-687">Se asigna a [Microsoft. SpeechRecognition](#speech-recognition) a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="edbdd-687">Maps to [Microsoft.SpeechRecognition](#speech-recognition) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="edbdd-688">Microsoft. TaskbarAndStartMenu</span><span class="sxs-lookup"><span data-stu-id="edbdd-688">Microsoft.TaskbarAndStartMenu</span></span>                               | <span data-ttu-id="edbdd-689">Barra de tareas y menú Inicio</span><span class="sxs-lookup"><span data-stu-id="edbdd-689">Taskbar and Start Menu</span></span>            | <span data-ttu-id="edbdd-690">{0DF44EAA-FF21-4412-828E-260A8728E7F1}</span><span class="sxs-lookup"><span data-stu-id="edbdd-690">{0DF44EAA-FF21-4412-828E-260A8728E7F1}</span></span> | <span data-ttu-id="edbdd-691">Asigna a [Microsoft. Taskbar](#speech-recognition) a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="edbdd-691">Maps to [Microsoft.Taskbar](#speech-recognition) as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="edbdd-692">Microsoft. WelcomeCenter</span><span class="sxs-lookup"><span data-stu-id="edbdd-692">Microsoft.WelcomeCenter</span></span>                                     | <span data-ttu-id="edbdd-693">Centro de bienvenida</span><span class="sxs-lookup"><span data-stu-id="edbdd-693">Welcome Center</span></span>                    | <span data-ttu-id="edbdd-694">{CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1}</span><span class="sxs-lookup"><span data-stu-id="edbdd-694">{CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1}</span></span> | <span data-ttu-id="edbdd-695">Se asigna a Microsoft. GettingStarted en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="edbdd-695">Maps to Microsoft.GettingStarted in Windows 7.</span></span> <span data-ttu-id="edbdd-696">Inicia la Página principal del panel de control a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="edbdd-696">Launches the Control Panel home page as of Windows 8.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="edbdd-697">Microsoft. WindowsSidebarProperties</span><span class="sxs-lookup"><span data-stu-id="edbdd-697">Microsoft.WindowsSidebarProperties</span></span>                          | <span data-ttu-id="edbdd-698">Propiedades de Windows Sidebar</span><span class="sxs-lookup"><span data-stu-id="edbdd-698">Windows Sidebar Properties</span></span>        | <span data-ttu-id="edbdd-699">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span><span class="sxs-lookup"><span data-stu-id="edbdd-699">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span></span> | <span data-ttu-id="edbdd-700">Se asigna a Microsoft. DesktopGadgets en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="edbdd-700">Maps to Microsoft.DesktopGadgets in Windows 7.</span></span> <span data-ttu-id="edbdd-701">Se quita a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="edbdd-701">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="edbdd-702">Microsoft. WindowsSideShow</span><span class="sxs-lookup"><span data-stu-id="edbdd-702">Microsoft.WindowsSideShow</span></span>                                   | <span data-ttu-id="edbdd-703">Windows SideShow</span><span class="sxs-lookup"><span data-stu-id="edbdd-703">Windows SideShow</span></span>                  | <span data-ttu-id="edbdd-704">{E95A4861-D57A-4be1-AD0F-35267E261739}</span><span class="sxs-lookup"><span data-stu-id="edbdd-704">{E95A4861-D57A-4be1-AD0F-35267E261739}</span></span> | <span data-ttu-id="edbdd-705">Característica desusada en Windows 8, quitada de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="edbdd-705">Feature deprecated in Windows 8, removed as of Windows 8.1.</span></span>                                                                                                                                                                                                                                                                                               |



 

## <a name="using-canonical-names-in-local-group-policy"></a><span data-ttu-id="edbdd-706">Usar nombres canónicos en directiva de grupo locales</span><span class="sxs-lookup"><span data-stu-id="edbdd-706">Using Canonical Names in Local Group Policy</span></span>

<span data-ttu-id="edbdd-707">A partir de Windows 7, puede usar nombres canónicos para restringir el acceso a elementos individuales del panel de control mediante la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="edbdd-707">As of Windows 7, you can use canonical names to restrict access to individual Control Panel items through group policy.</span></span> <span data-ttu-id="edbdd-708">Este mismo procedimiento se puede usar en Windows Vista, pero tiene que usar el nombre del módulo en lugar del nombre canónico.</span><span class="sxs-lookup"><span data-stu-id="edbdd-708">This same procedure can be used in Windows Vista, but you have to use the module name instead of the canonical name.</span></span>

### <a name="hiding-individual-control-panel-items"></a><span data-ttu-id="edbdd-709">Ocultar elementos individuales del panel de control</span><span class="sxs-lookup"><span data-stu-id="edbdd-709">Hiding individual Control Panel items</span></span>

<span data-ttu-id="edbdd-710">Use este método si desea mostrar más elementos del panel de control de los que desea ocultar.</span><span class="sxs-lookup"><span data-stu-id="edbdd-710">Use this method if you want to show more Control Panel items than you want to hide.</span></span>

1.  <span data-ttu-id="edbdd-711">Ejecute el archivo gpedit. msc para iniciar el Editor de directivas de grupo local.</span><span class="sxs-lookup"><span data-stu-id="edbdd-711">Run the Gpedit.msc file to launch the Local Group Policy Editor.</span></span> <span data-ttu-id="edbdd-712">También puede escribir "Directiva de grupo" en la Windows 8.1 pantalla Inicio y seleccionar **Editar Directiva de grupo** en los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="edbdd-712">You can also type "group policy" at the Windows 8.1 Start screen and select **Edit group policy** from the search results.</span></span>
2.  <span data-ttu-id="edbdd-713">Seleccione **configuración de usuario**  >  **plantillas administrativas**  >  **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="edbdd-713">Select **User Configuration** > **Administrative Templates** > **Control Panel**.</span></span>
3.  <span data-ttu-id="edbdd-714">Seleccione **ocultar los elementos especificados del panel de control**.</span><span class="sxs-lookup"><span data-stu-id="edbdd-714">Select **Hide specified Control Panel items**.</span></span>
4.  <span data-ttu-id="edbdd-715">En la ventana **Ocultar elementos especificados del panel de control** que se abre, haga clic en **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="edbdd-715">In the **Hide Specified Control Panel Items** window that opens, click **Enabled**.</span></span>
5.  <span data-ttu-id="edbdd-716">Haga clic en el botón **Mostrar** en el panel de opciones para mostrar la lista de elementos del panel de control no permitidos.</span><span class="sxs-lookup"><span data-stu-id="edbdd-716">Click the **Show** button in the Options panel to show the list of disallowed Control Panel items.</span></span>
6.  <span data-ttu-id="edbdd-717">En la ventana **Mostrar contenido** que se abre, escriba un nombre canónico en la columna **valor** .</span><span class="sxs-lookup"><span data-stu-id="edbdd-717">In the **Show Contents** window that opens, type a canonical name into the **Value** column.</span></span> <span data-ttu-id="edbdd-718">Repita este paso las veces que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="edbdd-718">Repeat as necessary.</span></span>
7.  <span data-ttu-id="edbdd-719">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="edbdd-719">Click **OK**.</span></span>

### <a name="showing-individual-control-panel-items"></a><span data-ttu-id="edbdd-720">Mostrar elementos individuales del panel de control</span><span class="sxs-lookup"><span data-stu-id="edbdd-720">Showing individual Control Panel items</span></span>

<span data-ttu-id="edbdd-721">Use este método si desea ocultar más elementos del panel de control de los que desea mostrar.</span><span class="sxs-lookup"><span data-stu-id="edbdd-721">Use this method if you want to hide more Control Panel items than you want to show.</span></span>

1.  <span data-ttu-id="edbdd-722">Ejecute el archivo gpedit. msc para iniciar el Editor de directivas de grupo local.</span><span class="sxs-lookup"><span data-stu-id="edbdd-722">Run the Gpedit.msc file to launch the Local Group Policy Editor.</span></span> <span data-ttu-id="edbdd-723">También puede escribir "Directiva de grupo" en la Windows 8.1 pantalla Inicio y seleccionar **Editar Directiva de grupo** en los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="edbdd-723">You can also type "group policy" at the Windows 8.1 Start screen and select **Edit group policy** from the search results.</span></span>
2.  <span data-ttu-id="edbdd-724">Seleccione **configuración de usuario**  >  **plantillas administrativas**  >  **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="edbdd-724">Select **User Configuration** > **Administrative Templates** > **Control Panel**.</span></span>
3.  <span data-ttu-id="edbdd-725">Seleccione **Mostrar solo los elementos especificados del panel de control**.</span><span class="sxs-lookup"><span data-stu-id="edbdd-725">Select **Show only specified Control Panel items**.</span></span>
4.  <span data-ttu-id="edbdd-726">En la ventana **Mostrar solo los elementos especificados del panel de control** que se abre, haga clic en **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="edbdd-726">In the **Show Only Specified Control Panel Items** window that opens, click **Enabled**.</span></span> <span data-ttu-id="edbdd-727">Esto oculta todo en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="edbdd-727">This hides everything in the Control Panel.</span></span>
5.  <span data-ttu-id="edbdd-728">Haga clic en el botón **Mostrar** en el panel de opciones para mostrar la lista de elementos permitidos del panel de control.</span><span class="sxs-lookup"><span data-stu-id="edbdd-728">Click the **Show** button in the Options panel to show the list of allowed Control Panel items.</span></span>
6.  <span data-ttu-id="edbdd-729">En la ventana **Mostrar contenido** que se abre, escriba un nombre canónico en la columna **valor** .</span><span class="sxs-lookup"><span data-stu-id="edbdd-729">In the **Show Contents** window that opens, type a canonical name into the **Value** column.</span></span> <span data-ttu-id="edbdd-730">Repita este paso las veces que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="edbdd-730">Repeat as necessary.</span></span>
7.  <span data-ttu-id="edbdd-731">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="edbdd-731">Click **OK**.</span></span>

<span data-ttu-id="edbdd-732">Si desea quitar todas las entradas que ha agregado a una lista Mostrar u ocultar elementos del panel de control, vuelva a la pantalla del paso 4 y seleccione **sin configurar** para borrar la lista.</span><span class="sxs-lookup"><span data-stu-id="edbdd-732">If you want to remove all of the entries that you've added to a Show or Hide Control Panel items list, return to the screen in step 4 and select **Not Configured** to clear the list.</span></span> <span data-ttu-id="edbdd-733">Si desea conservar las entradas pero suspender las restricciones, seleccione **deshabilitado**.</span><span class="sxs-lookup"><span data-stu-id="edbdd-733">If you want to retain your entries but suspend the restrictions, select **Disabled**.</span></span>

## <a name="remarks"></a><span data-ttu-id="edbdd-734">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edbdd-734">Remarks</span></span>

<span data-ttu-id="edbdd-735">Es posible que aparezcan elementos en el panel de control que no se muestran aquí.</span><span class="sxs-lookup"><span data-stu-id="edbdd-735">You might see items in your Control Panel that are not listed here.</span></span> <span data-ttu-id="edbdd-736">Estos elementos no forman parte de Windows, pero en su lugar se agregan durante la instalación de varios programas de software y hardware, como Microsoft Office o una tarjeta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="edbdd-736">Those items are not part of Windows, but instead are added during the installation of various software and hardware, such as Microsoft Office or a video card.</span></span> <span data-ttu-id="edbdd-737">Los elementos del panel de control que no son de Windows pueden tener o no un nombre canónico.</span><span class="sxs-lookup"><span data-stu-id="edbdd-737">Non-Windows Control Panel items may or may not have a canonical name.</span></span> <span data-ttu-id="edbdd-738">Para buscar el nombre canónico de un elemento del panel de control que no aparece aquí, busque en el registro en estas rutas de acceso:</span><span class="sxs-lookup"><span data-stu-id="edbdd-738">To find the canonical name of a Control Panel item not listed here, look in the registry under these paths:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID of the Control Panel item}
         System.ApplicationName
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         CLSID
            {CLSID of the Control Panel item}
               System.ApplicationName
```

<span data-ttu-id="edbdd-739">Para obtener más información que pueda ayudarle a detectar los CLSID necesarios, consulte [Cómo registrar elementos del panel de control ejecutable](how-to-register-an-executable-control-panel-item-registration-.md) y [Cómo registrar elementos del panel de control de archivos dll](how-to-register-dll-control-panel-item-registration-.md).</span><span class="sxs-lookup"><span data-stu-id="edbdd-739">For more information that can help you discover the necessary CLSIDs, see [How to Register Executable Control Panel Items](how-to-register-an-executable-control-panel-item-registration-.md) and [How to Register DLL Control Panel Items](how-to-register-dll-control-panel-item-registration-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="edbdd-740">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="edbdd-740">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edbdd-741">Ejecutar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="edbdd-741">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="edbdd-742">**IOpenControlPanel**</span><span class="sxs-lookup"><span data-stu-id="edbdd-742">**IOpenControlPanel**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel)
</dt> </dl>

 

 



