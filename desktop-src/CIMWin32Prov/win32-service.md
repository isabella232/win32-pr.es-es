---
description: Representa un servicio en un equipo que ejecuta Windows.
ms.assetid: 713402d3-ee73-4a6c-afb9-ad8033a4c580
ms.tgt_platform: multiple
title: Win32_Service (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service
- Win32_Service.AcceptPause
- Win32_Service.AcceptStop
- Win32_Service.Caption
- Win32_Service.CheckPoint
- Win32_Service.CreationClassName
- Win32_Service.DelayedAutoStart
- Win32_Service.Description
- Win32_Service.DesktopInteract
- Win32_Service.DisplayName
- Win32_Service.ErrorControl
- Win32_Service.ExitCode
- Win32_Service.InstallDate
- Win32_Service.Name
- Win32_Service.PathName
- Win32_Service.ProcessId
- Win32_Service.ServiceSpecificExitCode
- Win32_Service.ServiceType
- Win32_Service.Started
- Win32_Service.StartMode
- Win32_Service.StartName
- Win32_Service.State
- Win32_Service.Status
- Win32_Service.SystemCreationClassName
- Win32_Service.SystemName
- Win32_Service.TagId
- Win32_Service.WaitHint
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b342282bfa3b49fe72e62cf79377a0ead11276eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080117"
---
# <a name="win32_service-class"></a><span data-ttu-id="ef1b1-103">\_Clase de servicio Win32</span><span class="sxs-lookup"><span data-stu-id="ef1b1-103">Win32\_Service class</span></span>

<span data-ttu-id="ef1b1-104">La [clase WMI](../wmisdk/retrieving-a-class.md) del **\_ servicio Win32** representa un servicio en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-104">The **Win32\_Service** [WMI class](../wmisdk/retrieving-a-class.md) represents a service on a computer system running Windows.</span></span>

<span data-ttu-id="ef1b1-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ef1b1-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1b1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef1b1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D9-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services"), AMENDMENT]
class Win32_Service : Win32_BaseService
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
};
```

## <a name="members"></a><span data-ttu-id="ef1b1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ef1b1-108">Members</span></span>

<span data-ttu-id="ef1b1-109">La clase de **\_ servicio Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ef1b1-109">The **Win32\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="ef1b1-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ef1b1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ef1b1-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ef1b1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ef1b1-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ef1b1-112">Methods</span></span>

<span data-ttu-id="ef1b1-113">La clase de **\_ servicio Win32** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-113">The **Win32\_Service** class has these methods.</span></span>



| <span data-ttu-id="ef1b1-114">Método</span><span class="sxs-lookup"><span data-stu-id="ef1b1-114">Method</span></span>                                                                               | <span data-ttu-id="ef1b1-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef1b1-115">Description</span></span>                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef1b1-116">**Cambio**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-116">**Change**</span></span>](change-method-in-class-win32-service.md)                               | <span data-ttu-id="ef1b1-117">Modifica un servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-117">Modifies a service.</span></span><br/>                                                                       |
| [<span data-ttu-id="ef1b1-118">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-118">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-service.md)             | <span data-ttu-id="ef1b1-119">Modifica el modo de inicio de un servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-119">Modifies the start mode of a service.</span></span><br/>                                                     |
| [<span data-ttu-id="ef1b1-120">**A**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-120">**Create**</span></span>](create-method-in-class-win32-service.md)                               | <span data-ttu-id="ef1b1-121">Crea un nuevo servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-121">Creates a new service.</span></span><br/>                                                                    |
| [<span data-ttu-id="ef1b1-122">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-122">**Delete**</span></span>](delete-method-in-class-win32-service.md)                               | <span data-ttu-id="ef1b1-123">Elimina un servicio existente.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-123">Deletes an existing service.</span></span><br/>                                                              |
| [<span data-ttu-id="ef1b1-124">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-124">**GetSecurityDescriptor**</span></span>](getsecuritydescriptor-method-in-class-win32-service.md) | <span data-ttu-id="ef1b1-125">Devuelve el descriptor de seguridad que controla el acceso al servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-125">Returns the security descriptor that controls access to the service.</span></span><br/>                      |
| [<span data-ttu-id="ef1b1-126">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-126">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-service.md)       | <span data-ttu-id="ef1b1-127">Solicita que un servicio actualice su estado al administrador de servicios.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-127">Requests that a service update its state to the service manager.</span></span><br/>                          |
| [<span data-ttu-id="ef1b1-128">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-128">**PauseService**</span></span>](pauseservice-method-in-class-win32-service.md)                   | <span data-ttu-id="ef1b1-129">Intenta poner un servicio en estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-129">Attempts to place a service in the paused state.</span></span><br/>                                          |
| [<span data-ttu-id="ef1b1-130">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-130">**ResumeService**</span></span>](resumeservice-method-in-class-win32-service.md)                 | <span data-ttu-id="ef1b1-131">Intenta poner un servicio en estado reanudado.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-131">Attempts to place a service in the resumed state.</span></span><br/>                                         |
| [<span data-ttu-id="ef1b1-132">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-132">**SetSecurityDescriptor**</span></span>](setsecuritydescriptor-method-in-class-win32-service.md) | <span data-ttu-id="ef1b1-133">Escribe una versión actualizada del descriptor de seguridad que controla el acceso al servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-133">Writes an updated version of the security descriptor that controls access to the service.</span></span><br/> |
| [<span data-ttu-id="ef1b1-134">**StartService**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-134">**StartService**</span></span>](startservice-method-in-class-win32-service.md)                   | <span data-ttu-id="ef1b1-135">Intenta colocar un servicio en el estado de inicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-135">Attempts to place a service into the startup state.</span></span><br/>                                       |
| [<span data-ttu-id="ef1b1-136">**StopService**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-136">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)                     | <span data-ttu-id="ef1b1-137">Coloca un servicio en estado detenido.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-137">Places a service in the stopped state.</span></span><br/>                                                    |
| [<span data-ttu-id="ef1b1-138">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-138">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-service.md)       | <span data-ttu-id="ef1b1-139">Intenta enviar un código de control definido por el usuario a un servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-139">Attempts to send a user-defined control code to a service.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="ef1b1-140">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ef1b1-140">Properties</span></span>

<span data-ttu-id="ef1b1-141">La clase de **\_ servicio Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-141">The **Win32\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef1b1-142">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-142">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-143">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-145">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures Service \| [**\_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| Service \_ Accept \_ PAUSE \_ Continue"), [**displayName**](../wmisdk/standard-qualifiers.md) ("el servicio acepta la pausa")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-146">Indica si se puede pausar el servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-146">Indicates whether the service can be paused.</span></span>

<span data-ttu-id="ef1b1-147">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-147">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-148">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-148">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-149">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-151">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures Service \| [**\_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status)servicio \| dwControlsAccepted \| \_ \_ Stop"), [**displayName**](../wmisdk/standard-qualifiers.md) ("el servicio acepta la detención")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-151">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-152">Indica si se puede detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-152">Indicates whether the service can be stopped.</span></span>

<span data-ttu-id="ef1b1-153">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-153">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-154">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-157">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-157">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-158">Breve descripción del servicio: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-158">Short description of the service —a one-line string.</span></span>

<span data-ttu-id="ef1b1-159">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-160">**SnapSure**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-160">**CheckPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-161">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-163">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwCheckPoint"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Check Point Count")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Check Point Count")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-164">Valor que el servicio incrementa periódicamente para informar sobre su progreso durante una operación larga de inicio, detención, pausa o continuación.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-164">Value that the service increments periodically to report its progress during a long start, stop, pause, or continue operation.</span></span> <span data-ttu-id="ef1b1-165">Por ejemplo, el servicio incrementa este valor a medida que completa cada paso de su inicialización cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-165">For example, the service increments this value as it completes each step of its initialization when it is starting up.</span></span> <span data-ttu-id="ef1b1-166">El programa de interfaz de usuario que invoca la operación en el servicio usa este valor para realizar el seguimiento del progreso del servicio durante una operación larga.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-166">The user interface program that invokes the operation on the service uses this value to track the progress of the service during a lengthy operation.</span></span> <span data-ttu-id="ef1b1-167">Este valor no es válido y debe ser cero cuando el servicio no tiene pendiente una operación de inicio, detención, pausa o continuación.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-167">This value is not valid and should be zero when the service does not have a start, stop, pause, or continue operation pending.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-168">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-168">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-171">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-171">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-172">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-172">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="ef1b1-173">Cuando se usa con las otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-173">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ef1b1-174">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-174">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-175">**DelayedAutoStart**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-175">**DelayedAutoStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-176">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-178">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api Service \| Structures \| [**\_ retardo \_ auto \_ Start \_ info**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Inicio automático retrasado")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info)\|fDelayedAutostart"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Delayed Auto-Start")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-179">Si es **true**, el servicio se inicia después de que se inicien otros servicios de inicio automático más un breve retraso.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-179">If **True**, the service is started after other auto-start services are started plus a short delay.</span></span>

<span data-ttu-id="ef1b1-180">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows Server 2016 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-181">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-184">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-184">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-185">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-185">Description of the object.</span></span>

<span data-ttu-id="ef1b1-186">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-187">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-187">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-188">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-188">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-190">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| Service \_ Interactive \_ Process"), [**displayName**](../wmisdk/standard-qualifiers.md) ("interactúa con Desktop")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-190">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-191">Indica si el servicio puede crear o comunicarse con Windows en el escritorio y, por tanto, interactuar de algún modo con un usuario.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-191">Indicates whether the service can create or communicate with windows on the desktop, and thus interact in some way with a user.</span></span> <span data-ttu-id="ef1b1-192">Los servicios interactivos deben ejecutarse en la cuenta de sistema local.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-192">Interactive services must run under the Local System account.</span></span> <span data-ttu-id="ef1b1-193">La mayoría de los servicios no son interactivos; es decir, no se comunican con el usuario de ningún modo.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-193">Most services are not interactive; that is, they do not communicate with the user in any way.</span></span>

<span data-ttu-id="ef1b1-194">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-194">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-195">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-195">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-196">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-198">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpDisplayName"), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre para mostrar")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-199">Nombre del servicio tal como se ve en el complemento Servicios.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-199">Name of the service as viewed in the Services snap-in.</span></span> <span data-ttu-id="ef1b1-200">Esta cadena tiene una longitud máxima de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-200">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="ef1b1-201">Tenga en cuenta que el nombre para mostrar y el nombre del servicio (que se almacena en el registro) no son siempre los mismos.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-201">Note that the display name and the service name (which is stored in the registry) are not always the same.</span></span> <span data-ttu-id="ef1b1-202">Por ejemplo, el servicio de cliente DHCP tiene el nombre de servicio DHCP, pero el cliente DHCP de nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-202">For example, the DHCP Client service has the service name Dhcp but the display name DHCP Client.</span></span> <span data-ttu-id="ef1b1-203">El nombre se conserva en las mayúsculas y minúsculas en el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-203">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="ef1b1-204">Sin embargo, las comparaciones de **displayName** siempre distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-204">However, **DisplayName** comparisons are always case-insensitive.</span></span>

<span data-ttu-id="ef1b1-205">Constraint: acepta el mismo valor que la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="ef1b1-205">Constraint: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="ef1b1-206">Ejemplo: "Endisco"</span><span class="sxs-lookup"><span data-stu-id="ef1b1-206">Example: "Atdisk"</span></span>

<span data-ttu-id="ef1b1-207">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-207">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-208">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-208">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-209">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-211">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**displayName**](../wmisdk/standard-qualifiers.md) ("gravedad del error de inicio")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-211">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-212">Gravedad del error si este servicio no se inicia durante el inicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-212">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="ef1b1-213">El valor indica la acción realizada por el programa de inicio si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-213">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="ef1b1-214">El sistema registra todos los errores.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-214">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="ef1b1-215"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Omitir** ("omitir")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-215"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="ef1b1-216">No se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-216">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="ef1b1-217"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("normal")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-217"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="ef1b1-218">Se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-218">User is notified.</span></span> <span data-ttu-id="ef1b1-219">Normalmente, se trata de un cuadro de mensaje que informa al usuario del problema.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-219">Usually this will be a message box display notifying the user of the problem.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="ef1b1-220"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("grave")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-220"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="ef1b1-221">El sistema se reinicia con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-221">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="ef1b1-222"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** ("crítico")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-222"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="ef1b1-223">El sistema intenta reiniciarse con una configuración válida.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-223">System attempts to restart with a good configuration.</span></span> <span data-ttu-id="ef1b1-224">Si el servicio no se inicia por segunda vez, se produce un error de inicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-224">If the service fails to start a second time, startup fails.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef1b1-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="ef1b1-226">Se desconoce la gravedad del error.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-226">Severity of the error is unknown.</span></span>

</dd> </dl>

<span data-ttu-id="ef1b1-227">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-227">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-228">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-228">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-229">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-231">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**displayName**](../wmisdk/standard-qualifiers.md) ("código de salida")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-232">Código de error de Windows que define los errores detectados al iniciar o detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-232">Windows error code that defines errors encountered in starting or stopping the service.</span></span> <span data-ttu-id="ef1b1-233">Esta propiedad se establece en **\_ \_ \_ error específico del servicio de error** (1066) cuando el error es exclusivo del servicio representado por esta clase, y la información sobre el error está disponible en la propiedad **ServiceSpecificExitCode** .</span><span class="sxs-lookup"><span data-stu-id="ef1b1-233">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="ef1b1-234">El servicio establece este valor en **ningún \_ error** cuando se ejecuta y de nuevo tras la terminación normal.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-234">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="ef1b1-235">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-235">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-236">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-236">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-237">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-237">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-239">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-240">El objeto de fecha está instalado.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-240">Date object is installed.</span></span> <span data-ttu-id="ef1b1-241">Esta propiedad no requiere un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-241">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ef1b1-242">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-243">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-243">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-244">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-246">Calificadores: [ **clave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="ef1b1-246">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-247">Identificador único del servicio que proporciona una indicación de la funcionalidad que se administra.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-247">Unique identifier of the service that provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="ef1b1-248">Esta funcionalidad se describe en la propiedad **Description** del objeto.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-248">This functionality is described in the **Description** property of the object.</span></span>

<span data-ttu-id="ef1b1-249">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-249">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-250">**PathName**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-250">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-251">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-253">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**displayName**](../wmisdk/standard-qualifiers.md) ("File path name")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-253">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-254">Ruta de acceso completa al archivo binario del servicio que implementa el servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-254">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="ef1b1-255">Ejemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="ef1b1-255">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="ef1b1-256">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-256">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-257">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-257">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-258">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-258">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-260">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**Service \_ status \_ Process**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Process ID")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-260">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS\_PROCESS**](/windows/win32/api/winsvc/ns-winsvc-service_status_process)\|dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-261">Identificador de proceso del servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-261">Process identifier of the service.</span></span>

<span data-ttu-id="ef1b1-262">Ejemplo: 324</span><span class="sxs-lookup"><span data-stu-id="ef1b1-262">Example: 324</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-263">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-263">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-264">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-266">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**displayName**](../wmisdk/standard-qualifiers.md) ("código de salida específico del servidor")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-266">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-267">Código de error específico del servicio para los errores que se producen mientras el servicio se está iniciando o deteniendo.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-267">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="ef1b1-268">Los códigos de salida se definen mediante el servicio representado por esta clase.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-268">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="ef1b1-269">Este valor solo se establece cuando el valor de la propiedad **ExitCode** es **\_ \_ \_ error específico del servicio de error** (1066).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-269">This value is only set when the **ExitCode** property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="ef1b1-270">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-270">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-271">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-271">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-272">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-273">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-274">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-274">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-275">Tipo de servicio proporcionado a los procesos de llamada.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-275">Type of service provided to calling processes.</span></span>

<span data-ttu-id="ef1b1-276">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="ef1b1-276">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="ef1b1-277">**Controlador de kernel** ("controlador de kernel")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-277">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="ef1b1-278">**Controlador del sistema de archivos** ("controlador del sistema de archivos")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-278">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="ef1b1-279">**Adaptador** ("adaptador")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-279">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="ef1b1-280">**Controlador del reconocedor** ("controlador del reconocedor")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-280">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="ef1b1-281">**Proceso propio** ("propio proceso")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-281">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="ef1b1-282">**Proceso de recurso compartido** ("proceso de recurso compartido")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-282">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="ef1b1-283">**Proceso interactivo** ("proceso interactivo")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-283">**Interactive Process** ("Interactive Process")</span></span>


<span data-ttu-id="ef1b1-284"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ef1b1-284"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="ef1b1-285">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-285">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-286">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-286">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-287">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-289">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-290">Indica si se ha iniciado o no el servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-290">Indicates whether or not the service is started.</span></span>

<span data-ttu-id="ef1b1-291">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-291">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-292">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-292">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-293">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-295">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("modo de inicio")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-295">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-296">Modo de inicio del servicio base de Windows.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-296">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="ef1b1-297"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Arranque** ("arranque")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-297"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="ef1b1-298">Controlador de dispositivo Iniciado por el cargador del sistema operativo (válido solo para los servicios de controlador).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-298">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="ef1b1-299"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("System")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-299"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="ef1b1-300">Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-300">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="ef1b1-301">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-301">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="ef1b1-302"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("auto")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-302"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="ef1b1-303">Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-303">Service to be started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="ef1b1-304">Los servicios automáticos se inician incluso si un usuario no inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-304">Auto services are started even if a user does not log on.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="ef1b1-305"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-305"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="ef1b1-306">Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="ef1b1-306">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="ef1b1-307">Estos servicios no se inician a menos que un usuario inicie sesión y los inicie.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-307">These services do not start unless a user logs on and starts them.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ef1b1-308"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("deshabilitado")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-308"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="ef1b1-309">Servicio que no se puede iniciar hasta que su StartMode se cambie a automático o manual.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-309">Service that cannot be started until its StartMode is changed to either Auto or Manual.</span></span>

</dd> </dl>

<span data-ttu-id="ef1b1-310">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-310">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-311">**StartName**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-311">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-312">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-314">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de la cuenta de inicio")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-314">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-315">Nombre de cuenta con la que se ejecuta un servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-315">Account name under which a service runs.</span></span> <span data-ttu-id="ef1b1-316">Dependiendo del tipo de servicio, el nombre de la cuenta puede tener el formato "nombreDeDominio \\ nombreDeUsuario" o el formato UPN (" *Username@DomainName* ").</span><span class="sxs-lookup"><span data-stu-id="ef1b1-316">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format ("*Username@DomainName*").</span></span> <span data-ttu-id="ef1b1-317">El proceso de servicio se registra con una de estas dos formas cuando se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-317">The service process is logged by using one of these two forms when it runs.</span></span> <span data-ttu-id="ef1b1-318">Si la cuenta pertenece al dominio integrado, ". \\ Se puede especificar username.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-318">If the account belongs to the built-in domain, then ".\\Username" can be specified.</span></span> <span data-ttu-id="ef1b1-319">En el caso de los controladores de kernel o de nivel de sistema, **StartName** contiene el nombre de objeto del controlador (es decir, " \\ filesystem \\ RDR" o " \\ controlador \\ XNS") que usa el sistema de e/s para cargar el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-319">For kernel or system-level drivers, **StartName** contains the driver object name (that is, "\\FileSystem\\Rdr" or "\\Driver\\Xns") which the I/O system uses to load the device driver.</span></span> <span data-ttu-id="ef1b1-320">Además, si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de e/s basado en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-320">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="ef1b1-321">Ejemplo: "DWDOM \\ admin"</span><span class="sxs-lookup"><span data-stu-id="ef1b1-321">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="ef1b1-322">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-322">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-323">**State**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-323">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-325">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-325">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-326">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**displayName**](../wmisdk/standard-qualifiers.md) ("State")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-326">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-327">Estado actual del servicio base.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-327">Current state of the base service.</span></span>

<span data-ttu-id="ef1b1-328">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="ef1b1-328">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="ef1b1-329">**Detenido** ("detenido")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-329">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="ef1b1-330">**Inicio pendiente** ("Inicio pendiente")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-330">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="ef1b1-331">**Detención pendiente** ("detención pendiente")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-331">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="ef1b1-332">En **ejecución** ("en ejecución")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-332">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="ef1b1-333">**Continuar pendiente** ("continuar pendiente")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-333">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="ef1b1-334">**Pausar pendiente** ("pausa pendiente")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-334">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ef1b1-335">En **pausa** ("en pausa")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-335">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef1b1-336">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-336">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="ef1b1-337"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ef1b1-337"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="ef1b1-338">**Windows Server 2008 y Windows Vista:** Esta propiedad es de solo lectura antes de Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-338">**Windows Server 2008 and Windows Vista:** This property is read-only before Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="ef1b1-339">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-339">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-340">**Estado**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-340">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-341">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-343">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-343">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-344">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-344">Current status of the object.</span></span> <span data-ttu-id="ef1b1-345">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-345">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ef1b1-346">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-346">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ef1b1-347">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="ef1b1-347">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ef1b1-348">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-348">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ef1b1-349">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-349">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ef1b1-350">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ef1b1-351">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="ef1b1-351">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ef1b1-352">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-352">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ef1b1-353">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-353">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ef1b1-354">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-354">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef1b1-355">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-355">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ef1b1-356">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-356">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ef1b1-357">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-357">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ef1b1-358">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-358">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ef1b1-359">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-359">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ef1b1-360">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-360">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ef1b1-361">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-361">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ef1b1-362">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-362">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ef1b1-363">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-363">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef1b1-364">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-364">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-365">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-367">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" System Class name ")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-367">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-368">Nombre de tipo del sistema que hospeda este servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-368">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="ef1b1-369">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-369">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-370">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-370">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-371">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-373">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre del sistema ")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-373">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-374">Nombre del sistema que hospeda este servicio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-374">Name of the system that hosts this service.</span></span>

<span data-ttu-id="ef1b1-375">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-375">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-376">**TagId**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-376">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-377">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-377">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-378">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-379">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**displayName**](../wmisdk/standard-qualifiers.md) ("ID. de etiqueta")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-379">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-380">Valor de etiqueta único para este servicio en el grupo.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-380">Unique tag value for this service in the group.</span></span> <span data-ttu-id="ef1b1-381">Un valor de 0 (cero) indica que el servicio no tiene una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-381">A value of 0 (zero) indicates that the service does not have a tag.</span></span> <span data-ttu-id="ef1b1-382">Se puede usar una etiqueta para ordenar el inicio del servicio en un grupo de orden de carga mediante la especificación de un vector de orden de etiquetas en el registro ubicado en:</span><span class="sxs-lookup"><span data-stu-id="ef1b1-382">A tag can be used to order service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="ef1b1-383">**HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local GroupOrderList    </span><span class="sxs-lookup"><span data-stu-id="ef1b1-383">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **GroupOrderList**</span></span>

<span data-ttu-id="ef1b1-384">Las etiquetas solo se evalúan para el controlador de kernel y los servicios de tipo de inicio de controlador del sistema de archivos que tienen modos de inicio o de inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-384">Tags are only evaluated for Kernel Driver and File System Driver start type services that have Boot or System start modes.</span></span>

<span data-ttu-id="ef1b1-385">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-385">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-386">**WaitHint**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-386">**WaitHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1b1-387">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-387">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef1b1-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1b1-389">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**displayName**](../wmisdk/standard-qualifiers.md) ("tiempo de espera estimado")</span><span class="sxs-lookup"><span data-stu-id="ef1b1-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWaitHint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Estimated Wait Time")</span></span>
</dt> </dl>

<span data-ttu-id="ef1b1-390">Tiempo estimado necesario, en milisegundos, para una operación pendiente de inicio, detención, pausa o continuación.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-390">Estimated time required, in milliseconds, for a pending start, stop, pause, or continue operation.</span></span> <span data-ttu-id="ef1b1-391">Una vez transcurrido el tiempo especificado, el servicio realiza su siguiente llamada al método **SetServiceStatus** con un valor de punto de **comprobación** incrementado o un cambio en **CurrentState**.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-391">After the specified time has elapsed, the service makes its next call to the **SetServiceStatus** method with either an incremented **CheckPoint** value or a change in **CurrentState**.</span></span> <span data-ttu-id="ef1b1-392">Si la cantidad de tiempo especificada por **WaitHint** pasa y el **punto de comprobación** no se ha incrementado o **CurrentState** no ha cambiado, el administrador de control de servicios o el programa de control de servicio supone que se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-392">If the amount of time specified by **WaitHint** passes, and **CheckPoint** has not been incremented, or **CurrentState** has not changed, the service control manager or service control program assumes that an error has occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef1b1-393">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef1b1-393">Remarks</span></span>

<span data-ttu-id="ef1b1-394">La clase de **\_ servicio Win32** se deriva de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-394">The **Win32\_Service** class is derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="ef1b1-395">La forma en que se administra un equipo específico depende en gran medida del rol que desempeña el equipo.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-395">The way in which you manage a specific computer depends greatly on the role that computer plays.</span></span> <span data-ttu-id="ef1b1-396">Por ejemplo, en general, se supervisan distintos aspectos de un servidor DNS que un servidor DHCP.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-396">For example, you generally monitor different aspects of a DNS server than a DHCP server.</span></span> <span data-ttu-id="ef1b1-397">Aunque ninguna propiedad puede indicar si un equipo determinado es un servidor de base de datos, un servidor de correo electrónico o un servidor multimedia, a menudo puede identificar el rol que reproduce un equipo mediante la identificación de los servicios instalados en él.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-397">Although no single property can tell you whether a particular computer is a database server, an e-mail server, or a multimedia server, you can often identify the role a computer plays by identifying the services installed on it.</span></span>

<span data-ttu-id="ef1b1-398">En organizaciones de gran tamaño, es probable que solo uno de los servicios principales (como el correo electrónico) esté instalado en un solo equipo.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-398">In large organizations, only one of the major services (such as e-mail) is likely to be installed on a single computer.</span></span> <span data-ttu-id="ef1b1-399">Es poco habitual que un servidor de correo también funcione como servidor de Microsoft® archivos del reproductor de Windows Media® Technologies.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-399">It would be unusual for a mail server to also perform as a server for Microsoft® Windows Media® technologies player files.</span></span> <span data-ttu-id="ef1b1-400">Debido a esto, la identificación de un servicio instalado en un equipo puede ayudar a identificar el rol del equipo en la red.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-400">Because of this, identifying a service installed on a computer can help identify the computer's role in the network.</span></span> <span data-ttu-id="ef1b1-401">Si el servicio Microsoft® Exchange Server está instalado y en ejecución en un equipo, por lo general es seguro suponer que este equipo funciona como un servidor de correo.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-401">If the Microsoft® Exchange Server service is installed and running on a computer, it is generally safe to assume that this computer functions as a mail server.</span></span>

<span data-ttu-id="ef1b1-402">Puede utilizar la clase de **\_ servicio Win32** de WMI para enumerar los servicios instalados en un equipo.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-402">You can use the WMI **Win32\_Service** class to enumerate the services installed on a computer.</span></span> <span data-ttu-id="ef1b1-403">Además, puede usar esta clase para determinar si esos servicios se están ejecutando actualmente y para devolver cualquier otra información necesaria sobre el servicio y cómo se ha configurado.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-403">In addition, you can use this class to determine whether those services are currently running and to return any other required information about that service and how it has been configured.</span></span>

<span data-ttu-id="ef1b1-404">Una aplicación de servicio se ajusta a las reglas de la interfaz del administrador de control de servicios (SCM) y un usuario puede iniciarla automáticamente en el inicio del sistema a través de la utilidad servicios del panel de control, o bien mediante una aplicación que usa las funciones de servicio incluidas en la API de Windows.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-404">A service application conforms to the interface rules of the Service Control Manager (SCM), and can be started by a user automatically at system start through the Services control panel utility, or by an application that uses the service functions included in the Windows API.</span></span> <span data-ttu-id="ef1b1-405">Los servicios pueden iniciarse cuando no haya usuarios con sesión iniciada en el equipo.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-405">Services can start when there are no users logged on to the computer.</span></span>

<span data-ttu-id="ef1b1-406">Un usuario que se conecta desde un equipo remoto debe tener el privilegio de **\_ \_ conexión SC Manager** habilitado para poder enumerar esta clase.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-406">A user connecting from a remote computer must have the **SC\_MANAGER\_CONNECT** privilege enabled to be able to enumerate this class.</span></span> <span data-ttu-id="ef1b1-407">Para obtener más información, consulte [seguridad del servicio y derechos de acceso](../services/service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-407">For more information, see [Service Security and Access Rights](../services/service-security-and-access-rights.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ef1b1-408">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ef1b1-408">Examples</span></span>

<span data-ttu-id="ef1b1-409">La [consulta PS-WMI que devuelve el servicio "estado" en un grupo de dispositivos ejemplo de](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) PowerShell en la galería de TechNet usa el **\_ servicio Win32** para crear una lista de dispositivos a partir de Active Directory y, a continuación, consultar cada dispositivo que responde con pingfor un servicio específico en ejecución.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-409">The [PS- WMI Query that returns Service 'State' on a group of devices](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) PowerShell sample on TechNet Gallery uses **Win32\_Service** to create a list of devices from Active Directory, and then query each device that responds with pingfor a specific service running.</span></span>

<span data-ttu-id="ef1b1-410">El ejemplo de PowerShell para [informes de servidor](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) en la galería de TechNet utiliza el **\_ servicio Win32** para recopilar información del servidor y publicar en un documento de Word.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-410">The [Server Report](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell sample on TechNet Gallery uses **Win32\_Service** to gather server information and publish in Word document.</span></span>

<span data-ttu-id="ef1b1-411">En el siguiente ejemplo de código de VBScript se muestran todos los servicios instalados actualmente.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-411">The following VBScript code sample displays all currently installed services.</span></span>


```VB
for each Service in _ 
    GetObject("winmgmts:").InstancesOf ("Win32_Service")
 WScript.Echo ""
 WScript.Echo Service.Name

 description = Service.Description 
 if IsNull(description) then description = "<No description>"

 pathName = Service.PathName
 if IsNull(pathName) then pathName = "<No path>"

 startName = Service.StartName
 if IsNull(startName) then startName = "<None>"

 WScript.Echo "  Description:  ", description
 WScript.Echo "  Executable:   ", pathName
 WScript.Echo "  Status:       ", Service.Status
 WScript.Echo "  State:        ", Service.State
 WScript.Echo "  Start Mode:   ", Service.StartMode
 Wscript.Echo "  Start Name:   ", startName
next
```



<span data-ttu-id="ef1b1-412">El siguiente ejemplo de código de VBScript describe los servicios en pausa, en ejecución y detenido en el equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-412">The following VBScript code sample describes the paused, running, and stopped services on the specified computer.</span></span>


```VB
On Error Resume Next
 StateString = "Paused,Running,Stopped"
 StateArray = Split(StateString, ",", -1, 1) 
 ComputerName = InputBox("Enter the computer name", "List Service", "localhost")

 For x = 0 to Ubound (StateArray)
 Set Services = GetObject("winmgmts:\\" & ComputerName & "\Root\CIMv2").ExecQuery("SELECT * FROM Win32_Service where State='" & StateArray(x) & "'")
 
 For Each Service in Services
  SList = SList & Service.Name & VBlf 
 Next

 WScript.Echo StateArray(x) & " Services: " & VBlf & SList
 SList = ""

Next
```



<span data-ttu-id="ef1b1-413">El siguiente script Perl muestra cómo recuperar una lista de los servicios en ejecución de las instancias del **\_ servicio de Win32**.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-413">The following Perl script demonstrates how to retrieve a list of running services from instances of **Win32\_Service**.</span></span>


```
use strict;
use Win32::OLE;

my ( $ServiceSet, $Service );

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE State=\"Running\""); };
unless ($@)
{
 print "\n";
 foreach $Service (in $ServiceSet) 
 {
  print $Service->{Name}, "\n";
  if( $Service->{Description} ) 
   {
    print "  $Service->{Description}\n";
   }
  else
   {
    print "  <No description>\n";
   }
  print "  Process ID: ", $Service->{ProcessId}, "\n";
  print "  Start Mode: ", $Service->{StartMode}, "\n";
  print "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="ef1b1-414">En el siguiente \# ejemplo de c se usa [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) para recuperar todos los servicios que se están ejecutando en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-414">The following c\# sample uses [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) to retrieve all the running services on the local machine.</span></span>


```CSharp
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Service");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["State"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Status"].ToString());
                
                //Console.WriteLine(cimObj.CimInstanceProperties["NetworkAddress"].ToString());
                Console.WriteLine();

            }

            Console.ReadLine();
        }
    
```



<span data-ttu-id="ef1b1-415">El siguiente \# ejemplo de código C usa el espacio de nombres [System. Management](/dotnet/api/system.management) para recuperar todos los servicios en ejecución en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-415">The following C\# code sample uses [System.Management](/dotnet/api/system.management) namespace to retrieve all running services on the local machine.</span></span>

> [!Note]  
> <span data-ttu-id="ef1b1-416">[System. Management](/dotnet/api/system.management) contiene las clases originales utilizadas para tener acceso a WMI. sin embargo, se consideran más lentos y, por lo general, no se escalan, así como sus homólogos [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ef1b1-416">[System.Management](/dotnet/api/system.management) contains the original classes used to access WMI; however, they are considered slower and generally do not scale as well as their [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) counterparts.</span></span>

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_Service");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("State : {0}", m["State"]);
                Console.WriteLine("Status : {0}", m["Status"]);
                Console.WriteLine();
            }

            Console.ReadLine();


        }
```



## <a name="requirements"></a><span data-ttu-id="ef1b1-417">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef1b1-417">Requirements</span></span>



| <span data-ttu-id="ef1b1-418">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef1b1-418">Requirement</span></span> | <span data-ttu-id="ef1b1-419">Value</span><span class="sxs-lookup"><span data-stu-id="ef1b1-419">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1b1-420">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef1b1-420">Minimum supported client</span></span><br/> | <span data-ttu-id="ef1b1-421">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef1b1-421">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef1b1-422">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef1b1-422">Minimum supported server</span></span><br/> | <span data-ttu-id="ef1b1-423">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef1b1-423">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef1b1-424">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ef1b1-424">Namespace</span></span><br/>                | <span data-ttu-id="ef1b1-425">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ef1b1-425">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ef1b1-426">MOF</span><span class="sxs-lookup"><span data-stu-id="ef1b1-426">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef1b1-427"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef1b1-427"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef1b1-428">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef1b1-428">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef1b1-429"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef1b1-429"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef1b1-430">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef1b1-430">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef1b1-431">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-431">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="ef1b1-432">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="ef1b1-432">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="ef1b1-433">Tareas WMI: servicios</span><span class="sxs-lookup"><span data-stu-id="ef1b1-433">WMI Tasks: Services</span></span>](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 
