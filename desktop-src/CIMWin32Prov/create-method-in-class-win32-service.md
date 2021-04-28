---
description: 'Método Create de la Win32_Service (proveedores WMI CIMWin32): crea un nuevo servicio del sistema.'
ms.assetid: 164e9065-bb0d-4c93-a9fe-c86db1ea7cb7
ms.tgt_platform: multiple
title: Método Create de la clase Win32_Service (proveedores WMI CIMWin32)
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
ms.openlocfilehash: 71bc0f4edb879fc4a51a012bc53db67031056f47
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089694"
---
# <a name="create-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="28e04-103">Método Create de la clase Win32_Service (proveedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="28e04-103">Create method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="28e04-104">El **método de** clase Create [WMI](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuevo servicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="28e04-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="28e04-105">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="28e04-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="28e04-106">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="28e04-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="28e04-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28e04-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="28e04-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28e04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28e04-109">*Nombre* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="28e04-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e04-110">Nombre del servicio que se instalará en el **método Create.**</span><span class="sxs-lookup"><span data-stu-id="28e04-110">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="28e04-111">La longitud máxima de la cadena es de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="28e04-111">The maximum string length is 256 characters.</span></span> <span data-ttu-id="28e04-112">La base de datos de Service Control Manager conserva las mayúsculas y minúsculas de los caracteres, pero las comparaciones de nombres de servicio siempre no tienen en cuenta las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="28e04-112">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="28e04-113">Las barras diagonales (/) y las dos barras diagonales () son \\ caracteres de nombre de servicio no válidos.</span><span class="sxs-lookup"><span data-stu-id="28e04-113">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-114">*DisplayName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="28e04-114">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e04-115">Nombre para mostrar del servicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-115">Display name of the service.</span></span> <span data-ttu-id="28e04-116">Esta cadena tiene una longitud máxima de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="28e04-116">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="28e04-117">El nombre se conserva entre mayúsculas y minúsculas en Service Control Manager.</span><span class="sxs-lookup"><span data-stu-id="28e04-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="28e04-118">*Las comparaciones* de DisplayName siempre no tienen en cuenta las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="28e04-118">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="28e04-119">Restricciones: acepta el mismo valor que el *parámetro Name.*</span><span class="sxs-lookup"><span data-stu-id="28e04-119">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="28e04-120">Ejemplo: "Atdisk".</span><span class="sxs-lookup"><span data-stu-id="28e04-120">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="28e04-121">*PathName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="28e04-121">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e04-122">Ruta de acceso completa al archivo ejecutable que implementa el servicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-122">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="28e04-123">Ejemplo: " \\ SystemRoot \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="28e04-123">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="28e04-124">*ServiceType* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="28e04-124">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e04-125">Tipo de servicios proporcionados a los procesos que los llaman.</span><span class="sxs-lookup"><span data-stu-id="28e04-125">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="28e04-126">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="28e04-126">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="28e04-127">Kernel Driver</span><span class="sxs-lookup"><span data-stu-id="28e04-127">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="28e04-128">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="28e04-128">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="28e04-129">Controlador del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="28e04-129">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="28e04-130">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="28e04-130">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="28e04-131">Adapter (Adaptador)</span><span class="sxs-lookup"><span data-stu-id="28e04-131">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="28e04-132">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="28e04-132">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="28e04-133">Controlador de reconocedor</span><span class="sxs-lookup"><span data-stu-id="28e04-133">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="28e04-134">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="28e04-134">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="28e04-135">Proceso propio</span><span class="sxs-lookup"><span data-stu-id="28e04-135">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="28e04-136">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="28e04-136">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="28e04-137">Proceso de recurso compartido</span><span class="sxs-lookup"><span data-stu-id="28e04-137">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="28e04-138">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="28e04-138">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="28e04-139">Proceso interactivo</span><span class="sxs-lookup"><span data-stu-id="28e04-139">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="28e04-140">*ErrorControl* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="28e04-140">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e04-141">Gravedad del error si el **método Create** no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="28e04-141">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="28e04-142">El valor indica la acción realizada por el programa de inicio si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="28e04-142">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="28e04-143">El sistema registra todos los errores.</span><span class="sxs-lookup"><span data-stu-id="28e04-143">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="28e04-144">0</span><span class="sxs-lookup"><span data-stu-id="28e04-144">0</span></span>
</dt> <dd>

<span data-ttu-id="28e04-145">No se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="28e04-145">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-146">1</span><span class="sxs-lookup"><span data-stu-id="28e04-146">1</span></span>
</dt> <dd>

<span data-ttu-id="28e04-147">Se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="28e04-147">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-148">2</span><span class="sxs-lookup"><span data-stu-id="28e04-148">2</span></span>
</dt> <dd>

<span data-ttu-id="28e04-149">El sistema se reinicia con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="28e04-149">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-150">3</span><span class="sxs-lookup"><span data-stu-id="28e04-150">3</span></span>
</dt> <dd>

<span data-ttu-id="28e04-151">El sistema intenta comenzar con una buena configuración.</span><span class="sxs-lookup"><span data-stu-id="28e04-151">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="28e04-152">*StartMode* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="28e04-152">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e04-153">Modo de inicio del servicio base de Windows.</span><span class="sxs-lookup"><span data-stu-id="28e04-153">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="28e04-154">Arranque</span><span class="sxs-lookup"><span data-stu-id="28e04-154">Boot</span></span>
</dt> <dd>

<span data-ttu-id="28e04-155">Controlador de dispositivo iniciado por el cargador del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="28e04-155">Device driver started by the operating system loader.</span></span> <span data-ttu-id="28e04-156">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="28e04-156">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-157">Sistema</span><span class="sxs-lookup"><span data-stu-id="28e04-157">System</span></span>
</dt> <dd>

<span data-ttu-id="28e04-158">Controlador de dispositivo iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="28e04-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="28e04-159">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="28e04-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-160">Automático</span><span class="sxs-lookup"><span data-stu-id="28e04-160">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="28e04-161">Servicio que el Administrador de control de servicios iniciará automáticamente durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="28e04-161">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-162">Manual</span><span class="sxs-lookup"><span data-stu-id="28e04-162">Manual</span></span>
</dt> <dd>

<span data-ttu-id="28e04-163">Servicio que debe iniciar el Administrador de control de servicios cuando un proceso llame al [**método StartService.**](startservice-method-in-class-win32-service.md)</span><span class="sxs-lookup"><span data-stu-id="28e04-163">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-164">Disabled</span><span class="sxs-lookup"><span data-stu-id="28e04-164">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="28e04-165">Servicio que ya no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="28e04-165">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="28e04-166">*DesktopInteract* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="28e04-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e04-167">Si **es true,** el servicio puede crear o comunicarse con ventanas en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="28e04-167">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-168">*StartName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="28e04-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e04-169">Nombre de cuenta con el que se ejecuta el servicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-169">Account name under which the service runs.</span></span> <span data-ttu-id="28e04-170">Según el tipo de servicio, el nombre de la cuenta puede tener el formato nombredeusuario de nombre de dominio o nombre \\ principal de usuario (UPN) ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="28e04-170">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="28e04-171">El proceso de servicio se registra mediante uno de estos dos formularios cuando se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="28e04-171">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="28e04-172">Si la cuenta pertenece al dominio integrado, . \\ Se puede especificar el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="28e04-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="28e04-173">Si se especifica **NULL,** el servicio se inicia sesión como la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="28e04-173">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="28e04-174">Para un kernel o controladores de nivel de sistema, *StartName* contiene el nombre del objeto de controlador (es decir, FileSystem Rdr o Driver Xns) que el sistema de entrada y salida \\ \\ \\ (E/S) usa para cargar el controlador de \\ dispositivo.</span><span class="sxs-lookup"><span data-stu-id="28e04-174">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="28e04-175">Si se especifica **NULL,** el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de E/S en función del nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-175">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="28e04-176">Ejemplo: Administrador de \\ DWDOM.</span><span class="sxs-lookup"><span data-stu-id="28e04-176">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-177">*StartPassword* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="28e04-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e04-178">Contraseña en el nombre de cuenta especificado por el *parámetro StartName.*</span><span class="sxs-lookup"><span data-stu-id="28e04-178">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="28e04-179">Especifique **NULL** si no va a cambiar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="28e04-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="28e04-180">Especifique una cadena vacía si el servicio no tiene contraseña.</span><span class="sxs-lookup"><span data-stu-id="28e04-180">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-181">*LoadOrderGroup* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="28e04-181">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e04-182">Nombre de grupo asociado al nuevo servicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-182">Group name associated with the new service.</span></span> <span data-ttu-id="28e04-183">Los grupos de orden de carga se encuentran en el Registro y determinan la secuencia en la que se cargan los servicios en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="28e04-183">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="28e04-184">Si el puntero es **NULL** o si apunta a una cadena vacía, el servicio no pertenece a un grupo.</span><span class="sxs-lookup"><span data-stu-id="28e04-184">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="28e04-185">Las dependencias entre grupos deben aparecer en *el parámetro LoadOrderGroupDependencies.*</span><span class="sxs-lookup"><span data-stu-id="28e04-185">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="28e04-186">Los servicios de la lista de grupos de ordenación de carga se inician primero, seguidos de los servicios de los grupos que no están en la lista de grupos de ordenación de carga, seguidos de los servicios que no pertenecen a un grupo.</span><span class="sxs-lookup"><span data-stu-id="28e04-186">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="28e04-187">El registro tiene una lista de grupos de pedidos de carga ubicados en:</span><span class="sxs-lookup"><span data-stu-id="28e04-187">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="28e04-188">**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="28e04-188">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="28e04-189">*LoadOrderGroupDependencies* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="28e04-189">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e04-190">Matriz de grupos de ordenación de carga que deben iniciarse antes de este servicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-190">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="28e04-191">Cada elemento de la matriz está delimitado por **NULL** y la lista termina con dos **valores NULL.**</span><span class="sxs-lookup"><span data-stu-id="28e04-191">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="28e04-192">En Visual Basic o script puede pasar una vbArray.</span><span class="sxs-lookup"><span data-stu-id="28e04-192">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="28e04-193">Si el puntero es **NULL o** si apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="28e04-193">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="28e04-194">Los nombres de grupo deben ir precedidos por el carácter **SC \_ GROUP \_ IDENTIFIER** (definido en el archivo Winsvc.h) para diferenciarlo de un nombre de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="28e04-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="28e04-195">La dependencia de un grupo significa que este servicio se puede ejecutar si al menos un miembro del grupo se está ejecutando después de un intento de iniciar todos los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="28e04-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-196">*ServiceDependencies* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="28e04-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e04-197">Matriz que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-197">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="28e04-198">Cada elemento de la matriz está delimitado por **NULL** y la lista termina con dos **valores NULL.**</span><span class="sxs-lookup"><span data-stu-id="28e04-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="28e04-199">En Visual Basic o script puede pasar una vbArray.</span><span class="sxs-lookup"><span data-stu-id="28e04-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="28e04-200">Si el puntero es **NULL** o si apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="28e04-200">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="28e04-201">La dependencia de un servicio significa que este servicio solo se puede ejecutar si el servicio del que depende se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="28e04-201">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28e04-202">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28e04-202">Return value</span></span>

<span data-ttu-id="28e04-203">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="28e04-203">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="28e04-204">Para obtener códigos de error adicionales, [**vea Constantes de error WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="28e04-204">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="28e04-205">Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="28e04-205">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="28e04-206">**0**</span><span class="sxs-lookup"><span data-stu-id="28e04-206">**0**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-207">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="28e04-207">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-208">**1**</span><span class="sxs-lookup"><span data-stu-id="28e04-208">**1**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-209">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="28e04-209">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-210">**2**</span><span class="sxs-lookup"><span data-stu-id="28e04-210">**2**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-211">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="28e04-211">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-212">**3**</span><span class="sxs-lookup"><span data-stu-id="28e04-212">**3**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-213">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="28e04-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-214">**4**</span><span class="sxs-lookup"><span data-stu-id="28e04-214">**4**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-215">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-215">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-216">**5**</span><span class="sxs-lookup"><span data-stu-id="28e04-216">**5**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-217">El código de control solicitado no se puede enviar al servicio porque el estado del servicio (propiedad **State** de la clase [**\_ BaseService win32)**](win32-baseservice.md) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="28e04-217">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](win32-baseservice.md) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-218">**6**</span><span class="sxs-lookup"><span data-stu-id="28e04-218">**6**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-219">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="28e04-219">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-220">**7**</span><span class="sxs-lookup"><span data-stu-id="28e04-220">**7**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-221">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-221">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-222">**8**</span><span class="sxs-lookup"><span data-stu-id="28e04-222">**8**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-223">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-223">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-224">**9**</span><span class="sxs-lookup"><span data-stu-id="28e04-224">**9**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-225">No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-225">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-226">**10**</span><span class="sxs-lookup"><span data-stu-id="28e04-226">**10**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-227">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="28e04-227">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-228">**11**</span><span class="sxs-lookup"><span data-stu-id="28e04-228">**11**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-229">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="28e04-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-230">**12**</span><span class="sxs-lookup"><span data-stu-id="28e04-230">**12**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-231">Se ha quitado del sistema una dependencia en la que se basa este servicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-231">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-232">**13**</span><span class="sxs-lookup"><span data-stu-id="28e04-232">**13**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-233">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="28e04-233">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-234">**14**</span><span class="sxs-lookup"><span data-stu-id="28e04-234">**14**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-235">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="28e04-235">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-236">**15**</span><span class="sxs-lookup"><span data-stu-id="28e04-236">**15**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-237">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="28e04-237">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-238">**16**</span><span class="sxs-lookup"><span data-stu-id="28e04-238">**16**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-239">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="28e04-239">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-240">**17**</span><span class="sxs-lookup"><span data-stu-id="28e04-240">**17**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-241">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="28e04-241">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-242">**18**</span><span class="sxs-lookup"><span data-stu-id="28e04-242">**18**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-243">El servicio tiene dependencias circulares cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="28e04-243">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-244">**19**</span><span class="sxs-lookup"><span data-stu-id="28e04-244">**19**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-245">Un servicio se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="28e04-245">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-246">**20**</span><span class="sxs-lookup"><span data-stu-id="28e04-246">**20**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-247">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="28e04-247">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-248">**21**</span><span class="sxs-lookup"><span data-stu-id="28e04-248">**21**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-249">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-249">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-250">**22**</span><span class="sxs-lookup"><span data-stu-id="28e04-250">**22**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-251">La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-251">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-252">**23**</span><span class="sxs-lookup"><span data-stu-id="28e04-252">**23**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-253">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="28e04-253">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="28e04-254">**24**</span><span class="sxs-lookup"><span data-stu-id="28e04-254">**24**</span></span>
</dt> <dd>

<span data-ttu-id="28e04-255">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="28e04-255">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28e04-256">Comentarios</span><span class="sxs-lookup"><span data-stu-id="28e04-256">Remarks</span></span>

<span data-ttu-id="28e04-257">Por lo general, los servicios se instalan de una de estas dos maneras: como parte de la instalación del sistema operativo o mediante un programa de instalación proporcionado por el desarrollador del servicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-257">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="28e04-258">Sin embargo, es posible que algunos servicios, especialmente los creados de forma local, no tengan un programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="28e04-258">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="28e04-259">En esos casos, puede usar el **método Create** para instalar servicios mediante programación.</span><span class="sxs-lookup"><span data-stu-id="28e04-259">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="28e04-260">A pesar del nombre, el método Create no crea realmente un servicio; simplemente instala un servicio existente.</span><span class="sxs-lookup"><span data-stu-id="28e04-260">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="28e04-261">Para usar este comando, debe copiar el archivo ejecutable de servicio en un equipo y, a continuación, usar **Crear** para instalar el servicio.</span><span class="sxs-lookup"><span data-stu-id="28e04-261">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="28e04-262">El **método Create** es similar al método [**Change.**](change-method-in-class-win32-service.md)</span><span class="sxs-lookup"><span data-stu-id="28e04-262">The **Create** method is similar to the [**Change**](change-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="28e04-263">En ambos casos, las propiedades del servicio se pasan como parámetros al método .</span><span class="sxs-lookup"><span data-stu-id="28e04-263">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="28e04-264">Al igual que con los parámetros usados con **el método Change,** el orden en el que se pasan estos parámetros es muy importante.</span><span class="sxs-lookup"><span data-stu-id="28e04-264">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="28e04-265">El *parámetro LoadOrderGroup representa* una agrupación de servicios del sistema que definen las dependencias de ejecución.</span><span class="sxs-lookup"><span data-stu-id="28e04-265">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="28e04-266">Los servicios deben iniciarse en el orden especificado por el grupo de pedidos de carga, ya que los servicios dependen entre sí.</span><span class="sxs-lookup"><span data-stu-id="28e04-266">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="28e04-267">Estos servicios dependientes requieren la presencia de los servicios antecedentes para funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="28e04-267">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="28e04-268">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="28e04-268">Examples</span></span>

<span data-ttu-id="28e04-269">El siguiente VBScript instala un servicio denominado DbService.</span><span class="sxs-lookup"><span data-stu-id="28e04-269">The following VBScript installs a service named DbService</span></span>


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



## <a name="requirements"></a><span data-ttu-id="28e04-270">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28e04-270">Requirements</span></span>



| <span data-ttu-id="28e04-271">Requisito</span><span class="sxs-lookup"><span data-stu-id="28e04-271">Requirement</span></span> | <span data-ttu-id="28e04-272">Valor</span><span class="sxs-lookup"><span data-stu-id="28e04-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28e04-273">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28e04-273">Minimum supported client</span></span><br/> | <span data-ttu-id="28e04-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28e04-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="28e04-275">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28e04-275">Minimum supported server</span></span><br/> | <span data-ttu-id="28e04-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28e04-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="28e04-277">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="28e04-277">Namespace</span></span><br/>                | <span data-ttu-id="28e04-278">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="28e04-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="28e04-279">MOF</span><span class="sxs-lookup"><span data-stu-id="28e04-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28e04-280"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="28e04-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="28e04-281">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28e04-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28e04-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28e04-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28e04-283">Consulte también</span><span class="sxs-lookup"><span data-stu-id="28e04-283">See also</span></span>

<dl> <dt>

<span data-ttu-id="28e04-284">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28e04-284">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="28e04-285">**Servicio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="28e04-285">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="28e04-286">Tareas wmi: servicios</span><span class="sxs-lookup"><span data-stu-id="28e04-286">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

