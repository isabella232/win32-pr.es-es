---
title: Método de cambio de la clase Win32_Service (Mbnapi. h) (TerminalService)
description: Modifica un TerminalService de Win32 \_ .
ms.assetid: 19E43A80-47C9-4C5A-8E73-723F206AA7C0
ms.tgt_platform: multiple
keywords:
- Cambiar método Servicios de Escritorio remoto
- Cambiar Servicios de Escritorio remoto de método, Win32_Service clase
- Win32_Service Servicios de Escritorio remoto de clase, Change (método)
topic_type:
- apiref
api_name:
- Win32_Service.Change
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa34ea0c9c38cd0b11f97a0bbf651f1aebf37a46
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389209"
---
# <a name="change-method-of-the-win32_service-class-mbnapih---terminalservice"></a><span data-ttu-id="5e0d1-106">Método de cambio de la clase Win32_Service (Mbnapi. h)-TerminalService</span><span class="sxs-lookup"><span data-stu-id="5e0d1-106">Change method of the Win32_Service class (Mbnapi.h) - TerminalService</span></span>

<span data-ttu-id="5e0d1-107">El método de clase **Change** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) modifica un [**\_ TerminalService de Win32**](win32-terminalservice.md).</span><span class="sxs-lookup"><span data-stu-id="5e0d1-107">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_TerminalService**](win32-terminalservice.md).</span></span>

<span data-ttu-id="5e0d1-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="5e0d1-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5e0d1-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5e0d1-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5e0d1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e0d1-110">Syntax</span></span>


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint32  ServiceType,
  [in] uint32  ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies,
  [in] string  ServiceDependencies
);
```



## <a name="parameters"></a><span data-ttu-id="5e0d1-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e0d1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e0d1-112">*DisplayName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e0d1-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-113">Nombre para mostrar del servicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-113">The display name of the service.</span></span> <span data-ttu-id="5e0d1-114">Esta cadena tiene una longitud máxima de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="5e0d1-115">El nombre se conserva en las mayúsculas y minúsculas en el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-115">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="5e0d1-116">Las comparaciones de *displayName* siempre distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-116">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="5e0d1-117">Constraints: acepta el mismo valor que la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="5e0d1-117">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="5e0d1-118">Ejemplo, "Endisco".</span><span class="sxs-lookup"><span data-stu-id="5e0d1-118">Example, "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-119">*Nombreruta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e0d1-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-120">Ruta de acceso completa al archivo ejecutable que implementa el servicio, por ejemplo, " \\ raízDelSistema \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="5e0d1-120">The fully qualified path to the executable file that implements the service, for example, "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-121">*ServiceType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e0d1-121">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-122">Tipo de servicios proporcionados a los procesos que los llaman.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-122">The type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="5e0d1-123">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="5e0d1-123">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-124">Controlador de kernel</span><span class="sxs-lookup"><span data-stu-id="5e0d1-124">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-125">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="5e0d1-125">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-126">Controlador del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="5e0d1-126">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-127">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="5e0d1-127">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-128">Adapter (Adaptador)</span><span class="sxs-lookup"><span data-stu-id="5e0d1-128">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-129">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="5e0d1-129">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-130">Controlador del reconocedor</span><span class="sxs-lookup"><span data-stu-id="5e0d1-130">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-131">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="5e0d1-131">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-132">Proceso propio</span><span class="sxs-lookup"><span data-stu-id="5e0d1-132">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-133">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="5e0d1-133">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-134">Compartir proceso</span><span class="sxs-lookup"><span data-stu-id="5e0d1-134">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-135">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="5e0d1-135">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-136">Proceso interactivo</span><span class="sxs-lookup"><span data-stu-id="5e0d1-136">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5e0d1-137">*ErrorControl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e0d1-137">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-138">Gravedad del error si este servicio no se inicia durante el inicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-138">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="5e0d1-139">El valor indica la acción realizada por el programa de inicio si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-139">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="5e0d1-140">El sistema registra todos los errores.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-140">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="5e0d1-141">0</span><span class="sxs-lookup"><span data-stu-id="5e0d1-141">0</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-142">**Ignore**.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-142">**Ignore**.</span></span> <span data-ttu-id="5e0d1-143">El inicio continúa.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-143">Startup continues.</span></span> <span data-ttu-id="5e0d1-144">No se proporciona ninguna notificación al usuario de que se produjo un error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-144">No notification is given to the user that the service failed.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-145">1</span><span class="sxs-lookup"><span data-stu-id="5e0d1-145">1</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-146">**Sin.**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-146">**Normal.**</span></span> <span data-ttu-id="5e0d1-147">El inicio continúa.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-147">Startup continues.</span></span> <span data-ttu-id="5e0d1-148">Antes de que el usuario inicie sesión, el usuario recibe la notificación, "error al menos un servicio o dispositivo durante el inicio".</span><span class="sxs-lookup"><span data-stu-id="5e0d1-148">Before the user logs on, the user receives the notification, "At least one service or device failed during startup."</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-149">2</span><span class="sxs-lookup"><span data-stu-id="5e0d1-149">2</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-150">**Fuertes.**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-150">**Severe.**</span></span> <span data-ttu-id="5e0d1-151">El equipo intenta reiniciarse con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-151">Computer attempts to restart with last-known good configuration.</span></span> <span data-ttu-id="5e0d1-152">Si se produce un error de nuevo en el servicio, el inicio continúa y se le concede una notificación al usuario.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-152">If the service fails again, startup continues and notification is given to the user.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-153">3</span><span class="sxs-lookup"><span data-stu-id="5e0d1-153">3</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-154">**Suma.**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-154">**Critical.**</span></span> <span data-ttu-id="5e0d1-155">El equipo intenta reiniciarse con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-155">Computer attempts to restart with last-known good configuration.</span></span> <span data-ttu-id="5e0d1-156">Si se produce un error en el servicio, se detiene el inicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-156">If the service fails again, startup stops.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5e0d1-157">*StartMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e0d1-157">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-158">Modo de inicio del servicio base de Windows.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-158">Start mode of the Windows base service.</span></span> <span data-ttu-id="5e0d1-159">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-159">For more information, see the Remarks section.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="5e0d1-160"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Arranque**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-160"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="5e0d1-161">Controlador de dispositivo Iniciado por el cargador del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-161">Device driver started by the operating system loader.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="5e0d1-162"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Integrado**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-162"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="5e0d1-163">Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-163">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="5e0d1-164">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-164">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="5e0d1-165"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automático**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-165"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="5e0d1-166">El administrador de control de servicios inicia automáticamente el servicio durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-166">Service is started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="5e0d1-167">Los servicios de inicio automático se inician antes de que un usuario inicie sesión en el equipo y se ejecuten incluso si ningún usuario inicia sesión en el equipo.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-167">Autostart services start before a user logs on to the computer and run even if no user logs on to the computer.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="5e0d1-168"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-168"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="5e0d1-169">Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](win32-terminalservice-startservice.md) .</span><span class="sxs-lookup"><span data-stu-id="5e0d1-169">Service to be started by the service control manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span> <span data-ttu-id="5e0d1-170">Aunque los servicios manuales deben ser iniciados específicamente por un usuario (o mediante un script), siguen ejecutándose incluso si el usuario cierra la sesión.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-170">Although manual services must be specifically started by a user (or by a script), they continue to run even if the user logs off.</span></span> <span data-ttu-id="5e0d1-171">Los servicios manuales se suelen denominar servicios a petición.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-171">Manual services are often referred to as on-demand services.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5e0d1-172"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disponible**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-172"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="5e0d1-173">Servicio que ya no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-173">Service that can no longer be started.</span></span> <span data-ttu-id="5e0d1-174">Para iniciar un servicio deshabilitado, primero debe cambiar la opción de inicio a automático o manual.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-174">To start a disabled service, you must first change the startup option to either Auto or Manual.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5e0d1-175">*DesktopInteract* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e0d1-175">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-176">Si **es true**, el servicio puede crear o comunicarse con una ventana en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-176">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-177">*StartName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e0d1-177">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-178">Nombre de la cuenta con la que se ejecuta el servicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-178">Account name the service runs under.</span></span> <span data-ttu-id="5e0d1-179">Dependiendo del tipo de servicio, el nombre de la cuenta puede tener el formato nombreDeDominio \\ nombreDeUsuario o. \\ Nombre.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-179">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="5e0d1-180">El proceso de servicio se registrará con una de estas dos formas cuando se ejecute.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-180">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="5e0d1-181">Si la cuenta pertenece al dominio integrado,. \\ Se puede especificar el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-181">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="5e0d1-182">Si se especifica **null** , el servicio se iniciará sesión como la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-182">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="5e0d1-183">En el caso de los controladores de kernel o de nivel de sistema, *StartName* contiene el nombre de objeto del controlador (es decir, sistema de \\ archivos \\ RDR o \\ XNS del controlador \\ ) que usa el sistema de entrada y salida (e/s) para cargar el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-183">For kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="5e0d1-184">Si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de e/s basado en el nombre del servicio, por ejemplo, "DWDOM \\ admin".</span><span class="sxs-lookup"><span data-stu-id="5e0d1-184">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name, for example, "DWDOM\\Admin".</span></span>

<span data-ttu-id="5e0d1-185">También puede usar el formato de nombre principal de usuario (UPN) para especificar **StartName**, por ejemplo, *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="5e0d1-185">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-186">*StartPassword* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e0d1-186">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-187">Contraseña para el nombre de cuenta especificado por el parámetro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="5e0d1-187">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="5e0d1-188">Especifique **null** si no va a cambiar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-188">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="5e0d1-189">Especifique una cadena vacía si el servicio no tiene contraseña.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-189">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="5e0d1-190">Al cambiar un servicio de un sistema local a una red, o de una red a un sistema local, *StartPassword* debe ser una cadena vacía ("") y no **null**.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-190">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="5e0d1-191">*LoadOrderGroup* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e0d1-191">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-192">Nombre del grupo al que está asociado.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-192">Group name that it is associated with.</span></span> <span data-ttu-id="5e0d1-193">Los grupos de pedidos de carga se incluyen en el registro del sistema y determinan la secuencia en la que se cargan los servicios en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-193">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="5e0d1-194">Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no pertenece a un grupo.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-194">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="5e0d1-195">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-195">For more information, see the Remarks section.</span></span>

<span data-ttu-id="5e0d1-196">Las dependencias entre grupos deben aparecer en el parámetro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="5e0d1-196">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="5e0d1-197">Los servicios de la lista de grupos de orden de carga se inician en primer lugar, seguidos de los servicios de los grupos que no están en la lista de grupos de orden de carga, seguidos de los servicios que no pertenecen a un grupo.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-197">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="5e0d1-198">El registro del sistema tiene una lista de grupos de orden de carga que se encuentran en:</span><span class="sxs-lookup"><span data-stu-id="5e0d1-198">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="5e0d1-199">**HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local ServiceGroupOrder</span><span class="sxs-lookup"><span data-stu-id="5e0d1-199">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-200">*LoadOrderGroupDependencies* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e0d1-200">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-201">Lista de grupos de orden de carga que deben iniciarse antes de que se inicie este servicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-201">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="5e0d1-202">La matriz termina en **null**.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-202">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="5e0d1-203">Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-203">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="5e0d1-204">Los nombres de grupo deben ir precedidos del **\_ \_ identificador de grupo SC** (definido en el archivo Winsvc. h) para diferenciarlos de los nombres de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-204">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names because services and service groups share the same namespace.</span></span> <span data-ttu-id="5e0d1-205">La dependencia de un grupo significa que este servicio se puede ejecutar si se está ejecutando al menos un miembro del grupo después de un intento de iniciar todos los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-205">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-206">*ServiceDependencies* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e0d1-206">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-207">Lista que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-207">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="5e0d1-208">La matriz termina en **null**.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-208">The array is doubly **NULL**-terminated.</span></span> <span data-ttu-id="5e0d1-209">Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-209">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="5e0d1-210">La dependencia de un servicio indica que este servicio solo se puede ejecutar si se está ejecutando el servicio del que depende.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-210">Dependency on a service indicates that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e0d1-211">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e0d1-211">Return value</span></span>

<span data-ttu-id="5e0d1-212">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-212">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="5e0d1-213">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5e0d1-213">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5e0d1-214">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5e0d1-214">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5e0d1-215">**0**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-215">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-216">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-216">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-217">**1**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-217">**1**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-218">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-218">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-219">**2**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-219">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-220">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-220">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-221">**3**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-221">**3**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-222">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-222">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-223">**4**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-223">**4**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-224">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-224">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-225">**5**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-225">**5**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-226">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-226">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-227">**6**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-227">**6**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-228">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-228">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-229">**7**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-229">**7**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-230">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-230">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-231">**8**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-231">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-232">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-232">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-233">**9**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-233">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-234">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-234">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-235">**10**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-235">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-236">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-236">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-237">**11**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-237">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-238">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-238">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-239">**12**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-239">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-240">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-240">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-241">**13**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-241">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-242">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-242">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-243">**14**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-243">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-244">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-244">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-245">**15**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-245">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-246">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-246">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-247">**16**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-247">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-248">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-248">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-249">**17**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-249">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-250">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-250">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-251">**18**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-251">**18**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-252">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-252">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-253">**19**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-253">**19**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-254">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-254">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-255">**20**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-255">**20**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-256">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-256">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-257">**21**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-257">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-258">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-258">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-259">**22**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-259">**22**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-260">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-260">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-261">**23**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-261">**23**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-262">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-262">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5e0d1-263">**24**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-263">**24**</span></span>
</dt> <dd>

<span data-ttu-id="5e0d1-264">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-264">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e0d1-265">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5e0d1-265">Remarks</span></span>

<span data-ttu-id="5e0d1-266">Cuando se inicia un equipo, también se inician todos los servicios de inicio automático.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-266">When a computer starts, all the autostart services also start.</span></span> <span data-ttu-id="5e0d1-267">En ocasiones, es posible que uno de estos servicios no se inicie junto con el equipo.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-267">On occasion, one of these services might fail to start along with the computer.</span></span> <span data-ttu-id="5e0d1-268">Cuando se produce un error en un servicio durante el inicio del sistema, el equipo toma medidas según el valor del código de control de errores del servicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-268">When a service fails during system startup, the computer takes action based on the value of the service error control code.</span></span>

<span data-ttu-id="5e0d1-269">la mayoría de los servicios se instalan con el código de control de errores normal.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-269">most services are installed using the Normal error control code.</span></span> <span data-ttu-id="5e0d1-270">Algunas de las excepciones, que se instalan con el código de error ignore, incluyen:</span><span class="sxs-lookup"><span data-stu-id="5e0d1-270">A few of the exceptions, which are installed using the Ignore error code, include:</span></span>

-   <span data-ttu-id="5e0d1-271">Servicio de replicación de archivos</span><span class="sxs-lookup"><span data-stu-id="5e0d1-271">File Replication Service</span></span>
-   <span data-ttu-id="5e0d1-272">Tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="5e0d1-272">Smart Card</span></span>
-   <span data-ttu-id="5e0d1-273">Inicio de sesión secundario</span><span class="sxs-lookup"><span data-stu-id="5e0d1-273">Secondary Logon</span></span>
-   <span data-ttu-id="5e0d1-274">WMI</span><span class="sxs-lookup"><span data-stu-id="5e0d1-274">WMI</span></span>

<span data-ttu-id="5e0d1-275">En el caso de los servicios que se instalan con el código de error ignore, no se proporciona ninguna notificación al usuario de que se ha producido un error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-275">For the services installed using the Ignore error code, no notification is given to the user that the service has failed.</span></span> <span data-ttu-id="5e0d1-276">Si prefiere recibir una notificación en pantalla de que no se pudo iniciar un servicio, puede usar WMI para cambiar el código de control de errores.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-276">If you prefer on-screen notification that a service could not start, you can use WMI to change the error control code.</span></span> <span data-ttu-id="5e0d1-277">Los códigos de control de errores solo se aplican al inicio del equipo; los códigos de control de errores no se usan si detiene e intenta reiniciar un servicio después de que el equipo se esté ejecutando.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-277">Error control codes apply only to computer startup; error control codes are not used if you stop and then attempt to restart a service after the computer is running.</span></span>

<span data-ttu-id="5e0d1-278">En alguna ocasión, es posible que necesite cambiar la cuenta en la que se ejecuta un servicio determinado.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-278">On occasion, you might need to change the account under which a given service runs.</span></span> <span data-ttu-id="5e0d1-279">Por ejemplo, puede ejecutar un servicio en una cuenta administrativa.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-279">For example, you might run a service under an administrative account.</span></span> <span data-ttu-id="5e0d1-280">Como esto puede crear una vulnerabilidad de seguridad, puede cambiar el servicio a una cuenta con menos privilegios.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-280">Because this can create a security vulnerability, you might switch the service to an account with fewer privileges.</span></span> <span data-ttu-id="5e0d1-281">Como alternativa, es posible que los servicios se ejecuten en una cuenta que esté a punto de eliminarse, o puede que desee asegurarse de que, en todos los servidores, determinados servicios se ejecuten en determinadas cuentas.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-281">Alternatively, you might have services running under an account that is about to be deleted, or you might want to ensure that, on all your servers, certain services run under certain accounts.</span></span> <span data-ttu-id="5e0d1-282">Puede usar el método **Change** de la clase [**Win32 \_ TerminalService**](win32-terminalservice.md) para configurar los servicios de para que se ejecuten en una cuenta de usuario especificada.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-282">You can use the **Change** method of the [**Win32\_TerminalService**](win32-terminalservice.md) class to configure services to run under a specified user account.</span></span> <span data-ttu-id="5e0d1-283">Al seleccionar una cuenta, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5e0d1-283">When selecting an account, keep in mind the following:</span></span>

-   <span data-ttu-id="5e0d1-284">La cuenta que se usa como cuenta de servicio debe tener el derecho de iniciar sesión como servicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-284">The account being used as a service account must have the right to log on as a service.</span></span> <span data-ttu-id="5e0d1-285">Este derecho se puede conceder mediante directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-285">This right can be granted by using Group Policy.</span></span>
-   <span data-ttu-id="5e0d1-286">La cuenta que se usa como cuenta de servicio no debe ser miembro de un grupo local, de dominio o de administradores de organización.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-286">The account being used as a service account should not be a member of a local, domain, or enterprise Administrators group.</span></span>
-   <span data-ttu-id="5e0d1-287">Cada instancia de un servicio se debe ejecutar con una cuenta de usuario única.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-287">Each instance of a service should run under a unique user account.</span></span> <span data-ttu-id="5e0d1-288">Esto proporciona seguridad adicional y habilita la auditoría de instancias de servicio individuales.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-288">This provides additional security, and enables the auditing of individual service instances.</span></span>
-   <span data-ttu-id="5e0d1-289">Si el servicio es interactivo, el servicio debe ejecutarse en la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-289">If the service is interactive, then the service must run under the LocalSystem account.</span></span>

    <span data-ttu-id="5e0d1-290">Se requiere LocalSystem porque solo una estación de ventana (WinSta0) puede ser visible e interactiva a la vez.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-290">LocalSystem is required because only one window station (WinSta0) can be visible and interactive at a time.</span></span> <span data-ttu-id="5e0d1-291">Si un servicio se ejecuta en una cuenta distinta de LocalSystem, se ejecuta en la estación de ventana de servicio-0x03e7 $ \\ predeterminada, que es una ventana invisible.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-291">If a service runs under an account other than LocalSystem, it runs in the Service-0x03e7$\\Default window station, which is an invisible window.</span></span> <span data-ttu-id="5e0d1-292">Los servicios que se ejecutan en esta estación de ventana no pueden recibir entradas ni mostrar resultados.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-292">Services running in this window station cannot receive input or display output.</span></span>

<span data-ttu-id="5e0d1-293">Cuando asigna una cuenta a un servicio, el SCM requiere la contraseña correcta para esa cuenta antes de realizar la asignación.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-293">When you assign an account to a service, the SCM requires the correct password for that account before it makes the assignment.</span></span> <span data-ttu-id="5e0d1-294">Si proporciona una contraseña incorrecta, el SCM rechazará la cuenta.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-294">If you supply an incorrect password, the SCM rejects the account.</span></span> <span data-ttu-id="5e0d1-295">Si configura una cuenta de servicio con la cuenta LocalSystem, LocalService o NetworkService, no es necesario que proporcione una contraseña de cuenta porque estas cuentas no tienen contraseñas.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-295">If you configure a service account using the LocalSystem, LocalService, or NetworkService account, you do not need to supply an account password because these accounts do not have passwords.</span></span>

<span data-ttu-id="5e0d1-296">El SCM almacena la contraseña de la cuenta en la base de datos de servicios.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-296">The SCM stores the account password in the services database.</span></span> <span data-ttu-id="5e0d1-297">Sin embargo, una vez asignada la contraseña, el SCM no garantiza que la contraseña almacenada en la base de datos de servicios y la contraseña asignada a la cuenta de usuario en Active Directory sigan coincidiendo.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-297">After the password is assigned, however, the SCM does not ensure that the password stored in the services database and the password assigned to the user account in Active Directory continue to match.</span></span> <span data-ttu-id="5e0d1-298">Por consiguiente, podría producirse una situación similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="5e0d1-298">Consequently, a situation similar to the following could occur:</span></span>

-   <span data-ttu-id="5e0d1-299">. Puede configurar un servicio para que se ejecute en una cuenta de usuario determinada.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-299">.You configure a service to run under a particular user account.</span></span>
-   <span data-ttu-id="5e0d1-300">El servicio se inicia con esa cuenta mediante la contraseña de la cuenta actual.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-300">The service starts up under that account by using the current account password.</span></span>
-   <span data-ttu-id="5e0d1-301">Puede cambiar la contraseña de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-301">You change the password for the user account.</span></span>
-   <span data-ttu-id="5e0d1-302">El servicio continúa ejecutándose.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-302">The service continues to run.</span></span> <span data-ttu-id="5e0d1-303">Sin embargo, si el servicio se detiene, no puede reiniciarlo porque el SCM sigue usando la contraseña antigua no válida.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-303">However, if the service stops, you cannot restart it because the SCM continues to use the old, invalid password.</span></span> <span data-ttu-id="5e0d1-304">El cambio de la contraseña en Active Directory no cambia la contraseña almacenada en la base de datos de servicios.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-304">Changing the password in Active Directory does not change the password stored in the services database.</span></span>

<span data-ttu-id="5e0d1-305">Si ejecuta servicios en cuentas de usuario normales, deberá actualizar esas contraseñas de servicio cada vez que cambie la contraseña de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-305">If you run services under regular user accounts, you need to update those service passwords each time the user account password changes.</span></span> <span data-ttu-id="5e0d1-306">Esto puede llevar mucho tiempo si no está seguro de qué servicios se están ejecutando en esa cuenta o qué equipos tienen servicios en ejecución en esa cuenta.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-306">This can be particularly time-consuming if you are not sure which services are running under that account or which computers have services running under that account.</span></span> <span data-ttu-id="5e0d1-307">Afortunadamente, puede usar WMI para comprobar las cuentas de servicio en todos los equipos y, si es necesario, cambiar la contraseña de la cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-307">Fortunately, you can use WMI to check the service accounts on all your computers and, if necessary, change the service account password.</span></span>

<span data-ttu-id="5e0d1-308">El [**parámetro \_ LoadOrderGroup de Win32**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) representa un grupo de servicios del sistema que definen las dependencias de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-308">The [**Win32\_LoadOrderGroup**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="5e0d1-309">Los servicios deben iniciarse en el orden especificado por el grupo de orden de carga, ya que los servicios dependen entre sí.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-309">The services must be initiated in the order specified by the Load Order Group because the services depend on each other.</span></span> <span data-ttu-id="5e0d1-310">Estos servicios dependientes requieren la presencia de los servicios antecedentes para que funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-310">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="5e0d1-311">Para cambiar un servicio de un servicio de red a un sistema local, los parámetros *StartName* y *StartPassword* deben tener los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="5e0d1-311">To change a service from a network service to a local system the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="5e0d1-312">Para cambiar un servicio de un servicio de sistema local a una red, los parámetros *StartName* y *StartPassword* deben tener los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="5e0d1-312">To change a service from a local system service to a network the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a><span data-ttu-id="5e0d1-313">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5e0d1-313">Examples</span></span>

<span data-ttu-id="5e0d1-314">El siguiente VBScript cambia la cuenta de servicio para que los servicios se ejecuten con una cuenta de usuario especificada en LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="5e0d1-314">The following VBScript changes the service account for services from running under a specified user account to LocalSystem.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change _
 ( , , , , , , ".\LocalSystem" , "")
Next
```



<span data-ttu-id="5e0d1-315">El siguiente VBScript cambia la contraseña de la cuenta de servicio para todos los scripts que se ejecutan en netsvc</span><span class="sxs-lookup"><span data-stu-id="5e0d1-315">The following VBScript changes the service account password for all scripts running under Netsvc</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a><span data-ttu-id="5e0d1-316">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e0d1-316">Requirements</span></span>



| <span data-ttu-id="5e0d1-317">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e0d1-317">Requirement</span></span> | <span data-ttu-id="5e0d1-318">Valor</span><span class="sxs-lookup"><span data-stu-id="5e0d1-318">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e0d1-319">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e0d1-319">Minimum supported client</span></span><br/> | <span data-ttu-id="5e0d1-320">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e0d1-320">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e0d1-321">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e0d1-321">Minimum supported server</span></span><br/> | <span data-ttu-id="5e0d1-322">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e0d1-322">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e0d1-323">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5e0d1-323">Namespace</span></span><br/>                | <span data-ttu-id="5e0d1-324">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5e0d1-324">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5e0d1-325">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e0d1-325">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e0d1-326"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e0d1-326"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="5e0d1-327">MOF</span><span class="sxs-lookup"><span data-stu-id="5e0d1-327">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e0d1-328"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e0d1-328"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e0d1-329">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e0d1-329">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e0d1-330"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e0d1-330"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e0d1-331">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e0d1-331">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e0d1-332">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-332">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="5e0d1-333">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="5e0d1-333">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="5e0d1-334">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-334">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="5e0d1-335">Tareas WMI: servicios</span><span class="sxs-lookup"><span data-stu-id="5e0d1-335">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

