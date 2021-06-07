---
title: Método Create de la clase Win32_Service (Servicios de Escritorio remoto)
description: 'Método Create de la Win32_Service (Servicios de Escritorio remoto): crea un nuevo servicio del sistema.'
ms.assetid: 805754AA-B62A-4324-B289-503C42BEFA49
ms.tgt_platform: multiple
keywords:
- Crear método Servicios de Escritorio remoto
- Create method Servicios de Escritorio remoto , Win32_Service class
- Win32_Service clase Servicios de Escritorio remoto , Create (método)
topic_type:
- apiref
api_name:
- Win32_Service.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14b776d3e451d84c63be5bb61b98ed22081e1a29
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387124"
---
# <a name="create-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="004e8-106">Método Create de la clase Win32_Service (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="004e8-106">Create method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="004e8-107">El **método Create** WMI [Class](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuevo servicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="004e8-107">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="004e8-108">En este tema se usa Managed Object Format sintaxis de MOF.</span><span class="sxs-lookup"><span data-stu-id="004e8-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="004e8-109">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="004e8-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="004e8-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="004e8-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="004e8-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="004e8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="004e8-112">*Nombre* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="004e8-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="004e8-113">Nombre del servicio que se instalará en **el método Create.**</span><span class="sxs-lookup"><span data-stu-id="004e8-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="004e8-114">La longitud máxima de la cadena es de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="004e8-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="004e8-115">La base de datos del Administrador de control de servicios conserva las mayúsculas y minúsculas de los caracteres, pero las comparaciones de nombres de servicio siempre no tienen en cuenta las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="004e8-115">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="004e8-116">Las barras diagonales (/) y las barras diagonales dobles \\ \\ () son caracteres de nombre de servicio no válidos.</span><span class="sxs-lookup"><span data-stu-id="004e8-116">Forward-slashes (/) and double back-slashes (\\\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-117">*DisplayName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="004e8-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="004e8-118">Nombre para mostrar del servicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-118">Display name of the service.</span></span> <span data-ttu-id="004e8-119">Esta cadena tiene una longitud máxima de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="004e8-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="004e8-120">El nombre se conserva en el Administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="004e8-120">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="004e8-121">*Las comparaciones* de DisplayName siempre no tienen en cuenta mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="004e8-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="004e8-122">Restricciones: acepta el mismo valor que el *parámetro Name.*</span><span class="sxs-lookup"><span data-stu-id="004e8-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="004e8-123">Ejemplo: "Atdisk".</span><span class="sxs-lookup"><span data-stu-id="004e8-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="004e8-124">*PathName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="004e8-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="004e8-125">Ruta de acceso completa al archivo ejecutable que implementa el servicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="004e8-126">Ejemplo: \\ "SystemRoot \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="004e8-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="004e8-127">*ServiceType* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="004e8-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="004e8-128">Tipo de servicios proporcionados a los procesos que los llaman.</span><span class="sxs-lookup"><span data-stu-id="004e8-128">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="004e8-129">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="004e8-129">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="004e8-130">Kernel Driver</span><span class="sxs-lookup"><span data-stu-id="004e8-130">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="004e8-131">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="004e8-131">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="004e8-132">Controlador del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="004e8-132">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="004e8-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="004e8-133">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="004e8-134">Adapter (Adaptador)</span><span class="sxs-lookup"><span data-stu-id="004e8-134">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="004e8-135">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="004e8-135">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="004e8-136">Controlador de reconocedor</span><span class="sxs-lookup"><span data-stu-id="004e8-136">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="004e8-137">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="004e8-137">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="004e8-138">Proceso propio</span><span class="sxs-lookup"><span data-stu-id="004e8-138">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="004e8-139">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="004e8-139">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="004e8-140">Proceso de recurso compartido</span><span class="sxs-lookup"><span data-stu-id="004e8-140">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="004e8-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="004e8-141">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="004e8-142">Proceso interactivo</span><span class="sxs-lookup"><span data-stu-id="004e8-142">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="004e8-143">*ErrorControl* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="004e8-143">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="004e8-144">Gravedad del error si no se puede iniciar el método **Create.**</span><span class="sxs-lookup"><span data-stu-id="004e8-144">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="004e8-145">El valor indica la acción realizada por el programa de inicio si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="004e8-145">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="004e8-146">El sistema registra todos los errores.</span><span class="sxs-lookup"><span data-stu-id="004e8-146">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="004e8-147">0</span><span class="sxs-lookup"><span data-stu-id="004e8-147">0</span></span>
</dt> <dd>

<span data-ttu-id="004e8-148">No se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="004e8-148">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-149">1</span><span class="sxs-lookup"><span data-stu-id="004e8-149">1</span></span>
</dt> <dd>

<span data-ttu-id="004e8-150">Se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="004e8-150">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-151">2</span><span class="sxs-lookup"><span data-stu-id="004e8-151">2</span></span>
</dt> <dd>

<span data-ttu-id="004e8-152">El sistema se reinicia con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="004e8-152">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-153">3</span><span class="sxs-lookup"><span data-stu-id="004e8-153">3</span></span>
</dt> <dd>

<span data-ttu-id="004e8-154">El sistema intenta comenzar con una buena configuración.</span><span class="sxs-lookup"><span data-stu-id="004e8-154">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="004e8-155">*StartMode* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="004e8-155">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="004e8-156">Modo de inicio del servicio base de Windows.</span><span class="sxs-lookup"><span data-stu-id="004e8-156">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="004e8-157">Arranque</span><span class="sxs-lookup"><span data-stu-id="004e8-157">Boot</span></span>
</dt> <dd>

<span data-ttu-id="004e8-158">Controlador de dispositivo iniciado por el cargador del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="004e8-158">Device driver started by the operating system loader.</span></span> <span data-ttu-id="004e8-159">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="004e8-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-160">Sistema</span><span class="sxs-lookup"><span data-stu-id="004e8-160">System</span></span>
</dt> <dd>

<span data-ttu-id="004e8-161">Controlador de dispositivo iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="004e8-161">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="004e8-162">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="004e8-162">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-163">Automático</span><span class="sxs-lookup"><span data-stu-id="004e8-163">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="004e8-164">Servicio que el Administrador de control de servicios iniciará automáticamente durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="004e8-164">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-165">Manual</span><span class="sxs-lookup"><span data-stu-id="004e8-165">Manual</span></span>
</dt> <dd>

<span data-ttu-id="004e8-166">Servicio que debe iniciar el Administrador de control de servicios cuando un proceso llame al [**método StartService.**](win32-terminalservice-startservice.md)</span><span class="sxs-lookup"><span data-stu-id="004e8-166">Service to be started by the Service Control Manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-167">Disabled</span><span class="sxs-lookup"><span data-stu-id="004e8-167">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="004e8-168">Servicio que ya no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="004e8-168">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="004e8-169">*DesktopInteract* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="004e8-169">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="004e8-170">Si **es true,** el servicio puede crear o comunicarse con ventanas en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="004e8-170">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-171">*StartName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="004e8-171">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="004e8-172">Nombre de cuenta con el que se ejecuta el servicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-172">Account name under which the service runs.</span></span> <span data-ttu-id="004e8-173">Según el tipo de servicio, el nombre de la cuenta puede tener el formato nombreDeUsuario de NombreDeServidor o Nombre principal de \\ usuario (UPN) ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="004e8-173">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="004e8-174">El proceso de servicio se registra mediante uno de estos dos formularios cuando se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="004e8-174">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="004e8-175">Si la cuenta pertenece al dominio integrado, . \\ Se puede especificar el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="004e8-175">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="004e8-176">Si se especifica **NULL,** el servicio inicia sesión como la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="004e8-176">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="004e8-177">Para un kernel o controladores de nivel de sistema, *StartName* contiene el nombre del objeto de controlador (es decir, FileSystem Rdr o Driver Xns) que el sistema de entrada y salida \\ \\ \\ (E/S) usa para cargar el controlador de \\ dispositivo.</span><span class="sxs-lookup"><span data-stu-id="004e8-177">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="004e8-178">Si se especifica **NULL,** el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de E/S basado en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-178">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="004e8-179">Ejemplo: Administrador de \\ DWDOM.</span><span class="sxs-lookup"><span data-stu-id="004e8-179">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-180">*StartPassword* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="004e8-180">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="004e8-181">Contraseña del nombre de cuenta especificado por el *parámetro StartName.*</span><span class="sxs-lookup"><span data-stu-id="004e8-181">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="004e8-182">Especifique **NULL** si no va a cambiar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="004e8-182">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="004e8-183">Especifique una cadena vacía si el servicio no tiene contraseña.</span><span class="sxs-lookup"><span data-stu-id="004e8-183">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-184">*LoadOrderGroup* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="004e8-184">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="004e8-185">Nombre de grupo asociado al nuevo servicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-185">Group name associated with the new service.</span></span> <span data-ttu-id="004e8-186">Los grupos de orden de carga se encuentran en el Registro y determinan la secuencia en la que se cargan los servicios en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="004e8-186">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="004e8-187">Si el puntero es **NULL** o si apunta a una cadena vacía, el servicio no pertenece a un grupo.</span><span class="sxs-lookup"><span data-stu-id="004e8-187">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="004e8-188">Las dependencias entre grupos deben aparecer en *el parámetro LoadOrderGroupDependencies.*</span><span class="sxs-lookup"><span data-stu-id="004e8-188">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="004e8-189">Los servicios de la lista de grupos de ordenación de carga se inician primero, seguidos de los servicios de los grupos que no están en la lista de grupos de ordenación de carga, seguidos de los servicios que no pertenecen a un grupo.</span><span class="sxs-lookup"><span data-stu-id="004e8-189">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="004e8-190">El registro tiene una lista de grupos de pedidos de carga ubicados en:</span><span class="sxs-lookup"><span data-stu-id="004e8-190">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="004e8-191">**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="004e8-191">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="004e8-192">*LoadOrderGroupDependencies* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="004e8-192">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="004e8-193">Matriz de grupos de ordenación de carga que deben iniciarse antes de este servicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-193">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="004e8-194">Cada elemento de la matriz está delimitado por **NULL** y la lista termina con dos **valores NULL.**</span><span class="sxs-lookup"><span data-stu-id="004e8-194">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="004e8-195">En Visual Basic o script puede pasar una vbArray.</span><span class="sxs-lookup"><span data-stu-id="004e8-195">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="004e8-196">Si el puntero es **NULL o** si apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="004e8-196">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="004e8-197">Los nombres de grupo deben ir precedidos por el carácter **SC \_ GROUP \_ IDENTIFIER** (definido en el archivo Winsvc.h) para diferenciarlo de un nombre de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="004e8-197">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="004e8-198">La dependencia de un grupo significa que este servicio se puede ejecutar si al menos un miembro del grupo se está ejecutando después de un intento de iniciar todos los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="004e8-198">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-199">*ServiceDependencies* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="004e8-199">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="004e8-200">Matriz que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-200">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="004e8-201">Cada elemento de la matriz está delimitado por **NULL** y la lista termina con dos **valores NULL.**</span><span class="sxs-lookup"><span data-stu-id="004e8-201">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="004e8-202">En Visual Basic o script puede pasar una vbArray.</span><span class="sxs-lookup"><span data-stu-id="004e8-202">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="004e8-203">Si el puntero es **NULL** o si apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="004e8-203">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="004e8-204">La dependencia de un servicio significa que este servicio solo se puede ejecutar si el servicio del que depende se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="004e8-204">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="004e8-205">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="004e8-205">Return value</span></span>

<span data-ttu-id="004e8-206">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="004e8-206">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="004e8-207">Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="004e8-207">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="004e8-208">Para obtener los **valores HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="004e8-208">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="004e8-209">**0**</span><span class="sxs-lookup"><span data-stu-id="004e8-209">**0**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-210">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="004e8-210">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-211">**1**</span><span class="sxs-lookup"><span data-stu-id="004e8-211">**1**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-212">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="004e8-212">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-213">**2**</span><span class="sxs-lookup"><span data-stu-id="004e8-213">**2**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-214">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="004e8-214">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-215">**3**</span><span class="sxs-lookup"><span data-stu-id="004e8-215">**3**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-216">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="004e8-216">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-217">**4**</span><span class="sxs-lookup"><span data-stu-id="004e8-217">**4**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-218">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-218">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-219">**5**</span><span class="sxs-lookup"><span data-stu-id="004e8-219">**5**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-220">El código de control solicitado no se puede enviar al servicio porque el estado del servicio (propiedad **State** de la clase [**\_ BaseService de Win32)**](/windows/desktop/CIMWin32Prov/win32-baseservice) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="004e8-220">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-221">**6**</span><span class="sxs-lookup"><span data-stu-id="004e8-221">**6**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-222">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="004e8-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-223">**7**</span><span class="sxs-lookup"><span data-stu-id="004e8-223">**7**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-224">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-224">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-225">**8**</span><span class="sxs-lookup"><span data-stu-id="004e8-225">**8**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-226">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-226">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-227">**9**</span><span class="sxs-lookup"><span data-stu-id="004e8-227">**9**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-228">No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-228">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-229">**10**</span><span class="sxs-lookup"><span data-stu-id="004e8-229">**10**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-230">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="004e8-230">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-231">**11**</span><span class="sxs-lookup"><span data-stu-id="004e8-231">**11**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-232">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="004e8-232">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-233">**12**</span><span class="sxs-lookup"><span data-stu-id="004e8-233">**12**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-234">Se ha quitado del sistema una dependencia en la que se basa este servicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-234">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-235">**13**</span><span class="sxs-lookup"><span data-stu-id="004e8-235">**13**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-236">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="004e8-236">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-237">**14**</span><span class="sxs-lookup"><span data-stu-id="004e8-237">**14**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-238">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="004e8-238">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-239">**15**</span><span class="sxs-lookup"><span data-stu-id="004e8-239">**15**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-240">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="004e8-240">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-241">**16**</span><span class="sxs-lookup"><span data-stu-id="004e8-241">**16**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-242">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="004e8-242">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-243">**17**</span><span class="sxs-lookup"><span data-stu-id="004e8-243">**17**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-244">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="004e8-244">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-245">**18**</span><span class="sxs-lookup"><span data-stu-id="004e8-245">**18**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-246">El servicio tiene dependencias circulares cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="004e8-246">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-247">**19**</span><span class="sxs-lookup"><span data-stu-id="004e8-247">**19**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-248">Un servicio se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="004e8-248">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-249">**20**</span><span class="sxs-lookup"><span data-stu-id="004e8-249">**20**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-250">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="004e8-250">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-251">**21**</span><span class="sxs-lookup"><span data-stu-id="004e8-251">**21**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-252">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-252">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-253">**22**</span><span class="sxs-lookup"><span data-stu-id="004e8-253">**22**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-254">La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-254">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-255">**23**</span><span class="sxs-lookup"><span data-stu-id="004e8-255">**23**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-256">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="004e8-256">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="004e8-257">**24**</span><span class="sxs-lookup"><span data-stu-id="004e8-257">**24**</span></span>
</dt> <dd>

<span data-ttu-id="004e8-258">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="004e8-258">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="004e8-259">Comentarios</span><span class="sxs-lookup"><span data-stu-id="004e8-259">Remarks</span></span>

<span data-ttu-id="004e8-260">Por lo general, los servicios se instalan de dos maneras: como parte de la instalación del sistema operativo o mediante un programa de instalación proporcionado por el desarrollador del servicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-260">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="004e8-261">Sin embargo, es posible que algunos servicios, especialmente los creados de forma local, no tengan un programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="004e8-261">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="004e8-262">En esos casos, puede usar el **método Create** para instalar servicios mediante programación.</span><span class="sxs-lookup"><span data-stu-id="004e8-262">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="004e8-263">A pesar del nombre, el método Create no crea realmente un servicio; simplemente instala un servicio existente.</span><span class="sxs-lookup"><span data-stu-id="004e8-263">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="004e8-264">Para usar este comando, debe copiar el archivo ejecutable de servicio en un equipo y, a continuación, usar **Crear** para instalar el servicio.</span><span class="sxs-lookup"><span data-stu-id="004e8-264">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="004e8-265">El **método Create** es similar al método [**Change.**](win32-terminalservice-change.md)</span><span class="sxs-lookup"><span data-stu-id="004e8-265">The **Create** method is similar to the [**Change**](win32-terminalservice-change.md) method.</span></span> <span data-ttu-id="004e8-266">En ambos casos, las propiedades del servicio se pasan como parámetros al método .</span><span class="sxs-lookup"><span data-stu-id="004e8-266">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="004e8-267">Al igual que con los parámetros usados con **el método Change,** el orden en el que se pasan estos parámetros es muy importante.</span><span class="sxs-lookup"><span data-stu-id="004e8-267">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="004e8-268">El *parámetro LoadOrderGroup representa* una agrupación de servicios del sistema que definen las dependencias de ejecución.</span><span class="sxs-lookup"><span data-stu-id="004e8-268">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="004e8-269">Los servicios deben iniciarse en el orden especificado por el grupo de pedidos de carga, ya que los servicios dependen entre sí.</span><span class="sxs-lookup"><span data-stu-id="004e8-269">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="004e8-270">Estos servicios dependientes requieren la presencia de los servicios antecedentes para funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="004e8-270">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="requirements"></a><span data-ttu-id="004e8-271">Requisitos</span><span class="sxs-lookup"><span data-stu-id="004e8-271">Requirements</span></span>



| <span data-ttu-id="004e8-272">Requisito</span><span class="sxs-lookup"><span data-stu-id="004e8-272">Requirement</span></span> | <span data-ttu-id="004e8-273">Valor</span><span class="sxs-lookup"><span data-stu-id="004e8-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="004e8-274">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="004e8-274">Minimum supported client</span></span><br/> | <span data-ttu-id="004e8-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="004e8-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="004e8-276">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="004e8-276">Minimum supported server</span></span><br/> | <span data-ttu-id="004e8-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="004e8-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="004e8-278">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="004e8-278">Namespace</span></span><br/>                | <span data-ttu-id="004e8-279">\\TerminalServices de CIMv2 \\ raíz</span><span class="sxs-lookup"><span data-stu-id="004e8-279">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="004e8-280">MOF</span><span class="sxs-lookup"><span data-stu-id="004e8-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="004e8-281"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="004e8-281"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="004e8-282">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="004e8-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="004e8-283"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="004e8-283"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="004e8-284">Vea también</span><span class="sxs-lookup"><span data-stu-id="004e8-284">See also</span></span>

<dl> <dt>

[<span data-ttu-id="004e8-285">**Servicio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="004e8-285">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="004e8-286">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="004e8-286">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="004e8-287">**TerminalService de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="004e8-287">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="004e8-288">Tareas wmi: servicios</span><span class="sxs-lookup"><span data-stu-id="004e8-288">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

