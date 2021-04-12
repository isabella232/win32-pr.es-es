---
title: Clase Win32_TerminalService
description: Una subclase de la clase de servicio de Win32 \_ . Win32 \_ TerminalService representa la propiedad de elemento de la \_ Asociación TerminalServiceToSetting de Win32.
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Win32_TerminalService clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TerminalService de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TerminalService
- Win32_TerminalService.AcceptPause
- Win32_TerminalService.AcceptStop
- Win32_TerminalService.Caption
- Win32_TerminalService.CheckPoint
- Win32_TerminalService.CreationClassName
- Win32_TerminalService.DelayedAutoStart
- Win32_TerminalService.Description
- Win32_TerminalService.DesktopInteract
- Win32_TerminalService.DisplayName
- Win32_TerminalService.ErrorControl
- Win32_TerminalService.ExitCode
- Win32_TerminalService.InstallDate
- Win32_TerminalService.Name
- Win32_TerminalService.PathName
- Win32_TerminalService.ProcessId
- Win32_TerminalService.ServiceSpecificExitCode
- Win32_TerminalService.ServiceType
- Win32_TerminalService.Started
- Win32_TerminalService.StartMode
- Win32_TerminalService.StartName
- Win32_TerminalService.State
- Win32_TerminalService.Status
- Win32_TerminalService.SystemCreationClassName
- Win32_TerminalService.SystemName
- Win32_TerminalService.TagId
- Win32_TerminalService.WaitHint
- Win32_TerminalService.DisconnectedSessions
- Win32_TerminalService.TotalSessions
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba5646c6ac9abf41fddc023ad39884e611681a71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492736"
---
# <a name="win32_terminalservice-class"></a><span data-ttu-id="dc5f6-106">\_Clase Win32 TerminalService</span><span class="sxs-lookup"><span data-stu-id="dc5f6-106">Win32\_TerminalService class</span></span>

<span data-ttu-id="dc5f6-107">La clase WMI **\_ TerminalService de Win32** es una subclase de la clase de [**\_ servicio de Win32**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="dc5f6-107">The **Win32\_TerminalService** WMI class is a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class.</span></span> <span data-ttu-id="dc5f6-108">**Win32 \_ TerminalService** representa la propiedad de **elemento** de la Asociación [**\_ TerminalServiceToSetting de Win32**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="dc5f6-108">**Win32\_TerminalService** represents the **Element** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="dc5f6-109">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-109">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc5f6-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc5f6-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICE_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalService : Win32_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  uint32   CheckPoint;
  string   CreationClassName;
  boolean  DelayedAutoStart;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
  uint32   ProcessId;
  uint32   ServiceSpecificExitCode;
  string   ServiceType;
  boolean  Started;
  string   StartMode;
  string   StartName;
  string   State;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TagId;
  uint32   WaitHint;
  uint32   DisconnectedSessions;
  uint32   TotalSessions;
};
```

## <a name="members"></a><span data-ttu-id="dc5f6-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc5f6-111">Members</span></span>

<span data-ttu-id="dc5f6-112">La **clase \_ TerminalService de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dc5f6-112">The **Win32\_TerminalService** class has these types of members:</span></span>

-   [<span data-ttu-id="dc5f6-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc5f6-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="dc5f6-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc5f6-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dc5f6-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc5f6-115">Methods</span></span>

<span data-ttu-id="dc5f6-116">La clase **Win32 \_ TerminalService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-116">The **Win32\_TerminalService** class has these methods.</span></span>



| <span data-ttu-id="dc5f6-117">Método</span><span class="sxs-lookup"><span data-stu-id="dc5f6-117">Method</span></span>                                                                       | <span data-ttu-id="dc5f6-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc5f6-118">Description</span></span>                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc5f6-119">**Cambio**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-119">**Change**</span></span>](win32-terminalservice-change.md)                               | <span data-ttu-id="dc5f6-120">Modifica un servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-120">Modifies a service.</span></span><br/>                                                                       |
| [<span data-ttu-id="dc5f6-121">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-121">**ChangeStartMode**</span></span>](win32-terminalservice-changestartmode.md)             | <span data-ttu-id="dc5f6-122">Modifica el modo de inicio de un servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-122">Modifies the start mode of a service.</span></span><br/>                                                     |
| [<span data-ttu-id="dc5f6-123">**A**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-123">**Create**</span></span>](win32-terminalservice-create.md)                               | <span data-ttu-id="dc5f6-124">Crea un nuevo servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-124">Creates a new service.</span></span><br/>                                                                    |
| [<span data-ttu-id="dc5f6-125">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-125">**Delete**</span></span>](win32-terminalservice-delete.md)                               | <span data-ttu-id="dc5f6-126">Elimina un servicio existente.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-126">Deletes an existing service.</span></span><br/>                                                              |
| [<span data-ttu-id="dc5f6-127">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-127">**GetSecurityDescriptor**</span></span>](win32-terminalservice-getsecuritydescriptor.md) | <span data-ttu-id="dc5f6-128">Devuelve el descriptor de seguridad que controla el acceso al servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-128">Returns the security descriptor that controls access to the service.</span></span><br/>                      |
| [<span data-ttu-id="dc5f6-129">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-129">**InterrogateService**</span></span>](win32-terminalservice-interrogateservice.md)       | <span data-ttu-id="dc5f6-130">Solicita que un servicio actualice su estado al administrador de servicios.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-130">Requests that a service update its state to the service manager.</span></span><br/>                          |
| [<span data-ttu-id="dc5f6-131">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-131">**PauseService**</span></span>](win32-terminalservice-pauseservice.md)                   | <span data-ttu-id="dc5f6-132">Intenta poner un servicio en estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-132">Attempts to place a service in the paused state.</span></span><br/>                                          |
| [<span data-ttu-id="dc5f6-133">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-133">**ResumeService**</span></span>](win32-terminalservice-resumeservice.md)                 | <span data-ttu-id="dc5f6-134">Intenta poner un servicio en estado reanudado.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-134">Attempts to place a service in the resumed state.</span></span><br/>                                         |
| [<span data-ttu-id="dc5f6-135">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-135">**SetSecurityDescriptor**</span></span>](win32-terminalservice-setsecuritydescriptor.md) | <span data-ttu-id="dc5f6-136">Escribe una versión actualizada del descriptor de seguridad que controla el acceso al servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-136">Writes an updated version of the security descriptor that controls access to the service.</span></span><br/> |
| [<span data-ttu-id="dc5f6-137">**StartService**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-137">**StartService**</span></span>](win32-terminalservice-startservice.md)                   | <span data-ttu-id="dc5f6-138">Intenta colocar un servicio en el estado de inicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-138">Attempts to place a service into the startup state.</span></span><br/>                                       |
| [<span data-ttu-id="dc5f6-139">**StopService**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-139">**StopService**</span></span>](win32-terminalservice-stopservice.md)                     | <span data-ttu-id="dc5f6-140">Coloca un servicio en estado detenido.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-140">Places a service in the stopped state.</span></span><br/>                                                    |
| [<span data-ttu-id="dc5f6-141">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-141">**UserControlService**</span></span>](win32-terminalservice-usercontrolservice.md)       | <span data-ttu-id="dc5f6-142">Intenta enviar un código de control definido por el usuario a un servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-142">Attempts to send a user-defined control code to a service.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="dc5f6-143">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc5f6-143">Properties</span></span>

<span data-ttu-id="dc5f6-144">La **clase \_ TerminalService de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-144">The **Win32\_TerminalService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc5f6-145">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-145">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-146">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-148">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures Service \| [**\_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| Service \_ Accept \_ PAUSE \_ Continue"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("el servicio acepta la pausa")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-149">Indica si se puede pausar el servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-149">Indicates whether the service can be paused.</span></span>

<span data-ttu-id="dc5f6-150">Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-150">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-151">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-151">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-152">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-154">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures Service \| [**\_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status)servicio \| dwControlsAccepted \| \_ \_ Stop"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("el servicio acepta la detención")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-155">Indica si se puede detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-155">Indicates whether the service can be stopped.</span></span>

<span data-ttu-id="dc5f6-156">Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-156">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-157">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-160">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-160">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-161">Breve descripción del servicio: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-161">Short description of the service  a one-line string.</span></span>

<span data-ttu-id="dc5f6-162">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-163">**SnapSure**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-163">**CheckPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-164">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-166">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwCheckPoint"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point Count")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point Count")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-167">Valor que el servicio incrementa periódicamente para informar sobre su progreso durante una operación larga de inicio, detención, pausa o continuación.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-167">Value that the service increments periodically to report its progress during a long start, stop, pause, or continue operation.</span></span> <span data-ttu-id="dc5f6-168">Por ejemplo, el servicio incrementa este valor a medida que completa cada paso de su inicialización cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-168">For example, the service increments this value as it completes each step of its initialization when it is starting up.</span></span> <span data-ttu-id="dc5f6-169">El programa de interfaz de usuario que invoca la operación en el servicio usa este valor para realizar el seguimiento del progreso del servicio durante una operación larga.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-169">The user interface program that invokes the operation on the service uses this value to track the progress of the service during a lengthy operation.</span></span> <span data-ttu-id="dc5f6-170">Este valor no es válido y debe ser cero cuando el servicio no tiene pendiente una operación de inicio, detención, pausa o continuación.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-170">This value is not valid and should be zero when the service does not have a start, stop, pause, or continue operation pending.</span></span>

<span data-ttu-id="dc5f6-171">Esta propiedad se hereda del [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-171">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-172">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-172">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-175">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-175">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-176">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-176">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="dc5f6-177">Cuando se usa con las otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-177">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="dc5f6-178">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-178">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-179">**DelayedAutoStart**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-179">**DelayedAutoStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-180">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-182">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api Service \| Structures \| [**\_ retardo \_ auto \_ Start \_ info**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Inicio automático retrasado")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info)\|fDelayedAutostart"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Delayed Auto-Start")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-183">Si es **true**, el servicio se inicia después de que se inicien otros servicios de inicio automático más un breve retraso.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-183">If **True**, the service is started after other auto-start services are started plus a short delay.</span></span>

<span data-ttu-id="dc5f6-184">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows Server 2016 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-184">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

<span data-ttu-id="dc5f6-185">Esta propiedad se hereda del [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-185">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-186">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-186">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-189">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-189">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-190">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-190">Description of the object.</span></span>

<span data-ttu-id="dc5f6-191">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-192">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-192">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-193">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-195">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| Service \_ Interactive \_ Process"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("interactúa con Desktop")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-196">Indica si el servicio puede crear o comunicarse con Windows en el escritorio y, por tanto, interactuar de algún modo con un usuario.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-196">Indicates whether the service can create or communicate with windows on the desktop, and thus interact in some way with a user.</span></span> <span data-ttu-id="dc5f6-197">Los servicios interactivos deben ejecutarse en la cuenta de sistema local.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-197">Interactive services must run under the Local System account.</span></span> <span data-ttu-id="dc5f6-198">La mayoría de los servicios no son interactivos; es decir, no se comunican con el usuario de ningún modo.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-198">Most services are not interactive; that is, they do not communicate with the user in any way.</span></span>

<span data-ttu-id="dc5f6-199">Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-199">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-200">**DisconnectedSessions**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-200">**DisconnectedSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-201">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-203">El número de sesiones desconectadas en el servidor actual.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-203">The number of disconnected sessions on the current server.</span></span> <span data-ttu-id="dc5f6-204">Estas sesiones pueden seguir consumiendo activamente recursos del servidor, pero actualmente no tienen ninguna conexión de red con un cliente.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-204">These sessions may still be actively consuming server resources, however they currently have no network connection with a client.</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-205">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-205">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-206">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-208">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpDisplayName"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre para mostrar")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-208">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-209">Nombre del servicio tal como se ve en el complemento Servicios.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-209">Name of the service as viewed in the Services snap-in.</span></span> <span data-ttu-id="dc5f6-210">Esta cadena tiene una longitud máxima de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-210">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="dc5f6-211">Tenga en cuenta que el nombre para mostrar y el nombre del servicio (que se almacena en el registro) no son siempre los mismos.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-211">Note that the display name and the service name (which is stored in the registry) are not always the same.</span></span> <span data-ttu-id="dc5f6-212">Por ejemplo, el servicio de cliente DHCP tiene el nombre de servicio DHCP, pero el cliente DHCP de nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-212">For example, the DHCP Client service has the service name Dhcp but the display name DHCP Client.</span></span> <span data-ttu-id="dc5f6-213">El nombre se conserva en las mayúsculas y minúsculas en el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-213">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="dc5f6-214">Sin embargo, las comparaciones de [**displayName**](/windows/desktop/CIMWin32Prov/win32-service) siempre distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-214">However, [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) comparisons are always case-insensitive.</span></span>

<span data-ttu-id="dc5f6-215">Constraint: acepta el mismo valor que la propiedad [**Name**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="dc5f6-215">Constraint: Accepts the same value as the [**Name**](/windows/desktop/CIMWin32Prov/win32-service) property.</span></span>

<span data-ttu-id="dc5f6-216">Ejemplo: "Endisco"</span><span class="sxs-lookup"><span data-stu-id="dc5f6-216">Example: "Atdisk"</span></span>

<span data-ttu-id="dc5f6-217">Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-217">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-218">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-218">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-221">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("gravedad del error de inicio")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-222">Gravedad del error si este servicio no se inicia durante el inicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-222">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="dc5f6-223">El valor indica la acción realizada por el programa de inicio si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-223">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="dc5f6-224">El sistema registra todos los errores.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-224">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="dc5f6-225"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Omitir** ("omitir")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-225"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="dc5f6-226">No se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-226">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="dc5f6-227"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("normal")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-227"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="dc5f6-228">Se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-228">User is notified.</span></span> <span data-ttu-id="dc5f6-229">Normalmente, se trata de un cuadro de mensaje que informa al usuario del problema.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-229">Usually this will be a message box display notifying the user of the problem.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="dc5f6-230"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("grave")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-230"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="dc5f6-231">El sistema se reinicia con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-231">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="dc5f6-232"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** ("crítico")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-232"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="dc5f6-233">El sistema intenta reiniciarse con una configuración válida.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-233">System attempts to restart with a good configuration.</span></span> <span data-ttu-id="dc5f6-234">Si el servicio no se inicia por segunda vez, se produce un error de inicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-234">If the service fails to start a second time, startup fails.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc5f6-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="dc5f6-236">Se desconoce la gravedad del error.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-236">Severity of the error is unknown.</span></span>

</dd> </dl>

<span data-ttu-id="dc5f6-237">Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-237">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-238">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-238">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-239">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-241">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("código de salida")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-241">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-242">Código de error de Windows que define los errores detectados al iniciar o detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-242">Windows error code that defines errors encountered in starting or stopping the service.</span></span> <span data-ttu-id="dc5f6-243">Esta propiedad se establece en **\_ \_ \_ error específico del servicio de error** (1066) cuando el error es exclusivo del servicio representado por esta clase, y la información sobre el error está disponible en la propiedad [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="dc5f6-243">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) property.</span></span> <span data-ttu-id="dc5f6-244">El servicio establece este valor en **ningún \_ error** cuando se ejecuta y de nuevo tras la terminación normal.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-244">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="dc5f6-245">Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-245">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-246">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-246">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-247">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-247">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-249">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-249">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-250">El objeto de fecha está instalado.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-250">Date object is installed.</span></span> <span data-ttu-id="dc5f6-251">Esta propiedad no requiere un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-251">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dc5f6-252">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-252">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-253">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-253">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-254">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-255">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-256">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dc5f6-256">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-257">Identificador único del servicio que proporciona una indicación de la funcionalidad que se administra.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-257">Unique identifier of the service that provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="dc5f6-258">Esta funcionalidad se describe en la propiedad [**Description**](/windows/desktop/CIMWin32Prov/win32-service) del objeto.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-258">This functionality is described in the [**Description**](/windows/desktop/CIMWin32Prov/win32-service) property of the object.</span></span>

<span data-ttu-id="dc5f6-259">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-260">**PathName**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-260">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-263">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File path name")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-263">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-264">Ruta de acceso completa al archivo binario del servicio que implementa el servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-264">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="dc5f6-265">Ejemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="dc5f6-265">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="dc5f6-266">Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-266">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-267">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-267">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-268">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-268">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-270">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**Service \_ status \_ Process**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Process ID")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-270">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS\_PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process)\|dwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-271">Identificador de proceso del servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-271">Process identifier of the service.</span></span>

<span data-ttu-id="dc5f6-272">Ejemplo: 324</span><span class="sxs-lookup"><span data-stu-id="dc5f6-272">Example: 324</span></span>

<span data-ttu-id="dc5f6-273">Esta propiedad se hereda del [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-273">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-274">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-274">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-275">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-277">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("código de salida específico del servidor")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-277">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-278">Código de error específico del servicio para los errores que se producen mientras el servicio se está iniciando o deteniendo.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-278">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="dc5f6-279">Los códigos de salida se definen mediante el servicio representado por esta clase.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-279">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="dc5f6-280">Este valor solo se establece cuando el valor de la propiedad [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) es **\_ \_ \_ error específico del servicio de error** (1066).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-280">This value is only set when the [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="dc5f6-281">Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-281">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-282">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-282">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-283">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-285">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-285">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-286">Tipo de servicio proporcionado a los procesos de llamada.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-286">Type of service provided to calling processes.</span></span>

<span data-ttu-id="dc5f6-287">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="dc5f6-287">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="dc5f6-288">**Controlador de kernel** ("controlador de kernel")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-288">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="dc5f6-289">**Controlador del sistema de archivos** ("controlador del sistema de archivos")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-289">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="dc5f6-290">**Adaptador** ("adaptador")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-290">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="dc5f6-291">**Controlador del reconocedor** ("controlador del reconocedor")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-291">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="dc5f6-292">**Proceso propio** ("propio proceso")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-292">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="dc5f6-293">**Proceso de recurso compartido** ("proceso de recurso compartido")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-293">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="dc5f6-294">**Proceso interactivo** ("proceso interactivo")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-294">**Interactive Process** ("Interactive Process")</span></span>


<span data-ttu-id="dc5f6-295"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dc5f6-295"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="dc5f6-296">Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-296">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-297">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-297">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-298">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-300">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-300">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-301">Indica si se ha iniciado o no el servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-301">Indicates whether or not the service is started.</span></span>

<span data-ttu-id="dc5f6-302">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-302">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-303">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-303">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-304">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-306">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modo de inicio")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-307">Modo de inicio del servicio base de Windows.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-307">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="dc5f6-308"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Arranque** ("arranque")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-308"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="dc5f6-309">Controlador de dispositivo Iniciado por el cargador del sistema operativo (válido solo para los servicios de controlador).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-309">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="dc5f6-310"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("System")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-310"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="dc5f6-311">Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-311">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="dc5f6-312">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-312">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="dc5f6-313"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("auto")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-313"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="dc5f6-314">Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-314">Service to be started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="dc5f6-315">Los servicios automáticos se inician incluso si un usuario no inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-315">Auto services are started even if a user does not log on.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="dc5f6-316"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-316"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="dc5f6-317">Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .</span><span class="sxs-lookup"><span data-stu-id="dc5f6-317">Service to be started by the Service Control Manager when a process calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span> <span data-ttu-id="dc5f6-318">Estos servicios no se inician a menos que un usuario inicie sesión y los inicie.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-318">These services do not start unless a user logs on and starts them.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dc5f6-319"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("deshabilitado")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-319"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="dc5f6-320">Servicio que no se puede iniciar hasta que su StartMode se cambie a automático o manual.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-320">Service that cannot be started until its StartMode is changed to either Auto or Manual.</span></span>

</dd> </dl>

<span data-ttu-id="dc5f6-321">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-321">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-322">**StartName**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-322">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-323">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-325">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de la cuenta de inicio")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-326">Nombre de cuenta con la que se ejecuta un servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-326">Account name under which a service runs.</span></span> <span data-ttu-id="dc5f6-327">Dependiendo del tipo de servicio, el nombre de la cuenta puede tener el formato "nombreDeDominio \\ nombreDeUsuario" o el formato UPN (" *Username@DomainName* ").</span><span class="sxs-lookup"><span data-stu-id="dc5f6-327">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format ("*Username@DomainName*").</span></span> <span data-ttu-id="dc5f6-328">El proceso de servicio se registra con una de estas dos formas cuando se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-328">The service process is logged by using one of these two forms when it runs.</span></span> <span data-ttu-id="dc5f6-329">Si la cuenta pertenece al dominio integrado, ". \\ Se puede especificar username.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-329">If the account belongs to the built-in domain, then ".\\Username" can be specified.</span></span> <span data-ttu-id="dc5f6-330">En el caso de los controladores de kernel o de nivel de sistema, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contiene el nombre de objeto del controlador (es decir, " \\ filesystem \\ RDR" o " \\ controlador \\ XNS") que usa el sistema de e/s para cargar el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-330">For kernel or system-level drivers, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contains the driver object name (that is, "\\FileSystem\\Rdr" or "\\Driver\\Xns") which the I/O system uses to load the device driver.</span></span> <span data-ttu-id="dc5f6-331">Además, si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de e/s basado en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-331">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="dc5f6-332">Ejemplo: "DWDOM \\ admin"</span><span class="sxs-lookup"><span data-stu-id="dc5f6-332">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="dc5f6-333">Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-333">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-334">**State**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-334">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-335">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-336">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-336">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-337">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-338">Estado actual del servicio base.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-338">Current state of the base service.</span></span>

<span data-ttu-id="dc5f6-339">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="dc5f6-339">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="dc5f6-340">**Detenido** ("detenido")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-340">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="dc5f6-341">**Inicio pendiente** ("Inicio pendiente")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-341">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="dc5f6-342">**Detención pendiente** ("detención pendiente")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-342">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="dc5f6-343">En **ejecución** ("en ejecución")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-343">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="dc5f6-344">**Continuar pendiente** ("continuar pendiente")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-344">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="dc5f6-345">**Pausar pendiente** ("pausa pendiente")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-345">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="dc5f6-346">En **pausa** ("en pausa")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-346">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc5f6-347">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-347">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="dc5f6-348"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dc5f6-348"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="dc5f6-349">**Windows Server 2008 y Windows Vista:** Esta propiedad es de solo lectura antes de Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-349">**Windows Server 2008 and Windows Vista:** This property is read-only before Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="dc5f6-350">Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-350">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-351">**Estado**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-351">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-354">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-354">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-355">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-355">Current status of the object.</span></span> <span data-ttu-id="dc5f6-356">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-356">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="dc5f6-357">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-357">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="dc5f6-358">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="dc5f6-358">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="dc5f6-359">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-359">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="dc5f6-360">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-360">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="dc5f6-361">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="dc5f6-361">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dc5f6-362">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-362">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dc5f6-363">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-363">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dc5f6-364">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-364">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc5f6-365">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-365">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dc5f6-366">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-366">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dc5f6-367">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-367">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dc5f6-368">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-368">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dc5f6-369">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-369">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dc5f6-370">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-370">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dc5f6-371">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-371">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dc5f6-372">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-372">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dc5f6-373">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-373">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="dc5f6-374"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dc5f6-374"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="dc5f6-375">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-375">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-376">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-376">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-377">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-378">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-379">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system). CreationClassName "), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class name ")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-379">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).CreationClassName"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-380">Nombre de tipo del sistema que hospeda este servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-380">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="dc5f6-381">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-381">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-382">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-382">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-383">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-384">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-385">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system). Nombre "), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre del sistema ")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-385">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).Name"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-386">Nombre del sistema que hospeda este servicio.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-386">Name of the system that hosts this service.</span></span>

<span data-ttu-id="dc5f6-387">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-387">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-388">**TagId**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-388">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-389">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-391">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ID. de etiqueta")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-391">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-392">Valor de etiqueta único para este servicio en el grupo.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-392">Unique tag value for this service in the group.</span></span> <span data-ttu-id="dc5f6-393">Un valor de 0 (cero) indica que el servicio no tiene una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-393">A value of 0 (zero) indicates that the service does not have a tag.</span></span> <span data-ttu-id="dc5f6-394">Se puede usar una etiqueta para ordenar el inicio del servicio en un grupo de orden de carga mediante la especificación de un vector de orden de etiquetas en el registro ubicado en:</span><span class="sxs-lookup"><span data-stu-id="dc5f6-394">A tag can be used to order service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="dc5f6-395">**HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local GroupOrderList    </span><span class="sxs-lookup"><span data-stu-id="dc5f6-395">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **GroupOrderList**</span></span>

<span data-ttu-id="dc5f6-396">Las etiquetas solo se evalúan para el controlador de kernel y los servicios de tipo de inicio de controlador del sistema de archivos que tienen modos de inicio o de inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-396">Tags are only evaluated for Kernel Driver and File System Driver start type services that have Boot or System start modes.</span></span>

<span data-ttu-id="dc5f6-397">Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-397">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-398">**TotalSessions**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-398">**TotalSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-399">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-399">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-401">Número total de sesiones en el servidor actual.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-401">The total number of sessions on the current server.</span></span> <span data-ttu-id="dc5f6-402">Esto incluye las sesiones conectadas y desconectadas.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-402">This includes both connected and disconnected sessions.</span></span>

</dd> <dt>

<span data-ttu-id="dc5f6-403">**WaitHint**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-403">**WaitHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc5f6-404">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-405">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc5f6-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc5f6-406">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tiempo de espera estimado")</span><span class="sxs-lookup"><span data-stu-id="dc5f6-406">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWaitHint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Estimated Wait Time")</span></span>
</dt> </dl>

<span data-ttu-id="dc5f6-407">Tiempo estimado necesario, en milisegundos, para una operación pendiente de inicio, detención, pausa o continuación.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-407">Estimated time required, in milliseconds, for a pending start, stop, pause, or continue operation.</span></span> <span data-ttu-id="dc5f6-408">Una vez transcurrido el tiempo especificado, el servicio realiza su siguiente llamada al método **SetServiceStatus** con un valor de punto de [**comprobación**](/windows/desktop/CIMWin32Prov/win32-service) incrementado o un cambio en **CurrentState**.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-408">After the specified time has elapsed, the service makes its next call to the **SetServiceStatus** method with either an incremented [**CheckPoint**](/windows/desktop/CIMWin32Prov/win32-service) value or a change in **CurrentState**.</span></span> <span data-ttu-id="dc5f6-409">Si la cantidad de tiempo especificada por **WaitHint** pasa y el **punto de comprobación** no se ha incrementado o **CurrentState** no ha cambiado, el administrador de control de servicios o el programa de control de servicio supone que se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-409">If the amount of time specified by **WaitHint** passes, and **CheckPoint** has not been incremented, or **CurrentState** has not changed, the service control manager or service control program assumes that an error has occurred.</span></span>

<span data-ttu-id="dc5f6-410">Esta propiedad se hereda del [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-410">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc5f6-411">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc5f6-411">Remarks</span></span>

<span data-ttu-id="dc5f6-412">Dado que la clase **Win32 \_ TerminalService** es una subclase de la clase de [**\_ servicio de Win32**](/windows/desktop/CIMWin32Prov/win32-service) , la clase hereda todas las propiedades y los métodos del **\_ servicio Win32**.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-412">Since the **Win32\_TerminalService** class is a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class, the class inherits all properties and methods of **Win32\_Service**.</span></span>

<span data-ttu-id="dc5f6-413">[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) está asociado a **Win32 \_ TerminalService** como la propiedad **Setting** de la [**Asociación \_ TerminalServiceToSetting de Win32**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="dc5f6-413">[**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) is associated to **Win32\_TerminalService** as the **Setting** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="dc5f6-414">[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) está asociado a **Win32 \_ TerminalService** como la propiedad **Setting** de la [**Asociación \_ TSSessionDirectorySetting de Win32**](win32-tssessiondirectorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="dc5f6-414">[**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) is associated to **Win32\_TerminalService** as the **Setting** property of the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) association.</span></span>

<span data-ttu-id="dc5f6-415">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-415">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dc5f6-416">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-416">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="dc5f6-417">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="dc5f6-417">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dc5f6-418">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="dc5f6-418">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc5f6-419">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc5f6-419">Requirements</span></span>



| <span data-ttu-id="dc5f6-420">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc5f6-420">Requirement</span></span> | <span data-ttu-id="dc5f6-421">Value</span><span class="sxs-lookup"><span data-stu-id="dc5f6-421">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc5f6-422">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc5f6-422">Minimum supported client</span></span><br/> | <span data-ttu-id="dc5f6-423">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc5f6-423">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc5f6-424">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc5f6-424">Minimum supported server</span></span><br/> | <span data-ttu-id="dc5f6-425">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc5f6-425">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc5f6-426">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dc5f6-426">Namespace</span></span><br/>                | <span data-ttu-id="dc5f6-427">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="dc5f6-427">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="dc5f6-428">MOF</span><span class="sxs-lookup"><span data-stu-id="dc5f6-428">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc5f6-429"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc5f6-429"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc5f6-430">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc5f6-430">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc5f6-431"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc5f6-431"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc5f6-432">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc5f6-432">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc5f6-433">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-433">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="dc5f6-434">**Win32 \_ TerminalServiceToSetting**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-434">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dt>

[<span data-ttu-id="dc5f6-435">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-435">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> <dt>

[<span data-ttu-id="dc5f6-436">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-436">**Win32\_BaseService**</span></span>](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[<span data-ttu-id="dc5f6-437">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="dc5f6-437">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

