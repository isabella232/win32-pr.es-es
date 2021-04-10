---
description: Crea un nuevo servicio.
ms.assetid: e000b896-3b49-4650-b706-548592cfe721
ms.tgt_platform: multiple
title: Método Create de la clase Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c8115ed3d9795720796b5f944c11a519ff366983
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153046"
---
# <a name="create-method-of-the-win32_baseservice-class"></a><span data-ttu-id="8e118-103">Método Create de la \_ clase Win32 BaseService</span><span class="sxs-lookup"><span data-stu-id="8e118-103">Create method of the Win32\_BaseService class</span></span>

<span data-ttu-id="8e118-104">El método **crear** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuevo servicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new service.</span></span> <span data-ttu-id="8e118-105">El parámetro *LoadOrderGroup* representa una agrupación de los servicios del sistema que definen las dependencias de ejecución.</span><span class="sxs-lookup"><span data-stu-id="8e118-105">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="8e118-106">Los servicios deben iniciarse en el orden especificado por el grupo de orden de carga, ya que los servicios dependen entre sí.</span><span class="sxs-lookup"><span data-stu-id="8e118-106">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="8e118-107">Estos servicios dependientes requieren la presencia de los servicios antecedentes para que funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="8e118-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="8e118-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="8e118-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8e118-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8e118-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e118-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e118-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="8e118-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e118-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e118-112">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8e118-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e118-113">Nombre del servicio que se va a instalar en el método **Create** .</span><span class="sxs-lookup"><span data-stu-id="8e118-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="8e118-114">La longitud de cadena máxima es de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8e118-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="8e118-115">La base de datos del administrador de control de servicios conserva el uso de mayúsculas y minúsculas de los caracteres, pero las comparaciones de nombres de servicio no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8e118-115">The service control manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="8e118-116">Las barras diagonales (/) y dos barras diagonales inversas ( \\ ) son caracteres de nombre de servicio no válidos.</span><span class="sxs-lookup"><span data-stu-id="8e118-116">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-117">*DisplayName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e118-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e118-118">Nombre para mostrar del servicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-118">Display name of the service.</span></span> <span data-ttu-id="8e118-119">Esta cadena tiene una longitud máxima de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8e118-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="8e118-120">El nombre se conserva en las mayúsculas y minúsculas en el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="8e118-120">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="8e118-121">Las comparaciones de *displayName* siempre distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8e118-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="8e118-122">Constraints: acepta el mismo valor que el parámetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="8e118-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="8e118-123">Ejemplo: "Endisco".</span><span class="sxs-lookup"><span data-stu-id="8e118-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="8e118-124">*Nombreruta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e118-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e118-125">Ruta de acceso completa al archivo ejecutable que implementa el servicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="8e118-126">Ejemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="8e118-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="8e118-127">*ServiceType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e118-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e118-128">Tipo de servicios proporcionados a los procesos que los llaman.</span><span class="sxs-lookup"><span data-stu-id="8e118-128">Type of services provided to processes that call them.</span></span> <span data-ttu-id="8e118-129">El valor es un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="8e118-129">The value is a bitmap.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="8e118-130"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Controlador de kernel** (1)</span><span class="sxs-lookup"><span data-stu-id="8e118-130"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Driver** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="8e118-131"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Controlador del sistema de archivos** (2)</span><span class="sxs-lookup"><span data-stu-id="8e118-131"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**File System Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="8e118-132"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adaptador** (4)</span><span class="sxs-lookup"><span data-stu-id="8e118-132"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="8e118-133"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Controlador de reconocedor** (8)</span><span class="sxs-lookup"><span data-stu-id="8e118-133"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Recognizer Driver** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="8e118-134"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Proceso propio** (16)</span><span class="sxs-lookup"><span data-stu-id="8e118-134"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Own Process** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="8e118-135"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Proceso de uso compartido** (32)</span><span class="sxs-lookup"><span data-stu-id="8e118-135"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Share Process** (32)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="8e118-136">256</span><span class="sxs-lookup"><span data-stu-id="8e118-136">256</span></span>
</dt> <dd>

<span data-ttu-id="8e118-137">Proceso interactivo</span><span class="sxs-lookup"><span data-stu-id="8e118-137">Interactive Process</span></span>

</dd> <dt>




</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="8e118-138">*ErrorControl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e118-138">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e118-139">Gravedad del error si el método **Create** no se inicia.</span><span class="sxs-lookup"><span data-stu-id="8e118-139">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="8e118-140">El valor indica la acción realizada por el programa de inicio si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="8e118-140">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="8e118-141">El sistema registra todos los errores.</span><span class="sxs-lookup"><span data-stu-id="8e118-141">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="8e118-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Omitir** (0)</span><span class="sxs-lookup"><span data-stu-id="8e118-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8e118-143">No se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="8e118-143">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="8e118-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="8e118-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8e118-145">Se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="8e118-145">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="8e118-146"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)</span><span class="sxs-lookup"><span data-stu-id="8e118-146"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8e118-147">El sistema se reinicia con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="8e118-147">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="8e118-148"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="8e118-148"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8e118-149">El sistema intenta iniciarse con una configuración válida.</span><span class="sxs-lookup"><span data-stu-id="8e118-149">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8e118-150">*StartMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e118-150">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e118-151">Modo de inicio del servicio base de Windows.</span><span class="sxs-lookup"><span data-stu-id="8e118-151">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="8e118-152"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicio de arranque** ("arranque")</span><span class="sxs-lookup"><span data-stu-id="8e118-152"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="8e118-153">Controlador de dispositivo Iniciado por el cargador del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8e118-153">Device driver started by the operating system loader.</span></span> <span data-ttu-id="8e118-154">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="8e118-154">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="8e118-155"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Inicio del sistema** ("System")</span><span class="sxs-lookup"><span data-stu-id="8e118-155"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="8e118-156">Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8e118-156">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="8e118-157">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="8e118-157">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="8e118-158"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Inicio automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="8e118-158"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="8e118-159">Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e118-159">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="8e118-160"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Inicio** de la demanda ("manual")</span><span class="sxs-lookup"><span data-stu-id="8e118-160"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="8e118-161">Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="8e118-161">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8e118-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("deshabilitado")</span><span class="sxs-lookup"><span data-stu-id="8e118-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="8e118-163">Servicio que ya no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="8e118-163">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8e118-164">*DesktopInteract* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e118-164">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e118-165">Si **es true**, el servicio puede crear o comunicarse con Windows en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="8e118-165">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-166">*StartName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e118-166">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e118-167">Nombre de cuenta con la que se ejecuta el servicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-167">Account name under which the service runs.</span></span> <span data-ttu-id="8e118-168">Dependiendo del tipo de servicio, el nombre de la cuenta puede tener el formato "nombreDeDominio \\ nombreDeUsuario".</span><span class="sxs-lookup"><span data-stu-id="8e118-168">Depending on the service type, the account name may be in the form of "DomainName\\Username".</span></span> <span data-ttu-id="8e118-169">El proceso de servicio se registra con una de estas dos formas cuando se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="8e118-169">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="8e118-170">Si la cuenta pertenece al dominio integrado, ". \\ Se puede especificar username.</span><span class="sxs-lookup"><span data-stu-id="8e118-170">If the account belongs to the built-in domain, ".\\Username" can be specified.</span></span> <span data-ttu-id="8e118-171">Si se especifica **null** , el servicio inicia sesión como la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="8e118-171">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="8e118-172">En el caso de los controladores de kernel o de nivel de sistema, *StartName* contiene el nombre de objeto del controlador (es decir, sistema de \\ archivos \\ RDR o \\ XNS del controlador \\ ) que usa el sistema de entrada y salida (e/s) para cargar el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e118-172">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="8e118-173">Si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de e/s basado en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-173">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="8e118-174">Ejemplo: DWDOM \\ admin.</span><span class="sxs-lookup"><span data-stu-id="8e118-174">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-175">*StartPassword* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e118-175">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e118-176">Contraseña para el nombre de cuenta especificado por el parámetro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="8e118-176">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="8e118-177">Especifique **null** si no va a cambiar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="8e118-177">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="8e118-178">Especifique una cadena vacía si el servicio no tiene contraseña.</span><span class="sxs-lookup"><span data-stu-id="8e118-178">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-179">*LoadOrderGroup* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e118-179">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e118-180">Nombre de grupo asociado al nuevo servicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-180">Group name associated with the new service.</span></span> <span data-ttu-id="8e118-181">Los grupos de pedidos de carga se incluyen en el registro y determinan la secuencia en la que se cargan los servicios en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8e118-181">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="8e118-182">Si el puntero es **null** o apunta a una cadena vacía, el servicio no pertenece a un grupo.</span><span class="sxs-lookup"><span data-stu-id="8e118-182">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="8e118-183">Las dependencias entre grupos deben aparecer en el parámetro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="8e118-183">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="8e118-184">Los servicios de la lista de grupos de orden de carga se inician en primer lugar, seguidos de los servicios de los grupos que no están en la lista de grupos de orden de carga, seguidos de los servicios que no pertenecen a un grupo.</span><span class="sxs-lookup"><span data-stu-id="8e118-184">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="8e118-185">El registro tiene una lista de grupos de orden de carga que se encuentran en:</span><span class="sxs-lookup"><span data-stu-id="8e118-185">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="8e118-186">**HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local ServiceGroupOrder</span><span class="sxs-lookup"><span data-stu-id="8e118-186">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="8e118-187">*LoadOrderGroupDependencies* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e118-187">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e118-188">Matriz de grupos de orden de carga que deben iniciarse antes de este servicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-188">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="8e118-189">Cada elemento de la matriz está delimitado por **null** y la lista termina en dos valores **null** .</span><span class="sxs-lookup"><span data-stu-id="8e118-189">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="8e118-190">En Visual Basic o script puede pasar un objeto vbArray.</span><span class="sxs-lookup"><span data-stu-id="8e118-190">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="8e118-191">Si el puntero es **null** o apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="8e118-191">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="8e118-192">Los nombres de grupo deben ir precedidos del \_ identificador de grupo SC \_ (definido en el archivo Winsvc. h) para diferenciarlo de un nombre de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="8e118-192">Group names must be prefixed by the SC\_GROUP\_IDENTIFIER (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="8e118-193">La dependencia de un grupo significa que este servicio se puede ejecutar si se está ejecutando al menos un miembro del grupo después de un intento de iniciar todos los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="8e118-193">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-194">*ServiceDependencies* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e118-194">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e118-195">Matriz de que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-195">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="8e118-196">Cada elemento de la matriz está delimitado por **null** y la lista termina en dos valores **null** .</span><span class="sxs-lookup"><span data-stu-id="8e118-196">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="8e118-197">En Visual Basic o script puede pasar un objeto vbArray.</span><span class="sxs-lookup"><span data-stu-id="8e118-197">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="8e118-198">Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="8e118-198">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="8e118-199">La dependencia de un servicio significa que este servicio solo se puede ejecutar si se está ejecutando el servicio del que depende.</span><span class="sxs-lookup"><span data-stu-id="8e118-199">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e118-200">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e118-200">Return value</span></span>

<span data-ttu-id="8e118-201">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="8e118-201">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="8e118-202">**Success**</span><span class="sxs-lookup"><span data-stu-id="8e118-202">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-203">0</span><span class="sxs-lookup"><span data-stu-id="8e118-203">0</span></span>

<span data-ttu-id="8e118-204">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8e118-204">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-205">**No compatible**</span><span class="sxs-lookup"><span data-stu-id="8e118-205">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-206">1</span><span class="sxs-lookup"><span data-stu-id="8e118-206">1</span></span>

<span data-ttu-id="8e118-207">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8e118-207">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-208">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="8e118-208">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-209">2</span><span class="sxs-lookup"><span data-stu-id="8e118-209">2</span></span>

<span data-ttu-id="8e118-210">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="8e118-210">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-211">**Servicios dependientes en ejecución**</span><span class="sxs-lookup"><span data-stu-id="8e118-211">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-212">3</span><span class="sxs-lookup"><span data-stu-id="8e118-212">3</span></span>

<span data-ttu-id="8e118-213">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="8e118-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-214">**Control de servicio no válido**</span><span class="sxs-lookup"><span data-stu-id="8e118-214">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-215">4</span><span class="sxs-lookup"><span data-stu-id="8e118-215">4</span></span>

<span data-ttu-id="8e118-216">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-216">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-217">**El servicio no puede aceptar el control**</span><span class="sxs-lookup"><span data-stu-id="8e118-217">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-218">5</span><span class="sxs-lookup"><span data-stu-id="8e118-218">5</span></span>

<span data-ttu-id="8e118-219">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="8e118-219">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-220">**Servicio no activo**</span><span class="sxs-lookup"><span data-stu-id="8e118-220">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-221">6</span><span class="sxs-lookup"><span data-stu-id="8e118-221">6</span></span>

<span data-ttu-id="8e118-222">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="8e118-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-223">**Tiempo de espera de solicitud de servicio**</span><span class="sxs-lookup"><span data-stu-id="8e118-223">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-224">7</span><span class="sxs-lookup"><span data-stu-id="8e118-224">7</span></span>

<span data-ttu-id="8e118-225">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-225">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-226">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="8e118-226">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-227">8</span><span class="sxs-lookup"><span data-stu-id="8e118-227">8</span></span>

<span data-ttu-id="8e118-228">Proceso interactivo.</span><span class="sxs-lookup"><span data-stu-id="8e118-228">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-229">**Ruta de acceso no encontrada**</span><span class="sxs-lookup"><span data-stu-id="8e118-229">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-230">9</span><span class="sxs-lookup"><span data-stu-id="8e118-230">9</span></span>

<span data-ttu-id="8e118-231">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-231">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-232">**El servicio ya se está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="8e118-232">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-233">10</span><span class="sxs-lookup"><span data-stu-id="8e118-233">10</span></span>

<span data-ttu-id="8e118-234">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="8e118-234">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-235">**Base de datos de servicio bloqueada**</span><span class="sxs-lookup"><span data-stu-id="8e118-235">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-236">11</span><span class="sxs-lookup"><span data-stu-id="8e118-236">11</span></span>

<span data-ttu-id="8e118-237">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="8e118-237">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-238">**Dependencia de servicio eliminada**</span><span class="sxs-lookup"><span data-stu-id="8e118-238">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-239">12</span><span class="sxs-lookup"><span data-stu-id="8e118-239">12</span></span>

<span data-ttu-id="8e118-240">Una dependencia en la que se basaba este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e118-240">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-241">**Error de dependencia de servicio**</span><span class="sxs-lookup"><span data-stu-id="8e118-241">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-242">13</span><span class="sxs-lookup"><span data-stu-id="8e118-242">13</span></span>

<span data-ttu-id="8e118-243">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="8e118-243">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-244">**Servicio deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="8e118-244">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-245">14</span><span class="sxs-lookup"><span data-stu-id="8e118-245">14</span></span>

<span data-ttu-id="8e118-246">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e118-246">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-247">**Error de inicio de sesión de servicio**</span><span class="sxs-lookup"><span data-stu-id="8e118-247">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-248">15</span><span class="sxs-lookup"><span data-stu-id="8e118-248">15</span></span>

<span data-ttu-id="8e118-249">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="8e118-249">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-250">**Servicio marcado para eliminación**</span><span class="sxs-lookup"><span data-stu-id="8e118-250">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-251">16</span><span class="sxs-lookup"><span data-stu-id="8e118-251">16</span></span>

<span data-ttu-id="8e118-252">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e118-252">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-253">**Servicio sin subproceso**</span><span class="sxs-lookup"><span data-stu-id="8e118-253">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-254">17</span><span class="sxs-lookup"><span data-stu-id="8e118-254">17</span></span>

<span data-ttu-id="8e118-255">No hay ningún subproceso de ejecución para el servicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-255">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-256">**Estado dependencia circular**</span><span class="sxs-lookup"><span data-stu-id="8e118-256">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-257">18</span><span class="sxs-lookup"><span data-stu-id="8e118-257">18</span></span>

<span data-ttu-id="8e118-258">Hay dependencias circulares al iniciarse el servicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-258">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-259">**Estado nombre duplicado**</span><span class="sxs-lookup"><span data-stu-id="8e118-259">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-260">19</span><span class="sxs-lookup"><span data-stu-id="8e118-260">19</span></span>

<span data-ttu-id="8e118-261">Hay un servicio que se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="8e118-261">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-262">**Estado nombre no válido**</span><span class="sxs-lookup"><span data-stu-id="8e118-262">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-263">20</span><span class="sxs-lookup"><span data-stu-id="8e118-263">20</span></span>

<span data-ttu-id="8e118-264">Hay caracteres no válidos en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-264">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-265">**Estado parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="8e118-265">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-266">21</span><span class="sxs-lookup"><span data-stu-id="8e118-266">21</span></span>

<span data-ttu-id="8e118-267">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-267">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-268">**Estado cuenta de servicio no válida**</span><span class="sxs-lookup"><span data-stu-id="8e118-268">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-269">22</span><span class="sxs-lookup"><span data-stu-id="8e118-269">22</span></span>

<span data-ttu-id="8e118-270">La cuenta con la que se va a ejecutar este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="8e118-270">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-271">**El servicio de estado existe**</span><span class="sxs-lookup"><span data-stu-id="8e118-271">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-272">23</span><span class="sxs-lookup"><span data-stu-id="8e118-272">23</span></span>

<span data-ttu-id="8e118-273">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e118-273">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-274">**Servicio ya pausado**</span><span class="sxs-lookup"><span data-stu-id="8e118-274">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-275">24</span><span class="sxs-lookup"><span data-stu-id="8e118-275">24</span></span>

<span data-ttu-id="8e118-276">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="8e118-276">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="8e118-277">**Otros**</span><span class="sxs-lookup"><span data-stu-id="8e118-277">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8e118-278">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="8e118-278">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e118-279">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e118-279">Requirements</span></span>



| <span data-ttu-id="8e118-280">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e118-280">Requirement</span></span> | <span data-ttu-id="8e118-281">Value</span><span class="sxs-lookup"><span data-stu-id="8e118-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e118-282">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e118-282">Minimum supported client</span></span><br/> | <span data-ttu-id="8e118-283">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e118-283">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e118-284">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e118-284">Minimum supported server</span></span><br/> | <span data-ttu-id="8e118-285">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e118-285">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e118-286">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8e118-286">Namespace</span></span><br/>                | <span data-ttu-id="8e118-287">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8e118-287">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e118-288">MOF</span><span class="sxs-lookup"><span data-stu-id="8e118-288">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e118-289"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e118-289"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e118-290">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8e118-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e118-291"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e118-291"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e118-292">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e118-292">See also</span></span>

<dl> <dt>

<span data-ttu-id="8e118-293">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8e118-293">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8e118-294">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="8e118-294">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

