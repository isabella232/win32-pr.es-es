---
description: Modifica un servicio de Win32 \_ .
ms.assetid: b32753c5-8fcf-44ee-a95f-e4f6076e0f28
ms.tgt_platform: multiple
title: Método de cambio de la clase Win32_Service (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 321b27239114fc86861c0360d507db6c8c520a9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539094"
---
# <a name="change-method-of-the-win32_service-class-mbnapih"></a><span data-ttu-id="06927-103">Método de cambio de la clase Win32_Service (Mbnapi. h)</span><span class="sxs-lookup"><span data-stu-id="06927-103">Change method of the Win32_Service class (Mbnapi.h)</span></span>

<span data-ttu-id="06927-104">El método de clase **Change** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) modifica un [**\_ servicio de Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="06927-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_Service**](win32-service.md).</span></span>

<span data-ttu-id="06927-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="06927-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="06927-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="06927-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="06927-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06927-107">Syntax</span></span>


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
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a><span data-ttu-id="06927-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06927-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06927-109">*DisplayName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06927-109">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06927-110">Nombre para mostrar del servicio.</span><span class="sxs-lookup"><span data-stu-id="06927-110">The display name of the service.</span></span> <span data-ttu-id="06927-111">Esta cadena tiene una longitud máxima de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="06927-111">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="06927-112">El nombre se conserva en las mayúsculas y minúsculas en el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="06927-112">The name is case- preserved in the service control manager.</span></span> <span data-ttu-id="06927-113">Las comparaciones de *displayName* siempre distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="06927-113">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="06927-114">Constraints: acepta el mismo valor que la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="06927-114">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="06927-115">Ejemplo, "Endisco".</span><span class="sxs-lookup"><span data-stu-id="06927-115">Example, "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="06927-116">*Nombreruta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06927-116">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06927-117">Ruta de acceso completa al archivo ejecutable que implementa el servicio, por ejemplo, " \\ raízDelSistema \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="06927-117">The fully qualified path to the executable file that implements the service, for example, "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="06927-118">*ServiceType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06927-118">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06927-119">Tipo de servicios proporcionados a los procesos que los llaman.</span><span class="sxs-lookup"><span data-stu-id="06927-119">The type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="06927-120">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="06927-120">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="06927-121">Controlador de kernel</span><span class="sxs-lookup"><span data-stu-id="06927-121">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="06927-122">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="06927-122">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="06927-123">Controlador del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="06927-123">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="06927-124">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="06927-124">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="06927-125">Adapter (Adaptador)</span><span class="sxs-lookup"><span data-stu-id="06927-125">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="06927-126">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="06927-126">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="06927-127">Controlador del reconocedor</span><span class="sxs-lookup"><span data-stu-id="06927-127">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="06927-128">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="06927-128">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="06927-129">Proceso propio</span><span class="sxs-lookup"><span data-stu-id="06927-129">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="06927-130">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="06927-130">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="06927-131">Compartir proceso</span><span class="sxs-lookup"><span data-stu-id="06927-131">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="06927-132">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="06927-132">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="06927-133">Proceso interactivo</span><span class="sxs-lookup"><span data-stu-id="06927-133">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="06927-134">*ErrorControl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06927-134">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06927-135">Gravedad del error si este servicio no se inicia durante el inicio.</span><span class="sxs-lookup"><span data-stu-id="06927-135">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="06927-136">El valor indica la acción realizada por el programa de inicio si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="06927-136">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="06927-137">El sistema registra todos los errores.</span><span class="sxs-lookup"><span data-stu-id="06927-137">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="06927-138"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Omitir** (0)</span><span class="sxs-lookup"><span data-stu-id="06927-138"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="06927-139">No se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="06927-139">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="06927-140"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="06927-140"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="06927-141">Normal.</span><span class="sxs-lookup"><span data-stu-id="06927-141">Normal.</span></span> <span data-ttu-id="06927-142">Se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="06927-142">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="06927-143"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)</span><span class="sxs-lookup"><span data-stu-id="06927-143"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="06927-144">El sistema se reinicia con la última configuración válida.</span><span class="sxs-lookup"><span data-stu-id="06927-144">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="06927-145"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="06927-145"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="06927-146">El sistema intenta reiniciarse con una configuración válida.</span><span class="sxs-lookup"><span data-stu-id="06927-146">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="06927-147">*StartMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06927-147">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06927-148">Modo de inicio del servicio base de Windows.</span><span class="sxs-lookup"><span data-stu-id="06927-148">Start mode of the Windows base service.</span></span> <span data-ttu-id="06927-149">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="06927-149">For more information, see the Remarks section.</span></span>

<dt>

<span data-ttu-id="06927-150">Arranque</span><span class="sxs-lookup"><span data-stu-id="06927-150">Boot</span></span>
</dt> <dd>

<span data-ttu-id="06927-151">Controlador de dispositivo Iniciado por el cargador del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="06927-151">Device driver started by the operating system loader.</span></span> <span data-ttu-id="06927-152">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="06927-152">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="06927-153">System</span><span class="sxs-lookup"><span data-stu-id="06927-153">System</span></span>
</dt> <dd>

<span data-ttu-id="06927-154">Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="06927-154">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="06927-155">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="06927-155">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="06927-156">Automático</span><span class="sxs-lookup"><span data-stu-id="06927-156">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="06927-157">Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="06927-157">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="06927-158">Manual</span><span class="sxs-lookup"><span data-stu-id="06927-158">Manual</span></span>
</dt> <dd>

<span data-ttu-id="06927-159">Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="06927-159">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="06927-160">Disabled</span><span class="sxs-lookup"><span data-stu-id="06927-160">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="06927-161">Servicio que ya no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="06927-161">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="06927-162">*DesktopInteract* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06927-162">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06927-163">Si **es true**, el servicio puede crear o comunicarse con una ventana en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="06927-163">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="06927-164">*StartName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06927-164">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06927-165">Nombre de la cuenta con la que se ejecuta el servicio.</span><span class="sxs-lookup"><span data-stu-id="06927-165">Account name the service runs under.</span></span> <span data-ttu-id="06927-166">Dependiendo del tipo de servicio, el nombre de la cuenta puede tener el formato nombreDeDominio \\ nombreDeUsuario o. \\ Nombre.</span><span class="sxs-lookup"><span data-stu-id="06927-166">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="06927-167">El proceso de servicio se registrará con una de estas dos formas cuando se ejecute.</span><span class="sxs-lookup"><span data-stu-id="06927-167">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="06927-168">Si la cuenta pertenece al dominio integrado,. \\ Se puede especificar el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="06927-168">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="06927-169">Si se especifica **null** , el servicio se iniciará sesión como la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="06927-169">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="06927-170">En el caso de los controladores de kernel o de nivel de sistema, *StartName* contiene el nombre de objeto del controlador (es decir, sistema de \\ archivos \\ RDR o \\ XNS del controlador \\ ) que usa el sistema de entrada y salida (e/s) para cargar el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="06927-170">For kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="06927-171">Si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de e/s basado en el nombre del servicio, por ejemplo, "DWDOM \\ admin".</span><span class="sxs-lookup"><span data-stu-id="06927-171">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name, for example, "DWDOM\\Admin".</span></span>

<span data-ttu-id="06927-172">También puede usar el formato de nombre principal de usuario (UPN) para especificar **StartName**, por ejemplo, *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="06927-172">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="06927-173">*StartPassword* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06927-173">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06927-174">Contraseña para el nombre de cuenta especificado por el parámetro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="06927-174">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="06927-175">Especifique **null** si no va a cambiar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="06927-175">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="06927-176">Especifique una cadena vacía si el servicio no tiene contraseña.</span><span class="sxs-lookup"><span data-stu-id="06927-176">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="06927-177">Al cambiar un servicio de un sistema local a una red, o de una red a un sistema local, *StartPassword* debe ser una cadena vacía ("") y no **null**.</span><span class="sxs-lookup"><span data-stu-id="06927-177">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="06927-178">*LoadOrderGroup* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06927-178">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06927-179">Nombre del grupo al que está asociado.</span><span class="sxs-lookup"><span data-stu-id="06927-179">Group name that it is associated with.</span></span> <span data-ttu-id="06927-180">Los grupos de pedidos de carga se incluyen en el registro del sistema y determinan la secuencia en la que se cargan los servicios en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="06927-180">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="06927-181">Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no pertenece a un grupo.</span><span class="sxs-lookup"><span data-stu-id="06927-181">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="06927-182">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="06927-182">For more information, see the Remarks section.</span></span>

<span data-ttu-id="06927-183">Las dependencias entre grupos deben aparecer en el parámetro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="06927-183">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="06927-184">Los servicios de la lista de grupos de orden de carga se inician en primer lugar, seguidos de los servicios de los grupos que no están en la lista de grupos de orden de carga, seguidos de los servicios que no pertenecen a un grupo.</span><span class="sxs-lookup"><span data-stu-id="06927-184">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="06927-185">El registro del sistema tiene una lista de grupos de orden de carga que se encuentran en:</span><span class="sxs-lookup"><span data-stu-id="06927-185">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="06927-186">**HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local ServiceGroupOrder</span><span class="sxs-lookup"><span data-stu-id="06927-186">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="06927-187">*LoadOrderGroupDependencies* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06927-187">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06927-188">Lista de grupos de orden de carga que deben iniciarse antes de que se inicie este servicio.</span><span class="sxs-lookup"><span data-stu-id="06927-188">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="06927-189">La matriz termina en **null**.</span><span class="sxs-lookup"><span data-stu-id="06927-189">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="06927-190">Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="06927-190">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="06927-191">Los nombres de grupo deben ir precedidos del **\_ \_ identificador de grupo SC** (definido en el archivo Winsvc. h) para diferenciarlos de los nombres de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="06927-191">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names because services and service groups share the same namespace.</span></span> <span data-ttu-id="06927-192">La dependencia de un grupo significa que este servicio se puede ejecutar si se está ejecutando al menos un miembro del grupo después de un intento de iniciar todos los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="06927-192">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="06927-193">*ServiceDependencies* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06927-193">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06927-194">Lista que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio.</span><span class="sxs-lookup"><span data-stu-id="06927-194">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="06927-195">La matriz termina en **null**.</span><span class="sxs-lookup"><span data-stu-id="06927-195">The array is doubly **NULL**-terminated.</span></span> <span data-ttu-id="06927-196">Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="06927-196">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="06927-197">La dependencia de un servicio indica que este servicio solo se puede ejecutar si se está ejecutando el servicio del que depende.</span><span class="sxs-lookup"><span data-stu-id="06927-197">Dependency on a service indicates that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06927-198">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06927-198">Return value</span></span>

<span data-ttu-id="06927-199">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="06927-199">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="06927-200">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="06927-200">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="06927-201">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="06927-201">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="06927-202">**Success**</span><span class="sxs-lookup"><span data-stu-id="06927-202">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="06927-203">0</span><span class="sxs-lookup"><span data-stu-id="06927-203">0</span></span>

<span data-ttu-id="06927-204">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="06927-204">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="06927-205">**No compatible**</span><span class="sxs-lookup"><span data-stu-id="06927-205">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="06927-206">1</span><span class="sxs-lookup"><span data-stu-id="06927-206">1</span></span>

<span data-ttu-id="06927-207">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="06927-207">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="06927-208">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="06927-208">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="06927-209">2</span><span class="sxs-lookup"><span data-stu-id="06927-209">2</span></span>

<span data-ttu-id="06927-210">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="06927-210">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="06927-211">**Servicios dependientes en ejecución**</span><span class="sxs-lookup"><span data-stu-id="06927-211">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="06927-212">3</span><span class="sxs-lookup"><span data-stu-id="06927-212">3</span></span>

<span data-ttu-id="06927-213">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="06927-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="06927-214">**Control de servicio no válido**</span><span class="sxs-lookup"><span data-stu-id="06927-214">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="06927-215">4</span><span class="sxs-lookup"><span data-stu-id="06927-215">4</span></span>

<span data-ttu-id="06927-216">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="06927-216">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="06927-217">**El servicio no puede aceptar el control**</span><span class="sxs-lookup"><span data-stu-id="06927-217">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="06927-218">5</span><span class="sxs-lookup"><span data-stu-id="06927-218">5</span></span>

<span data-ttu-id="06927-219">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="06927-219">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="06927-220">**Servicio no activo**</span><span class="sxs-lookup"><span data-stu-id="06927-220">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="06927-221">6</span><span class="sxs-lookup"><span data-stu-id="06927-221">6</span></span>

<span data-ttu-id="06927-222">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="06927-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="06927-223">**Tiempo de espera de solicitud de servicio**</span><span class="sxs-lookup"><span data-stu-id="06927-223">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="06927-224">7</span><span class="sxs-lookup"><span data-stu-id="06927-224">7</span></span>

<span data-ttu-id="06927-225">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="06927-225">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="06927-226">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="06927-226">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="06927-227">8</span><span class="sxs-lookup"><span data-stu-id="06927-227">8</span></span>

<span data-ttu-id="06927-228">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="06927-228">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="06927-229">**Ruta de acceso no encontrada**</span><span class="sxs-lookup"><span data-stu-id="06927-229">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="06927-230">9</span><span class="sxs-lookup"><span data-stu-id="06927-230">9</span></span>

<span data-ttu-id="06927-231">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="06927-231">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="06927-232">**El servicio ya se está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="06927-232">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="06927-233">10</span><span class="sxs-lookup"><span data-stu-id="06927-233">10</span></span>

<span data-ttu-id="06927-234">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="06927-234">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="06927-235">**Base de datos de servicio bloqueada**</span><span class="sxs-lookup"><span data-stu-id="06927-235">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="06927-236">11</span><span class="sxs-lookup"><span data-stu-id="06927-236">11</span></span>

<span data-ttu-id="06927-237">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="06927-237">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="06927-238">**Dependencia de servicio eliminada**</span><span class="sxs-lookup"><span data-stu-id="06927-238">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="06927-239">12</span><span class="sxs-lookup"><span data-stu-id="06927-239">12</span></span>

<span data-ttu-id="06927-240">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="06927-240">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="06927-241">**Error de dependencia de servicio**</span><span class="sxs-lookup"><span data-stu-id="06927-241">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="06927-242">13</span><span class="sxs-lookup"><span data-stu-id="06927-242">13</span></span>

<span data-ttu-id="06927-243">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="06927-243">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="06927-244">**Servicio deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="06927-244">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="06927-245">14</span><span class="sxs-lookup"><span data-stu-id="06927-245">14</span></span>

<span data-ttu-id="06927-246">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="06927-246">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="06927-247">**Error de inicio de sesión de servicio**</span><span class="sxs-lookup"><span data-stu-id="06927-247">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="06927-248">15</span><span class="sxs-lookup"><span data-stu-id="06927-248">15</span></span>

<span data-ttu-id="06927-249">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="06927-249">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="06927-250">**Servicio marcado para eliminación**</span><span class="sxs-lookup"><span data-stu-id="06927-250">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="06927-251">16</span><span class="sxs-lookup"><span data-stu-id="06927-251">16</span></span>

<span data-ttu-id="06927-252">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="06927-252">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="06927-253">**Servicio sin subproceso**</span><span class="sxs-lookup"><span data-stu-id="06927-253">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="06927-254">17</span><span class="sxs-lookup"><span data-stu-id="06927-254">17</span></span>

<span data-ttu-id="06927-255">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="06927-255">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="06927-256">**Estado dependencia circular**</span><span class="sxs-lookup"><span data-stu-id="06927-256">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="06927-257">18</span><span class="sxs-lookup"><span data-stu-id="06927-257">18</span></span>

<span data-ttu-id="06927-258">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="06927-258">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="06927-259">**Estado nombre duplicado**</span><span class="sxs-lookup"><span data-stu-id="06927-259">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="06927-260">19</span><span class="sxs-lookup"><span data-stu-id="06927-260">19</span></span>

<span data-ttu-id="06927-261">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="06927-261">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="06927-262">**Estado nombre no válido**</span><span class="sxs-lookup"><span data-stu-id="06927-262">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="06927-263">20</span><span class="sxs-lookup"><span data-stu-id="06927-263">20</span></span>

<span data-ttu-id="06927-264">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="06927-264">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="06927-265">**Estado parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="06927-265">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="06927-266">21</span><span class="sxs-lookup"><span data-stu-id="06927-266">21</span></span>

<span data-ttu-id="06927-267">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="06927-267">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="06927-268">**Estado cuenta de servicio no válida**</span><span class="sxs-lookup"><span data-stu-id="06927-268">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="06927-269">22</span><span class="sxs-lookup"><span data-stu-id="06927-269">22</span></span>

<span data-ttu-id="06927-270">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="06927-270">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="06927-271">**El servicio de estado existe**</span><span class="sxs-lookup"><span data-stu-id="06927-271">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="06927-272">23</span><span class="sxs-lookup"><span data-stu-id="06927-272">23</span></span>

<span data-ttu-id="06927-273">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="06927-273">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="06927-274">**Servicio ya pausado**</span><span class="sxs-lookup"><span data-stu-id="06927-274">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="06927-275">24</span><span class="sxs-lookup"><span data-stu-id="06927-275">24</span></span>

<span data-ttu-id="06927-276">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="06927-276">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="06927-277">**Otros**</span><span class="sxs-lookup"><span data-stu-id="06927-277">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="06927-278">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="06927-278">25 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06927-279">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06927-279">Remarks</span></span>

<span data-ttu-id="06927-280">Cuando se inicia un equipo, también se inician todos los servicios de inicio automático.</span><span class="sxs-lookup"><span data-stu-id="06927-280">When a computer starts, all the autostart services also start.</span></span> <span data-ttu-id="06927-281">En ocasiones, es posible que uno de estos servicios no se inicie junto con el equipo.</span><span class="sxs-lookup"><span data-stu-id="06927-281">On occasion, one of these services might fail to start along with the computer.</span></span> <span data-ttu-id="06927-282">Cuando se produce un error en un servicio durante el inicio del sistema, el equipo toma medidas según el valor del código de control de errores del servicio.</span><span class="sxs-lookup"><span data-stu-id="06927-282">When a service fails during system startup, the computer takes action based on the value of the service error control code.</span></span>

<span data-ttu-id="06927-283">la mayoría de los servicios se instalan con el código de control de errores normal.</span><span class="sxs-lookup"><span data-stu-id="06927-283">most services are installed using the Normal error control code.</span></span> <span data-ttu-id="06927-284">Algunas de las excepciones, que se instalan con el código de error ignore, incluyen:</span><span class="sxs-lookup"><span data-stu-id="06927-284">A few of the exceptions, which are installed using the Ignore error code, include:</span></span>

-   <span data-ttu-id="06927-285">Servicio de replicación de archivos</span><span class="sxs-lookup"><span data-stu-id="06927-285">File Replication Service</span></span>
-   <span data-ttu-id="06927-286">Tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="06927-286">Smart Card</span></span>
-   <span data-ttu-id="06927-287">Inicio de sesión secundario</span><span class="sxs-lookup"><span data-stu-id="06927-287">Secondary Logon</span></span>
-   <span data-ttu-id="06927-288">WMI</span><span class="sxs-lookup"><span data-stu-id="06927-288">WMI</span></span>

<span data-ttu-id="06927-289">En el caso de los servicios que se instalan con el código de error ignore, no se proporciona ninguna notificación al usuario de que se ha producido un error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="06927-289">For the services installed using the Ignore error code, no notification is given to the user that the service has failed.</span></span> <span data-ttu-id="06927-290">Si prefiere recibir una notificación en pantalla de que no se pudo iniciar un servicio, puede usar WMI para cambiar el código de control de errores.</span><span class="sxs-lookup"><span data-stu-id="06927-290">If you prefer on-screen notification that a service could not start, you can use WMI to change the error control code.</span></span> <span data-ttu-id="06927-291">Los códigos de control de errores solo se aplican al inicio del equipo; los códigos de control de errores no se usan si detiene e intenta reiniciar un servicio después de que el equipo se esté ejecutando.</span><span class="sxs-lookup"><span data-stu-id="06927-291">Error control codes apply only to computer startup; error control codes are not used if you stop and then attempt to restart a service after the computer is running.</span></span>

<span data-ttu-id="06927-292">En alguna ocasión, es posible que necesite cambiar la cuenta en la que se ejecuta un servicio determinado.</span><span class="sxs-lookup"><span data-stu-id="06927-292">On occasion, you might need to change the account under which a given service runs.</span></span> <span data-ttu-id="06927-293">Por ejemplo, puede ejecutar un servicio en una cuenta administrativa.</span><span class="sxs-lookup"><span data-stu-id="06927-293">For example, you might run a service under an administrative account.</span></span> <span data-ttu-id="06927-294">Como esto puede crear una vulnerabilidad de seguridad, puede cambiar el servicio a una cuenta con menos privilegios.</span><span class="sxs-lookup"><span data-stu-id="06927-294">Because this can create a security vulnerability, you might switch the service to an account with fewer privileges.</span></span> <span data-ttu-id="06927-295">Como alternativa, es posible que los servicios se ejecuten en una cuenta que esté a punto de eliminarse, o puede que desee asegurarse de que, en todos los servidores, determinados servicios se ejecuten en determinadas cuentas.</span><span class="sxs-lookup"><span data-stu-id="06927-295">Alternatively, you might have services running under an account that is about to be deleted, or you might want to ensure that, on all your servers, certain services run under certain accounts.</span></span> <span data-ttu-id="06927-296">Puede utilizar el método de **cambio** de la clase de [**\_ servicio Win32**](win32-service.md) para configurar los servicios de para que se ejecuten en una cuenta de usuario especificada.</span><span class="sxs-lookup"><span data-stu-id="06927-296">You can use the **Change** method of the [**Win32\_Service**](win32-service.md) class to configure services to run under a specified user account.</span></span> <span data-ttu-id="06927-297">Al seleccionar una cuenta, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="06927-297">When selecting an account, keep in mind the following:</span></span>

-   <span data-ttu-id="06927-298">La cuenta que se usa como cuenta de servicio debe tener el derecho de iniciar sesión como servicio.</span><span class="sxs-lookup"><span data-stu-id="06927-298">The account being used as a service account must have the right to log on as a service.</span></span> <span data-ttu-id="06927-299">Este derecho se puede conceder mediante directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="06927-299">This right can be granted by using Group Policy.</span></span>
-   <span data-ttu-id="06927-300">La cuenta que se usa como cuenta de servicio no debe ser miembro de un grupo local, de dominio o de administradores de organización.</span><span class="sxs-lookup"><span data-stu-id="06927-300">The account being used as a service account should not be a member of a local, domain, or enterprise Administrators group.</span></span>
-   <span data-ttu-id="06927-301">Cada instancia de un servicio se debe ejecutar con una cuenta de usuario única.</span><span class="sxs-lookup"><span data-stu-id="06927-301">Each instance of a service should run under a unique user account.</span></span> <span data-ttu-id="06927-302">Esto proporciona seguridad adicional y habilita la auditoría de instancias de servicio individuales.</span><span class="sxs-lookup"><span data-stu-id="06927-302">This provides additional security, and enables the auditing of individual service instances.</span></span>
-   <span data-ttu-id="06927-303">Si el servicio es interactivo, el servicio debe ejecutarse en la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="06927-303">If the service is interactive, then the service must run under the LocalSystem account.</span></span>

    <span data-ttu-id="06927-304">Se requiere LocalSystem porque solo una estación de ventana (WinSta0) puede ser visible e interactiva a la vez.</span><span class="sxs-lookup"><span data-stu-id="06927-304">LocalSystem is required because only one window station (WinSta0) can be visible and interactive at a time.</span></span> <span data-ttu-id="06927-305">Si un servicio se ejecuta en una cuenta distinta de LocalSystem, se ejecuta en la estación de ventana de servicio-0x03e7 $ \\ predeterminada, que es una ventana invisible.</span><span class="sxs-lookup"><span data-stu-id="06927-305">If a service runs under an account other than LocalSystem, it runs in the Service-0x03e7$\\Default window station, which is an invisible window.</span></span> <span data-ttu-id="06927-306">Los servicios que se ejecutan en esta estación de ventana no pueden recibir entradas ni mostrar resultados.</span><span class="sxs-lookup"><span data-stu-id="06927-306">Services running in this window station cannot receive input or display output.</span></span>

<span data-ttu-id="06927-307">Cuando asigna una cuenta a un servicio, el SCM requiere la contraseña correcta para esa cuenta antes de realizar la asignación.</span><span class="sxs-lookup"><span data-stu-id="06927-307">When you assign an account to a service, the SCM requires the correct password for that account before it makes the assignment.</span></span> <span data-ttu-id="06927-308">Si proporciona una contraseña incorrecta, el SCM rechazará la cuenta.</span><span class="sxs-lookup"><span data-stu-id="06927-308">If you supply an incorrect password, the SCM rejects the account.</span></span> <span data-ttu-id="06927-309">Si configura una cuenta de servicio con la cuenta LocalSystem, LocalService o NetworkService, no es necesario que proporcione una contraseña de cuenta porque estas cuentas no tienen contraseñas.</span><span class="sxs-lookup"><span data-stu-id="06927-309">If you configure a service account using the LocalSystem, LocalService, or NetworkService account, you do not need to supply an account password because these accounts do not have passwords.</span></span>

<span data-ttu-id="06927-310">El SCM almacena la contraseña de la cuenta en la base de datos de servicios.</span><span class="sxs-lookup"><span data-stu-id="06927-310">The SCM stores the account password in the services database.</span></span> <span data-ttu-id="06927-311">Sin embargo, una vez asignada la contraseña, el SCM no garantiza que la contraseña almacenada en la base de datos de servicios y la contraseña asignada a la cuenta de usuario en Active Directory sigan coincidiendo.</span><span class="sxs-lookup"><span data-stu-id="06927-311">After the password is assigned, however, the SCM does not ensure that the password stored in the services database and the password assigned to the user account in Active Directory continue to match.</span></span> <span data-ttu-id="06927-312">Por consiguiente, podría producirse una situación similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="06927-312">Consequently, a situation similar to the following could occur:</span></span>

-   <span data-ttu-id="06927-313">Puede configurar un servicio para que se ejecute en una cuenta de usuario determinada.</span><span class="sxs-lookup"><span data-stu-id="06927-313">You configure a service to run under a particular user account.</span></span>
-   <span data-ttu-id="06927-314">El servicio se inicia con esa cuenta mediante la contraseña de la cuenta actual.</span><span class="sxs-lookup"><span data-stu-id="06927-314">The service starts up under that account by using the current account password.</span></span>
-   <span data-ttu-id="06927-315">Puede cambiar la contraseña de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="06927-315">You change the password for the user account.</span></span>
-   <span data-ttu-id="06927-316">El servicio continúa ejecutándose.</span><span class="sxs-lookup"><span data-stu-id="06927-316">The service continues to run.</span></span> <span data-ttu-id="06927-317">Sin embargo, si el servicio se detiene, no puede reiniciarlo porque el SCM sigue usando la contraseña antigua no válida.</span><span class="sxs-lookup"><span data-stu-id="06927-317">However, if the service stops, you cannot restart it because the SCM continues to use the old, invalid password.</span></span> <span data-ttu-id="06927-318">El cambio de la contraseña en Active Directory no cambia la contraseña almacenada en la base de datos de servicios.</span><span class="sxs-lookup"><span data-stu-id="06927-318">Changing the password in Active Directory does not change the password stored in the services database.</span></span>

<span data-ttu-id="06927-319">Si ejecuta servicios en cuentas de usuario normales, deberá actualizar esas contraseñas de servicio cada vez que cambie la contraseña de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="06927-319">If you run services under regular user accounts, you need to update those service passwords each time the user account password changes.</span></span> <span data-ttu-id="06927-320">Esto puede llevar mucho tiempo si no está seguro de qué servicios se están ejecutando en esa cuenta o qué equipos tienen servicios en ejecución en esa cuenta.</span><span class="sxs-lookup"><span data-stu-id="06927-320">This can be particularly time-consuming if you are not sure which services are running under that account or which computers have services running under that account.</span></span> <span data-ttu-id="06927-321">Afortunadamente, puede usar WMI para comprobar las cuentas de servicio en todos los equipos y, si es necesario, cambiar la contraseña de la cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="06927-321">Fortunately, you can use WMI to check the service accounts on all your computers and, if necessary, change the service account password.</span></span>

<span data-ttu-id="06927-322">El [**parámetro \_ LoadOrderGroup de Win32**](win32-loadordergroup.md) representa un grupo de servicios del sistema que definen las dependencias de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="06927-322">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="06927-323">Los servicios deben iniciarse en el orden especificado por el grupo de orden de carga, ya que los servicios dependen entre sí.</span><span class="sxs-lookup"><span data-stu-id="06927-323">The services must be initiated in the order specified by the Load Order Group because the services depend on each other.</span></span> <span data-ttu-id="06927-324">Estos servicios dependientes requieren la presencia de los servicios antecedentes para que funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="06927-324">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="06927-325">Para cambiar un servicio de un servicio de red a un sistema local, los parámetros *StartName* y *StartPassword* deben tener los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="06927-325">To change a service from a network service to a local system the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="06927-326">Para cambiar un servicio de un servicio de sistema local a una red, los parámetros *StartName* y *StartPassword* deben tener los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="06927-326">To change a service from a local system service to a network the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a><span data-ttu-id="06927-327">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="06927-327">Examples</span></span>

<span data-ttu-id="06927-328">El siguiente VBScript cambia la cuenta de servicio para que los servicios se ejecuten con una cuenta de usuario especificada en LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="06927-328">The following VBScript changes the service account for services from running under a specified user account to LocalSystem.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change( , , , , , , ".\LocalSystem" , "")
Next
```



<span data-ttu-id="06927-329">El siguiente VBScript cambia la contraseña de la cuenta de servicio para todos los scripts que se ejecutan en netsvc</span><span class="sxs-lookup"><span data-stu-id="06927-329">The following VBScript changes the service account password for all scripts running under Netsvc</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a><span data-ttu-id="06927-330">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06927-330">Requirements</span></span>



| <span data-ttu-id="06927-331">Requisito</span><span class="sxs-lookup"><span data-stu-id="06927-331">Requirement</span></span> | <span data-ttu-id="06927-332">Value</span><span class="sxs-lookup"><span data-stu-id="06927-332">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06927-333">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06927-333">Minimum supported client</span></span><br/> | <span data-ttu-id="06927-334">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06927-334">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06927-335">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06927-335">Minimum supported server</span></span><br/> | <span data-ttu-id="06927-336">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06927-336">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06927-337">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="06927-337">Namespace</span></span><br/>                | <span data-ttu-id="06927-338">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="06927-338">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="06927-339">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06927-339">Header</span></span><br/>                   | <dl> <span data-ttu-id="06927-340"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="06927-340"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="06927-341">MOF</span><span class="sxs-lookup"><span data-stu-id="06927-341">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06927-342"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06927-342"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="06927-343">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="06927-343">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06927-344"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06927-344"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06927-345">Vea también</span><span class="sxs-lookup"><span data-stu-id="06927-345">See also</span></span>

<dl> <dt>

<span data-ttu-id="06927-346">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="06927-346">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="06927-347">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="06927-347">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="06927-348">Tareas WMI: servicios</span><span class="sxs-lookup"><span data-stu-id="06927-348">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

