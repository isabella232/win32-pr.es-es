---
description: Crea un nuevo servicio de sistema.
ms.assetid: 164e9065-bb0d-4c93-a9fe-c86db1ea7cb7
ms.tgt_platform: multiple
title: Método Create de la clase Win32_Service (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f23bc2a5c49a85a20765172d4c5d361a8d18316
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807928"
---
# <a name="create-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="d94ce-103">Método Create de la clase Win32_Service (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="d94ce-103">Create method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="d94ce-104">El método **crear** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuevo servicio de sistema.</span><span class="sxs-lookup"><span data-stu-id="d94ce-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="d94ce-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="d94ce-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d94ce-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d94ce-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d94ce-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d94ce-107">Syntax</span></span>


```mof
uint32 Create(
  [in] string  Name,
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a><span data-ttu-id="d94ce-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d94ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d94ce-109">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d94ce-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-110">Nombre del servicio que se va a instalar en el método **Create** .</span><span class="sxs-lookup"><span data-stu-id="d94ce-110">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="d94ce-111">La longitud de cadena máxima es de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d94ce-111">The maximum string length is 256 characters.</span></span> <span data-ttu-id="d94ce-112">La base de datos del administrador de control de servicios conserva el uso de mayúsculas y minúsculas de los caracteres, pero las comparaciones de nombres de servicio no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d94ce-112">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="d94ce-113">Las barras diagonales (/) y dos barras diagonales inversas ( \\ ) son caracteres de nombre de servicio no válidos.</span><span class="sxs-lookup"><span data-stu-id="d94ce-113">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-114">*DisplayName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d94ce-114">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-115">Nombre para mostrar del servicio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-115">Display name of the service.</span></span> <span data-ttu-id="d94ce-116">Esta cadena tiene una longitud máxima de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d94ce-116">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="d94ce-117">El nombre se conserva en las mayúsculas y minúsculas en el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="d94ce-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="d94ce-118">Las comparaciones de *displayName* siempre distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d94ce-118">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="d94ce-119">Constraints: acepta el mismo valor que el parámetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="d94ce-119">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="d94ce-120">Ejemplo: "Endisco".</span><span class="sxs-lookup"><span data-stu-id="d94ce-120">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-121">*Nombreruta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d94ce-121">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-122">Ruta de acceso completa al archivo ejecutable que implementa el servicio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-122">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="d94ce-123">Ejemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="d94ce-123">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-124">*ServiceType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d94ce-124">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-125">Tipo de servicios proporcionados a los procesos que los llaman.</span><span class="sxs-lookup"><span data-stu-id="d94ce-125">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="d94ce-126">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d94ce-126">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-127">Controlador de kernel</span><span class="sxs-lookup"><span data-stu-id="d94ce-127">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-128">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="d94ce-128">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-129">Controlador del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="d94ce-129">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-130">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="d94ce-130">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-131">Adapter (Adaptador)</span><span class="sxs-lookup"><span data-stu-id="d94ce-131">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-132">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="d94ce-132">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-133">Controlador del reconocedor</span><span class="sxs-lookup"><span data-stu-id="d94ce-133">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-134">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="d94ce-134">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-135">Proceso propio</span><span class="sxs-lookup"><span data-stu-id="d94ce-135">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-136">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="d94ce-136">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-137">Compartir proceso</span><span class="sxs-lookup"><span data-stu-id="d94ce-137">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-138">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="d94ce-138">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-139">Proceso interactivo</span><span class="sxs-lookup"><span data-stu-id="d94ce-139">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d94ce-140">*ErrorControl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d94ce-140">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-141">Gravedad del error si el método **Create** no se inicia.</span><span class="sxs-lookup"><span data-stu-id="d94ce-141">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="d94ce-142">El valor indica la acción realizada por el programa de inicio si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="d94ce-142">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="d94ce-143">El sistema registra todos los errores.</span><span class="sxs-lookup"><span data-stu-id="d94ce-143">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="d94ce-144">0</span><span class="sxs-lookup"><span data-stu-id="d94ce-144">0</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-145">No se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="d94ce-145">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-146">1</span><span class="sxs-lookup"><span data-stu-id="d94ce-146">1</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-147">Se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="d94ce-147">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-148">2</span><span class="sxs-lookup"><span data-stu-id="d94ce-148">2</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-149">El sistema se reinicia con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="d94ce-149">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-150">3</span><span class="sxs-lookup"><span data-stu-id="d94ce-150">3</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-151">El sistema intenta iniciarse con una configuración válida.</span><span class="sxs-lookup"><span data-stu-id="d94ce-151">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d94ce-152">*StartMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d94ce-152">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-153">Modo de inicio del servicio base de Windows.</span><span class="sxs-lookup"><span data-stu-id="d94ce-153">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="d94ce-154">Arranque</span><span class="sxs-lookup"><span data-stu-id="d94ce-154">Boot</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-155">Controlador de dispositivo Iniciado por el cargador del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d94ce-155">Device driver started by the operating system loader.</span></span> <span data-ttu-id="d94ce-156">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="d94ce-156">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-157">System</span><span class="sxs-lookup"><span data-stu-id="d94ce-157">System</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-158">Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d94ce-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="d94ce-159">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="d94ce-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-160">Automático</span><span class="sxs-lookup"><span data-stu-id="d94ce-160">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-161">Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="d94ce-161">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-162">Manual</span><span class="sxs-lookup"><span data-stu-id="d94ce-162">Manual</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-163">Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="d94ce-163">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-164">Disabled</span><span class="sxs-lookup"><span data-stu-id="d94ce-164">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-165">Servicio que ya no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="d94ce-165">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d94ce-166">*DesktopInteract* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d94ce-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-167">Si **es true**, el servicio puede crear o comunicarse con Windows en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-167">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-168">*StartName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d94ce-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-169">Nombre de cuenta con la que se ejecuta el servicio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-169">Account name under which the service runs.</span></span> <span data-ttu-id="d94ce-170">Dependiendo del tipo de servicio, el nombre de cuenta puede tener el \\ formato nombrededominio nombredeusuario o nombre principal de usuario (UPN) ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="d94ce-170">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="d94ce-171">El proceso de servicio se registra con una de estas dos formas cuando se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="d94ce-171">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="d94ce-172">Si la cuenta pertenece al dominio integrado,. \\ Se puede especificar el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="d94ce-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="d94ce-173">Si se especifica **null** , el servicio inicia sesión como la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="d94ce-173">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="d94ce-174">En el caso de los controladores de kernel o de nivel de sistema, *StartName* contiene el nombre de objeto del controlador (es decir, sistema de \\ archivos \\ RDR o \\ XNS del controlador \\ ) que usa el sistema de entrada y salida (e/s) para cargar el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d94ce-174">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="d94ce-175">Si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de e/s basado en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-175">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="d94ce-176">Ejemplo: DWDOM \\ admin.</span><span class="sxs-lookup"><span data-stu-id="d94ce-176">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-177">*StartPassword* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d94ce-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-178">Contraseña para el nombre de cuenta especificado por el parámetro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="d94ce-178">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="d94ce-179">Especifique **null** si no va a cambiar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="d94ce-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="d94ce-180">Especifique una cadena vacía si el servicio no tiene contraseña.</span><span class="sxs-lookup"><span data-stu-id="d94ce-180">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-181">*LoadOrderGroup* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d94ce-181">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-182">Nombre de grupo asociado al nuevo servicio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-182">Group name associated with the new service.</span></span> <span data-ttu-id="d94ce-183">Los grupos de pedidos de carga se incluyen en el registro y determinan la secuencia en la que se cargan los servicios en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d94ce-183">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="d94ce-184">Si el puntero es **null** o apunta a una cadena vacía, el servicio no pertenece a un grupo.</span><span class="sxs-lookup"><span data-stu-id="d94ce-184">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="d94ce-185">Las dependencias entre grupos deben aparecer en el parámetro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="d94ce-185">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="d94ce-186">Los servicios de la lista de grupos de orden de carga se inician en primer lugar, seguidos de los servicios de los grupos que no están en la lista de grupos de orden de carga, seguidos de los servicios que no pertenecen a un grupo.</span><span class="sxs-lookup"><span data-stu-id="d94ce-186">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="d94ce-187">El registro tiene una lista de grupos de orden de carga que se encuentran en:</span><span class="sxs-lookup"><span data-stu-id="d94ce-187">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="d94ce-188">**HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local ServiceGroupOrder</span><span class="sxs-lookup"><span data-stu-id="d94ce-188">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-189">*LoadOrderGroupDependencies* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d94ce-189">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-190">Matriz de grupos de orden de carga que deben iniciarse antes de este servicio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-190">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="d94ce-191">Cada elemento de la matriz está delimitado por **null** y la lista termina en dos valores **null** .</span><span class="sxs-lookup"><span data-stu-id="d94ce-191">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="d94ce-192">En Visual Basic o script puede pasar un objeto vbArray.</span><span class="sxs-lookup"><span data-stu-id="d94ce-192">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="d94ce-193">Si el puntero es **null** o apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="d94ce-193">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="d94ce-194">Los nombres de grupo deben ir precedidos del **\_ \_ identificador de grupo SC** (definido en el archivo Winsvc. h) para diferenciarlo de un nombre de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="d94ce-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="d94ce-195">La dependencia de un grupo significa que este servicio se puede ejecutar si se está ejecutando al menos un miembro del grupo después de un intento de iniciar todos los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="d94ce-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-196">*ServiceDependencies* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d94ce-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-197">Matriz de que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-197">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="d94ce-198">Cada elemento de la matriz está delimitado por **null** y la lista termina en dos valores **null** .</span><span class="sxs-lookup"><span data-stu-id="d94ce-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="d94ce-199">En Visual Basic o script puede pasar un objeto vbArray.</span><span class="sxs-lookup"><span data-stu-id="d94ce-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="d94ce-200">Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="d94ce-200">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="d94ce-201">La dependencia de un servicio significa que este servicio solo se puede ejecutar si se está ejecutando el servicio del que depende.</span><span class="sxs-lookup"><span data-stu-id="d94ce-201">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d94ce-202">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d94ce-202">Return value</span></span>

<span data-ttu-id="d94ce-203">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="d94ce-203">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="d94ce-204">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d94ce-204">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d94ce-205">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d94ce-205">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d94ce-206">**0**</span><span class="sxs-lookup"><span data-stu-id="d94ce-206">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-207">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d94ce-207">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-208">**1**</span><span class="sxs-lookup"><span data-stu-id="d94ce-208">**1**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-209">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d94ce-209">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-210">**2**</span><span class="sxs-lookup"><span data-stu-id="d94ce-210">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-211">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="d94ce-211">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-212">**3**</span><span class="sxs-lookup"><span data-stu-id="d94ce-212">**3**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-213">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="d94ce-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-214">**4**</span><span class="sxs-lookup"><span data-stu-id="d94ce-214">**4**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-215">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-215">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-216">**5**</span><span class="sxs-lookup"><span data-stu-id="d94ce-216">**5**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-217">El código de control solicitado no se puede enviar al servicio porque el estado de la propiedad Service (**State** de la clase [**\_ BaseService de Win32**](win32-baseservice.md) ) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="d94ce-217">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](win32-baseservice.md) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-218">**6**</span><span class="sxs-lookup"><span data-stu-id="d94ce-218">**6**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-219">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="d94ce-219">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-220">**7**</span><span class="sxs-lookup"><span data-stu-id="d94ce-220">**7**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-221">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-221">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-222">**8**</span><span class="sxs-lookup"><span data-stu-id="d94ce-222">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-223">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-223">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-224">**9**</span><span class="sxs-lookup"><span data-stu-id="d94ce-224">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-225">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-225">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-226">**10**</span><span class="sxs-lookup"><span data-stu-id="d94ce-226">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-227">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="d94ce-227">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-228">**11**</span><span class="sxs-lookup"><span data-stu-id="d94ce-228">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-229">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="d94ce-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-230">**12**</span><span class="sxs-lookup"><span data-stu-id="d94ce-230">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-231">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="d94ce-231">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-232">**13**</span><span class="sxs-lookup"><span data-stu-id="d94ce-232">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-233">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="d94ce-233">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-234">**14**</span><span class="sxs-lookup"><span data-stu-id="d94ce-234">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-235">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="d94ce-235">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-236">**15**</span><span class="sxs-lookup"><span data-stu-id="d94ce-236">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-237">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="d94ce-237">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-238">**16**</span><span class="sxs-lookup"><span data-stu-id="d94ce-238">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-239">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="d94ce-239">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-240">**17**</span><span class="sxs-lookup"><span data-stu-id="d94ce-240">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-241">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d94ce-241">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-242">**18**</span><span class="sxs-lookup"><span data-stu-id="d94ce-242">**18**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-243">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="d94ce-243">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-244">**19**</span><span class="sxs-lookup"><span data-stu-id="d94ce-244">**19**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-245">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="d94ce-245">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-246">**20**</span><span class="sxs-lookup"><span data-stu-id="d94ce-246">**20**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-247">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="d94ce-247">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-248">**21**</span><span class="sxs-lookup"><span data-stu-id="d94ce-248">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-249">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-249">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-250">**22**</span><span class="sxs-lookup"><span data-stu-id="d94ce-250">**22**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-251">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-251">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-252">**23**</span><span class="sxs-lookup"><span data-stu-id="d94ce-252">**23**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-253">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="d94ce-253">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d94ce-254">**24**</span><span class="sxs-lookup"><span data-stu-id="d94ce-254">**24**</span></span>
</dt> <dd>

<span data-ttu-id="d94ce-255">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="d94ce-255">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d94ce-256">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d94ce-256">Remarks</span></span>

<span data-ttu-id="d94ce-257">Normalmente, los servicios se instalan de una de estas dos maneras: como parte de la instalación del sistema operativo o mediante un programa de instalación proporcionado por el desarrollador del servicio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-257">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="d94ce-258">Sin embargo, es posible que algunos servicios, especialmente los creados internamente, no tengan un programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="d94ce-258">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="d94ce-259">En esos casos, puede utilizar el método **Create** para instalar los servicios mediante programación.</span><span class="sxs-lookup"><span data-stu-id="d94ce-259">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="d94ce-260">A pesar del nombre, el método Create no crea un servicio en realidad. simplemente instala un servicio existente.</span><span class="sxs-lookup"><span data-stu-id="d94ce-260">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="d94ce-261">Para usar este comando, debe copiar el archivo ejecutable del servicio en un equipo y, a continuación, usar **crear** para instalar el servicio.</span><span class="sxs-lookup"><span data-stu-id="d94ce-261">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="d94ce-262">El método **Create** es similar al método [**Change**](change-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="d94ce-262">The **Create** method is similar to the [**Change**](change-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="d94ce-263">En ambos casos, las propiedades del servicio se pasan como parámetros al método.</span><span class="sxs-lookup"><span data-stu-id="d94ce-263">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="d94ce-264">Al igual que con los parámetros que se usan con el método **Change** , el orden en el que se pasan estos parámetros es muy importante.</span><span class="sxs-lookup"><span data-stu-id="d94ce-264">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="d94ce-265">El parámetro *LoadOrderGroup* representa una agrupación de los servicios del sistema que definen las dependencias de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d94ce-265">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="d94ce-266">Los servicios deben iniciarse en el orden especificado por el grupo de orden de carga, ya que los servicios dependen entre sí.</span><span class="sxs-lookup"><span data-stu-id="d94ce-266">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="d94ce-267">Estos servicios dependientes requieren la presencia de los servicios antecedentes para que funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="d94ce-267">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="d94ce-268">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d94ce-268">Examples</span></span>

<span data-ttu-id="d94ce-269">El siguiente VBScript instala un servicio denominado DbService</span><span class="sxs-lookup"><span data-stu-id="d94ce-269">The following VBScript installs a service named DbService</span></span>


```VB
Const OWN_PROCESS = 16
Const NOT_INTERACTIVE = True
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objService = objWMIService.Get("Win32_BaseService")
errReturn = objService.Create ("DbService", "Personnel Database", _
"c:\windows\system32\db.exe", OWN_PROCESS ,2 ,"Automatic" , _
 NOT_INTERACTIVE ,".\LocalSystem" ,"")
```



## <a name="requirements"></a><span data-ttu-id="d94ce-270">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d94ce-270">Requirements</span></span>



| <span data-ttu-id="d94ce-271">Requisito</span><span class="sxs-lookup"><span data-stu-id="d94ce-271">Requirement</span></span> | <span data-ttu-id="d94ce-272">Value</span><span class="sxs-lookup"><span data-stu-id="d94ce-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d94ce-273">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d94ce-273">Minimum supported client</span></span><br/> | <span data-ttu-id="d94ce-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d94ce-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d94ce-275">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d94ce-275">Minimum supported server</span></span><br/> | <span data-ttu-id="d94ce-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d94ce-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d94ce-277">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d94ce-277">Namespace</span></span><br/>                | <span data-ttu-id="d94ce-278">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d94ce-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d94ce-279">MOF</span><span class="sxs-lookup"><span data-stu-id="d94ce-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d94ce-280"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d94ce-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d94ce-281">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d94ce-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d94ce-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d94ce-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d94ce-283">Vea también</span><span class="sxs-lookup"><span data-stu-id="d94ce-283">See also</span></span>

<dl> <dt>

<span data-ttu-id="d94ce-284">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d94ce-284">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d94ce-285">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="d94ce-285">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="d94ce-286">Tareas WMI: servicios</span><span class="sxs-lookup"><span data-stu-id="d94ce-286">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

