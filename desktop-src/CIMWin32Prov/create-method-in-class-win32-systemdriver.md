---
description: Crea un nuevo servicio administrado por el controlador del sistema.
ms.assetid: 212c88eb-f26d-4b07-b8fe-8508050c97fc
ms.tgt_platform: multiple
title: Método Create de la clase Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a4ae14243582ea1239e8cc68c1e1d5464339a45b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153569"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="4e12c-103">Método Create de la \_ clase Win32 SystemDriver</span><span class="sxs-lookup"><span data-stu-id="4e12c-103">Create method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="4e12c-104">El método **crear** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuevo servicio administrado por el controlador del sistema.</span><span class="sxs-lookup"><span data-stu-id="4e12c-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new service managed by the system driver.</span></span> <span data-ttu-id="4e12c-105">El *parámetro \_ LoadOrderGroup de Win32* representa una agrupación de los servicios del sistema que definen las dependencias de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4e12c-105">The *Win32\_LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="4e12c-106">Los servicios deben iniciarse en el orden especificado por el grupo de orden de carga, ya que los servicios dependen entre sí.</span><span class="sxs-lookup"><span data-stu-id="4e12c-106">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="4e12c-107">Estos servicios dependientes requieren la presencia de los servicios antecedentes para que funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="4e12c-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="4e12c-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4e12c-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4e12c-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4e12c-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4e12c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e12c-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="4e12c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e12c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e12c-112">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4e12c-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-113">Nombre del servicio que se va a instalar en el método **Create** .</span><span class="sxs-lookup"><span data-stu-id="4e12c-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="4e12c-114">La longitud de cadena máxima es de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4e12c-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="4e12c-115">La base de datos del administrador de control de servicios conserva el uso de mayúsculas y minúsculas de los caracteres, pero las comparaciones de nombres de servicio no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4e12c-115">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="4e12c-116">Las barras diagonales (/) y dos barras diagonales inversas ( \\ ) son caracteres de nombre de servicio no válidos.</span><span class="sxs-lookup"><span data-stu-id="4e12c-116">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-117">*DisplayName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e12c-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-118">Nombre para mostrar del servicio.</span><span class="sxs-lookup"><span data-stu-id="4e12c-118">Display name of the service.</span></span> <span data-ttu-id="4e12c-119">Esta cadena tiene una longitud máxima de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4e12c-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="4e12c-120">El nombre se conserva en las mayúsculas y minúsculas en el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="4e12c-120">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="4e12c-121">Las comparaciones de *displayName* siempre distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4e12c-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="4e12c-122">Constraints: acepta el mismo valor que el parámetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="4e12c-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="4e12c-123">Ejemplo: "Endisco".</span><span class="sxs-lookup"><span data-stu-id="4e12c-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-124">*Nombreruta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e12c-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-125">Ruta de acceso completa al archivo ejecutable que implementa el servicio.</span><span class="sxs-lookup"><span data-stu-id="4e12c-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="4e12c-126">Ejemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="4e12c-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-127">*ServiceType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e12c-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-128">Tipo de servicios proporcionados a los procesos que los llaman.</span><span class="sxs-lookup"><span data-stu-id="4e12c-128">Type of services provided to the processes that call them.</span></span>

<dt>

<span data-ttu-id="4e12c-129">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4e12c-129">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-130">Controlador de kernel</span><span class="sxs-lookup"><span data-stu-id="4e12c-130">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-131">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="4e12c-131">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-132">Controlador del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="4e12c-132">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="4e12c-133">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-134">Adapter (Adaptador)</span><span class="sxs-lookup"><span data-stu-id="4e12c-134">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-135">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="4e12c-135">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-136">Controlador del reconocedor</span><span class="sxs-lookup"><span data-stu-id="4e12c-136">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-137">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="4e12c-137">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-138">Proceso propio</span><span class="sxs-lookup"><span data-stu-id="4e12c-138">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-139">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="4e12c-139">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-140">Compartir proceso</span><span class="sxs-lookup"><span data-stu-id="4e12c-140">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="4e12c-141">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-142">Proceso interactivo</span><span class="sxs-lookup"><span data-stu-id="4e12c-142">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4e12c-143">*ErrorControl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e12c-143">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-144">Gravedad del error si el método **Create** no se inicia.</span><span class="sxs-lookup"><span data-stu-id="4e12c-144">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="4e12c-145">Este valor indica la acción realizada por el programa de inicio si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="4e12c-145">This value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="4e12c-146">El sistema registra todos los errores.</span><span class="sxs-lookup"><span data-stu-id="4e12c-146">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="4e12c-147">0</span><span class="sxs-lookup"><span data-stu-id="4e12c-147">0</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-148">Omitir</span><span class="sxs-lookup"><span data-stu-id="4e12c-148">"Ignore"</span></span>

<span data-ttu-id="4e12c-149">No se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="4e12c-149">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-150">1</span><span class="sxs-lookup"><span data-stu-id="4e12c-150">1</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-151">"Normal"</span><span class="sxs-lookup"><span data-stu-id="4e12c-151">"Normal"</span></span>

<span data-ttu-id="4e12c-152">Se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="4e12c-152">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-153">2</span><span class="sxs-lookup"><span data-stu-id="4e12c-153">2</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-154">Fuertes</span><span class="sxs-lookup"><span data-stu-id="4e12c-154">"Severe"</span></span>

<span data-ttu-id="4e12c-155">El sistema se reinicia con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="4e12c-155">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-156">3</span><span class="sxs-lookup"><span data-stu-id="4e12c-156">3</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-157">Suma</span><span class="sxs-lookup"><span data-stu-id="4e12c-157">"Critical"</span></span>

<span data-ttu-id="4e12c-158">El sistema intenta iniciarse con una configuración válida.</span><span class="sxs-lookup"><span data-stu-id="4e12c-158">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4e12c-159">*StartMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e12c-159">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-160">Modo de inicio del servicio base de Windows.</span><span class="sxs-lookup"><span data-stu-id="4e12c-160">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="4e12c-161"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Arranque**</span><span class="sxs-lookup"><span data-stu-id="4e12c-161"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="4e12c-162">Controlador de dispositivo Iniciado por el cargador del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4e12c-162">Device driver started by the operating system loader.</span></span> <span data-ttu-id="4e12c-163">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="4e12c-163">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="4e12c-164"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Integrado**</span><span class="sxs-lookup"><span data-stu-id="4e12c-164"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="4e12c-165">Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4e12c-165">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="4e12c-166">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="4e12c-166">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="4e12c-167"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automático**</span><span class="sxs-lookup"><span data-stu-id="4e12c-167"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="4e12c-168">Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="4e12c-168">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="4e12c-169"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span><span class="sxs-lookup"><span data-stu-id="4e12c-169"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="4e12c-170">Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="4e12c-170">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4e12c-171"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disponible**</span><span class="sxs-lookup"><span data-stu-id="4e12c-171"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="4e12c-172">Servicio que ya no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="4e12c-172">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4e12c-173">*DesktopInteract* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e12c-173">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-174">Si **es true**, el servicio puede crear o comunicarse con las ventanas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="4e12c-174">If **true**, the service can create or communicate with the windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-175">*StartName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e12c-175">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-176">Nombre de cuenta con la que se ejecuta el servicio.</span><span class="sxs-lookup"><span data-stu-id="4e12c-176">Account name under which the service runs.</span></span> <span data-ttu-id="4e12c-177">Dependiendo del tipo de servicio, el nombre de cuenta puede tener el \\ formato nombrededominio nombredeusuario o nombre principal de usuario (UPN) ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="4e12c-177">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="4e12c-178">El proceso de servicio se registra con una de estas dos formas cuando se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="4e12c-178">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="4e12c-179">Si la cuenta pertenece al dominio integrado,. \\ Se puede especificar el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="4e12c-179">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="4e12c-180">Si se especifica **null** , el servicio inicia sesión como la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="4e12c-180">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="4e12c-181">En el caso de los controladores de kernel o de nivel de sistema, *StartName* contiene el nombre de objeto del controlador (es decir, sistema de \\ archivos \\ RDR o \\ XNS del controlador \\ ) que usa el sistema de entrada y salida (e/s) para cargar el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e12c-181">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="4e12c-182">Si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de e/s basado en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="4e12c-182">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="4e12c-183">Ejemplo: DWDOM \\ admin</span><span class="sxs-lookup"><span data-stu-id="4e12c-183">Example: DWDOM\\Admin</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-184">*StartPassword* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e12c-184">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-185">Contraseña para el nombre de cuenta especificado por el parámetro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="4e12c-185">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="4e12c-186">Especifique **null** si no va a cambiar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="4e12c-186">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="4e12c-187">Especifique una cadena vacía si el servicio no tiene contraseña.</span><span class="sxs-lookup"><span data-stu-id="4e12c-187">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-188">*LoadOrderGroup* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e12c-188">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-189">Nombre de grupo asociado al nuevo servicio.</span><span class="sxs-lookup"><span data-stu-id="4e12c-189">Group name associated with the new service.</span></span> <span data-ttu-id="4e12c-190">Los grupos de pedidos de carga se incluyen en el registro y determinan la secuencia en la que se cargan los servicios en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4e12c-190">Load order groups are contained in the registry and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="4e12c-191">Si el puntero es **null** o apunta a una cadena vacía, el servicio no pertenece a un grupo.</span><span class="sxs-lookup"><span data-stu-id="4e12c-191">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="4e12c-192">Las dependencias entre grupos deben aparecer en el parámetro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="4e12c-192">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="4e12c-193">Los servicios de la lista de grupos de orden de carga se inician en primer lugar, seguidos de los servicios de los grupos que no están en la lista de grupos de orden de carga, seguidos de los servicios que no pertenecen a un grupo.</span><span class="sxs-lookup"><span data-stu-id="4e12c-193">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="4e12c-194">El registro tiene una lista de grupos de orden de carga que se encuentran en:</span><span class="sxs-lookup"><span data-stu-id="4e12c-194">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="4e12c-195">**HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local ServiceGroupOrder</span><span class="sxs-lookup"><span data-stu-id="4e12c-195">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-196">*LoadOrderGroupDependencies* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e12c-196">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-197">Matriz de grupos de orden de carga que deben iniciarse antes de este servicio.</span><span class="sxs-lookup"><span data-stu-id="4e12c-197">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="4e12c-198">Cada elemento de la matriz está delimitado por **null** y la lista termina en dos valores **null** .</span><span class="sxs-lookup"><span data-stu-id="4e12c-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="4e12c-199">En Visual Basic o script puede pasar un objeto vbArray.</span><span class="sxs-lookup"><span data-stu-id="4e12c-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="4e12c-200">Si el puntero es **null** o apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="4e12c-200">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="4e12c-201">Los nombres de grupo deben ir precedidos del **\_ \_ identificador de grupo SC** (definido en el archivo Winsvc. h) para diferenciarlo de un nombre de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="4e12c-201">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="4e12c-202">La dependencia de un grupo significa que este servicio se puede ejecutar si se está ejecutando al menos un miembro del grupo después de un intento de iniciar todos los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="4e12c-202">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="4e12c-203">*ServiceDependencies* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e12c-203">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e12c-204">Una matriz que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio.</span><span class="sxs-lookup"><span data-stu-id="4e12c-204">An array that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="4e12c-205">Cada elemento de la matriz está delimitado por **null** y la lista termina en dos valores **null** .</span><span class="sxs-lookup"><span data-stu-id="4e12c-205">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="4e12c-206">En Visual Basic o script puede pasar un objeto vbArray.</span><span class="sxs-lookup"><span data-stu-id="4e12c-206">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="4e12c-207">Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="4e12c-207">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="4e12c-208">La dependencia de un servicio significa que este servicio solo se puede ejecutar si se está ejecutando el servicio del que depende.</span><span class="sxs-lookup"><span data-stu-id="4e12c-208">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e12c-209">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e12c-209">Return value</span></span>

<span data-ttu-id="4e12c-210">Devuelve un valor de 0 (cero) si el servicio se creó correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="4e12c-210">Returns a value of 0 (zero) if the service was successfully created, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e12c-211">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e12c-211">Requirements</span></span>



| <span data-ttu-id="4e12c-212">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e12c-212">Requirement</span></span> | <span data-ttu-id="4e12c-213">Value</span><span class="sxs-lookup"><span data-stu-id="4e12c-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e12c-214">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e12c-214">Minimum supported client</span></span><br/> | <span data-ttu-id="4e12c-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e12c-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e12c-216">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e12c-216">Minimum supported server</span></span><br/> | <span data-ttu-id="4e12c-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e12c-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e12c-218">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4e12c-218">Namespace</span></span><br/>                | <span data-ttu-id="4e12c-219">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4e12c-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e12c-220">MOF</span><span class="sxs-lookup"><span data-stu-id="4e12c-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e12c-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e12c-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e12c-222">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e12c-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e12c-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e12c-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e12c-224">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e12c-224">See also</span></span>

<dl> <dt>

<span data-ttu-id="4e12c-225">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4e12c-225">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4e12c-226">**Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="4e12c-226">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

