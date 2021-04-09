---
description: Modifica un objeto de servicio derivado de Win32 \_ BaseService.
ms.assetid: d5f4f472-e7d9-4664-9430-9c77034a5978
ms.tgt_platform: multiple
title: Método de cambio de la clase Win32_BaseService (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a70ee83229a830e22fba4241a6c50eb8d971c5ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153301"
---
# <a name="change-method-of-the-win32_baseservice-class"></a><span data-ttu-id="c8335-103">Método de cambio de la \_ clase Win32 BaseService</span><span class="sxs-lookup"><span data-stu-id="c8335-103">Change method of the Win32\_BaseService class</span></span>

<span data-ttu-id="c8335-104">El método de clase **Change** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) modifica un objeto de servicio derivado de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="c8335-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a service object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span> <span data-ttu-id="c8335-105">El [**parámetro \_ LoadOrderGroup de Win32**](win32-loadordergroup.md) representa un grupo de servicios del sistema que definen las dependencias de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="c8335-105">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="c8335-106">Los servicios deben iniciarse en el orden especificado por el grupo de orden de carga, ya que los servicios dependen entre sí.</span><span class="sxs-lookup"><span data-stu-id="c8335-106">The services must be initiated in the order specified by the Load Order Group, because the services depend on each other.</span></span> <span data-ttu-id="c8335-107">Estos servicios dependientes requieren que los servicios antecedentes funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="c8335-107">These dependent services require antecedent services to function correctly.</span></span>

<span data-ttu-id="c8335-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c8335-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c8335-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c8335-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8335-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8335-110">Syntax</span></span>


```mof
uint32 Change(
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



## <a name="parameters"></a><span data-ttu-id="c8335-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8335-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8335-112">*DisplayName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8335-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8335-113">Nombre para mostrar de un servicio.</span><span class="sxs-lookup"><span data-stu-id="c8335-113">The display name for a service.</span></span> <span data-ttu-id="c8335-114">Esta cadena tiene una longitud máxima de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c8335-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="c8335-115">El nombre es mayúsculas y minúsculas en el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="c8335-115">The name is case preserved in the service control manager.</span></span> <span data-ttu-id="c8335-116">Las comparaciones de *displayName* siempre distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c8335-116">*DisplayName* comparisons are always case insensitive.</span></span>

<span data-ttu-id="c8335-117">Constraints: acepta el mismo valor que el parámetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="c8335-117">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="c8335-118">Ejemplo: "Endisco".</span><span class="sxs-lookup"><span data-stu-id="c8335-118">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="c8335-119">*Nombreruta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8335-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8335-120">Ruta de acceso completa al archivo ejecutable que implementa un servicio.</span><span class="sxs-lookup"><span data-stu-id="c8335-120">The fully qualified path to the executable file that implements a service.</span></span>

<span data-ttu-id="c8335-121">Ejemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="c8335-121">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="c8335-122">*ServiceType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8335-122">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8335-123">Tipo de servicios proporcionados a los procesos que los llaman.</span><span class="sxs-lookup"><span data-stu-id="c8335-123">Type of services provided to processes that call them.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="c8335-124"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Controlador de kernel** (1)</span><span class="sxs-lookup"><span data-stu-id="c8335-124"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Driver** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="c8335-125"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Controlador del sistema de archivos** (2)</span><span class="sxs-lookup"><span data-stu-id="c8335-125"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**File System Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="c8335-126"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adaptador** (4)</span><span class="sxs-lookup"><span data-stu-id="c8335-126"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="c8335-127"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Controlador de reconocedor** (8)</span><span class="sxs-lookup"><span data-stu-id="c8335-127"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Recognizer Driver** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="c8335-128"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Proceso propio** (16)</span><span class="sxs-lookup"><span data-stu-id="c8335-128"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Own Process** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="c8335-129"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Proceso de uso compartido** (32)</span><span class="sxs-lookup"><span data-stu-id="c8335-129"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Share Process** (32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c8335-130">(256)</span><span class="sxs-lookup"><span data-stu-id="c8335-130">(256)</span></span>


</dt> <dd>

<span data-ttu-id="c8335-131">Proceso interactivo</span><span class="sxs-lookup"><span data-stu-id="c8335-131">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c8335-132">*ErrorControl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8335-132">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8335-133">Gravedad de un error si este servicio no se inicia durante el inicio.</span><span class="sxs-lookup"><span data-stu-id="c8335-133">Severity of an error if this service does not start during startup.</span></span> <span data-ttu-id="c8335-134">El valor indica la acción que realiza el programa de inicio si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="c8335-134">The value indicates the action that the startup program takes if failure occurs.</span></span> <span data-ttu-id="c8335-135">El sistema registra todos los errores.</span><span class="sxs-lookup"><span data-stu-id="c8335-135">The system logs all errors.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="c8335-136"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Omitir** (0)</span><span class="sxs-lookup"><span data-stu-id="c8335-136"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c8335-137">No se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="c8335-137">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="c8335-138"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="c8335-138"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c8335-139">Normal.</span><span class="sxs-lookup"><span data-stu-id="c8335-139">Normal.</span></span> <span data-ttu-id="c8335-140">Se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="c8335-140">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="c8335-141"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)</span><span class="sxs-lookup"><span data-stu-id="c8335-141"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c8335-142">El sistema se reinicia con la última configuración válida.</span><span class="sxs-lookup"><span data-stu-id="c8335-142">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="c8335-143"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="c8335-143"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c8335-144">El sistema intenta reiniciarse con una configuración válida.</span><span class="sxs-lookup"><span data-stu-id="c8335-144">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c8335-145">*StartMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8335-145">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8335-146">Modo de inicio del servicio base de Windows.</span><span class="sxs-lookup"><span data-stu-id="c8335-146">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="c8335-147"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicio de arranque** ("arranque")</span><span class="sxs-lookup"><span data-stu-id="c8335-147"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="c8335-148">Controlador de dispositivo que inicia el cargador del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c8335-148">Device driver that the operating system loader starts.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="c8335-149"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Inicio del sistema** ("System")</span><span class="sxs-lookup"><span data-stu-id="c8335-149"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="c8335-150">Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c8335-150">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="c8335-151">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="c8335-151">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="c8335-152"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Inicio automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="c8335-152"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="c8335-153">Servicio que el administrador de control de servicios inicia automáticamente durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="c8335-153">Service to start automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="c8335-154"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Inicio** de la demanda ("manual")</span><span class="sxs-lookup"><span data-stu-id="c8335-154"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="c8335-155">Servicio que va a iniciar el administrador de control de servicios cuando un proceso llama al método [**StartService**](startservice-method-in-class-win32-baseservice.md) .</span><span class="sxs-lookup"><span data-stu-id="c8335-155">Service to start by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c8335-156"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("deshabilitado")</span><span class="sxs-lookup"><span data-stu-id="c8335-156"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="c8335-157">Servicio que no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="c8335-157">Service that cannot be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c8335-158">*DesktopInteract* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8335-158">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8335-159">Si **es true**, el servicio puede crear o comunicarse con una ventana en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="c8335-159">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-160">*StartName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8335-160">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8335-161">Nombre de cuenta con el que se ejecuta el servicio, que depende del tipo de servicio.</span><span class="sxs-lookup"><span data-stu-id="c8335-161">Account name that the service runs under, which depends on the service type.</span></span> <span data-ttu-id="c8335-162">El nombre de la cuenta puede tener el formato nombreDeDominio \\ nombreDeUsuario o. \\ Nombre.</span><span class="sxs-lookup"><span data-stu-id="c8335-162">The account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="c8335-163">Cuando se ejecuta, el proceso de servicio se registra con una de las dos formas anteriores.</span><span class="sxs-lookup"><span data-stu-id="c8335-163">When it runs, the service process is logged by using one of the previous two forms.</span></span> <span data-ttu-id="c8335-164">Si la cuenta pertenece al dominio integrado,. \\ Se puede especificar el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="c8335-164">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="c8335-165">Si se especifica una cadena vacía, el servicio inicia sesión como la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="c8335-165">If an empty string is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="c8335-166">En el caso de los controladores de kernel o de nivel de sistema, *StartName* contiene el nombre de objeto del controlador, por ejemplo, \\ filesystem \\ RDR o \\ \\ el controlador XNS, que el sistema de entrada y salida (e/s) utiliza para cargar el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8335-166">For kernel or system-level drivers, *StartName* contains the driver object name, for example, \\FileSystem\\Rdr or \\Driver\\Xns, which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="c8335-167">Si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado que el sistema de e/s crea en función del nombre del servicio, por ejemplo, DWDOM \\ admin.</span><span class="sxs-lookup"><span data-stu-id="c8335-167">If **NULL** is specified, the driver runs with a default object name that the I/O system creates based on the service name, for example, DWDOM\\Admin.</span></span>

<span data-ttu-id="c8335-168">También puede usar el formato de nombre principal de usuario (UPN) para especificar **StartName**, por ejemplo, *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="c8335-168">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-169">*StartPassword* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8335-169">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8335-170">Contraseña del nombre de la cuenta que especifica el parámetro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="c8335-170">Password to the account name that the *StartName* parameter specifies.</span></span> <span data-ttu-id="c8335-171">Especifique **null** cuando no cambie la contraseña.</span><span class="sxs-lookup"><span data-stu-id="c8335-171">Specify **NULL** when you do not change the password.</span></span> <span data-ttu-id="c8335-172">Especifique una cadena vacía si el servicio no tiene una contraseña.</span><span class="sxs-lookup"><span data-stu-id="c8335-172">Specify an empty string if the service does not have a password.</span></span>

> [!Note]  
> <span data-ttu-id="c8335-173">Al cambiar un servicio de sistema local a red o de red a sistema local, *StartPassword* debe ser una cadena vacía ("") y no **null**.</span><span class="sxs-lookup"><span data-stu-id="c8335-173">When you change a service from local system to network or from network to local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="c8335-174">*LoadOrderGroup* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8335-174">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8335-175">Nombre del grupo al que está asociado.</span><span class="sxs-lookup"><span data-stu-id="c8335-175">Group name that it is associated with.</span></span> <span data-ttu-id="c8335-176">Los grupos de pedidos de carga se incluyen en el registro del sistema y determinan la secuencia en la que se cargan los servicios en un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c8335-176">Load order groups are contained in the system registry, and determine the sequence that services are loaded into an operating system.</span></span> <span data-ttu-id="c8335-177">Si el puntero es **null**, o apunta a una cadena vacía, el servicio no pertenece a un grupo.</span><span class="sxs-lookup"><span data-stu-id="c8335-177">If the pointer is **NULL**, or points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="c8335-178">Las dependencias entre grupos deben aparecer en el parámetro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="c8335-178">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="c8335-179">Los servicios de la lista de grupos de orden de carga se inician en primer lugar, seguidos de los servicios de los grupos que no están en la lista de grupos de orden de carga, seguidos de los servicios que no pertenecen a un grupo.</span><span class="sxs-lookup"><span data-stu-id="c8335-179">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="c8335-180">El registro del sistema tiene una lista de grupos de orden de carga ubicados en **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **control** \\ **ServiceGroupOrder**.</span><span class="sxs-lookup"><span data-stu-id="c8335-180">The system registry has a list of load ordering groups located at **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-181">*LoadOrderGroupDependencies* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8335-181">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8335-182">Lista de grupos de orden de carga que deben iniciarse antes de que se inicie este servicio.</span><span class="sxs-lookup"><span data-stu-id="c8335-182">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="c8335-183">La matriz termina en **null**.</span><span class="sxs-lookup"><span data-stu-id="c8335-183">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="c8335-184">Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="c8335-184">If the pointer is **NULL**, or if it points to an empty string, the service does not have dependencies.</span></span> <span data-ttu-id="c8335-185">Los nombres de grupo deben ir precedidos del **\_ \_ identificador de grupo SC** (definido en el archivo Winsvc. h) para diferenciarlos de los nombres de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="c8335-185">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names, because services and service groups share the same namespace.</span></span> <span data-ttu-id="c8335-186">La dependencia de un grupo significa que este servicio se puede ejecutar si se está ejecutando al menos un miembro del grupo después de un intento de iniciar todos los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="c8335-186">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-187">*ServiceDependencies* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8335-187">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8335-188">Lista que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio.</span><span class="sxs-lookup"><span data-stu-id="c8335-188">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="c8335-189">La matriz termina en **null**.</span><span class="sxs-lookup"><span data-stu-id="c8335-189">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="c8335-190">Si el puntero es **null**, o apunta a una cadena vacía, el servicio no tiene dependencias.</span><span class="sxs-lookup"><span data-stu-id="c8335-190">If the pointer is **NULL**, or points to an empty string, the service does not have dependencies.</span></span> <span data-ttu-id="c8335-191">La dependencia de un servicio significa que este servicio solo se puede ejecutar si se está ejecutando el servicio del que depende.</span><span class="sxs-lookup"><span data-stu-id="c8335-191">Dependency on a service means that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8335-192">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8335-192">Return value</span></span>

<span data-ttu-id="c8335-193">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="c8335-193">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c8335-194">**Success**</span><span class="sxs-lookup"><span data-stu-id="c8335-194">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-195">0</span><span class="sxs-lookup"><span data-stu-id="c8335-195">0</span></span>

<span data-ttu-id="c8335-196">Se acepta la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c8335-196">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-197">**No compatible**</span><span class="sxs-lookup"><span data-stu-id="c8335-197">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-198">1</span><span class="sxs-lookup"><span data-stu-id="c8335-198">1</span></span>

<span data-ttu-id="c8335-199">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c8335-199">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-200">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="c8335-200">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-201">2</span><span class="sxs-lookup"><span data-stu-id="c8335-201">2</span></span>

<span data-ttu-id="c8335-202">El usuario no tiene los privilegios de acceso necesarios.</span><span class="sxs-lookup"><span data-stu-id="c8335-202">The user does not have the necessary access privileges.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-203">**Servicios dependientes en ejecución**</span><span class="sxs-lookup"><span data-stu-id="c8335-203">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-204">3</span><span class="sxs-lookup"><span data-stu-id="c8335-204">3</span></span>

<span data-ttu-id="c8335-205">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="c8335-205">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-206">**Control de servicio no válido**</span><span class="sxs-lookup"><span data-stu-id="c8335-206">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-207">4</span><span class="sxs-lookup"><span data-stu-id="c8335-207">4</span></span>

<span data-ttu-id="c8335-208">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="c8335-208">The requested control code is not valid, or is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-209">**El servicio no puede aceptar el control**</span><span class="sxs-lookup"><span data-stu-id="c8335-209">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-210">5</span><span class="sxs-lookup"><span data-stu-id="c8335-210">5</span></span>

<span data-ttu-id="c8335-211">El código de control solicitado no se puede enviar al servicio porque la propiedad [**State**](win32-baseservice.md) del objeto [**Win32 \_ BaseService**](win32-baseservice.md) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="c8335-211">The requested control code cannot be sent to the service because the [**State**](win32-baseservice.md) property in the [**Win32\_BaseService**](win32-baseservice.md) object is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-212">**Servicio no activo**</span><span class="sxs-lookup"><span data-stu-id="c8335-212">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-213">6</span><span class="sxs-lookup"><span data-stu-id="c8335-213">6</span></span>

<span data-ttu-id="c8335-214">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="c8335-214">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-215">**Tiempo de espera de solicitud de servicio**</span><span class="sxs-lookup"><span data-stu-id="c8335-215">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-216">7</span><span class="sxs-lookup"><span data-stu-id="c8335-216">7</span></span>

<span data-ttu-id="c8335-217">El servicio no responde rápidamente a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="c8335-217">The service does not respond to the start request quickly.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-218">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="c8335-218">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-219">8</span><span class="sxs-lookup"><span data-stu-id="c8335-219">8</span></span>

<span data-ttu-id="c8335-220">Proceso interactivo.</span><span class="sxs-lookup"><span data-stu-id="c8335-220">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-221">**Ruta de acceso no encontrada**</span><span class="sxs-lookup"><span data-stu-id="c8335-221">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-222">9</span><span class="sxs-lookup"><span data-stu-id="c8335-222">9</span></span>

<span data-ttu-id="c8335-223">No se encuentra la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="c8335-223">The directory path to the service executable file is not found.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-224">**El servicio ya se está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="c8335-224">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-225">10</span><span class="sxs-lookup"><span data-stu-id="c8335-225">10</span></span>

<span data-ttu-id="c8335-226">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="c8335-226">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-227">**Base de datos de servicio bloqueada**</span><span class="sxs-lookup"><span data-stu-id="c8335-227">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-228">11</span><span class="sxs-lookup"><span data-stu-id="c8335-228">11</span></span>

<span data-ttu-id="c8335-229">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="c8335-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-230">**Dependencia de servicio eliminada**</span><span class="sxs-lookup"><span data-stu-id="c8335-230">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-231">12</span><span class="sxs-lookup"><span data-stu-id="c8335-231">12</span></span>

<span data-ttu-id="c8335-232">Una dependencia para la que se basa este servicio se quita del sistema.</span><span class="sxs-lookup"><span data-stu-id="c8335-232">A dependency for which this service relies on is removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-233">**Error de dependencia de servicio**</span><span class="sxs-lookup"><span data-stu-id="c8335-233">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-234">13</span><span class="sxs-lookup"><span data-stu-id="c8335-234">13</span></span>

<span data-ttu-id="c8335-235">El servicio no encuentra el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="c8335-235">The service does not find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-236">**Servicio deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="c8335-236">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-237">14</span><span class="sxs-lookup"><span data-stu-id="c8335-237">14</span></span>

<span data-ttu-id="c8335-238">El servicio está deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="c8335-238">The service is disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-239">**Error de inicio de sesión de servicio**</span><span class="sxs-lookup"><span data-stu-id="c8335-239">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-240">15</span><span class="sxs-lookup"><span data-stu-id="c8335-240">15</span></span>

<span data-ttu-id="c8335-241">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="c8335-241">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-242">**Servicio marcado para eliminación**</span><span class="sxs-lookup"><span data-stu-id="c8335-242">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-243">16</span><span class="sxs-lookup"><span data-stu-id="c8335-243">16</span></span>

<span data-ttu-id="c8335-244">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="c8335-244">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-245">**Servicio sin subproceso**</span><span class="sxs-lookup"><span data-stu-id="c8335-245">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-246">17</span><span class="sxs-lookup"><span data-stu-id="c8335-246">17</span></span>

<span data-ttu-id="c8335-247">No hay ningún subproceso de ejecución para el servicio.</span><span class="sxs-lookup"><span data-stu-id="c8335-247">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-248">**Estado dependencia circular**</span><span class="sxs-lookup"><span data-stu-id="c8335-248">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-249">18</span><span class="sxs-lookup"><span data-stu-id="c8335-249">18</span></span>

<span data-ttu-id="c8335-250">Hay dependencias circulares al iniciarse el servicio.</span><span class="sxs-lookup"><span data-stu-id="c8335-250">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-251">**Estado nombre duplicado**</span><span class="sxs-lookup"><span data-stu-id="c8335-251">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-252">19</span><span class="sxs-lookup"><span data-stu-id="c8335-252">19</span></span>

<span data-ttu-id="c8335-253">Hay un servicio que se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="c8335-253">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-254">**Estado nombre no válido**</span><span class="sxs-lookup"><span data-stu-id="c8335-254">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-255">20</span><span class="sxs-lookup"><span data-stu-id="c8335-255">20</span></span>

<span data-ttu-id="c8335-256">Hay caracteres no válidos en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="c8335-256">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-257">**Estado parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="c8335-257">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-258">21</span><span class="sxs-lookup"><span data-stu-id="c8335-258">21</span></span>

<span data-ttu-id="c8335-259">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="c8335-259">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-260">**Estado cuenta de servicio no válida**</span><span class="sxs-lookup"><span data-stu-id="c8335-260">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-261">22</span><span class="sxs-lookup"><span data-stu-id="c8335-261">22</span></span>

<span data-ttu-id="c8335-262">La cuenta para la que se ejecuta este servicio no es válida o no tiene permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="c8335-262">The account for this service to run under is not valid or does not have the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-263">**El servicio de estado existe**</span><span class="sxs-lookup"><span data-stu-id="c8335-263">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-264">23</span><span class="sxs-lookup"><span data-stu-id="c8335-264">23</span></span>

<span data-ttu-id="c8335-265">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="c8335-265">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-266">**Servicio ya pausado**</span><span class="sxs-lookup"><span data-stu-id="c8335-266">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-267">24</span><span class="sxs-lookup"><span data-stu-id="c8335-267">24</span></span>

<span data-ttu-id="c8335-268">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="c8335-268">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="c8335-269">**Otros**</span><span class="sxs-lookup"><span data-stu-id="c8335-269">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c8335-270">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="c8335-270">25 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8335-271">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8335-271">Remarks</span></span>

<span data-ttu-id="c8335-272">Para cambiar un servicio de una red a un sistema local, use los siguientes valores para los parámetros *StartName* y *StartPassword* :</span><span class="sxs-lookup"><span data-stu-id="c8335-272">To change a service from a network to a local system, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="c8335-273">Para cambiar un servicio de un sistema local a una red, use los siguientes valores para los parámetros *StartName* y *StartPassword* :</span><span class="sxs-lookup"><span data-stu-id="c8335-273">To change a service from a local system to a network, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a><span data-ttu-id="c8335-274">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8335-274">Requirements</span></span>



| <span data-ttu-id="c8335-275">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8335-275">Requirement</span></span> | <span data-ttu-id="c8335-276">Value</span><span class="sxs-lookup"><span data-stu-id="c8335-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8335-277">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8335-277">Minimum supported client</span></span><br/> | <span data-ttu-id="c8335-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8335-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c8335-279">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8335-279">Minimum supported server</span></span><br/> | <span data-ttu-id="c8335-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8335-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8335-281">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c8335-281">Namespace</span></span><br/>                | <span data-ttu-id="c8335-282">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c8335-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c8335-283">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8335-283">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8335-284"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8335-284"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="c8335-285">MOF</span><span class="sxs-lookup"><span data-stu-id="c8335-285">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8335-286"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8335-286"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8335-287">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8335-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8335-288"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8335-288"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8335-289">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8335-289">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8335-290">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c8335-290">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c8335-291">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="c8335-291">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

