---
description: Representa el estado del servicio de latido, que es responsable de supervisar el estado de una máquina virtual mediante la notificación de un latido a intervalos regulares.
ms.assetid: 72DB3CD9-B083-4483-BCCD-DC8C140DDBF4
title: Msvm_HeartbeatComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponent
- Msvm_HeartbeatComponent.SetPowerState
- Msvm_HeartbeatComponent.EnableDevice
- Msvm_HeartbeatComponent.OnlineDevice
- Msvm_HeartbeatComponent.QuiesceDevice
- Msvm_HeartbeatComponent.SaveProperties
- Msvm_HeartbeatComponent.RestoreProperties
- Msvm_HeartbeatComponent.InstanceID
- Msvm_HeartbeatComponent.Caption
- Msvm_HeartbeatComponent.Description
- Msvm_HeartbeatComponent.ElementName
- Msvm_HeartbeatComponent.InstallDate
- Msvm_HeartbeatComponent.Name
- Msvm_HeartbeatComponent.OperationalStatus
- Msvm_HeartbeatComponent.StatusDescriptions
- Msvm_HeartbeatComponent.Status
- Msvm_HeartbeatComponent.HealthState
- Msvm_HeartbeatComponent.CommunicationStatus
- Msvm_HeartbeatComponent.DetailedStatus
- Msvm_HeartbeatComponent.OperatingStatus
- Msvm_HeartbeatComponent.PrimaryStatus
- Msvm_HeartbeatComponent.EnabledState
- Msvm_HeartbeatComponent.OtherEnabledState
- Msvm_HeartbeatComponent.RequestedState
- Msvm_HeartbeatComponent.EnabledDefault
- Msvm_HeartbeatComponent.TimeOfLastStateChange
- Msvm_HeartbeatComponent.AvailableRequestedStates
- Msvm_HeartbeatComponent.TransitioningToState
- Msvm_HeartbeatComponent.SystemCreationClassName
- Msvm_HeartbeatComponent.SystemName
- Msvm_HeartbeatComponent.CreationClassName
- Msvm_HeartbeatComponent.DeviceID
- Msvm_HeartbeatComponent.PowerManagementSupported
- Msvm_HeartbeatComponent.PowerManagementCapabilities
- Msvm_HeartbeatComponent.Availability
- Msvm_HeartbeatComponent.StatusInfo
- Msvm_HeartbeatComponent.LastErrorCode
- Msvm_HeartbeatComponent.ErrorDescription
- Msvm_HeartbeatComponent.ErrorCleared
- Msvm_HeartbeatComponent.OtherIdentifyingInfo
- Msvm_HeartbeatComponent.PowerOnHours
- Msvm_HeartbeatComponent.TotalPowerOnHours
- Msvm_HeartbeatComponent.IdentifyingDescriptions
- Msvm_HeartbeatComponent.AdditionalAvailability
- Msvm_HeartbeatComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 61a3efaba52c2e592f405e1b95f1c62568a59229
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540331"
---
# <a name="msvm_heartbeatcomponent-class"></a><span data-ttu-id="576f9-103">MSVM \_ HeartbeatComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="576f9-103">Msvm\_HeartbeatComponent class</span></span>

<span data-ttu-id="576f9-104">Representa el estado del servicio de latido, que es responsable de supervisar el estado de una máquina virtual mediante la notificación de un latido a intervalos regulares.</span><span class="sxs-lookup"><span data-stu-id="576f9-104">Represents the state of the heartbeat service, which is responsible for monitoring the state of a virtual machine by reporting a heartbeat at regular intervals.</span></span>

<span data-ttu-id="576f9-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="576f9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="576f9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="576f9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Heartbeat";
  string   Description = "Microsoft Heartbeat Service";
  string   ElementName = "Heartbeat";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_HeartbeatComponent";
  string   DeviceID = "Microsoft:VMGUID\GUID";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="576f9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="576f9-107">Members</span></span>

<span data-ttu-id="576f9-108">La clase **MSVM \_ HeartbeatComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="576f9-108">The **Msvm\_HeartbeatComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="576f9-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="576f9-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="576f9-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="576f9-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="576f9-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="576f9-111">Methods</span></span>

<span data-ttu-id="576f9-112">La clase **MSVM \_ HeartbeatComponent** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="576f9-112">The **Msvm\_HeartbeatComponent** class has these methods.</span></span>



| <span data-ttu-id="576f9-113">Método</span><span class="sxs-lookup"><span data-stu-id="576f9-113">Method</span></span>                                                                   | <span data-ttu-id="576f9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="576f9-114">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="576f9-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="576f9-115">**EnableDevice**</span></span>                                                         | <span data-ttu-id="576f9-116">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="576f9-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="576f9-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="576f9-117">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="576f9-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="576f9-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="576f9-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="576f9-119">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="576f9-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="576f9-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="576f9-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="576f9-121">**RequestStateChange**</span></span>](msvm-heartbeatcomponent-requeststatechange.md) | <span data-ttu-id="576f9-122">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="576f9-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="576f9-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="576f9-123">**Reset**</span></span>](msvm-heartbeatcomponent-reset.md)                           | <span data-ttu-id="576f9-124">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="576f9-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="576f9-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="576f9-125">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="576f9-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="576f9-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="576f9-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="576f9-127">**SaveProperties**</span></span>                                                       | <span data-ttu-id="576f9-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="576f9-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="576f9-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="576f9-129">**SetPowerState**</span></span>                                                        | <span data-ttu-id="576f9-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="576f9-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="576f9-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="576f9-131">Properties</span></span>

<span data-ttu-id="576f9-132">La clase **MSVM \_ HeartbeatComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="576f9-132">The **Msvm\_HeartbeatComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="576f9-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="576f9-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-134">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="576f9-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="576f9-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-136">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576f9-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="576f9-137">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre está establecida en 6 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="576f9-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="576f9-138">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="576f9-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="576f9-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-141">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576f9-141">The primary availability and status of the device.</span></span> <span data-ttu-id="576f9-142">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="576f9-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-143">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="576f9-143">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-144">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="576f9-144">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="576f9-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-146">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="576f9-146">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="576f9-147">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="576f9-147">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="576f9-148">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="576f9-148">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="576f9-149">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="576f9-149">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="576f9-150">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="576f9-150">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="576f9-151"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="576f9-151"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="576f9-152"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="576f9-152"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="576f9-153"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="576f9-153"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="576f9-154"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="576f9-154"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="576f9-155"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="576f9-155"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="576f9-156"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="576f9-156"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="576f9-157"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="576f9-157"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="576f9-158"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="576f9-158"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="576f9-159"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="576f9-159"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="576f9-160"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="576f9-160"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="576f9-161">)</span><span class="sxs-lookup"><span data-stu-id="576f9-161">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="576f9-162">**Caption**</span><span class="sxs-lookup"><span data-stu-id="576f9-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="576f9-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-165">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="576f9-165">A short description of the object.</span></span> <span data-ttu-id="576f9-166">Esta propiedad se hereda de la clase de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) y siempre se establece en "latido".</span><span class="sxs-lookup"><span data-stu-id="576f9-166">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="576f9-167">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="576f9-167">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-168">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="576f9-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-170">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="576f9-170">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="576f9-171">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="576f9-171">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="576f9-172">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="576f9-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="576f9-173">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="576f9-173">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="576f9-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-176">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="576f9-176">The scoping system's creation class name.</span></span> <span data-ttu-id="576f9-177">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "MSVM \_ HeartbeatComponent".</span><span class="sxs-lookup"><span data-stu-id="576f9-177">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_HeartbeatComponent".</span></span>

</dd> <dt>

<span data-ttu-id="576f9-178">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="576f9-178">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="576f9-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-181">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="576f9-181">A description of the object.</span></span> <span data-ttu-id="576f9-182">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "servicio de latido de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="576f9-182">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Heartbeat Service".</span></span>

</dd> <dt>

<span data-ttu-id="576f9-183">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="576f9-183">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-184">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="576f9-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-186">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="576f9-186">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="576f9-187">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="576f9-187">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="576f9-188">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="576f9-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="576f9-189">**ID**</span><span class="sxs-lookup"><span data-stu-id="576f9-189">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="576f9-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-192">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="576f9-192">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="576f9-193">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "Microsoft:*VMGUID* \\ *GUID*", donde *VMGUID* es la propiedad **Name** del [**MSVM \_ ComputerSystem**](msvm-computersystem.md) asociado a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576f9-193">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-194">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="576f9-194">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="576f9-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-197">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="576f9-197">A display name for the object.</span></span> <span data-ttu-id="576f9-198">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "latido".</span><span class="sxs-lookup"><span data-stu-id="576f9-198">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="576f9-199">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="576f9-199">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-200">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="576f9-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-202">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre se establece en 7 (no valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="576f9-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 7 (No Default).</span></span>

</dd> <dt>

<span data-ttu-id="576f9-203">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="576f9-203">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-204">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="576f9-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-206">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="576f9-206">The enabled and disabled states of an element.</span></span> <span data-ttu-id="576f9-207">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) y tendrá uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="576f9-207">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>



| <span data-ttu-id="576f9-208">Value</span><span class="sxs-lookup"><span data-stu-id="576f9-208">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="576f9-209">Significado</span><span class="sxs-lookup"><span data-stu-id="576f9-209">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="576f9-210"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="576f9-210"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="576f9-211">El elemento se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="576f9-211">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="576f9-212"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="576f9-212"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="576f9-213">El elemento está desactivado.</span><span class="sxs-lookup"><span data-stu-id="576f9-213">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="576f9-214">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="576f9-214">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-215">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="576f9-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-217">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="576f9-217">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="576f9-218">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="576f9-218">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-219">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="576f9-219">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-220">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="576f9-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-222">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="576f9-222">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="576f9-223">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="576f9-223">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-224">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="576f9-224">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-225">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="576f9-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-227">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="576f9-227">The current health of the element.</span></span> <span data-ttu-id="576f9-228">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="576f9-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="576f9-229">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="576f9-229">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-230">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="576f9-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="576f9-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-232">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="576f9-232">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="576f9-233">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="576f9-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-234">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="576f9-234">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-235">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="576f9-235">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-237">Fecha y hora en que se instaló el servicio de integración en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="576f9-237">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="576f9-238">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="576f9-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="576f9-239">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="576f9-239">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-240">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="576f9-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="576f9-242">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="576f9-242">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="576f9-243">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="576f9-243">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="576f9-244">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="576f9-244">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="576f9-245">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="576f9-245">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-246">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="576f9-246">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-248">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="576f9-248">The last error code reported by the logical device.</span></span> <span data-ttu-id="576f9-249">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="576f9-249">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-250">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="576f9-250">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-251">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="576f9-251">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-253">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="576f9-253">This property has been deprecated.</span></span> <span data-ttu-id="576f9-254">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="576f9-254">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-255">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="576f9-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-256">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="576f9-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-258">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="576f9-258">The label by which the object is known.</span></span> <span data-ttu-id="576f9-259">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="576f9-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="576f9-260">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="576f9-260">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-261">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="576f9-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-263">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="576f9-263">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="576f9-264">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="576f9-264">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="576f9-265">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="576f9-265">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="576f9-266">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="576f9-266">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-267">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="576f9-267">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="576f9-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="576f9-269">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="576f9-269">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="576f9-270">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="576f9-270">The current status of the element.</span></span> <span data-ttu-id="576f9-271">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="576f9-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="576f9-272">A continuación se muestran los posibles valores para el valor de la propiedad **OperationalStatus** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="576f9-272">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="576f9-273"><span id="OK"></span><span id="ok"></span>**Aceptar** (2)</span><span class="sxs-lookup"><span data-stu-id="576f9-273"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd>

<span data-ttu-id="576f9-274">El servicio está funcionando con normalidad.</span><span class="sxs-lookup"><span data-stu-id="576f9-274">The service is operating normally.</span></span> <span data-ttu-id="576f9-275">Los valores de la propiedad **OperationalStatus** \[ 1 \] y **StatusDescriptions** \[ 1 \] pueden contener más información.</span><span class="sxs-lookup"><span data-stu-id="576f9-275">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="576f9-276"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (3)</span><span class="sxs-lookup"><span data-stu-id="576f9-276"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd>

<span data-ttu-id="576f9-277">El servicio está funcionando con normalidad, pero el servicio invitado negoció una versión del Protocolo de comunicaciones compatible.</span><span class="sxs-lookup"><span data-stu-id="576f9-277">The service is operating normally, but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="576f9-278">Los valores de la propiedad **OperationalStatus** \[ 1 \] y **StatusDescriptions** \[ 1 \] pueden contener más información.</span><span class="sxs-lookup"><span data-stu-id="576f9-278">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="576f9-279"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (7)</span><span class="sxs-lookup"><span data-stu-id="576f9-279"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="576f9-280">El invitado no es compatible con una versión de protocolo compatible.</span><span class="sxs-lookup"><span data-stu-id="576f9-280">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="576f9-281">Los valores de la propiedad **OperationalStatus** \[ 1 \] y **StatusDescriptions** \[ 1 \] pueden contener más información.</span><span class="sxs-lookup"><span data-stu-id="576f9-281">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="576f9-282"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (12)</span><span class="sxs-lookup"><span data-stu-id="576f9-282"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd>

<span data-ttu-id="576f9-283">El servicio invitado no está instalado o no se ha conectado todavía.</span><span class="sxs-lookup"><span data-stu-id="576f9-283">The guest service is not installed or has not yet been contacted.</span></span>

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="576f9-284"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (13)</span><span class="sxs-lookup"><span data-stu-id="576f9-284"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd>

<span data-ttu-id="576f9-285">El servicio invitado ya no responde normalmente.</span><span class="sxs-lookup"><span data-stu-id="576f9-285">The guest service is no longer responding normally.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="576f9-286"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (15)</span><span class="sxs-lookup"><span data-stu-id="576f9-286"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (15)</span></span>


</dt> <dd>

<span data-ttu-id="576f9-287">La máquina virtual está en pausa.</span><span class="sxs-lookup"><span data-stu-id="576f9-287">The virtual machine is paused.</span></span>

</dd> </dl>

<span data-ttu-id="576f9-288">El valor de la propiedad **OperationalStatus** \[ 1 \] indica los valores de estado de la aplicación fusionada.</span><span class="sxs-lookup"><span data-stu-id="576f9-288">The **OperationalStatus**\[1\] property value indicates the coalesced application state values.</span></span> <span data-ttu-id="576f9-289">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="576f9-289">This will be one of the following values.</span></span>

> [!Note]  
> <span data-ttu-id="576f9-290">El estado de una aplicación se establece en la máquina virtual mediante el método [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md) .</span><span class="sxs-lookup"><span data-stu-id="576f9-290">The state for an application is set on the virtual machine by using the [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md) method.</span></span>

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="576f9-291"><span id="OK"></span><span id="ok"></span>**Aceptar** (2)</span><span class="sxs-lookup"><span data-stu-id="576f9-291"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd>

<span data-ttu-id="576f9-292">Las aplicaciones que se ejecutan dentro de la máquina virtual funcionan con normalidad.</span><span class="sxs-lookup"><span data-stu-id="576f9-292">The applications running inside the virtual machine are operating normally.</span></span>

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="576f9-293"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>El **Protocolo no coincide** (32775)</span><span class="sxs-lookup"><span data-stu-id="576f9-293"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protocol Mismatch** (32775)</span></span>


</dt> <dd>

<span data-ttu-id="576f9-294">Los componentes invitado y host ejecutan diferentes versiones de protocolo.</span><span class="sxs-lookup"><span data-stu-id="576f9-294">The guest and the host components are running different protocol versions.</span></span>

</dd> <dt>

<span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>

<span data-ttu-id="576f9-295"><span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**Estado crítico** de la aplicación (32782)</span><span class="sxs-lookup"><span data-stu-id="576f9-295"><span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**Application Critical State** (32782)</span></span>


</dt> <dd>

<span data-ttu-id="576f9-296">Una o varias aplicaciones dentro de la máquina virtual están en un estado crítico.</span><span class="sxs-lookup"><span data-stu-id="576f9-296">One or more of the applications inside the virtual machine are in a critical state.</span></span>

</dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span data-ttu-id="576f9-297"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Tiempo de espera** de la comunicación (32783)</span><span class="sxs-lookup"><span data-stu-id="576f9-297"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Communication Timed Out** (32783)</span></span>


</dt> <dd>

<span data-ttu-id="576f9-298">Se agotó el tiempo de espera para una respuesta del componente invitado.</span><span class="sxs-lookup"><span data-stu-id="576f9-298">Timed out waiting for a response from the guest component.</span></span>

</dd> <dt>

<span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>

<span data-ttu-id="576f9-299"><span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>**Error de comunicación** (32784)</span><span class="sxs-lookup"><span data-stu-id="576f9-299"><span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>**Communication Failed** (32784)</span></span>


</dt> <dd>

<span data-ttu-id="576f9-300">No se pudo comunicar con el componente invitado.</span><span class="sxs-lookup"><span data-stu-id="576f9-300">Failed to communicate with the guest component.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="576f9-301">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="576f9-301">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-302">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="576f9-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-304">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="576f9-304">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="576f9-305">Esta propiedad debe establecerse en **null** cuando la propiedad **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="576f9-305">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="576f9-306">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="576f9-306">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-307">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="576f9-307">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-308">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="576f9-308">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="576f9-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-310">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="576f9-310">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="576f9-311">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="576f9-311">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-312">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="576f9-312">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-313">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="576f9-313">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="576f9-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-315">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576f9-315">The power management capabilities of the device.</span></span> <span data-ttu-id="576f9-316">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="576f9-316">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-317">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="576f9-317">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-318">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="576f9-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-320">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="576f9-320">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="576f9-321">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="576f9-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-322">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="576f9-322">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-323">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="576f9-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-325">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="576f9-325">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="576f9-326">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="576f9-326">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-327">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="576f9-327">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-328">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="576f9-328">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-330">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="576f9-330">Provides high level status information.</span></span> <span data-ttu-id="576f9-331">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="576f9-331">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="576f9-332">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="576f9-332">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="576f9-333">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="576f9-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="576f9-334">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="576f9-334">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-335">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="576f9-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-337">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="576f9-337">The last requested or desired state for the element.</span></span> <span data-ttu-id="576f9-338">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="576f9-338">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="576f9-339">**Estado**</span><span class="sxs-lookup"><span data-stu-id="576f9-339">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="576f9-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-342">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="576f9-342">The current status of the object.</span></span> <span data-ttu-id="576f9-343">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="576f9-343">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-344">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="576f9-344">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-345">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="576f9-345">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="576f9-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-347">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="576f9-347">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="576f9-348">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="576f9-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="576f9-349">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="576f9-349">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-350">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="576f9-350">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-352">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="576f9-352">The current state of the logical device.</span></span> <span data-ttu-id="576f9-353">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="576f9-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-354">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="576f9-354">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-355">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="576f9-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-357">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="576f9-357">The scoping system's creation class name.</span></span> <span data-ttu-id="576f9-358">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="576f9-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="576f9-359">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="576f9-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-360">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="576f9-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-362">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="576f9-362">The scoping system's name.</span></span> <span data-ttu-id="576f9-363">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y es el nombre del [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que está asociado a este servicio de latido.</span><span class="sxs-lookup"><span data-stu-id="576f9-363">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is the name of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) that is associated with this heartbeat service.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-364">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="576f9-364">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-365">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="576f9-365">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-367">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="576f9-367">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="576f9-368">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="576f9-368">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-369">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="576f9-369">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-370">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="576f9-370">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-372">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576f9-372">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="576f9-373">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="576f9-373">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="576f9-374">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="576f9-374">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="576f9-375">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="576f9-375">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="576f9-376">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="576f9-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="576f9-377">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="576f9-377">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="576f9-378">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="576f9-378">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="576f9-379">Observaciones</span><span class="sxs-lookup"><span data-stu-id="576f9-379">Remarks</span></span>

<span data-ttu-id="576f9-380">El acceso a la clase **MSVM \_ HeartbeatComponent** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="576f9-380">Access to the **Msvm\_HeartbeatComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="576f9-381">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="576f9-381">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="576f9-382">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="576f9-382">Examples</span></span>

<span data-ttu-id="576f9-383">En el siguiente ejemplo de C# se obtiene el estado de mantenimiento de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="576f9-383">The following C# sample obtains the application health status of a virtual machine.</span></span> <span data-ttu-id="576f9-384">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="576f9-384">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="576f9-385">Para que funcione correctamente, se debe ejecutar el siguiente código con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="576f9-385">To function correctly, the following code must be run with Administrator privileges.</span></span>

 


```CSharp
private UInt16 OperationalStatusOk = 2;
private UInt16 OperationalStatusApplicationCriticalState = 32782;

/// <summary>
/// Gets the applications status in the VM.
/// </summary>
/// <param name="hostMachine">The hostname of the machine on which
/// the VM is running.</param>
/// <param name="vmName">The VM name.</param>
public
void
GetAppHealthStatus(
    string hostMachine,
    string vmName
    )
{
    ManagementScope scope = new ManagementScope(
        @"\\" + hostMachine + @"\root\virtualization\v2", null);

    ManagementObject heartBeatComponent = null;

    // Get the VM object and its heart beat component.
    using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, scope))
    using (ManagementObjectCollection heartBeatCollection =
        vm.GetRelated("Msvm_HeartbeatComponent", "Msvm_SystemDevice",
            null, null, null, null, false, null))
    {
        foreach (ManagementObject element in heartBeatCollection)
        {
            heartBeatComponent = element;
            break;
        }
    }

    if (heartBeatComponent == null)
    {
        Console.WriteLine("The VM is not running.");
        return;
    }

    using (heartBeatComponent)
    {
        UInt16[] operationalStatus = (UInt16[])heartBeatComponent["OperationalStatus"];
        UInt16 vmStatus = operationalStatus[0];

        if (vmStatus != OperationalStatusOk)
        {
            Console.WriteLine("The VM heartbeat status is not OK");
            return;
        }

        if (operationalStatus.Length != 2)
        {
            Console.WriteLine("The required Integration Components are not running " +
                "or not installed.");
            return;
        }

        UInt16 appStatus = operationalStatus[1];
        if (appStatus == OperationalStatusOk)
        {
            Console.WriteLine("The VM applications health status: OK");
        }
        else if (appStatus == OperationalStatusApplicationCriticalState)
        {
            Console.WriteLine("The VM applications health status: Critical");
        }
        else
        {
            throw new ManagementException("Unknown application health status");
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="576f9-386">Requisitos</span><span class="sxs-lookup"><span data-stu-id="576f9-386">Requirements</span></span>



| <span data-ttu-id="576f9-387">Requisito</span><span class="sxs-lookup"><span data-stu-id="576f9-387">Requirement</span></span> | <span data-ttu-id="576f9-388">Value</span><span class="sxs-lookup"><span data-stu-id="576f9-388">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="576f9-389">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="576f9-389">Minimum supported client</span></span><br/> | <span data-ttu-id="576f9-390">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="576f9-390">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="576f9-391">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="576f9-391">Minimum supported server</span></span><br/> | <span data-ttu-id="576f9-392">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="576f9-392">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="576f9-393">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="576f9-393">Namespace</span></span><br/>                | <span data-ttu-id="576f9-394">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="576f9-394">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="576f9-395">MOF</span><span class="sxs-lookup"><span data-stu-id="576f9-395">MOF</span></span><br/>                      | <dl> <span data-ttu-id="576f9-396"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="576f9-396"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="576f9-397">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="576f9-397">DLL</span></span><br/>                      | <dl> <span data-ttu-id="576f9-398"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="576f9-398"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="576f9-399">Vea también</span><span class="sxs-lookup"><span data-stu-id="576f9-399">See also</span></span>

<dl> <dt>

[<span data-ttu-id="576f9-400">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="576f9-400">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="576f9-401">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="576f9-401">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> <dt>

[<span data-ttu-id="576f9-402">**MSVM \_ HeartbeatComponent**</span><span class="sxs-lookup"><span data-stu-id="576f9-402">**Msvm\_HeartbeatComponent**</span></span>](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponent)
</dt> </dl>

 

