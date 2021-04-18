---
description: Representa el estado del servicio de sincronización de hora, que es responsable de sincronizar la hora del sistema de una máquina virtual con la hora del sistema del sistema operativo que se ejecuta en el sistema operativo de administración.
ms.assetid: 551A81E9-E924-4A9C-965D-02FF25EE4A49
title: Msvm_TimeSyncComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TimeSyncComponent
- Msvm_TimeSyncComponent.SetPowerState
- Msvm_TimeSyncComponent.EnableDevice
- Msvm_TimeSyncComponent.OnlineDevice
- Msvm_TimeSyncComponent.QuiesceDevice
- Msvm_TimeSyncComponent.SaveProperties
- Msvm_TimeSyncComponent.RestoreProperties
- Msvm_TimeSyncComponent.InstanceID
- Msvm_TimeSyncComponent.Caption
- Msvm_TimeSyncComponent.Description
- Msvm_TimeSyncComponent.ElementName
- Msvm_TimeSyncComponent.InstallDate
- Msvm_TimeSyncComponent.Name
- Msvm_TimeSyncComponent.OperationalStatus
- Msvm_TimeSyncComponent.StatusDescriptions
- Msvm_TimeSyncComponent.Status
- Msvm_TimeSyncComponent.HealthState
- Msvm_TimeSyncComponent.CommunicationStatus
- Msvm_TimeSyncComponent.DetailedStatus
- Msvm_TimeSyncComponent.OperatingStatus
- Msvm_TimeSyncComponent.PrimaryStatus
- Msvm_TimeSyncComponent.EnabledState
- Msvm_TimeSyncComponent.OtherEnabledState
- Msvm_TimeSyncComponent.RequestedState
- Msvm_TimeSyncComponent.EnabledDefault
- Msvm_TimeSyncComponent.TimeOfLastStateChange
- Msvm_TimeSyncComponent.AvailableRequestedStates
- Msvm_TimeSyncComponent.TransitioningToState
- Msvm_TimeSyncComponent.SystemCreationClassName
- Msvm_TimeSyncComponent.SystemName
- Msvm_TimeSyncComponent.CreationClassName
- Msvm_TimeSyncComponent.DeviceID
- Msvm_TimeSyncComponent.PowerManagementSupported
- Msvm_TimeSyncComponent.PowerManagementCapabilities
- Msvm_TimeSyncComponent.Availability
- Msvm_TimeSyncComponent.StatusInfo
- Msvm_TimeSyncComponent.LastErrorCode
- Msvm_TimeSyncComponent.ErrorDescription
- Msvm_TimeSyncComponent.ErrorCleared
- Msvm_TimeSyncComponent.OtherIdentifyingInfo
- Msvm_TimeSyncComponent.PowerOnHours
- Msvm_TimeSyncComponent.TotalPowerOnHours
- Msvm_TimeSyncComponent.IdentifyingDescriptions
- Msvm_TimeSyncComponent.AdditionalAvailability
- Msvm_TimeSyncComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ea9a33d665a315861d9e6c51fd529f10f07b4aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687114"
---
# <a name="msvm_timesynccomponent-class"></a><span data-ttu-id="a60f5-103">MSVM \_ TimeSyncComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="a60f5-103">Msvm\_TimeSyncComponent class</span></span>

<span data-ttu-id="a60f5-104">Representa el estado del servicio de sincronización de hora, que es responsable de sincronizar la hora del sistema de una máquina virtual con la hora del sistema del sistema operativo que se ejecuta en el sistema operativo de administración.</span><span class="sxs-lookup"><span data-stu-id="a60f5-104">Represents the state of the time synchronization service, which is responsible for synchronizing the system time of a virtual machine with the system time of the operating system running in the management operating system.</span></span>

<span data-ttu-id="a60f5-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a60f5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a60f5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a60f5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TimeSyncComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Time Synchronization";
  string   Description = "Microsoft Time Synchronization Service";
  string   ElementName = "Time Synchronization";
  datetime InstallDate;
  string   Name = "Time Synchronization";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = {"OK"};
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_TimeSyncComponent";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="a60f5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a60f5-107">Members</span></span>

<span data-ttu-id="a60f5-108">La clase **MSVM \_ TimeSyncComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a60f5-108">The **Msvm\_TimeSyncComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="a60f5-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a60f5-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="a60f5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a60f5-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a60f5-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a60f5-111">Methods</span></span>

<span data-ttu-id="a60f5-112">La clase **MSVM \_ TimeSyncComponent** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a60f5-112">The **Msvm\_TimeSyncComponent** class has these methods.</span></span>



| <span data-ttu-id="a60f5-113">Método</span><span class="sxs-lookup"><span data-stu-id="a60f5-113">Method</span></span>                                                                  | <span data-ttu-id="a60f5-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a60f5-114">Description</span></span>                              |
|:------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="a60f5-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="a60f5-115">**EnableDevice**</span></span>                                                        | <span data-ttu-id="a60f5-116">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="a60f5-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a60f5-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="a60f5-117">**OnlineDevice**</span></span>                                                        | <span data-ttu-id="a60f5-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="a60f5-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a60f5-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="a60f5-119">**QuiesceDevice**</span></span>                                                       | <span data-ttu-id="a60f5-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="a60f5-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="a60f5-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="a60f5-121">**RequestStateChange**</span></span>](msvm-timesynccomponent-requeststatechange.md) | <span data-ttu-id="a60f5-122">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="a60f5-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="a60f5-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="a60f5-123">**Reset**</span></span>](msvm-timesynccomponent-reset.md)                           | <span data-ttu-id="a60f5-124">Restablece el componente.</span><span class="sxs-lookup"><span data-stu-id="a60f5-124">Resets the component.</span></span><br/>         |
| <span data-ttu-id="a60f5-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="a60f5-125">**RestoreProperties**</span></span>                                                   | <span data-ttu-id="a60f5-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="a60f5-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a60f5-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="a60f5-127">**SaveProperties**</span></span>                                                      | <span data-ttu-id="a60f5-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="a60f5-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a60f5-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a60f5-129">**SetPowerState**</span></span>                                                       | <span data-ttu-id="a60f5-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="a60f5-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a60f5-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a60f5-131">Properties</span></span>

<span data-ttu-id="a60f5-132">La clase **MSVM \_ TimeSyncComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a60f5-132">The **Msvm\_TimeSyncComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a60f5-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="a60f5-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-134">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a60f5-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-136">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a60f5-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="a60f5-137">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre está establecida en 6 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="a60f5-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-138">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="a60f5-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a60f5-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-141">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a60f5-141">The primary availability and status of the device.</span></span> <span data-ttu-id="a60f5-142">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a60f5-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="a60f5-143">Value</span><span class="sxs-lookup"><span data-stu-id="a60f5-143">Value</span></span>                                                                        | <span data-ttu-id="a60f5-144">Significado</span><span class="sxs-lookup"><span data-stu-id="a60f5-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a60f5-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a60f5-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="a60f5-146">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="a60f5-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a60f5-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="a60f5-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-148">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a60f5-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-150">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="a60f5-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="a60f5-151">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="a60f5-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-152">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a60f5-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a60f5-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-155">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a60f5-155">A short description of the object.</span></span> <span data-ttu-id="a60f5-156">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a60f5-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="a60f5-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-158">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a60f5-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-160">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="a60f5-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a60f5-161">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a60f5-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a60f5-162">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a60f5-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a60f5-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a60f5-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="a60f5-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="a60f5-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="a60f5-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="a60f5-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a60f5-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="a60f5-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a60f5-170">)</span><span class="sxs-lookup"><span data-stu-id="a60f5-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a60f5-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a60f5-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a60f5-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-174">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a60f5-174">The scoping system's creation class name.</span></span> <span data-ttu-id="a60f5-175">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a60f5-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-176">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a60f5-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a60f5-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-179">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a60f5-179">A description of the object.</span></span> <span data-ttu-id="a60f5-180">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a60f5-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a60f5-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-182">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a60f5-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-184">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="a60f5-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a60f5-185">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a60f5-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a60f5-186">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a60f5-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a60f5-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="a60f5-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="a60f5-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="a60f5-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="a60f5-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="a60f5-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="a60f5-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a60f5-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="a60f5-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a60f5-195">)</span><span class="sxs-lookup"><span data-stu-id="a60f5-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a60f5-196">**ID**</span><span class="sxs-lookup"><span data-stu-id="a60f5-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a60f5-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-199">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a60f5-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="a60f5-200">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "Microsoft:*VMGUID* \\ *GUID*", donde *VMGUID* es la propiedad **Name** de la instancia de [**MSVM \_ ComputerSystem**](msvm-computersystem.md) asociada con este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a60f5-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) instance associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a60f5-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a60f5-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-204">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="a60f5-204">A display name for the object.</span></span> <span data-ttu-id="a60f5-205">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a60f5-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-206">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="a60f5-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-207">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a60f5-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-209">Configuración predeterminada o de inicio de un administrador para **EnabledState** de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a60f5-209">An administrator's default or startup configuration for the **EnabledState** of an element.</span></span> <span data-ttu-id="a60f5-210">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a60f5-210">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="a60f5-211">Value</span><span class="sxs-lookup"><span data-stu-id="a60f5-211">Value</span></span>                                                                        | <span data-ttu-id="a60f5-212">Significado</span><span class="sxs-lookup"><span data-stu-id="a60f5-212">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="a60f5-213"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a60f5-213"><dt>7</dt></span></span> </dl> | <span data-ttu-id="a60f5-214">Sin valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="a60f5-214">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a60f5-215">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a60f5-215">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-216">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a60f5-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-218">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a60f5-218">The enabled and disabled states of an element.</span></span> <span data-ttu-id="a60f5-219">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) y está establecida en 2 (habilitado) o 3 (deshabilitada).</span><span class="sxs-lookup"><span data-stu-id="a60f5-219">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is either set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="a60f5-220">Value</span><span class="sxs-lookup"><span data-stu-id="a60f5-220">Value</span></span>                                                                        | <span data-ttu-id="a60f5-221">Significado</span><span class="sxs-lookup"><span data-stu-id="a60f5-221">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="a60f5-222"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a60f5-222"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a60f5-223">habilitado</span><span class="sxs-lookup"><span data-stu-id="a60f5-223">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="a60f5-224"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a60f5-224"><dt>3</dt></span></span> </dl> | <span data-ttu-id="a60f5-225">Disabled</span><span class="sxs-lookup"><span data-stu-id="a60f5-225">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a60f5-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a60f5-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-227">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a60f5-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-229">Indica si el error comunicado en la propiedad **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="a60f5-229">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="a60f5-230">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="a60f5-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a60f5-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-232">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a60f5-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-234">Una cadena que proporciona más información sobre el error registrado en la propiedad **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="a60f5-234">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="a60f5-235">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="a60f5-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-236">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a60f5-236">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-237">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a60f5-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-239">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="a60f5-239">The current health of the element.</span></span> <span data-ttu-id="a60f5-240">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a60f5-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="a60f5-241">Value</span><span class="sxs-lookup"><span data-stu-id="a60f5-241">Value</span></span>                                                                        | <span data-ttu-id="a60f5-242">Significado</span><span class="sxs-lookup"><span data-stu-id="a60f5-242">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="a60f5-243"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a60f5-243"><dt>5</dt></span></span> </dl> | <span data-ttu-id="a60f5-244">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a60f5-244">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a60f5-245">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a60f5-245">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-246">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="a60f5-246">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-248">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="a60f5-248">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="a60f5-249">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="a60f5-249">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-250">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a60f5-250">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-251">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a60f5-251">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-253">Fecha y hora en que se instaló el servicio de integración en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a60f5-253">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="a60f5-254">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a60f5-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-255">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a60f5-255">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-256">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a60f5-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-258">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="a60f5-258">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-259">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="a60f5-259">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a60f5-260">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a60f5-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-261">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a60f5-261">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-262">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a60f5-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-264">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a60f5-264">The last error code reported by the logical device.</span></span> <span data-ttu-id="a60f5-265">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="a60f5-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-266">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="a60f5-266">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-267">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a60f5-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-269">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="a60f5-269">This property has been deprecated.</span></span> <span data-ttu-id="a60f5-270">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a60f5-270">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-271">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a60f5-271">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-272">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a60f5-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-273">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-274">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="a60f5-274">The label by which the object is known.</span></span> <span data-ttu-id="a60f5-275">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a60f5-275">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-276">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="a60f5-276">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-277">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a60f5-277">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-279">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="a60f5-279">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a60f5-280">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a60f5-280">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a60f5-281">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a60f5-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a60f5-282"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a60f5-282"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-283"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="a60f5-283"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-284"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="a60f5-284"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-285"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="a60f5-285"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-286"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="a60f5-286"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-287"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="a60f5-287"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-288"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="a60f5-288"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-289"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="a60f5-289"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-290"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="a60f5-290"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-291"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="a60f5-291"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-292"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="a60f5-292"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-293"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="a60f5-293"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-294"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="a60f5-294"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-295"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="a60f5-295"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-296"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="a60f5-296"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-297"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="a60f5-297"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-298"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="a60f5-298"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a60f5-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="a60f5-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a60f5-301">)</span><span class="sxs-lookup"><span data-stu-id="a60f5-301">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a60f5-302">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a60f5-302">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-303">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a60f5-303">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-305">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="a60f5-305">The current status of the element.</span></span> <span data-ttu-id="a60f5-306">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a60f5-306">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="a60f5-307">A continuación se muestran los posibles valores para el valor de la propiedad **OperationalStatus** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="a60f5-307">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="a60f5-308">Value</span><span class="sxs-lookup"><span data-stu-id="a60f5-308">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="a60f5-309">Significado</span><span class="sxs-lookup"><span data-stu-id="a60f5-309">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a60f5-310"><dt>dos</dt></span><span class="sxs-lookup"><span data-stu-id="a60f5-310"><dt>{ 2 }</dt></span></span> </dl>                                                                                                                                                                                                    |                                                                                                                                                                                                                                          |
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="a60f5-311"><dt>**Aceptar**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a60f5-311"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="a60f5-312">El servicio está funcionando con normalidad.</span><span class="sxs-lookup"><span data-stu-id="a60f5-312">The service is operating normally.</span></span> <span data-ttu-id="a60f5-313">Los valores de la propiedad **OperationalStatus** \[ 1 \] y **StatusDescriptions** \[ 1 \] pueden contener más información.</span><span class="sxs-lookup"><span data-stu-id="a60f5-313">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="a60f5-314"><dt>**Degradado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a60f5-314"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="a60f5-315">El servicio está funcionando con normalidad, pero el servicio invitado negoció una versión del Protocolo de comunicaciones compatible.</span><span class="sxs-lookup"><span data-stu-id="a60f5-315">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="a60f5-316">Los valores de la propiedad **OperationalStatus** \[ 1 \] y **StatusDescriptions** \[ 1 \] pueden contener más información.</span><span class="sxs-lookup"><span data-stu-id="a60f5-316">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="a60f5-317"><dt>**Error no recuperable**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a60f5-317"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="a60f5-318">El invitado no es compatible con una versión de protocolo compatible.</span><span class="sxs-lookup"><span data-stu-id="a60f5-318">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="a60f5-319">Los valores de la propiedad **OperationalStatus** \[ 1 \] y **StatusDescriptions** \[ 1 \] pueden contener más información.</span><span class="sxs-lookup"><span data-stu-id="a60f5-319">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="a60f5-320"><dt>**No Contact**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a60f5-320"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="a60f5-321">El servicio invitado no está instalado o no se ha conectado todavía.</span><span class="sxs-lookup"><span data-stu-id="a60f5-321">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="a60f5-322"><dt>**Comunicación perdida**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="a60f5-322"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="a60f5-323">El servicio invitado ya no responde normalmente.</span><span class="sxs-lookup"><span data-stu-id="a60f5-323">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="a60f5-324">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="a60f5-324">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-325">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a60f5-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-327">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="a60f5-327">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="a60f5-328">Esta propiedad debe establecerse en **null** cuando la propiedad **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="a60f5-328">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="a60f5-329">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="a60f5-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-330">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="a60f5-330">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-331">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="a60f5-331">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-333">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a60f5-333">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="a60f5-334">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="a60f5-334">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-335">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a60f5-335">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-336">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a60f5-336">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-338">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a60f5-338">The power management capabilities of the device.</span></span> <span data-ttu-id="a60f5-339">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="a60f5-339">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-340">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a60f5-340">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-341">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a60f5-341">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-343">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="a60f5-343">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="a60f5-344">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="a60f5-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-345">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="a60f5-345">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-346">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a60f5-346">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-348">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="a60f5-348">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="a60f5-349">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="a60f5-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-350">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="a60f5-350">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-351">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a60f5-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-352">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-353">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="a60f5-353">Provides high level status information.</span></span> <span data-ttu-id="a60f5-354">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="a60f5-354">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="a60f5-355">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a60f5-355">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a60f5-356">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a60f5-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a60f5-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a60f5-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-358"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="a60f5-358"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-359"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="a60f5-359"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-360"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="a60f5-360"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-361"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a60f5-361"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-362"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="a60f5-362"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a60f5-363">)</span><span class="sxs-lookup"><span data-stu-id="a60f5-363">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a60f5-364">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="a60f5-364">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-365">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a60f5-365">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-367">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="a60f5-367">The last requested or desired state for the element.</span></span> <span data-ttu-id="a60f5-368">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a60f5-368">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="a60f5-369">Value</span><span class="sxs-lookup"><span data-stu-id="a60f5-369">Value</span></span>                                                                         | <span data-ttu-id="a60f5-370">Significado</span><span class="sxs-lookup"><span data-stu-id="a60f5-370">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a60f5-371"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a60f5-371"><dt>12</dt></span></span> </dl> | <span data-ttu-id="a60f5-372">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="a60f5-372">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a60f5-373">**Estado**</span><span class="sxs-lookup"><span data-stu-id="a60f5-373">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-374">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a60f5-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-376">Cadena que especifica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a60f5-376">A string that specifies the current status of the object.</span></span> <span data-ttu-id="a60f5-377">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="a60f5-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-378">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a60f5-378">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-379">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="a60f5-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-381">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="a60f5-381">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a60f5-382">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a60f5-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a60f5-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-384">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a60f5-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-385">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-386">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a60f5-386">The current state of the logical device.</span></span> <span data-ttu-id="a60f5-387">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="a60f5-387">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-388">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a60f5-388">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-389">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a60f5-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-391">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a60f5-391">The creation class name of the scoping system.</span></span> <span data-ttu-id="a60f5-392">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a60f5-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-393">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a60f5-393">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-394">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a60f5-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-395">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-396">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a60f5-396">The name of the scoping system.</span></span> <span data-ttu-id="a60f5-397">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a60f5-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-398">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="a60f5-398">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-399">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a60f5-399">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-401">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="a60f5-401">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="a60f5-402">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="a60f5-402">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-403">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="a60f5-403">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-404">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a60f5-404">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-405">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-406">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a60f5-406">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="a60f5-407">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="a60f5-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a60f5-408">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="a60f5-408">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a60f5-409">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a60f5-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a60f5-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a60f5-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a60f5-411">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="a60f5-411">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="a60f5-412">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a60f5-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="a60f5-413">Value</span><span class="sxs-lookup"><span data-stu-id="a60f5-413">Value</span></span>                                                                         | <span data-ttu-id="a60f5-414">Significado</span><span class="sxs-lookup"><span data-stu-id="a60f5-414">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a60f5-415"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a60f5-415"><dt>12</dt></span></span> </dl> | <span data-ttu-id="a60f5-416">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="a60f5-416">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a60f5-417">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a60f5-417">Remarks</span></span>

<span data-ttu-id="a60f5-418">El acceso a la clase **MSVM \_ TimeSyncComponent** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="a60f5-418">Access to the **Msvm\_TimeSyncComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a60f5-419">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a60f5-419">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a60f5-420">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a60f5-420">Requirements</span></span>



| <span data-ttu-id="a60f5-421">Requisito</span><span class="sxs-lookup"><span data-stu-id="a60f5-421">Requirement</span></span> | <span data-ttu-id="a60f5-422">Value</span><span class="sxs-lookup"><span data-stu-id="a60f5-422">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a60f5-423">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a60f5-423">Minimum supported client</span></span><br/> | <span data-ttu-id="a60f5-424">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a60f5-424">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a60f5-425">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a60f5-425">Minimum supported server</span></span><br/> | <span data-ttu-id="a60f5-426">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a60f5-426">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a60f5-427">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a60f5-427">Namespace</span></span><br/>                | <span data-ttu-id="a60f5-428">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a60f5-428">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a60f5-429">MOF</span><span class="sxs-lookup"><span data-stu-id="a60f5-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a60f5-430"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a60f5-430"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a60f5-431">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a60f5-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a60f5-432"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a60f5-432"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a60f5-433">Vea también</span><span class="sxs-lookup"><span data-stu-id="a60f5-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a60f5-434">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a60f5-434">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="a60f5-435">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a60f5-435">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

