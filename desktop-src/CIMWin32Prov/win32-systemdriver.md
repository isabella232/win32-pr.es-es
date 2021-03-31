---
description: Representa el controlador del sistema para un servicio base.
ms.assetid: 67dc6e14-c8c1-4168-8f99-b04c6ecd4ad2
ms.tgt_platform: multiple
title: Win32_SystemDriver (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver
- Win32_SystemDriver.AcceptPause
- Win32_SystemDriver.AcceptStop
- Win32_SystemDriver.Caption
- Win32_SystemDriver.CreationClassName
- Win32_SystemDriver.Description
- Win32_SystemDriver.DesktopInteract
- Win32_SystemDriver.DisplayName
- Win32_SystemDriver.ErrorControl
- Win32_SystemDriver.ExitCode
- Win32_SystemDriver.InstallDate
- Win32_SystemDriver.Name
- Win32_SystemDriver.PathName
- Win32_SystemDriver.ServiceSpecificExitCode
- Win32_SystemDriver.ServiceType
- Win32_SystemDriver.Started
- Win32_SystemDriver.StartMode
- Win32_SystemDriver.StartName
- Win32_SystemDriver.State
- Win32_SystemDriver.Status
- Win32_SystemDriver.SystemCreationClassName
- Win32_SystemDriver.SystemName
- Win32_SystemDriver.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15be9b176680e8abb259d3d011da9d6cec0c2fa8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807453"
---
# <a name="win32_systemdriver-class"></a><span data-ttu-id="71dbe-103">\_Clase Win32 SystemDriver</span><span class="sxs-lookup"><span data-stu-id="71dbe-103">Win32\_SystemDriver class</span></span>

<span data-ttu-id="71dbe-104">La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemDriver de Win32** representa el controlador del sistema para un servicio base.</span><span class="sxs-lookup"><span data-stu-id="71dbe-104">The **Win32\_SystemDriver** [WMI class](../wmisdk/retrieving-a-class.md) represents the system driver for a base service.</span></span>

<span data-ttu-id="71dbe-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="71dbe-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="71dbe-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="71dbe-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="71dbe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71dbe-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4C5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDriver : Win32_BaseService
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

## <a name="members"></a><span data-ttu-id="71dbe-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="71dbe-108">Members</span></span>

<span data-ttu-id="71dbe-109">La **clase \_ SystemDriver de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="71dbe-109">The **Win32\_SystemDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="71dbe-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="71dbe-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="71dbe-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="71dbe-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="71dbe-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="71dbe-112">Methods</span></span>

<span data-ttu-id="71dbe-113">La clase **Win32 \_ SystemDriver** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="71dbe-113">The **Win32\_SystemDriver** class has these methods.</span></span>



| <span data-ttu-id="71dbe-114">Método</span><span class="sxs-lookup"><span data-stu-id="71dbe-114">Method</span></span>                                                                              | <span data-ttu-id="71dbe-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="71dbe-115">Description</span></span>                                                                                     |
|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71dbe-116">**Cambio**</span><span class="sxs-lookup"><span data-stu-id="71dbe-116">**Change**</span></span>](change-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="71dbe-117">Método de clase que modifica un servicio.</span><span class="sxs-lookup"><span data-stu-id="71dbe-117">Class method that modifies a service.</span></span><br/>                                                |
| [<span data-ttu-id="71dbe-118">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="71dbe-118">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-systemdriver.md)       | <span data-ttu-id="71dbe-119">Método de clase que modifica el modo de inicio de un servicio.</span><span class="sxs-lookup"><span data-stu-id="71dbe-119">Class method that modifies the start mode of a service.</span></span><br/>                              |
| [<span data-ttu-id="71dbe-120">**A**</span><span class="sxs-lookup"><span data-stu-id="71dbe-120">**Create**</span></span>](create-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="71dbe-121">Método de clase que crea un nuevo servicio.</span><span class="sxs-lookup"><span data-stu-id="71dbe-121">Class method that creates a new service.</span></span><br/>                                             |
| [<span data-ttu-id="71dbe-122">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="71dbe-122">**Delete**</span></span>](delete-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="71dbe-123">Método de clase que elimina un servicio existente.</span><span class="sxs-lookup"><span data-stu-id="71dbe-123">Class method that deletes an existing service.</span></span><br/>                                       |
| [<span data-ttu-id="71dbe-124">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="71dbe-124">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-systemdriver.md) | <span data-ttu-id="71dbe-125">Método de clase que solicita que el servicio actualice su estado al administrador de servicios.</span><span class="sxs-lookup"><span data-stu-id="71dbe-125">Class method that requests that the service update its state to the service manager.</span></span><br/> |
| [<span data-ttu-id="71dbe-126">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="71dbe-126">**PauseService**</span></span>](pauseservice-method-in-class-win32-systemdriver.md)             | <span data-ttu-id="71dbe-127">Método de clase que intenta poner el servicio en estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="71dbe-127">Class method that attempts to place the service in the paused state.</span></span><br/>                 |
| [<span data-ttu-id="71dbe-128">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="71dbe-128">**ResumeService**</span></span>](resumeservice-method-in-class-win32-systemdriver.md)           | <span data-ttu-id="71dbe-129">Método de clase que intenta poner el servicio en estado reanudado.</span><span class="sxs-lookup"><span data-stu-id="71dbe-129">Class method that attempts to place the service in the resumed state.</span></span><br/>                |
| [<span data-ttu-id="71dbe-130">**StartService**</span><span class="sxs-lookup"><span data-stu-id="71dbe-130">**StartService**</span></span>](startservice-method-in-class-win32-systemdriver.md)             | <span data-ttu-id="71dbe-131">Método de clase que intenta poner el servicio en su estado de inicio.</span><span class="sxs-lookup"><span data-stu-id="71dbe-131">Class method that attempts to place the service into its startup state.</span></span><br/>              |
| [<span data-ttu-id="71dbe-132">**StopService**</span><span class="sxs-lookup"><span data-stu-id="71dbe-132">**StopService**</span></span>](stopservice-method-in-class-win32-systemdriver.md)               | <span data-ttu-id="71dbe-133">Método de clase que coloca el servicio en estado detenido.</span><span class="sxs-lookup"><span data-stu-id="71dbe-133">Class method that places the service in the stopped state.</span></span><br/>                           |
| [<span data-ttu-id="71dbe-134">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="71dbe-134">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-systemdriver.md) | <span data-ttu-id="71dbe-135">Método de clase que intenta enviar un código de control definido por el usuario a un servicio.</span><span class="sxs-lookup"><span data-stu-id="71dbe-135">Class method that attempts to send a user-defined control code to a service.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="71dbe-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="71dbe-136">Properties</span></span>

<span data-ttu-id="71dbe-137">La **clase \_ SystemDriver de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="71dbe-137">The **Win32\_SystemDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71dbe-138">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="71dbe-138">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-139">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="71dbe-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-141">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures Service \| [**\_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| Service \_ Accept \_ PAUSE \_ Continue"), [**displayName**](../wmisdk/standard-qualifiers.md) ("el servicio acepta la pausa")</span><span class="sxs-lookup"><span data-stu-id="71dbe-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-142">El servicio se puede pausar.</span><span class="sxs-lookup"><span data-stu-id="71dbe-142">Service can be paused.</span></span>

<span data-ttu-id="71dbe-143">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-143">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-144">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="71dbe-144">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-145">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="71dbe-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-147">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures Service \| [**\_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status)servicio \| dwControlsAccepted \| \_ \_ Stop"), [**displayName**](../wmisdk/standard-qualifiers.md) ("el servicio acepta la detención")</span><span class="sxs-lookup"><span data-stu-id="71dbe-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-148">Se puede detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="71dbe-148">Service can be stopped.</span></span>

<span data-ttu-id="71dbe-149">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-149">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-150">**Caption**</span><span class="sxs-lookup"><span data-stu-id="71dbe-150">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71dbe-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-153">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="71dbe-153">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-154">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="71dbe-154">Short description of the object.</span></span>

<span data-ttu-id="71dbe-155">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="71dbe-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71dbe-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-159">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="71dbe-159">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-160">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="71dbe-160">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="71dbe-161">Cuando se usa con las otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="71dbe-161">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="71dbe-162">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-162">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-163">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="71dbe-163">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71dbe-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-166">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="71dbe-166">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-167">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="71dbe-167">Description of the object.</span></span>

<span data-ttu-id="71dbe-168">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-169">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="71dbe-169">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-170">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="71dbe-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-172">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| Service \_ Interactive \_ Process"), [**displayName**](../wmisdk/standard-qualifiers.md) ("interactúa con Desktop")</span><span class="sxs-lookup"><span data-stu-id="71dbe-172">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-173">Este servicio puede crear o comunicarse con Windows en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="71dbe-173">This service can create or communicate with windows on the desktop.</span></span>

<span data-ttu-id="71dbe-174">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-174">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-175">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="71dbe-175">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71dbe-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-178">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpDisplayName"), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre para mostrar")</span><span class="sxs-lookup"><span data-stu-id="71dbe-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-179">Nombre para mostrar del servicio.</span><span class="sxs-lookup"><span data-stu-id="71dbe-179">Display name of the service.</span></span> <span data-ttu-id="71dbe-180">Esta cadena tiene una longitud máxima de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="71dbe-180">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="71dbe-181">El nombre se conserva en las mayúsculas y minúsculas en el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="71dbe-181">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="71dbe-182">Las comparaciones de **displayName** siempre distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="71dbe-182">**DisplayName** comparisons are always case-insensitive.</span></span>

<span data-ttu-id="71dbe-183">Constraints: acepta el mismo valor que la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="71dbe-183">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="71dbe-184">Ejemplo: "Endisco"</span><span class="sxs-lookup"><span data-stu-id="71dbe-184">Example: "Atdisk"</span></span>

<span data-ttu-id="71dbe-185">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-185">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-186">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="71dbe-186">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71dbe-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-189">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**displayName**](../wmisdk/standard-qualifiers.md) ("gravedad del error de inicio")</span><span class="sxs-lookup"><span data-stu-id="71dbe-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-190">Gravedad del error si este servicio no se inicia durante el inicio.</span><span class="sxs-lookup"><span data-stu-id="71dbe-190">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="71dbe-191">Este valor indica la acción realizada por el programa de inicio si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="71dbe-191">This value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="71dbe-192">El sistema registra todos los errores.</span><span class="sxs-lookup"><span data-stu-id="71dbe-192">All errors are logged by the computer system.</span></span>

<span data-ttu-id="71dbe-193">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-193">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="71dbe-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Omitir** ("omitir")</span><span class="sxs-lookup"><span data-stu-id="71dbe-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="71dbe-195">No se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="71dbe-195">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="71dbe-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("normal")</span><span class="sxs-lookup"><span data-stu-id="71dbe-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="71dbe-197">Se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="71dbe-197">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="71dbe-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("grave")</span><span class="sxs-lookup"><span data-stu-id="71dbe-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="71dbe-199">El sistema se reinicia con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="71dbe-199">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="71dbe-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** ("crítico")</span><span class="sxs-lookup"><span data-stu-id="71dbe-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="71dbe-201">El sistema intenta reiniciarse con una configuración válida.</span><span class="sxs-lookup"><span data-stu-id="71dbe-201">System attempts to restart with a good configuration.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71dbe-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="71dbe-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="71dbe-203">Se desconoce la causa del error.</span><span class="sxs-lookup"><span data-stu-id="71dbe-203">Cause of the failure is unknown.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="71dbe-204">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="71dbe-204">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-205">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71dbe-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-207">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**displayName**](../wmisdk/standard-qualifiers.md) ("código de salida")</span><span class="sxs-lookup"><span data-stu-id="71dbe-207">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-208">Código de error de Windows que define los problemas encontrados al iniciar o detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="71dbe-208">Windows error code defining any problems encountered in starting or stopping the service.</span></span> <span data-ttu-id="71dbe-209">Esta propiedad se establece en **\_ \_ \_ error específico del servicio de error** (1066) cuando el error es exclusivo del servicio representado por esta clase, y la información sobre el error está disponible en la propiedad **ServiceSpecificExitCode** .</span><span class="sxs-lookup"><span data-stu-id="71dbe-209">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="71dbe-210">El servicio establece este valor en **ningún \_ error** cuando se ejecuta y de nuevo tras la terminación normal.</span><span class="sxs-lookup"><span data-stu-id="71dbe-210">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="71dbe-211">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-211">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-212">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="71dbe-212">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-213">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="71dbe-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-215">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="71dbe-215">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-216">Objeto instalado.</span><span class="sxs-lookup"><span data-stu-id="71dbe-216">Object was installed.</span></span> <span data-ttu-id="71dbe-217">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="71dbe-217">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="71dbe-218">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-219">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="71dbe-219">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-220">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71dbe-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-222">Calificadores: [ **clave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="71dbe-222">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-223">Identificador único para el servicio que proporciona una indicación de la funcionalidad que se administra.</span><span class="sxs-lookup"><span data-stu-id="71dbe-223">Unique identifier for the service which provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="71dbe-224">Esta funcionalidad se describe con más detalle en la propiedad **Descripción** del objeto.</span><span class="sxs-lookup"><span data-stu-id="71dbe-224">This functionality is described in more detail in the object **Description** property.</span></span>

<span data-ttu-id="71dbe-225">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-225">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-226">**PathName**</span><span class="sxs-lookup"><span data-stu-id="71dbe-226">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71dbe-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-229">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**displayName**](../wmisdk/standard-qualifiers.md) ("File path name")</span><span class="sxs-lookup"><span data-stu-id="71dbe-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-230">Ruta de acceso completa al archivo binario del servicio que implementa el servicio.</span><span class="sxs-lookup"><span data-stu-id="71dbe-230">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="71dbe-231">Ejemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="71dbe-231">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="71dbe-232">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-232">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-233">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="71dbe-233">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-234">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71dbe-234">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-236">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**displayName**](../wmisdk/standard-qualifiers.md) ("código de salida específico del servidor")</span><span class="sxs-lookup"><span data-stu-id="71dbe-236">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-237">Código de error específico del servicio para los errores que se producen mientras el servicio se está iniciando o deteniendo.</span><span class="sxs-lookup"><span data-stu-id="71dbe-237">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="71dbe-238">Los códigos de salida se definen mediante el servicio representado por esta clase.</span><span class="sxs-lookup"><span data-stu-id="71dbe-238">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="71dbe-239">Este valor solo se establece cuando el valor de la propiedad **ExitCode** es **\_ \_ \_ error específico del servicio de error** (1066).</span><span class="sxs-lookup"><span data-stu-id="71dbe-239">This value is only set when the **ExitCode** property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="71dbe-240">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-240">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-241">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="71dbe-241">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-242">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71dbe-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-244">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span><span class="sxs-lookup"><span data-stu-id="71dbe-244">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-245">Tipo de servicio proporcionado a los procesos de llamada.</span><span class="sxs-lookup"><span data-stu-id="71dbe-245">Type of service provided to calling processes.</span></span>

<span data-ttu-id="71dbe-246">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-246">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="71dbe-247">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="71dbe-247">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="71dbe-248">**Controlador de kernel** ("controlador de kernel")</span><span class="sxs-lookup"><span data-stu-id="71dbe-248">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="71dbe-249">**Controlador del sistema de archivos** ("controlador del sistema de archivos")</span><span class="sxs-lookup"><span data-stu-id="71dbe-249">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="71dbe-250">**Adaptador** ("adaptador")</span><span class="sxs-lookup"><span data-stu-id="71dbe-250">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="71dbe-251">**Controlador del reconocedor** ("controlador del reconocedor")</span><span class="sxs-lookup"><span data-stu-id="71dbe-251">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="71dbe-252">**Proceso propio** ("propio proceso")</span><span class="sxs-lookup"><span data-stu-id="71dbe-252">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="71dbe-253">**Proceso de recurso compartido** ("proceso de recurso compartido")</span><span class="sxs-lookup"><span data-stu-id="71dbe-253">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="71dbe-254">**Proceso interactivo** ("proceso interactivo")</span><span class="sxs-lookup"><span data-stu-id="71dbe-254">**Interactive Process** ("Interactive Process")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71dbe-255">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="71dbe-255">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-256">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="71dbe-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-258">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="71dbe-258">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-259">El servicio se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="71dbe-259">Service has been started.</span></span>

<span data-ttu-id="71dbe-260">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-260">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-261">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="71dbe-261">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-262">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71dbe-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-264">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("modo de inicio")</span><span class="sxs-lookup"><span data-stu-id="71dbe-264">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-265">Modo de inicio del controlador del sistema.</span><span class="sxs-lookup"><span data-stu-id="71dbe-265">Start mode of the system driver.</span></span>

<span data-ttu-id="71dbe-266">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-266">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="71dbe-267"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Arranque** ("arranque")</span><span class="sxs-lookup"><span data-stu-id="71dbe-267"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="71dbe-268">Controlador de dispositivo Iniciado por el cargador del sistema operativo (válido solo para los servicios de controlador).</span><span class="sxs-lookup"><span data-stu-id="71dbe-268">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="71dbe-269"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("System")</span><span class="sxs-lookup"><span data-stu-id="71dbe-269"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="71dbe-270">Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="71dbe-270">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="71dbe-271">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="71dbe-271">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="71dbe-272"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("auto")</span><span class="sxs-lookup"><span data-stu-id="71dbe-272"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="71dbe-273">Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="71dbe-273">Service to be started automatically by the service control manager during system start up.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="71dbe-274"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="71dbe-274"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="71dbe-275">Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="71dbe-275">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="71dbe-276"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("deshabilitado")</span><span class="sxs-lookup"><span data-stu-id="71dbe-276"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="71dbe-277">Servicio que ya no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="71dbe-277">Service that can no longer be started.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="71dbe-278">**StartName**</span><span class="sxs-lookup"><span data-stu-id="71dbe-278">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-279">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71dbe-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-281">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de la cuenta de inicio")</span><span class="sxs-lookup"><span data-stu-id="71dbe-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-282">Nombre de cuenta con la que se ejecuta el servicio.</span><span class="sxs-lookup"><span data-stu-id="71dbe-282">Account name under which the service runs.</span></span> <span data-ttu-id="71dbe-283">En función del tipo de servicio, el nombre de la cuenta puede tener el formato nombreDeDominio \\ nombreDeUsuario.</span><span class="sxs-lookup"><span data-stu-id="71dbe-283">Depending on the service type, the account name may be in the form of DomainName\\Username.</span></span> <span data-ttu-id="71dbe-284">El proceso de servicio se registrará con una de estas dos formas cuando se ejecute.</span><span class="sxs-lookup"><span data-stu-id="71dbe-284">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="71dbe-285">Si la cuenta pertenece al dominio integrado,. \\ Se puede especificar el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="71dbe-285">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="71dbe-286">Si se especifica **null** , el servicio se iniciará sesión como la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="71dbe-286">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="71dbe-287">En el caso de los controladores de kernel o de nivel de sistema, **StartName** contiene el nombre de objeto del controlador (es decir, sistema de \\ archivos \\ RDR o \\ XNS del controlador \\ ) que usa el sistema de entrada y salida (e/s) para cargar el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71dbe-287">For kernel or system-level drivers, **StartName** contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="71dbe-288">Además, si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de e/s basado en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="71dbe-288">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="71dbe-289">Ejemplo: "DWDOM \\ admin"</span><span class="sxs-lookup"><span data-stu-id="71dbe-289">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="71dbe-290">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-290">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-291">**State**</span><span class="sxs-lookup"><span data-stu-id="71dbe-291">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-292">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71dbe-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-293">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="71dbe-293">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-294">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**displayName**](../wmisdk/standard-qualifiers.md) ("State")</span><span class="sxs-lookup"><span data-stu-id="71dbe-294">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-295">Estado actual del servicio base.</span><span class="sxs-lookup"><span data-stu-id="71dbe-295">Current state of the base service.</span></span>

<span data-ttu-id="71dbe-296">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-296">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="71dbe-297">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="71dbe-297">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="71dbe-298">**Detenido** ("detenido")</span><span class="sxs-lookup"><span data-stu-id="71dbe-298">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="71dbe-299">**Inicio pendiente** ("Inicio pendiente")</span><span class="sxs-lookup"><span data-stu-id="71dbe-299">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="71dbe-300">**Detención pendiente** ("detención pendiente")</span><span class="sxs-lookup"><span data-stu-id="71dbe-300">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="71dbe-301">En **ejecución** ("en ejecución")</span><span class="sxs-lookup"><span data-stu-id="71dbe-301">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="71dbe-302">**Continuar pendiente** ("continuar pendiente")</span><span class="sxs-lookup"><span data-stu-id="71dbe-302">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="71dbe-303">**Pausar pendiente** ("pausa pendiente")</span><span class="sxs-lookup"><span data-stu-id="71dbe-303">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="71dbe-304">En **pausa** ("en pausa")</span><span class="sxs-lookup"><span data-stu-id="71dbe-304">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71dbe-305">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="71dbe-305">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71dbe-306">**Estado**</span><span class="sxs-lookup"><span data-stu-id="71dbe-306">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71dbe-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-309">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="71dbe-309">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-310">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="71dbe-310">Current status of the object.</span></span> <span data-ttu-id="71dbe-311">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="71dbe-311">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="71dbe-312">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="71dbe-312">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="71dbe-313">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="71dbe-313">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="71dbe-314">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="71dbe-314">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="71dbe-315">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="71dbe-315">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="71dbe-316">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="71dbe-317">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="71dbe-317">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="71dbe-318">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="71dbe-318">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="71dbe-319">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="71dbe-319">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="71dbe-320">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="71dbe-320">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71dbe-321">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="71dbe-321">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="71dbe-322">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="71dbe-322">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="71dbe-323">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="71dbe-323">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="71dbe-324">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="71dbe-324">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="71dbe-325">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="71dbe-325">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="71dbe-326">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="71dbe-326">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="71dbe-327">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="71dbe-327">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="71dbe-328">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="71dbe-328">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="71dbe-329">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="71dbe-329">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71dbe-330">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="71dbe-330">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-331">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71dbe-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-333">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" System Class name ")</span><span class="sxs-lookup"><span data-stu-id="71dbe-333">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-334">Nombre de tipo del sistema que hospeda este servicio.</span><span class="sxs-lookup"><span data-stu-id="71dbe-334">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="71dbe-335">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-335">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-336">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="71dbe-336">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-337">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71dbe-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-339">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre del sistema ")</span><span class="sxs-lookup"><span data-stu-id="71dbe-339">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-340">Nombre del sistema que hospeda este servicio.</span><span class="sxs-lookup"><span data-stu-id="71dbe-340">Name of the system that hosts this service.</span></span>

<span data-ttu-id="71dbe-341">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-341">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dbe-342">**TagId**</span><span class="sxs-lookup"><span data-stu-id="71dbe-342">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71dbe-343">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71dbe-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71dbe-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71dbe-345">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**displayName**](../wmisdk/standard-qualifiers.md) ("ID. de etiqueta")</span><span class="sxs-lookup"><span data-stu-id="71dbe-345">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="71dbe-346">Valor de etiqueta único para este servicio en el grupo.</span><span class="sxs-lookup"><span data-stu-id="71dbe-346">Unique tag value for this service in the group.</span></span> <span data-ttu-id="71dbe-347">Un valor de 0 (cero) indica que el servicio no tiene asignada una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="71dbe-347">A value of 0 (zero) indicates that the service has not been assigned a tag.</span></span> <span data-ttu-id="71dbe-348">Una etiqueta se puede utilizar para ordenar el inicio del servicio en un grupo de orden de carga mediante la especificación de un vector de orden de etiquetas en el registro ubicado en:</span><span class="sxs-lookup"><span data-stu-id="71dbe-348">A tag can be used for ordering service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="71dbe-349">Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-349">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="71dbe-350">**HKEY \_ \_Sistema de equipo local \\ \\ CurrentControlSet \\ control \\ GroupOrderList**.</span><span class="sxs-lookup"><span data-stu-id="71dbe-350">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\GroupOrderList**.</span></span>

<span data-ttu-id="71dbe-351">Las etiquetas solo se evalúan para el controlador de kernel y los servicios de tipo de inicio del controlador del sistema de archivos que tienen modos de inicio o de inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="71dbe-351">Tags are only evaluated for Kernel Driver and File System Driver start-type services that have Boot or System start modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71dbe-352">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71dbe-352">Remarks</span></span>

<span data-ttu-id="71dbe-353">La **clase \_ SystemDriver de Win32** se deriva de [**\_ BaseService de Win32**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="71dbe-353">The **Win32\_SystemDriver** class is derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="71dbe-354">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="71dbe-354">Examples</span></span>

<span data-ttu-id="71dbe-355">El ejemplo [List System drivers](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) de VBScript muestra los controladores del sistema instalados en un archivo HTML.</span><span class="sxs-lookup"><span data-stu-id="71dbe-355">The [List System Drivers](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) VBScript sample Displays installed system drivers in an HTML file.</span></span>

<span data-ttu-id="71dbe-356">En el siguiente ejemplo de PowerShell se recupera un número de propiedades de los controladores del sistema en ejecución en un equipo.</span><span class="sxs-lookup"><span data-stu-id="71dbe-356">The following PowerShell example retrieves a number of properties from the running system drivers on a computer.</span></span>


```PowerShell
Get-WmiObject -Class Win32_SystemDriver | Where-Object -FilterScript {$_.State -eq "Running"} | Where-Object -FilterScript {$_.StartMode -eq "Manual"} | Format-Table -Property Name,DisplayName
```



## <a name="requirements"></a><span data-ttu-id="71dbe-357">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71dbe-357">Requirements</span></span>



| <span data-ttu-id="71dbe-358">Requisito</span><span class="sxs-lookup"><span data-stu-id="71dbe-358">Requirement</span></span> | <span data-ttu-id="71dbe-359">Value</span><span class="sxs-lookup"><span data-stu-id="71dbe-359">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71dbe-360">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71dbe-360">Minimum supported client</span></span><br/> | <span data-ttu-id="71dbe-361">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71dbe-361">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71dbe-362">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71dbe-362">Minimum supported server</span></span><br/> | <span data-ttu-id="71dbe-363">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71dbe-363">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71dbe-364">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="71dbe-364">Namespace</span></span><br/>                | <span data-ttu-id="71dbe-365">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="71dbe-365">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="71dbe-366">MOF</span><span class="sxs-lookup"><span data-stu-id="71dbe-366">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71dbe-367"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71dbe-367"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="71dbe-368">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="71dbe-368">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71dbe-369"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71dbe-369"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71dbe-370">Vea también</span><span class="sxs-lookup"><span data-stu-id="71dbe-370">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71dbe-371">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="71dbe-371">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="71dbe-372">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="71dbe-372">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
