---
description: La \_ clase WMI abstracta BaseService de Win32 representa objetos ejecutables que se instalan en una base de datos del registro mantenida por el administrador de control de servicios.
ms.assetid: 63673df9-3e41-4668-98fe-dc0e048328c1
ms.tgt_platform: multiple
title: Win32_BaseService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService
- Win32_BaseService.AcceptPause
- Win32_BaseService.AcceptStop
- Win32_BaseService.Caption
- Win32_BaseService.CreationClassName
- Win32_BaseService.Description
- Win32_BaseService.DesktopInteract
- Win32_BaseService.DisplayName
- Win32_BaseService.ErrorControl
- Win32_BaseService.ExitCode
- Win32_BaseService.InstallDate
- Win32_BaseService.Name
- Win32_BaseService.PathName
- Win32_BaseService.ServiceSpecificExitCode
- Win32_BaseService.ServiceType
- Win32_BaseService.Started
- Win32_BaseService.StartMode
- Win32_BaseService.StartName
- Win32_BaseService.State
- Win32_BaseService.Status
- Win32_BaseService.SystemCreationClassName
- Win32_BaseService.SystemName
- Win32_BaseService.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b46f3b4bd37770a5f3a7c1a2d2faa93d49bc079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153431"
---
# <a name="win32_baseservice-class"></a><span data-ttu-id="1696b-103">\_Clase Win32 BaseService</span><span class="sxs-lookup"><span data-stu-id="1696b-103">Win32\_BaseService class</span></span>

<span data-ttu-id="1696b-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) abstracta **\_ BaseService de Win32** representa objetos ejecutables que se instalan en una base de datos del registro mantenida por el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="1696b-104">The **Win32\_BaseService** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents executable objects that are installed in a registry database maintained by the Service Control Manager.</span></span> <span data-ttu-id="1696b-105">El archivo ejecutable asociado a un servicio se puede iniciar en el momento de arranque mediante un programa de arranque o el sistema.</span><span class="sxs-lookup"><span data-stu-id="1696b-105">The executable file associated with a service can be started at boot time by a boot program or by the system.</span></span> <span data-ttu-id="1696b-106">También se puede iniciar a petición mediante el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="1696b-106">It can also be started on-demand by the Service Control Manager.</span></span> <span data-ttu-id="1696b-107">Cualquier servicio o proceso que no es propiedad de un usuario específico, y que proporciona una interfaz a alguna funcionalidad compatible con el sistema del equipo, es un descendiente (o miembro) de esta clase.</span><span class="sxs-lookup"><span data-stu-id="1696b-107">Any service or process that is not owned by a specific user, and that provides an interface to some functionality supported by the computer system, is a descendant (or member) of this class.</span></span>

<span data-ttu-id="1696b-108">Ejemplo: el servicio de cliente del Protocolo de configuración dinámica de host (DHCP) en un equipo con Windows Server.</span><span class="sxs-lookup"><span data-stu-id="1696b-108">Example: The dynamic host configuration protocol (DHCP) client service on a computer system running Windows Server.</span></span>

<span data-ttu-id="1696b-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1696b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1696b-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="1696b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1696b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1696b-111">Syntax</span></span>

``` syntax
[SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C4C4-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("System Drivers and Services"), AMENDMENT]
class Win32_BaseService : CIM_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  string   CreationClassName;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
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
};
```

## <a name="members"></a><span data-ttu-id="1696b-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="1696b-112">Members</span></span>

<span data-ttu-id="1696b-113">La **clase \_ BaseService de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1696b-113">The **Win32\_BaseService** class has these types of members:</span></span>

-   [<span data-ttu-id="1696b-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="1696b-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="1696b-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1696b-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1696b-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="1696b-116">Methods</span></span>

<span data-ttu-id="1696b-117">La clase **Win32 \_ BaseService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1696b-117">The **Win32\_BaseService** class has these methods.</span></span>



| <span data-ttu-id="1696b-118">Método</span><span class="sxs-lookup"><span data-stu-id="1696b-118">Method</span></span>                                                                             | <span data-ttu-id="1696b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1696b-119">Description</span></span>                                                                   |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="1696b-120">**Cambio**</span><span class="sxs-lookup"><span data-stu-id="1696b-120">**Change**</span></span>](change-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="1696b-121">Modifica un servicio.</span><span class="sxs-lookup"><span data-stu-id="1696b-121">Modifies a service.</span></span><br/>                                                |
| [<span data-ttu-id="1696b-122">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="1696b-122">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-baseservice.md)       | <span data-ttu-id="1696b-123">Modifica el modo de inicio de un servicio.</span><span class="sxs-lookup"><span data-stu-id="1696b-123">Modifies the start mode of a service.</span></span><br/>                              |
| [<span data-ttu-id="1696b-124">**A**</span><span class="sxs-lookup"><span data-stu-id="1696b-124">**Create**</span></span>](create-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="1696b-125">Crea un nuevo servicio.</span><span class="sxs-lookup"><span data-stu-id="1696b-125">Creates a new service.</span></span><br/>                                             |
| [<span data-ttu-id="1696b-126">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="1696b-126">**Delete**</span></span>](delete-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="1696b-127">Elimina un servicio existente.</span><span class="sxs-lookup"><span data-stu-id="1696b-127">Deletes an existing service.</span></span><br/>                                       |
| [<span data-ttu-id="1696b-128">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="1696b-128">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-baseservice.md) | <span data-ttu-id="1696b-129">Solicita que el servicio actualice su estado al administrador de servicios.</span><span class="sxs-lookup"><span data-stu-id="1696b-129">Requests that the service update its state to the service manager.</span></span><br/> |
| [<span data-ttu-id="1696b-130">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="1696b-130">**PauseService**</span></span>](pauseservice-method-in-class-win32-baseservice.md)             | <span data-ttu-id="1696b-131">Intenta poner el servicio en estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="1696b-131">Attempts to place the service in the paused state.</span></span><br/>                 |
| [<span data-ttu-id="1696b-132">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="1696b-132">**ResumeService**</span></span>](resumeservice-method-in-class-win32-baseservice.md)           | <span data-ttu-id="1696b-133">Intenta poner el servicio en estado reanudado.</span><span class="sxs-lookup"><span data-stu-id="1696b-133">Attempts to place the service in the resumed state.</span></span><br/>                |
| [<span data-ttu-id="1696b-134">**StartService**</span><span class="sxs-lookup"><span data-stu-id="1696b-134">**StartService**</span></span>](startservice-method-in-class-win32-baseservice.md)             | <span data-ttu-id="1696b-135">Intenta poner el servicio en su estado de inicio.</span><span class="sxs-lookup"><span data-stu-id="1696b-135">Attempts to place the service into its startup state.</span></span><br/>              |
| [<span data-ttu-id="1696b-136">**StopService**</span><span class="sxs-lookup"><span data-stu-id="1696b-136">**StopService**</span></span>](stopservice-method-in-class-win32-baseservice.md)               | <span data-ttu-id="1696b-137">Método de clase que coloca el servicio en estado detenido.</span><span class="sxs-lookup"><span data-stu-id="1696b-137">Class method that places the service in the stopped state.</span></span><br/>         |
| [<span data-ttu-id="1696b-138">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="1696b-138">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-baseservice.md) | <span data-ttu-id="1696b-139">Intenta enviar un código de control definido por el usuario a un servicio.</span><span class="sxs-lookup"><span data-stu-id="1696b-139">Attempts to send a user-defined control code to a service.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="1696b-140">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1696b-140">Properties</span></span>

<span data-ttu-id="1696b-141">La **clase \_ BaseService de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1696b-141">The **Win32\_BaseService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1696b-142">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="1696b-142">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-143">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1696b-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-145">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures Service \| [**\_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| Service \_ Accept \_ PAUSE \_ Continue"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("el servicio acepta la pausa")</span><span class="sxs-lookup"><span data-stu-id="1696b-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-146">El servicio se puede pausar.</span><span class="sxs-lookup"><span data-stu-id="1696b-146">Service can be paused.</span></span>

</dd> <dt>

<span data-ttu-id="1696b-147">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="1696b-147">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-148">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1696b-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-150">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures Service \| [**\_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status)servicio \| dwControlsAccepted \| \_ \_ Stop"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("el servicio acepta la detención")</span><span class="sxs-lookup"><span data-stu-id="1696b-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-151">Se puede detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="1696b-151">Service can be stopped.</span></span>

</dd> <dt>

<span data-ttu-id="1696b-152">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1696b-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1696b-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-155">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1696b-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-156">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="1696b-156">Short description of the object.</span></span>

<span data-ttu-id="1696b-157">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1696b-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1696b-158">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1696b-158">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1696b-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-161">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="1696b-161">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-162">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="1696b-162">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="1696b-163">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="1696b-163">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1696b-164">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1696b-164">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1696b-165">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1696b-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1696b-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-168">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="1696b-168">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-169">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="1696b-169">Description of the object.</span></span>

<span data-ttu-id="1696b-170">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1696b-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1696b-171">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="1696b-171">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-172">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1696b-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-174">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| Service \_ Interactive \_ Process"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("interactúa con Desktop")</span><span class="sxs-lookup"><span data-stu-id="1696b-174">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-175">El servicio puede crear o comunicarse con Windows en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="1696b-175">Service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="1696b-176">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="1696b-176">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1696b-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-179">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpDisplayName"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre para mostrar")</span><span class="sxs-lookup"><span data-stu-id="1696b-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-180">Nombre para mostrar del servicio.</span><span class="sxs-lookup"><span data-stu-id="1696b-180">Display name of the service.</span></span> <span data-ttu-id="1696b-181">Esta cadena tiene una longitud máxima de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="1696b-181">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="1696b-182">El nombre se conserva en las mayúsculas y minúsculas en el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="1696b-182">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="1696b-183">Las comparaciones de **displayName** siempre distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1696b-183">Comparisons of **DisplayName** are always case-insensitive.</span></span>

<span data-ttu-id="1696b-184">Constraints: acepta el mismo valor que la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="1696b-184">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="1696b-185">Ejemplo: "Endisco"</span><span class="sxs-lookup"><span data-stu-id="1696b-185">Example: "Atdisk"</span></span>

</dd> <dt>

<span data-ttu-id="1696b-186">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="1696b-186">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1696b-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-189">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("gravedad del error de inicio")</span><span class="sxs-lookup"><span data-stu-id="1696b-189">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-190">Gravedad del error.</span><span class="sxs-lookup"><span data-stu-id="1696b-190">Severity of the error.</span></span> <span data-ttu-id="1696b-191">No se puede iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="1696b-191">Service fails to start.</span></span> <span data-ttu-id="1696b-192">El valor indica la acción realizada por el programa de inicio si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="1696b-192">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="1696b-193">El sistema registra todos los errores.</span><span class="sxs-lookup"><span data-stu-id="1696b-193">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="1696b-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Omitir** ("omitir")</span><span class="sxs-lookup"><span data-stu-id="1696b-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="1696b-195">No se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="1696b-195">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="1696b-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("normal")</span><span class="sxs-lookup"><span data-stu-id="1696b-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="1696b-197">Se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="1696b-197">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="1696b-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("grave")</span><span class="sxs-lookup"><span data-stu-id="1696b-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="1696b-199">El sistema se reinició con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="1696b-199">System restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="1696b-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** ("crítico")</span><span class="sxs-lookup"><span data-stu-id="1696b-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="1696b-201">El sistema intenta reiniciarse con una configuración válida.</span><span class="sxs-lookup"><span data-stu-id="1696b-201">System attempts to restart with a good configuration.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1696b-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="1696b-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="1696b-203">Acción realizada no especificada.</span><span class="sxs-lookup"><span data-stu-id="1696b-203">Action taken is unspecified.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1696b-204">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="1696b-204">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-205">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1696b-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-207">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("código de salida")</span><span class="sxs-lookup"><span data-stu-id="1696b-207">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-208">Definir los problemas encontrados al iniciar o detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="1696b-208">Defining any problems encountered in starting or stopping the service.</span></span> <span data-ttu-id="1696b-209">Esta propiedad se establece en **\_ \_ \_ error específico del servicio de error** (1066) cuando el error es exclusivo del servicio representado por esta clase, y la información sobre el error está disponible en la propiedad **ServiceSpecificExitCode** .</span><span class="sxs-lookup"><span data-stu-id="1696b-209">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="1696b-210">El servicio establece este valor en **ningún \_ error** cuando se ejecuta y de nuevo tras la terminación normal.</span><span class="sxs-lookup"><span data-stu-id="1696b-210">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

</dd> <dt>

<span data-ttu-id="1696b-211">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1696b-211">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-212">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1696b-212">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-214">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="1696b-214">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-215">Objeto instalado.</span><span class="sxs-lookup"><span data-stu-id="1696b-215">Object was installed.</span></span> <span data-ttu-id="1696b-216">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="1696b-216">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1696b-217">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1696b-217">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1696b-218">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1696b-218">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1696b-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-221">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1696b-221">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1696b-222">Identificador único del servicio, que proporciona una indicación de la funcionalidad que se administra.</span><span class="sxs-lookup"><span data-stu-id="1696b-222">Unique identifier of the service, which provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="1696b-223">Esta funcionalidad se describe con más detalle en la propiedad **Descripción** del objeto.</span><span class="sxs-lookup"><span data-stu-id="1696b-223">This functionality is described in more detail in the object's **Description** property.</span></span>

<span data-ttu-id="1696b-224">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1696b-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1696b-225">**PathName**</span><span class="sxs-lookup"><span data-stu-id="1696b-225">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-226">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1696b-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-227">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-228">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File path name")</span><span class="sxs-lookup"><span data-stu-id="1696b-228">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-229">Ruta de acceso completa al archivo binario del servicio que implementa el servicio.</span><span class="sxs-lookup"><span data-stu-id="1696b-229">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="1696b-230">Ejemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="1696b-230">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

</dd> <dt>

<span data-ttu-id="1696b-231">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="1696b-231">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-232">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1696b-232">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-234">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("código de salida específico del servidor")</span><span class="sxs-lookup"><span data-stu-id="1696b-234">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-235">Código de error específico del servicio para los errores que se producen mientras el servicio se está iniciando o deteniendo.</span><span class="sxs-lookup"><span data-stu-id="1696b-235">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="1696b-236">Los códigos de salida se definen mediante el servicio representado por esta clase.</span><span class="sxs-lookup"><span data-stu-id="1696b-236">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="1696b-237">Este valor solo se establece cuando el valor de **ExitCodeproperty** es **\_ \_ \_ error específico del servicio de error** (1066).</span><span class="sxs-lookup"><span data-stu-id="1696b-237">This value is only set when the **ExitCodeproperty** value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

</dd> <dt>

<span data-ttu-id="1696b-238">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="1696b-238">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-239">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1696b-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-241">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span><span class="sxs-lookup"><span data-stu-id="1696b-241">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-242">Servicio proporcionado a los procesos de llamada.</span><span class="sxs-lookup"><span data-stu-id="1696b-242">Service provided to calling processes.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="1696b-243">**Controlador de kernel** ("controlador de kernel")</span><span class="sxs-lookup"><span data-stu-id="1696b-243">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="1696b-244">**Controlador del sistema de archivos** ("controlador del sistema de archivos")</span><span class="sxs-lookup"><span data-stu-id="1696b-244">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="1696b-245">**Adaptador** ("adaptador")</span><span class="sxs-lookup"><span data-stu-id="1696b-245">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="1696b-246">**Controlador del reconocedor** ("controlador del reconocedor")</span><span class="sxs-lookup"><span data-stu-id="1696b-246">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="1696b-247">**Proceso propio** ("propio proceso")</span><span class="sxs-lookup"><span data-stu-id="1696b-247">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="1696b-248">**Proceso de recurso compartido** ("proceso de recurso compartido")</span><span class="sxs-lookup"><span data-stu-id="1696b-248">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="1696b-249">**Proceso interactivo** ("proceso interactivo")</span><span class="sxs-lookup"><span data-stu-id="1696b-249">**Interactive Process** ("Interactive Process")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1696b-250">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="1696b-250">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-251">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1696b-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-253">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="1696b-253">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-254">El servicio se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="1696b-254">Service has been started.</span></span>

<span data-ttu-id="1696b-255">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1696b-255">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1696b-256">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="1696b-256">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1696b-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-259">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartMode"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modo de inicio")</span><span class="sxs-lookup"><span data-stu-id="1696b-259">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartMode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-260">Modo de inicio del servicio base de Windows.</span><span class="sxs-lookup"><span data-stu-id="1696b-260">Start mode of the Windows base service.</span></span>

<span data-ttu-id="1696b-261">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1696b-261">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="1696b-262"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Arranque** ("arranque")</span><span class="sxs-lookup"><span data-stu-id="1696b-262"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="1696b-263">Controlador de dispositivo Iniciado por el cargador del sistema operativo (válido solo para los servicios de controlador).</span><span class="sxs-lookup"><span data-stu-id="1696b-263">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="1696b-264"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("System")</span><span class="sxs-lookup"><span data-stu-id="1696b-264"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="1696b-265">Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1696b-265">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="1696b-266">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="1696b-266">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="1696b-267"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("auto")</span><span class="sxs-lookup"><span data-stu-id="1696b-267"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="1696b-268">Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="1696b-268">Service to be started automatically by the service control manager during system start up.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="1696b-269"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="1696b-269"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="1696b-270">Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](startservice-method-in-class-win32-baseservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1696b-270">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1696b-271"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("deshabilitado")</span><span class="sxs-lookup"><span data-stu-id="1696b-271"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="1696b-272">Servicio que ya no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="1696b-272">Service that can no longer be started.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1696b-273">**StartName**</span><span class="sxs-lookup"><span data-stu-id="1696b-273">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-274">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1696b-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-276">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de la cuenta de inicio")</span><span class="sxs-lookup"><span data-stu-id="1696b-276">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-277">Nombre de cuenta con la que se ejecuta el servicio.</span><span class="sxs-lookup"><span data-stu-id="1696b-277">Account name under which the service runs.</span></span> <span data-ttu-id="1696b-278">Dependiendo del tipo de servicio, el nombre de la cuenta puede tener el formato "DomainName \\ nombreDeUsuario" o UPN ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="1696b-278">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format (Username@DomainName).</span></span> <span data-ttu-id="1696b-279">El proceso de servicio se registrará con una de estas dos formas cuando se ejecute.</span><span class="sxs-lookup"><span data-stu-id="1696b-279">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="1696b-280">Si la cuenta pertenece al dominio integrado, ". \\ Se puede especificar username.</span><span class="sxs-lookup"><span data-stu-id="1696b-280">If the account belongs to the built-in domain, ".\\Username" can be specified.</span></span> <span data-ttu-id="1696b-281">Si se especifica **null** , el servicio se iniciará sesión como la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="1696b-281">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="1696b-282">En el caso de los controladores de kernel o de nivel de sistema, **StartName** contiene el nombre de objeto del controlador (es decir, sistema de \\ archivos \\ RDR o \\ XNS del controlador \\ ) que usa el sistema de entrada y salida (e/s) para cargar el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1696b-282">For kernel or system-level drivers, **StartName** contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="1696b-283">Además, si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de e/s basado en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="1696b-283">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="1696b-284">Ejemplo: "DWDOM \\ admin".</span><span class="sxs-lookup"><span data-stu-id="1696b-284">Example: "DWDOM\\Admin".</span></span>

</dd> <dt>

<span data-ttu-id="1696b-285">**State**</span><span class="sxs-lookup"><span data-stu-id="1696b-285">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1696b-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-287">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1696b-287">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1696b-288">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span><span class="sxs-lookup"><span data-stu-id="1696b-288">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-289">Estado actual del servicio base.</span><span class="sxs-lookup"><span data-stu-id="1696b-289">Current state of the base service.</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="1696b-290">**Detenido** ("detenido")</span><span class="sxs-lookup"><span data-stu-id="1696b-290">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="1696b-291">**Inicio pendiente** ("Inicio pendiente")</span><span class="sxs-lookup"><span data-stu-id="1696b-291">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="1696b-292">**Detención pendiente** ("detención pendiente")</span><span class="sxs-lookup"><span data-stu-id="1696b-292">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="1696b-293">En **ejecución** ("en ejecución")</span><span class="sxs-lookup"><span data-stu-id="1696b-293">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="1696b-294">**Continuar pendiente** ("continuar pendiente")</span><span class="sxs-lookup"><span data-stu-id="1696b-294">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="1696b-295">**Pausar pendiente** ("pausa pendiente")</span><span class="sxs-lookup"><span data-stu-id="1696b-295">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1696b-296">En **pausa** ("en pausa")</span><span class="sxs-lookup"><span data-stu-id="1696b-296">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1696b-297">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="1696b-297">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="1696b-298"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1696b-298"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="1696b-299">**Windows Server 2008 y Windows Vista:** Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1696b-299">**Windows Server 2008 and Windows Vista:** This property is read-only.</span></span>

</dd> <dt>

<span data-ttu-id="1696b-300">**Estado**</span><span class="sxs-lookup"><span data-stu-id="1696b-300">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-301">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1696b-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-303">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="1696b-303">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-304">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1696b-304">Current status of the object.</span></span> <span data-ttu-id="1696b-305">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="1696b-305">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1696b-306">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="1696b-306">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1696b-307">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="1696b-307">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1696b-308">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="1696b-308">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1696b-309">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="1696b-309">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1696b-310">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1696b-310">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1696b-311">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="1696b-311">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1696b-312">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="1696b-312">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1696b-313">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="1696b-313">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1696b-314">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="1696b-314">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1696b-315">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="1696b-315">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1696b-316">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="1696b-316">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1696b-317">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="1696b-317">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1696b-318">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="1696b-318">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1696b-319">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="1696b-319">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1696b-320">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="1696b-320">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1696b-321">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="1696b-321">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1696b-322">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="1696b-322">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1696b-323">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="1696b-323">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1696b-324">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1696b-324">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-325">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1696b-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-327">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class name ")</span><span class="sxs-lookup"><span data-stu-id="1696b-327">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-328">Nombre de tipo del sistema que hospeda este servicio.</span><span class="sxs-lookup"><span data-stu-id="1696b-328">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="1696b-329">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1696b-329">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1696b-330">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1696b-330">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-331">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1696b-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-333">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre del sistema ")</span><span class="sxs-lookup"><span data-stu-id="1696b-333">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-334">Nombre del sistema que hospeda este servicio.</span><span class="sxs-lookup"><span data-stu-id="1696b-334">Name of the system that hosts this service.</span></span>

<span data-ttu-id="1696b-335">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1696b-335">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1696b-336">**TagId**</span><span class="sxs-lookup"><span data-stu-id="1696b-336">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1696b-337">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1696b-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1696b-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1696b-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1696b-339">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ID. de etiqueta")</span><span class="sxs-lookup"><span data-stu-id="1696b-339">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="1696b-340">Valor de etiqueta único para este servicio en el grupo.</span><span class="sxs-lookup"><span data-stu-id="1696b-340">Unique tag value for this service in the group.</span></span> <span data-ttu-id="1696b-341">Un valor de 0 (cero) indica que el servicio no tiene asignada una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="1696b-341">A value of 0 (zero) indicates that the service has not been assigned a tag.</span></span> <span data-ttu-id="1696b-342">Se puede usar una etiqueta para ordenar instalado de estrella de servicio en un grupo de orden de carga mediante la especificación de un vector de orden de etiquetas en el registro ubicado en: HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ GroupOrderList.</span><span class="sxs-lookup"><span data-stu-id="1696b-342">A tag can be used for ordering service star tup within a load order group by specifying a tag order vector in the registry located at: HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\GroupOrderList.</span></span> <span data-ttu-id="1696b-343">Las etiquetas solo se evalúan para el controlador de kernel y los servicios de tipo de inicio del controlador del sistema de archivos que tienen modos de inicio o de inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="1696b-343">Tags are only evaluated for Kernel Driver and File System Driver start-type services that have Boot or System start modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1696b-344">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1696b-344">Remarks</span></span>

<span data-ttu-id="1696b-345">La **clase \_ BaseService de Win32** se deriva [**del \_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1696b-345">The **Win32\_BaseService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1696b-346">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1696b-346">Requirements</span></span>



| <span data-ttu-id="1696b-347">Requisito</span><span class="sxs-lookup"><span data-stu-id="1696b-347">Requirement</span></span> | <span data-ttu-id="1696b-348">Value</span><span class="sxs-lookup"><span data-stu-id="1696b-348">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1696b-349">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1696b-349">Minimum supported client</span></span><br/> | <span data-ttu-id="1696b-350">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1696b-350">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1696b-351">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1696b-351">Minimum supported server</span></span><br/> | <span data-ttu-id="1696b-352">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1696b-352">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1696b-353">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1696b-353">Namespace</span></span><br/>                | <span data-ttu-id="1696b-354">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1696b-354">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1696b-355">MOF</span><span class="sxs-lookup"><span data-stu-id="1696b-355">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1696b-356"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1696b-356"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1696b-357">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1696b-357">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1696b-358"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1696b-358"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1696b-359">Vea también</span><span class="sxs-lookup"><span data-stu-id="1696b-359">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1696b-360">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="1696b-360">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

<span data-ttu-id="1696b-361">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1696b-361">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

