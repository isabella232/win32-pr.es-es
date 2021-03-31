---
description: Representa el estado del servicio de intercambio de pares clave-valor, que proporciona un mecanismo para intercambiar datos entre la máquina virtual y el sistema operativo que se ejecuta en el sistema operativo de administración.
ms.assetid: AA68BC74-A919-4029-B703-E08F00449F20
title: Msvm_KvpExchangeComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponent
- Msvm_KvpExchangeComponent.SetPowerState
- Msvm_KvpExchangeComponent.EnableDevice
- Msvm_KvpExchangeComponent.OnlineDevice
- Msvm_KvpExchangeComponent.QuiesceDevice
- Msvm_KvpExchangeComponent.SaveProperties
- Msvm_KvpExchangeComponent.RestoreProperties
- Msvm_KvpExchangeComponent.InstanceID
- Msvm_KvpExchangeComponent.Caption
- Msvm_KvpExchangeComponent.Description
- Msvm_KvpExchangeComponent.ElementName
- Msvm_KvpExchangeComponent.InstallDate
- Msvm_KvpExchangeComponent.Name
- Msvm_KvpExchangeComponent.OperationalStatus
- Msvm_KvpExchangeComponent.StatusDescriptions
- Msvm_KvpExchangeComponent.Status
- Msvm_KvpExchangeComponent.HealthState
- Msvm_KvpExchangeComponent.CommunicationStatus
- Msvm_KvpExchangeComponent.DetailedStatus
- Msvm_KvpExchangeComponent.OperatingStatus
- Msvm_KvpExchangeComponent.PrimaryStatus
- Msvm_KvpExchangeComponent.EnabledState
- Msvm_KvpExchangeComponent.OtherEnabledState
- Msvm_KvpExchangeComponent.RequestedState
- Msvm_KvpExchangeComponent.EnabledDefault
- Msvm_KvpExchangeComponent.TimeOfLastStateChange
- Msvm_KvpExchangeComponent.AvailableRequestedStates
- Msvm_KvpExchangeComponent.TransitioningToState
- Msvm_KvpExchangeComponent.SystemCreationClassName
- Msvm_KvpExchangeComponent.SystemName
- Msvm_KvpExchangeComponent.CreationClassName
- Msvm_KvpExchangeComponent.DeviceID
- Msvm_KvpExchangeComponent.PowerManagementSupported
- Msvm_KvpExchangeComponent.PowerManagementCapabilities
- Msvm_KvpExchangeComponent.Availability
- Msvm_KvpExchangeComponent.StatusInfo
- Msvm_KvpExchangeComponent.LastErrorCode
- Msvm_KvpExchangeComponent.ErrorDescription
- Msvm_KvpExchangeComponent.ErrorCleared
- Msvm_KvpExchangeComponent.OtherIdentifyingInfo
- Msvm_KvpExchangeComponent.PowerOnHours
- Msvm_KvpExchangeComponent.TotalPowerOnHours
- Msvm_KvpExchangeComponent.IdentifyingDescriptions
- Msvm_KvpExchangeComponent.AdditionalAvailability
- Msvm_KvpExchangeComponent.MaxQuiesceTime
- Msvm_KvpExchangeComponent.GuestExchangeItems
- Msvm_KvpExchangeComponent.GuestIntrinsicExchangeItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3aa7f269d24c284eef3ad2c519f5fdbf48513a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913130"
---
# <a name="msvm_kvpexchangecomponent-class"></a><span data-ttu-id="e307b-103">MSVM \_ KvpExchangeComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="e307b-103">Msvm\_KvpExchangeComponent class</span></span>

<span data-ttu-id="e307b-104">Representa el estado del servicio de intercambio de pares clave-valor, que proporciona un mecanismo para intercambiar datos entre la máquina virtual y el sistema operativo que se ejecuta en el sistema operativo de administración.</span><span class="sxs-lookup"><span data-stu-id="e307b-104">Represents the state of the key/value pair exchange service, which provides a mechanism to exchange data between the virtual machine and the operating system running on the management operating system.</span></span>

<span data-ttu-id="e307b-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e307b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e307b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e307b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Key-Value Pair Exchange";
  string   Description = "Microsoft Key-Value Pair Exchange Service";
  string   ElementName = "Key-Value pair Exchange";
  datetime InstallDate;
  string   Name = "Key-Value Pair Exchange";
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_KvpExchangeComponent";
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  string   GuestExchangeItems[];
  string   GuestIntrinsicExchangeItems[];
};
```

## <a name="members"></a><span data-ttu-id="e307b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e307b-107">Members</span></span>

<span data-ttu-id="e307b-108">La clase **MSVM \_ KvpExchangeComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e307b-108">The **Msvm\_KvpExchangeComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="e307b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e307b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="e307b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e307b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e307b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e307b-111">Methods</span></span>

<span data-ttu-id="e307b-112">La clase **MSVM \_ KvpExchangeComponent** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e307b-112">The **Msvm\_KvpExchangeComponent** class has these methods.</span></span>



| <span data-ttu-id="e307b-113">Método</span><span class="sxs-lookup"><span data-stu-id="e307b-113">Method</span></span>                                                                     | <span data-ttu-id="e307b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e307b-114">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="e307b-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="e307b-115">**EnableDevice**</span></span>                                                           | <span data-ttu-id="e307b-116">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e307b-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e307b-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="e307b-117">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="e307b-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e307b-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e307b-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="e307b-119">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="e307b-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e307b-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="e307b-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e307b-121">**RequestStateChange**</span></span>](msvm-kvpexchangecomponent-requeststatechange.md) | <span data-ttu-id="e307b-122">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="e307b-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="e307b-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="e307b-123">**Reset**</span></span>](msvm-kvpexchangecomponent-reset.md)                           | <span data-ttu-id="e307b-124">Restablece el componente.</span><span class="sxs-lookup"><span data-stu-id="e307b-124">Resets the component.</span></span><br/>         |
| <span data-ttu-id="e307b-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="e307b-125">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="e307b-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e307b-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e307b-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="e307b-127">**SaveProperties**</span></span>                                                         | <span data-ttu-id="e307b-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e307b-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e307b-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e307b-129">**SetPowerState**</span></span>                                                          | <span data-ttu-id="e307b-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e307b-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e307b-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e307b-131">Properties</span></span>

<span data-ttu-id="e307b-132">La clase **MSVM \_ KvpExchangeComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e307b-132">The **Msvm\_KvpExchangeComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e307b-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="e307b-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-134">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e307b-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e307b-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-136">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e307b-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="e307b-137">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e307b-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="e307b-138">Value</span><span class="sxs-lookup"><span data-stu-id="e307b-138">Value</span></span>                                                                            | <span data-ttu-id="e307b-139">Significado</span><span class="sxs-lookup"><span data-stu-id="e307b-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="e307b-140"><dt>1,8</dt></span><span class="sxs-lookup"><span data-stu-id="e307b-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="e307b-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e307b-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="e307b-142">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="e307b-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e307b-143">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="e307b-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-144">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e307b-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-146">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e307b-146">The primary availability and status of the device.</span></span> <span data-ttu-id="e307b-147">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e307b-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="e307b-148">Value</span><span class="sxs-lookup"><span data-stu-id="e307b-148">Value</span></span>                                                                        | <span data-ttu-id="e307b-149">Significado</span><span class="sxs-lookup"><span data-stu-id="e307b-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="e307b-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e307b-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="e307b-151">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="e307b-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e307b-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="e307b-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-153">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e307b-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e307b-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-155">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e307b-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="e307b-156">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e307b-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e307b-157">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e307b-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e307b-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-160">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e307b-160">A short description of the object.</span></span> <span data-ttu-id="e307b-161">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e307b-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e307b-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="e307b-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-163">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e307b-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-165">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="e307b-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e307b-166">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e307b-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e307b-167">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e307b-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e307b-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e307b-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="e307b-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="e307b-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="e307b-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="e307b-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e307b-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="e307b-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e307b-175">)</span><span class="sxs-lookup"><span data-stu-id="e307b-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e307b-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e307b-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e307b-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-179">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e307b-179">The scoping system's creation class name.</span></span> <span data-ttu-id="e307b-180">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e307b-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e307b-181">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e307b-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e307b-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-184">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e307b-184">A description of the object.</span></span> <span data-ttu-id="e307b-185">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e307b-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e307b-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e307b-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-187">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e307b-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-189">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="e307b-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e307b-190">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e307b-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e307b-191">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e307b-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e307b-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="e307b-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="e307b-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="e307b-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="e307b-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="e307b-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="e307b-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e307b-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="e307b-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e307b-200">)</span><span class="sxs-lookup"><span data-stu-id="e307b-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e307b-201">**ID**</span><span class="sxs-lookup"><span data-stu-id="e307b-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e307b-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-204">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e307b-204">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="e307b-205">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e307b-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e307b-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e307b-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e307b-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-209">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="e307b-209">A display name for the object.</span></span> <span data-ttu-id="e307b-210">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e307b-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e307b-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="e307b-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-212">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e307b-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-214">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e307b-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="e307b-215">Value</span><span class="sxs-lookup"><span data-stu-id="e307b-215">Value</span></span>                                                                        | <span data-ttu-id="e307b-216">Significado</span><span class="sxs-lookup"><span data-stu-id="e307b-216">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="e307b-217"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e307b-217"><dt>7</dt></span></span> </dl> | <span data-ttu-id="e307b-218">Sin valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="e307b-218">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e307b-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e307b-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-220">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e307b-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-222">Estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="e307b-222">The enabled state of the element.</span></span> <span data-ttu-id="e307b-223">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e307b-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="e307b-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="e307b-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e307b-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e307b-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e307b-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-227">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e307b-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-229">Indica si el error comunicado en la propiedad **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="e307b-229">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="e307b-230">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e307b-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e307b-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e307b-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-232">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e307b-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-234">Una cadena que proporciona más información sobre el error registrado en la propiedad **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="e307b-234">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="e307b-235">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e307b-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e307b-236">**GuestExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="e307b-236">**GuestExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-237">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e307b-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e307b-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e307b-239">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), **HyperVEmbeddedInstance** ("MSVM \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="e307b-239">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="e307b-240">Matriz de instancias de [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) incrustadas que contienen el conjunto de pares clave-valor que los servicios que se ejecutan en el sistema operativo invitado se han insertado para que los clientes externos puedan acceder a ellos.</span><span class="sxs-lookup"><span data-stu-id="e307b-240">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that services running within the guest operating system have pushed up to be available for access by external clients.</span></span> <span data-ttu-id="e307b-241">Esta matriz no contendrá ningún elemento intrínseco que el servicio de integración Inserte directamente.</span><span class="sxs-lookup"><span data-stu-id="e307b-241">This array will not contain any intrinsic items that are pushed by the integration service directly.</span></span>

</dd> <dt>

<span data-ttu-id="e307b-242">**GuestIntrinsicExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="e307b-242">**GuestIntrinsicExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-243">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e307b-243">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e307b-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e307b-245">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), **HyperVEmbeddedInstance** ("MSVM \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="e307b-245">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="e307b-246">Matriz de instancias de [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) incrustadas que contienen el conjunto de pares clave-valor que el sistema operativo invitado ha insertado para que los clientes externos puedan acceder a él.</span><span class="sxs-lookup"><span data-stu-id="e307b-246">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that the guest operating system has pushed up to be available for access by external clients.</span></span> <span data-ttu-id="e307b-247">Esta matriz no contendrá ningún elemento de datos insertado por otros servicios que se ejecuten en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="e307b-247">This array will not contain any data items pushed by other services running within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="e307b-248">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e307b-248">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-249">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e307b-249">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-251">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="e307b-251">The current health of the element.</span></span> <span data-ttu-id="e307b-252">Esto expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="e307b-252">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="e307b-253">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="e307b-253">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="e307b-254">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e307b-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e307b-255">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e307b-255">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-256">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e307b-256">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e307b-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-258">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="e307b-258">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="e307b-259">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e307b-259">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e307b-260">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e307b-260">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-261">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e307b-261">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-263">Fecha y hora en que se instaló el servicio de integración en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e307b-263">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="e307b-264">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e307b-264">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e307b-265">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e307b-265">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-266">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e307b-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e307b-268">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="e307b-268">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e307b-269">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="e307b-269">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e307b-270">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e307b-270">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e307b-271">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e307b-271">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-272">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e307b-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-273">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-274">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e307b-274">The last error code reported by the logical device.</span></span> <span data-ttu-id="e307b-275">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e307b-275">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e307b-276">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="e307b-276">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-277">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e307b-277">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-279">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="e307b-279">This property has been deprecated.</span></span> <span data-ttu-id="e307b-280">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e307b-280">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e307b-281">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="e307b-281">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-282">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e307b-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-284">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="e307b-284">The label by which the object is known.</span></span> <span data-ttu-id="e307b-285">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e307b-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e307b-286">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="e307b-286">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-287">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e307b-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-289">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="e307b-289">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e307b-290">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e307b-290">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e307b-291">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e307b-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e307b-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e307b-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="e307b-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="e307b-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="e307b-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="e307b-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="e307b-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="e307b-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="e307b-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="e307b-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="e307b-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="e307b-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="e307b-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="e307b-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="e307b-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="e307b-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="e307b-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="e307b-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e307b-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="e307b-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e307b-311">)</span><span class="sxs-lookup"><span data-stu-id="e307b-311">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e307b-312">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e307b-312">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-313">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e307b-313">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e307b-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-315">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="e307b-315">The current status of the element.</span></span> <span data-ttu-id="e307b-316">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e307b-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="e307b-317">A continuación se muestran los posibles valores para el valor de la propiedad **OperationalStatus** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="e307b-317">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="e307b-318">Value</span><span class="sxs-lookup"><span data-stu-id="e307b-318">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="e307b-319">Significado</span><span class="sxs-lookup"><span data-stu-id="e307b-319">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="e307b-320"><dt>**Aceptar**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e307b-320"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="e307b-321">El servicio está funcionando con normalidad.</span><span class="sxs-lookup"><span data-stu-id="e307b-321">The service is operating normally.</span></span> <span data-ttu-id="e307b-322">Los valores de la propiedad **OperationalStatus** \[ 1 \] y **StatusDescriptions** \[ 1 \] pueden contener más información.</span><span class="sxs-lookup"><span data-stu-id="e307b-322">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="e307b-323"><dt>**Degradado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e307b-323"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="e307b-324">El servicio está funcionando con normalidad, pero el servicio invitado negoció una versión del Protocolo de comunicaciones compatible.</span><span class="sxs-lookup"><span data-stu-id="e307b-324">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="e307b-325">Los valores de la propiedad **OperationalStatus** \[ 1 \] y **StatusDescriptions** \[ 1 \] pueden contener más información.</span><span class="sxs-lookup"><span data-stu-id="e307b-325">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="e307b-326"><dt>**Error no recuperable**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e307b-326"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="e307b-327">El invitado no es compatible con una versión de protocolo compatible.</span><span class="sxs-lookup"><span data-stu-id="e307b-327">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="e307b-328">Los valores de la propiedad **OperationalStatus** \[ 1 \] y **StatusDescriptions** \[ 1 \] pueden contener más información.</span><span class="sxs-lookup"><span data-stu-id="e307b-328">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="e307b-329"><dt>**No Contact**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="e307b-329"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="e307b-330">El servicio invitado no está instalado o no se ha conectado todavía.</span><span class="sxs-lookup"><span data-stu-id="e307b-330">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="e307b-331"><dt>**Comunicación perdida**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="e307b-331"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="e307b-332">El servicio invitado ya no responde normalmente.</span><span class="sxs-lookup"><span data-stu-id="e307b-332">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="e307b-333">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="e307b-333">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-334">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e307b-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-336">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="e307b-336">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="e307b-337">Esta propiedad debe establecerse en **null** cuando la propiedad **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="e307b-337">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="e307b-338">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e307b-338">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e307b-339">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e307b-339">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-340">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e307b-340">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e307b-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-342">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e307b-342">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="e307b-343">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="e307b-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e307b-344">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e307b-344">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-345">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e307b-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e307b-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-347">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e307b-347">The power management capabilities of the device.</span></span> <span data-ttu-id="e307b-348">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e307b-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e307b-349">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e307b-349">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-350">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e307b-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-352">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="e307b-352">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="e307b-353">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e307b-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e307b-354">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e307b-354">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-355">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e307b-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-357">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="e307b-357">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="e307b-358">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e307b-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e307b-359">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="e307b-359">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-360">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e307b-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-362">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="e307b-362">Provides high level status information.</span></span> <span data-ttu-id="e307b-363">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="e307b-363">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="e307b-364">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e307b-364">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e307b-365">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e307b-365">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e307b-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e307b-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-367"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="e307b-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="e307b-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="e307b-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e307b-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e307b-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="e307b-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e307b-372">)</span><span class="sxs-lookup"><span data-stu-id="e307b-372">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e307b-373">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e307b-373">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-374">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e307b-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-376">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="e307b-376">The last requested or desired state for the element.</span></span> <span data-ttu-id="e307b-377">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e307b-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="e307b-378">Value</span><span class="sxs-lookup"><span data-stu-id="e307b-378">Value</span></span>                                                                         | <span data-ttu-id="e307b-379">Significado</span><span class="sxs-lookup"><span data-stu-id="e307b-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="e307b-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="e307b-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="e307b-381">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="e307b-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e307b-382">**Estado**</span><span class="sxs-lookup"><span data-stu-id="e307b-382">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-383">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e307b-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-384">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-385">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="e307b-385">The current status of the object.</span></span> <span data-ttu-id="e307b-386">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e307b-386">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e307b-387">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e307b-387">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-388">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e307b-388">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e307b-389">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-390">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e307b-390">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e307b-391">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e307b-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e307b-392">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e307b-392">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-393">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e307b-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-395">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e307b-395">The current state of the logical device.</span></span> <span data-ttu-id="e307b-396">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e307b-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e307b-397">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e307b-397">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-398">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e307b-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-400">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e307b-400">The scoping system's creation class name.</span></span> <span data-ttu-id="e307b-401">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e307b-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e307b-402">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e307b-402">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-403">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e307b-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-405">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e307b-405">The scoping system's name.</span></span> <span data-ttu-id="e307b-406">Este valor corresponde al valor de la propiedad [**Name**](msvm-computersystem.md) de la clase **MSVM \_ ComputerSystem** para el ámbito de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e307b-406">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="e307b-407">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e307b-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e307b-408">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="e307b-408">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-409">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e307b-409">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-411">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="e307b-411">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e307b-412">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e307b-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e307b-413">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e307b-413">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-414">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e307b-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-415">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-416">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e307b-416">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="e307b-417">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e307b-417">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e307b-418">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="e307b-418">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e307b-419">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e307b-419">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e307b-420">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e307b-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e307b-421">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="e307b-421">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e307b-422">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e307b-422">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e307b-423">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e307b-423">Remarks</span></span>

<span data-ttu-id="e307b-424">El acceso a la clase **MSVM \_ KvpExchangeComponent** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="e307b-424">Access to the **Msvm\_KvpExchangeComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e307b-425">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e307b-425">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e307b-426">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e307b-426">Requirements</span></span>



| <span data-ttu-id="e307b-427">Requisito</span><span class="sxs-lookup"><span data-stu-id="e307b-427">Requirement</span></span> | <span data-ttu-id="e307b-428">Value</span><span class="sxs-lookup"><span data-stu-id="e307b-428">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e307b-429">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e307b-429">Minimum supported client</span></span><br/> | <span data-ttu-id="e307b-430">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e307b-430">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e307b-431">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e307b-431">Minimum supported server</span></span><br/> | <span data-ttu-id="e307b-432">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e307b-432">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e307b-433">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e307b-433">Namespace</span></span><br/>                | <span data-ttu-id="e307b-434">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e307b-434">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e307b-435">MOF</span><span class="sxs-lookup"><span data-stu-id="e307b-435">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e307b-436"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e307b-436"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e307b-437">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e307b-437">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e307b-438"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e307b-438"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e307b-439">Vea también</span><span class="sxs-lookup"><span data-stu-id="e307b-439">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e307b-440">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e307b-440">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="e307b-441">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e307b-441">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

