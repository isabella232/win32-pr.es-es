---
description: Representa el procesador virtual en una máquina virtual.
ms.assetid: 4BA91C44-0F85-42D1-A8B5-147E1D532FB5
title: Clase Msvm_Processor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Processor
- Msvm_Processor.SetPowerState
- Msvm_Processor.EnableDevice
- Msvm_Processor.OnlineDevice
- Msvm_Processor.QuiesceDevice
- Msvm_Processor.SaveProperties
- Msvm_Processor.RestoreProperties
- Msvm_Processor.InstanceID
- Msvm_Processor.Caption
- Msvm_Processor.Description
- Msvm_Processor.ElementName
- Msvm_Processor.InstallDate
- Msvm_Processor.Name
- Msvm_Processor.OperationalStatus
- Msvm_Processor.StatusDescriptions
- Msvm_Processor.Status
- Msvm_Processor.HealthState
- Msvm_Processor.CommunicationStatus
- Msvm_Processor.DetailedStatus
- Msvm_Processor.OperatingStatus
- Msvm_Processor.PrimaryStatus
- Msvm_Processor.EnabledState
- Msvm_Processor.OtherEnabledState
- Msvm_Processor.RequestedState
- Msvm_Processor.EnabledDefault
- Msvm_Processor.TimeOfLastStateChange
- Msvm_Processor.AvailableRequestedStates
- Msvm_Processor.TransitioningToState
- Msvm_Processor.SystemCreationClassName
- Msvm_Processor.SystemName
- Msvm_Processor.CreationClassName
- Msvm_Processor.DeviceID
- Msvm_Processor.PowerManagementSupported
- Msvm_Processor.PowerManagementCapabilities
- Msvm_Processor.Availability
- Msvm_Processor.StatusInfo
- Msvm_Processor.LastErrorCode
- Msvm_Processor.ErrorDescription
- Msvm_Processor.ErrorCleared
- Msvm_Processor.OtherIdentifyingInfo
- Msvm_Processor.PowerOnHours
- Msvm_Processor.TotalPowerOnHours
- Msvm_Processor.IdentifyingDescriptions
- Msvm_Processor.AdditionalAvailability
- Msvm_Processor.MaxQuiesceTime
- Msvm_Processor.Role
- Msvm_Processor.Family
- Msvm_Processor.OtherFamilyDescription
- Msvm_Processor.UpgradeMethod
- Msvm_Processor.MaxClockSpeed
- Msvm_Processor.CurrentClockSpeed
- Msvm_Processor.DataWidth
- Msvm_Processor.AddressWidth
- Msvm_Processor.LoadPercentage
- Msvm_Processor.Stepping
- Msvm_Processor.UniqueID
- Msvm_Processor.CPUStatus
- Msvm_Processor.ExternalBusClockSpeed
- Msvm_Processor.LoadPercentageHistory
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 14ed1e2bbb9e15f89376234da8981faffb1a6809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910146"
---
# <a name="msvm_processor-class"></a><span data-ttu-id="be7f7-103">\_Clase de procesador MSVM</span><span class="sxs-lookup"><span data-stu-id="be7f7-103">Msvm\_Processor class</span></span>

<span data-ttu-id="be7f7-104">Representa el procesador virtual en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="be7f7-104">Represents the virtual processor in a virtual machine.</span></span>

<span data-ttu-id="be7f7-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="be7f7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="be7f7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be7f7-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Processor : CIM_Processor
{
  string   InstanceID;
  string   Caption = "Processor";
  string   Description = " A logical processor of the hypervisor running on the host computer system.";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 2;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_Processor";
  string   DeviceID = "Microsoft:GUID\device specific data";
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
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  string   Role = "Central Processor";
  uint16   Family;
  string   OtherFamilyDescription;
  uint16   UpgradeMethod;
  uint32   MaxClockSpeed;
  uint32   CurrentClockSpeed;
  uint16   DataWidth;
  uint16   AddressWidth;
  uint16   LoadPercentage;
  string   Stepping;
  string   UniqueID;
  uint16   CPUStatus;
  uint32   ExternalBusClockSpeed;
  uint16   LoadPercentageHistory[];
};
```

## <a name="members"></a><span data-ttu-id="be7f7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="be7f7-107">Members</span></span>

<span data-ttu-id="be7f7-108">La clase de **\_ procesador MSVM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="be7f7-108">The **Msvm\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="be7f7-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="be7f7-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="be7f7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="be7f7-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="be7f7-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="be7f7-111">Methods</span></span>

<span data-ttu-id="be7f7-112">La clase de **\_ procesador MSVM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="be7f7-112">The **Msvm\_Processor** class has these methods.</span></span>



| <span data-ttu-id="be7f7-113">Método</span><span class="sxs-lookup"><span data-stu-id="be7f7-113">Method</span></span>                                                          | <span data-ttu-id="be7f7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="be7f7-114">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="be7f7-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="be7f7-115">**EnableDevice**</span></span>                                                | <span data-ttu-id="be7f7-116">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="be7f7-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="be7f7-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="be7f7-117">**OnlineDevice**</span></span>                                                | <span data-ttu-id="be7f7-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="be7f7-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="be7f7-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="be7f7-119">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="be7f7-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="be7f7-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="be7f7-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="be7f7-121">**RequestStateChange**</span></span>](msvm-processor-requeststatechange.md) | <span data-ttu-id="be7f7-122">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="be7f7-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="be7f7-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="be7f7-123">**Reset**</span></span>](msvm-processor-reset.md)                           | <span data-ttu-id="be7f7-124">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="be7f7-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="be7f7-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="be7f7-125">**RestoreProperties**</span></span>                                           | <span data-ttu-id="be7f7-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="be7f7-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="be7f7-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="be7f7-127">**SaveProperties**</span></span>                                              | <span data-ttu-id="be7f7-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="be7f7-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="be7f7-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="be7f7-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="be7f7-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="be7f7-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="be7f7-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="be7f7-131">Properties</span></span>

<span data-ttu-id="be7f7-132">La clase de **\_ procesador MSVM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="be7f7-132">The **Msvm\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be7f7-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="be7f7-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-134">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-136">Cualquier disponibilidad adicional y estado del dispositivo, más allá de lo especificado en la propiedad **Availability** .</span><span class="sxs-lookup"><span data-stu-id="be7f7-136">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="be7f7-137">La propiedad **Availability** denota el estado principal y la disponibilidad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be7f7-137">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="be7f7-138">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="be7f7-138">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-139">**AddressWidth**</span><span class="sxs-lookup"><span data-stu-id="be7f7-139">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-140">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-142">Ancho de la dirección del procesador, en bits.</span><span class="sxs-lookup"><span data-stu-id="be7f7-142">The processor address width, in bits.</span></span> <span data-ttu-id="be7f7-143">Esta propiedad se hereda del [**\_ procesador CIM**](/windows/desktop/CIMWin32Prov/cim-processor)y el valor es 32 o 64, en función de las características de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="be7f7-143">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and the value is either 32 or 64, depending on the characteristics of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-144">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="be7f7-144">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-145">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-147">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be7f7-147">The primary availability and status of the device.</span></span> <span data-ttu-id="be7f7-148">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="be7f7-148">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-149">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="be7f7-149">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-150">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-152">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="be7f7-152">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="be7f7-153">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="be7f7-153">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-154">**Caption**</span><span class="sxs-lookup"><span data-stu-id="be7f7-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-157">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="be7f7-157">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-158">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="be7f7-158">A short description of the object.</span></span> <span data-ttu-id="be7f7-159">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="be7f7-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-160">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="be7f7-160">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-161">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-163">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="be7f7-163">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="be7f7-164">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="be7f7-164">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="be7f7-165">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be7f7-165">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="be7f7-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="be7f7-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-167"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="be7f7-167"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-168"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="be7f7-168"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-169"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="be7f7-169"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-170"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="be7f7-170"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-171"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="be7f7-171"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-172"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="be7f7-172"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="be7f7-173">)</span><span class="sxs-lookup"><span data-stu-id="be7f7-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be7f7-174">**CPUStatus**</span><span class="sxs-lookup"><span data-stu-id="be7f7-174">**CPUStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-175">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-177">Estado actual del procesador.</span><span class="sxs-lookup"><span data-stu-id="be7f7-177">The current status of the processor.</span></span> <span data-ttu-id="be7f7-178">Esta propiedad se hereda del [**\_ procesador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="be7f7-178">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-179">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="be7f7-179">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-182">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="be7f7-182">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-183">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="be7f7-183">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="be7f7-184">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="be7f7-184">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="be7f7-185">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="be7f7-185">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-186">**CurrentClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="be7f7-186">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-187">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be7f7-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-189">La velocidad máxima del procesador físico, teniendo en cuenta la capacidad del procesador virtual.</span><span class="sxs-lookup"><span data-stu-id="be7f7-189">The maximum speed of the physical processor, taking into account the capacity for the virtual processor.</span></span> <span data-ttu-id="be7f7-190">Esta propiedad se hereda del [**\_ procesador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="be7f7-190">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-191">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="be7f7-191">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-192">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-194">El ancho de los datos del procesador, en bits.</span><span class="sxs-lookup"><span data-stu-id="be7f7-194">The processor data width, in bits.</span></span> <span data-ttu-id="be7f7-195">Esta propiedad se hereda del [**\_ procesador CIM**](/windows/desktop/CIMWin32Prov/cim-processor)y el valor es 32 o 64, en función de las características de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="be7f7-195">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and the value is either 32 or 64, depending on the characteristics of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-196">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="be7f7-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-199">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="be7f7-199">A description of the object.</span></span> <span data-ttu-id="be7f7-200">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="be7f7-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="be7f7-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-202">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-204">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="be7f7-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="be7f7-205">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="be7f7-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="be7f7-206">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be7f7-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="be7f7-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="be7f7-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="be7f7-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="be7f7-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="be7f7-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="be7f7-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="be7f7-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="be7f7-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="be7f7-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="be7f7-215">)</span><span class="sxs-lookup"><span data-stu-id="be7f7-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be7f7-216">**ID**</span><span class="sxs-lookup"><span data-stu-id="be7f7-216">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-219">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="be7f7-219">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="be7f7-220">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "Microsoft:*GUID* \\ *Device specific Data*".</span><span class="sxs-lookup"><span data-stu-id="be7f7-220">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*\\*device specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-221">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="be7f7-221">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-224">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="be7f7-224">A display name for the object.</span></span> <span data-ttu-id="be7f7-225">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="be7f7-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-226">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="be7f7-226">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-227">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-229">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="be7f7-229">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="be7f7-230">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be7f7-230">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-231">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="be7f7-231">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-232">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-234">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="be7f7-234">The enabled and disabled states of an element.</span></span> <span data-ttu-id="be7f7-235">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be7f7-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-236">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="be7f7-236">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-237">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="be7f7-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-239">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="be7f7-239">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="be7f7-240">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="be7f7-240">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-241">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="be7f7-241">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-242">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-244">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="be7f7-244">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="be7f7-245">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="be7f7-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-246">**ExternalBusClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="be7f7-246">**ExternalBusClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-247">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be7f7-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-249">Velocidad del reloj del bus externo del procesador físico subyacente.</span><span class="sxs-lookup"><span data-stu-id="be7f7-249">The external bus clock speed of the underlying physical processor.</span></span> <span data-ttu-id="be7f7-250">Esta propiedad se hereda del [**\_ procesador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="be7f7-250">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-251">**Familia**</span><span class="sxs-lookup"><span data-stu-id="be7f7-251">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-252">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-254">Familia de procesadores del procesador físico subyacente.</span><span class="sxs-lookup"><span data-stu-id="be7f7-254">The processor family of the underlying physical processor.</span></span> <span data-ttu-id="be7f7-255">Esta propiedad se hereda del [**\_ procesador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="be7f7-255">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-256">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="be7f7-256">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-257">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-259">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="be7f7-259">The current health of the element.</span></span> <span data-ttu-id="be7f7-260">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be7f7-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-261">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="be7f7-261">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-262">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="be7f7-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-264">Matriz de cadenas de formato libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz [**OtherIdentifyingInfo**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="be7f7-264">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="be7f7-265">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="be7f7-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-266">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="be7f7-266">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-267">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="be7f7-267">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-269">Fecha y hora en que se creó la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="be7f7-269">The date and time when the virtual machine was created.</span></span> <span data-ttu-id="be7f7-270">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be7f7-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="be7f7-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-272">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-273">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-274">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="be7f7-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-275">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="be7f7-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="be7f7-276">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="be7f7-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="be7f7-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-278">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be7f7-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-280">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="be7f7-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="be7f7-281">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="be7f7-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-282">**LoadPercentage**</span><span class="sxs-lookup"><span data-stu-id="be7f7-282">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-283">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-285">El porcentaje actual de la potencia de procesamiento total consumida por la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="be7f7-285">The current percentage of the total processing power being consumed by the virtual machine.</span></span> <span data-ttu-id="be7f7-286">Esta propiedad se hereda del [**\_ procesador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="be7f7-286">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-287">**LoadPercentageHistory**</span><span class="sxs-lookup"><span data-stu-id="be7f7-287">**LoadPercentageHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-288">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-288">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-290">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="be7f7-290">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-291">Historial registrado del porcentaje de la potencia de procesamiento total consumida por la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="be7f7-291">The recorded history of percentage of the total processing power being consumed by the virtual machine.</span></span> <span data-ttu-id="be7f7-292">Se trata de una matriz que contiene ejemplos.</span><span class="sxs-lookup"><span data-stu-id="be7f7-292">This is an array containing samples.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-293">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="be7f7-293">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-294">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be7f7-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-296">Velocidad máxima del reloj, en megahercios, del procesador virtual.</span><span class="sxs-lookup"><span data-stu-id="be7f7-296">The maximum clock speed, in megahertz, of the virtual processor.</span></span> <span data-ttu-id="be7f7-297">Esta propiedad se hereda del [**\_ procesador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="be7f7-297">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-298">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="be7f7-298">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-299">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be7f7-299">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-301">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="be7f7-301">This property has been deprecated.</span></span> <span data-ttu-id="be7f7-302">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="be7f7-302">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-303">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="be7f7-303">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-304">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-306">Calificadores: **MaxLen** (1024)</span><span class="sxs-lookup"><span data-stu-id="be7f7-306">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-307">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="be7f7-307">The label by which the object is known.</span></span> <span data-ttu-id="be7f7-308">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="be7f7-308">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="be7f7-309">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be7f7-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-310">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="be7f7-310">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-311">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-311">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-313">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="be7f7-313">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="be7f7-314">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="be7f7-314">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="be7f7-315">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be7f7-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="be7f7-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="be7f7-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-317"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="be7f7-317"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-318"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="be7f7-318"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-319"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="be7f7-319"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-320"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="be7f7-320"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-321"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="be7f7-321"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-322"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="be7f7-322"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-323"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="be7f7-323"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-324"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="be7f7-324"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-325"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="be7f7-325"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-326"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="be7f7-326"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-327"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="be7f7-327"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-328"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="be7f7-328"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-329"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="be7f7-329"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-330"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="be7f7-330"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-331"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="be7f7-331"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-332"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="be7f7-332"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="be7f7-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="be7f7-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="be7f7-335">)</span><span class="sxs-lookup"><span data-stu-id="be7f7-335">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be7f7-336">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="be7f7-336">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-337">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-339">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="be7f7-339">The current status of the element.</span></span> <span data-ttu-id="be7f7-340">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be7f7-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-341">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="be7f7-341">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-342">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-344">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="be7f7-344">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="be7f7-345">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="be7f7-345">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="be7f7-346">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be7f7-346">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-347">**OtherFamilyDescription**</span><span class="sxs-lookup"><span data-stu-id="be7f7-347">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-348">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-350">Descripción del tipo de familia de procesadores.</span><span class="sxs-lookup"><span data-stu-id="be7f7-350">A description of the processor family type.</span></span> <span data-ttu-id="be7f7-351">Esta propiedad se hereda del [**\_ procesador CIM**](/windows/desktop/CIMWin32Prov/cim-processor)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="be7f7-351">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-352">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="be7f7-352">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-353">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="be7f7-353">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-355">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="be7f7-355">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="be7f7-356">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="be7f7-356">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-357">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="be7f7-357">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-358">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-360">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be7f7-360">The power management capabilities of the device.</span></span> <span data-ttu-id="be7f7-361">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="be7f7-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-362">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="be7f7-362">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-363">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="be7f7-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-364">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-365">Indica si se admite la administración de energía en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be7f7-365">Indicates whether power management is supported on the device.</span></span> <span data-ttu-id="be7f7-366">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="be7f7-366">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-367">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="be7f7-367">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-368">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be7f7-368">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-370">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="be7f7-370">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="be7f7-371">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="be7f7-371">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-372">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="be7f7-372">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-373">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-374">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-375">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="be7f7-375">Provides high level status information.</span></span> <span data-ttu-id="be7f7-376">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="be7f7-376">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="be7f7-377">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="be7f7-377">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="be7f7-378">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be7f7-378">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="be7f7-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="be7f7-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-380"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="be7f7-380"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="be7f7-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-382"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="be7f7-382"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-383"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="be7f7-383"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-384"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="be7f7-384"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="be7f7-385">)</span><span class="sxs-lookup"><span data-stu-id="be7f7-385">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be7f7-386">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="be7f7-386">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-387">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-389">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="be7f7-389">The last requested or desired state for the element.</span></span> <span data-ttu-id="be7f7-390">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be7f7-390">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-391">**Rol**</span><span class="sxs-lookup"><span data-stu-id="be7f7-391">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-392">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-394">Cadena que describe el rol del procesador.</span><span class="sxs-lookup"><span data-stu-id="be7f7-394">A string that describes the role of the processor.</span></span> <span data-ttu-id="be7f7-395">Por ejemplo, "procesador central" o "procesador matemático".</span><span class="sxs-lookup"><span data-stu-id="be7f7-395">For example, "Central Processor" or "Math Processor".</span></span> <span data-ttu-id="be7f7-396">Esta propiedad se hereda del [**\_ procesador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="be7f7-396">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-397">**Estado**</span><span class="sxs-lookup"><span data-stu-id="be7f7-397">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-398">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-400">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="be7f7-400">The current status of the object.</span></span> <span data-ttu-id="be7f7-401">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="be7f7-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-402">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="be7f7-402">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-403">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="be7f7-403">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-405">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="be7f7-405">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="be7f7-406">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be7f7-406">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-407">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="be7f7-407">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-408">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-409">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-410">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="be7f7-410">The current state of the logical device.</span></span> <span data-ttu-id="be7f7-411">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="be7f7-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-412">**Recorrido paso a paso**</span><span class="sxs-lookup"><span data-stu-id="be7f7-412">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-413">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-414">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-415">El nivel de revisión del procesador dentro de la familia de procesadores del procesador físico subyacente.</span><span class="sxs-lookup"><span data-stu-id="be7f7-415">The revision level of the processor within the processor family of the underlying physical processor.</span></span> <span data-ttu-id="be7f7-416">Esta propiedad se hereda del [**\_ procesador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="be7f7-416">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-417">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="be7f7-417">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-418">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-419">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-420">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="be7f7-420">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-421">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="be7f7-421">The creation class name of the scoping system.</span></span> <span data-ttu-id="be7f7-422">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="be7f7-422">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-423">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="be7f7-423">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-424">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-425">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-426">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="be7f7-426">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-427">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="be7f7-427">The name of the scoping system.</span></span> <span data-ttu-id="be7f7-428">Este valor corresponde al valor de la propiedad [**Name**](msvm-computersystem.md) de la clase **MSVM \_ ComputerSystem** para el ámbito de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="be7f7-428">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="be7f7-429">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="be7f7-429">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-430">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="be7f7-430">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-431">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="be7f7-431">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-432">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-433">Fecha u hora en que se cambió el estado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="be7f7-433">The date or time at which the virtual machine's state was changed.</span></span> <span data-ttu-id="be7f7-434">Si el estado del elemento no ha cambiado y se rellena esta propiedad, debe establecerse en un valor de intervalo 0.</span><span class="sxs-lookup"><span data-stu-id="be7f7-434">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="be7f7-435">Si se solicitó un cambio de estado, pero se rechazó o no se procesó todavía, la propiedad no se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="be7f7-435">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="be7f7-436">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be7f7-436">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-437">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="be7f7-437">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-438">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be7f7-438">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-439">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-440">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be7f7-440">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="be7f7-441">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="be7f7-441">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-442">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="be7f7-442">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-443">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-443">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-444">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-445">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="be7f7-445">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="be7f7-446">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="be7f7-446">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-447">**UniqueID**</span><span class="sxs-lookup"><span data-stu-id="be7f7-447">**UniqueID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-448">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be7f7-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-449">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-450">Identificador único global para el procesador.</span><span class="sxs-lookup"><span data-stu-id="be7f7-450">A globally unique identifier for the processor.</span></span> <span data-ttu-id="be7f7-451">Este identificador solo puede ser único dentro de una familia de procesadores.</span><span class="sxs-lookup"><span data-stu-id="be7f7-451">This identifier can only be unique within a processor family.</span></span> <span data-ttu-id="be7f7-452">Esta propiedad se hereda del [**\_ procesador CIM**](/windows/desktop/CIMWin32Prov/cim-processor)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="be7f7-452">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-453">**UpgradeMethod**</span><span class="sxs-lookup"><span data-stu-id="be7f7-453">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7f7-454">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be7f7-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be7f7-455">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be7f7-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be7f7-456">La información del socket de la CPU, que incluye datos sobre cómo actualizar el procesador (si se admiten las actualizaciones).</span><span class="sxs-lookup"><span data-stu-id="be7f7-456">The CPU socket information, which includes data on how to upgrade the processor (if upgrades are supported).</span></span> <span data-ttu-id="be7f7-457">Esta propiedad se hereda del [**\_ procesador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="be7f7-457">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be7f7-458">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be7f7-458">Remarks</span></span>

<span data-ttu-id="be7f7-459">El acceso a la clase de **\_ procesador de MSVM** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="be7f7-459">Access to the **Msvm\_Processor** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="be7f7-460">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="be7f7-460">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="be7f7-461">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be7f7-461">Requirements</span></span>



| <span data-ttu-id="be7f7-462">Requisito</span><span class="sxs-lookup"><span data-stu-id="be7f7-462">Requirement</span></span> | <span data-ttu-id="be7f7-463">Value</span><span class="sxs-lookup"><span data-stu-id="be7f7-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be7f7-464">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be7f7-464">Minimum supported client</span></span><br/> | <span data-ttu-id="be7f7-465">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="be7f7-465">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="be7f7-466">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be7f7-466">Minimum supported server</span></span><br/> | <span data-ttu-id="be7f7-467">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="be7f7-467">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="be7f7-468">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="be7f7-468">Namespace</span></span><br/>                | <span data-ttu-id="be7f7-469">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="be7f7-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="be7f7-470">MOF</span><span class="sxs-lookup"><span data-stu-id="be7f7-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be7f7-471"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be7f7-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="be7f7-472">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="be7f7-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be7f7-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="be7f7-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="be7f7-474">Vea también</span><span class="sxs-lookup"><span data-stu-id="be7f7-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be7f7-475">**\_Procesador CIM**</span><span class="sxs-lookup"><span data-stu-id="be7f7-475">**CIM\_Processor**</span></span>](cim-processor.md)
</dt> <dt>

[<span data-ttu-id="be7f7-476">**\_Procesador CIM**</span><span class="sxs-lookup"><span data-stu-id="be7f7-476">**CIM\_Processor**</span></span>](/windows/desktop/CIMWin32Prov/cim-processor)
</dt> <dt>

[<span data-ttu-id="be7f7-477">Clases de procesador</span><span class="sxs-lookup"><span data-stu-id="be7f7-477">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

