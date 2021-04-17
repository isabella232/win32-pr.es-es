---
description: Representa el estado del servicio Servicio de instantáneas de volumen (VSS), que implementa el solicitante de VSS en el sistema operativo invitado.
ms.assetid: 4DD38929-1E3F-4105-BC1A-B367516F7B6E
title: Msvm_VssComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponent
- Msvm_VssComponent.SetPowerState
- Msvm_VssComponent.EnableDevice
- Msvm_VssComponent.OnlineDevice
- Msvm_VssComponent.QuiesceDevice
- Msvm_VssComponent.SaveProperties
- Msvm_VssComponent.RestoreProperties
- Msvm_VssComponent.InstanceID
- Msvm_VssComponent.Caption
- Msvm_VssComponent.Description
- Msvm_VssComponent.ElementName
- Msvm_VssComponent.InstallDate
- Msvm_VssComponent.Name
- Msvm_VssComponent.OperationalStatus
- Msvm_VssComponent.StatusDescriptions
- Msvm_VssComponent.Status
- Msvm_VssComponent.HealthState
- Msvm_VssComponent.CommunicationStatus
- Msvm_VssComponent.DetailedStatus
- Msvm_VssComponent.OperatingStatus
- Msvm_VssComponent.PrimaryStatus
- Msvm_VssComponent.EnabledState
- Msvm_VssComponent.OtherEnabledState
- Msvm_VssComponent.RequestedState
- Msvm_VssComponent.EnabledDefault
- Msvm_VssComponent.TimeOfLastStateChange
- Msvm_VssComponent.AvailableRequestedStates
- Msvm_VssComponent.TransitioningToState
- Msvm_VssComponent.SystemCreationClassName
- Msvm_VssComponent.SystemName
- Msvm_VssComponent.CreationClassName
- Msvm_VssComponent.DeviceID
- Msvm_VssComponent.PowerManagementSupported
- Msvm_VssComponent.PowerManagementCapabilities
- Msvm_VssComponent.Availability
- Msvm_VssComponent.StatusInfo
- Msvm_VssComponent.LastErrorCode
- Msvm_VssComponent.ErrorDescription
- Msvm_VssComponent.ErrorCleared
- Msvm_VssComponent.OtherIdentifyingInfo
- Msvm_VssComponent.PowerOnHours
- Msvm_VssComponent.TotalPowerOnHours
- Msvm_VssComponent.IdentifyingDescriptions
- Msvm_VssComponent.AdditionalAvailability
- Msvm_VssComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab4039ce110af9fa023a662c31d1f9962b080e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666311"
---
# <a name="msvm_vsscomponent-class"></a><span data-ttu-id="81bbe-103">MSVM \_ VssComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="81bbe-103">Msvm\_VssComponent class</span></span>

<span data-ttu-id="81bbe-104">Representa el estado del servicio Servicio de instantáneas de volumen (VSS), que implementa el solicitante de VSS en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="81bbe-104">Represents the state of the Volume Shadow Copy Service (VSS) service, which implements the VSS Requester in the guest operating system.</span></span>

<span data-ttu-id="81bbe-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="81bbe-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="81bbe-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81bbe-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "VSS";
  string   Description = "Microsoft VSS Service";
  string   ElementName = "VSS";
  datetime InstallDate;
  string   Name = "VSS";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
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
  string   CreationClassName = "Msvm_VssComponent";
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

## <a name="members"></a><span data-ttu-id="81bbe-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="81bbe-107">Members</span></span>

<span data-ttu-id="81bbe-108">La clase **MSVM \_ VssComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="81bbe-108">The **Msvm\_VssComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="81bbe-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="81bbe-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="81bbe-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81bbe-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="81bbe-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="81bbe-111">Methods</span></span>

<span data-ttu-id="81bbe-112">La clase **MSVM \_ VssComponent** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="81bbe-112">The **Msvm\_VssComponent** class has these methods.</span></span>



| <span data-ttu-id="81bbe-113">Método</span><span class="sxs-lookup"><span data-stu-id="81bbe-113">Method</span></span>                                                             | <span data-ttu-id="81bbe-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="81bbe-114">Description</span></span>                              |
|:-------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="81bbe-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="81bbe-115">**EnableDevice**</span></span>                                                   | <span data-ttu-id="81bbe-116">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="81bbe-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="81bbe-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="81bbe-117">**OnlineDevice**</span></span>                                                   | <span data-ttu-id="81bbe-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="81bbe-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="81bbe-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="81bbe-119">**QuiesceDevice**</span></span>                                                  | <span data-ttu-id="81bbe-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="81bbe-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="81bbe-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="81bbe-121">**RequestStateChange**</span></span>](msvm-vsscomponent-requeststatechange.md) | <span data-ttu-id="81bbe-122">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="81bbe-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="81bbe-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="81bbe-123">**Reset**</span></span>](msvm-vsscomponent-reset.md)                           | <span data-ttu-id="81bbe-124">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="81bbe-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="81bbe-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="81bbe-125">**RestoreProperties**</span></span>                                              | <span data-ttu-id="81bbe-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="81bbe-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="81bbe-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="81bbe-127">**SaveProperties**</span></span>                                                 | <span data-ttu-id="81bbe-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="81bbe-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="81bbe-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="81bbe-129">**SetPowerState**</span></span>                                                  | <span data-ttu-id="81bbe-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="81bbe-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="81bbe-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81bbe-131">Properties</span></span>

<span data-ttu-id="81bbe-132">La clase **MSVM \_ VssComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="81bbe-132">The **Msvm\_VssComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81bbe-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="81bbe-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-134">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbe-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-136">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81bbe-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="81bbe-137">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="81bbe-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-138">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="81bbe-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbe-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-141">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81bbe-141">The primary availability and status of the device.</span></span> <span data-ttu-id="81bbe-142">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="81bbe-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="81bbe-143">Value</span><span class="sxs-lookup"><span data-stu-id="81bbe-143">Value</span></span>                                                                        | <span data-ttu-id="81bbe-144">Significado</span><span class="sxs-lookup"><span data-stu-id="81bbe-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="81bbe-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="81bbe-146">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="81bbe-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="81bbe-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="81bbe-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-148">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbe-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-150">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="81bbe-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="81bbe-151">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="81bbe-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-152">**Caption**</span><span class="sxs-lookup"><span data-stu-id="81bbe-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81bbe-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-155">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="81bbe-155">A short description of the object.</span></span> <span data-ttu-id="81bbe-156">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="81bbe-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="81bbe-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-158">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbe-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-160">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="81bbe-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="81bbe-161">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="81bbe-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="81bbe-162">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81bbe-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="81bbe-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="81bbe-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="81bbe-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="81bbe-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="81bbe-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="81bbe-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="81bbe-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="81bbe-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="81bbe-170">)</span><span class="sxs-lookup"><span data-stu-id="81bbe-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81bbe-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="81bbe-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81bbe-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-174">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="81bbe-174">The scoping system's creation class name.</span></span> <span data-ttu-id="81bbe-175">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="81bbe-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-176">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="81bbe-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81bbe-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-179">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="81bbe-179">A description of the object.</span></span> <span data-ttu-id="81bbe-180">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="81bbe-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="81bbe-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-182">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbe-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-184">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="81bbe-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="81bbe-185">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="81bbe-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="81bbe-186">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81bbe-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="81bbe-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="81bbe-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="81bbe-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="81bbe-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="81bbe-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="81bbe-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="81bbe-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="81bbe-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="81bbe-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="81bbe-195">)</span><span class="sxs-lookup"><span data-stu-id="81bbe-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81bbe-196">**ID**</span><span class="sxs-lookup"><span data-stu-id="81bbe-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81bbe-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-199">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81bbe-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="81bbe-200">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "Microsoft:*VMGUID* \\ *GUID*", donde *VMGUID* es la propiedad **Name** del [**MSVM \_ ComputerSystem**](msvm-computersystem.md) asociado a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81bbe-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="81bbe-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81bbe-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-204">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="81bbe-204">A display name for the object.</span></span> <span data-ttu-id="81bbe-205">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="81bbe-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-206">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="81bbe-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-207">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbe-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-209">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre se establece en 7 (no valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="81bbe-209">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 7 (No Default).</span></span>



| <span data-ttu-id="81bbe-210">Value</span><span class="sxs-lookup"><span data-stu-id="81bbe-210">Value</span></span>                                                                        | <span data-ttu-id="81bbe-211">Significado</span><span class="sxs-lookup"><span data-stu-id="81bbe-211">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="81bbe-212"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-212"><dt>2</dt></span></span> </dl> | <span data-ttu-id="81bbe-213">habilitado</span><span class="sxs-lookup"><span data-stu-id="81bbe-213">Enabled</span></span><br/>    |
| <dl> <span data-ttu-id="81bbe-214"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-214"><dt>3</dt></span></span> </dl> | <span data-ttu-id="81bbe-215">Disabled</span><span class="sxs-lookup"><span data-stu-id="81bbe-215">Disabled</span></span><br/>   |
| <dl> <span data-ttu-id="81bbe-216"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-216"><dt>7</dt></span></span> </dl> | <span data-ttu-id="81bbe-217">Sin valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="81bbe-217">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="81bbe-218">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="81bbe-218">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-219">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbe-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-221">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="81bbe-221">The enabled and disabled states of an element.</span></span> <span data-ttu-id="81bbe-222">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81bbe-222">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="81bbe-223">Value</span><span class="sxs-lookup"><span data-stu-id="81bbe-223">Value</span></span>                                                                        | <span data-ttu-id="81bbe-224">Significado</span><span class="sxs-lookup"><span data-stu-id="81bbe-224">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="81bbe-225"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-225"><dt>2</dt></span></span> </dl> | <span data-ttu-id="81bbe-226">habilitado</span><span class="sxs-lookup"><span data-stu-id="81bbe-226">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="81bbe-227"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-227"><dt>3</dt></span></span> </dl> | <span data-ttu-id="81bbe-228">Disabled</span><span class="sxs-lookup"><span data-stu-id="81bbe-228">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="81bbe-229">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="81bbe-229">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-230">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="81bbe-230">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-232">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="81bbe-232">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="81bbe-233">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81bbe-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="81bbe-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-235">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81bbe-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-237">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="81bbe-237">A string that provides more information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span> <span data-ttu-id="81bbe-238">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81bbe-238">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-239">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="81bbe-239">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-240">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbe-240">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-242">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="81bbe-242">The current health of the element.</span></span> <span data-ttu-id="81bbe-243">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="81bbe-243">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="81bbe-244">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="81bbe-244">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="81bbe-245">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81bbe-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="81bbe-246">Value</span><span class="sxs-lookup"><span data-stu-id="81bbe-246">Value</span></span>                                                                        | <span data-ttu-id="81bbe-247">Significado</span><span class="sxs-lookup"><span data-stu-id="81bbe-247">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="81bbe-248"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-248"><dt>5</dt></span></span> </dl> | <span data-ttu-id="81bbe-249">Aceptar</span><span class="sxs-lookup"><span data-stu-id="81bbe-249">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="81bbe-250">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="81bbe-250">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-251">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="81bbe-251">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-253">Matriz de cadenas de formato libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="81bbe-253">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="81bbe-254">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81bbe-254">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-255">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="81bbe-255">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-256">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="81bbe-256">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-258">Fecha y hora en que se instaló el servicio de integración en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="81bbe-258">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="81bbe-259">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81bbe-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-260">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="81bbe-260">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81bbe-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-263">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="81bbe-263">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-264">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="81bbe-264">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="81bbe-265">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="81bbe-265">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-266">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="81bbe-266">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-267">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81bbe-267">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-269">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81bbe-269">The last error code reported by the logical device.</span></span> <span data-ttu-id="81bbe-270">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81bbe-270">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-271">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="81bbe-271">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-272">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81bbe-272">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-273">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-274">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="81bbe-274">This property has been deprecated.</span></span> <span data-ttu-id="81bbe-275">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="81bbe-275">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-276">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="81bbe-276">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-277">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81bbe-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-279">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="81bbe-279">The label by which the object is known.</span></span> <span data-ttu-id="81bbe-280">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81bbe-280">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-281">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="81bbe-281">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-282">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbe-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-284">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="81bbe-284">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="81bbe-285">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="81bbe-285">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="81bbe-286">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81bbe-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="81bbe-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="81bbe-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-288"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="81bbe-288"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-289"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="81bbe-289"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-290"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="81bbe-290"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-291"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="81bbe-291"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-292"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="81bbe-292"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-293"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="81bbe-293"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-294"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="81bbe-294"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-295"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="81bbe-295"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-296"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="81bbe-296"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-297"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="81bbe-297"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-298"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="81bbe-298"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-299"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="81bbe-299"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-300"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="81bbe-300"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-301"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="81bbe-301"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-302"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="81bbe-302"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-303"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="81bbe-303"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-304"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="81bbe-304"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-305"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="81bbe-305"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="81bbe-306">)</span><span class="sxs-lookup"><span data-stu-id="81bbe-306">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81bbe-307">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="81bbe-307">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-308">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbe-308">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-310">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="81bbe-310">The current status of the element.</span></span> <span data-ttu-id="81bbe-311">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81bbe-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="81bbe-312">A continuación se muestran los posibles valores para el valor de la propiedad **OperationalStatus** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="81bbe-312">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="81bbe-313">Value</span><span class="sxs-lookup"><span data-stu-id="81bbe-313">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="81bbe-314">Significado</span><span class="sxs-lookup"><span data-stu-id="81bbe-314">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81bbe-315"><dt>dos</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-315"><dt>{ 2 }</dt></span></span> </dl>                                                                                                                                                                                                    |                                                                                                                                                                                                                                          |
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="81bbe-316"><dt>**Aceptar**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-316"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="81bbe-317">El servicio está funcionando con normalidad.</span><span class="sxs-lookup"><span data-stu-id="81bbe-317">The service is operating normally.</span></span> <span data-ttu-id="81bbe-318">Los valores de la propiedad **OperationalStatus** \[ 1 \] y **StatusDescriptions** \[ 1 \] pueden contener más información.</span><span class="sxs-lookup"><span data-stu-id="81bbe-318">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="81bbe-319"><dt>**Degradado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-319"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="81bbe-320">El servicio está funcionando con normalidad, pero el servicio invitado negoció una versión del Protocolo de comunicaciones compatible.</span><span class="sxs-lookup"><span data-stu-id="81bbe-320">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="81bbe-321">Los valores de la propiedad **OperationalStatus** \[ 1 \] y **StatusDescriptions** \[ 1 \] pueden contener más información.</span><span class="sxs-lookup"><span data-stu-id="81bbe-321">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="81bbe-322"><dt>**Error no recuperable**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-322"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="81bbe-323">El invitado no es compatible con una versión de protocolo compatible.</span><span class="sxs-lookup"><span data-stu-id="81bbe-323">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="81bbe-324">Los valores de la propiedad **OperationalStatus** \[ 1 \] y **StatusDescriptions** \[ 1 \] pueden contener más información.</span><span class="sxs-lookup"><span data-stu-id="81bbe-324">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="81bbe-325"><dt>**No Contact**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-325"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="81bbe-326">El servicio invitado no está instalado o no se ha conectado todavía.</span><span class="sxs-lookup"><span data-stu-id="81bbe-326">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="81bbe-327"><dt>**Comunicación perdida**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-327"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="81bbe-328">El servicio invitado ya no responde normalmente.</span><span class="sxs-lookup"><span data-stu-id="81bbe-328">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="81bbe-329">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="81bbe-329">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-330">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81bbe-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-332">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="81bbe-332">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="81bbe-333">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="81bbe-333">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="81bbe-334">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81bbe-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-335">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="81bbe-335">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-336">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="81bbe-336">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-338">Datos adicionales, más allá de la información del ID. de dispositivo, que se pueden usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81bbe-338">Additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="81bbe-339">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="81bbe-339">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-340">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="81bbe-340">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-341">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbe-341">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-343">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81bbe-343">The power management capabilities of the device.</span></span> <span data-ttu-id="81bbe-344">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81bbe-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-345">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="81bbe-345">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-346">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="81bbe-346">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-348">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="81bbe-348">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="81bbe-349">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81bbe-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-350">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="81bbe-350">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-351">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81bbe-351">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-352">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-353">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="81bbe-353">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="81bbe-354">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81bbe-354">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-355">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="81bbe-355">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-356">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbe-356">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-358">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="81bbe-358">Provides high level status information.</span></span> <span data-ttu-id="81bbe-359">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="81bbe-359">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="81bbe-360">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="81bbe-360">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="81bbe-361">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81bbe-361">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="81bbe-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="81bbe-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-363"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="81bbe-363"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-364"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="81bbe-364"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-365"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="81bbe-365"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="81bbe-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="81bbe-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="81bbe-368">)</span><span class="sxs-lookup"><span data-stu-id="81bbe-368">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81bbe-369">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="81bbe-369">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-370">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbe-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-372">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="81bbe-372">The last requested or desired state for the element.</span></span> <span data-ttu-id="81bbe-373">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81bbe-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="81bbe-374">Value</span><span class="sxs-lookup"><span data-stu-id="81bbe-374">Value</span></span>                                                                         | <span data-ttu-id="81bbe-375">Significado</span><span class="sxs-lookup"><span data-stu-id="81bbe-375">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="81bbe-376"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-376"><dt>12</dt></span></span> </dl> | <span data-ttu-id="81bbe-377">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="81bbe-377">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="81bbe-378">**Estado**</span><span class="sxs-lookup"><span data-stu-id="81bbe-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-379">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81bbe-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-381">Cadena que especifica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="81bbe-381">A string that specifies the current status of the object.</span></span> <span data-ttu-id="81bbe-382">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81bbe-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-383">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="81bbe-383">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-384">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="81bbe-384">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-385">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-386">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="81bbe-386">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="81bbe-387">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81bbe-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-388">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="81bbe-388">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-389">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbe-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-391">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81bbe-391">The current state of the logical device.</span></span> <span data-ttu-id="81bbe-392">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81bbe-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-393">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="81bbe-393">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-394">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81bbe-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-395">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-396">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="81bbe-396">The scoping system's creation class name.</span></span> <span data-ttu-id="81bbe-397">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="81bbe-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-398">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="81bbe-398">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-399">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81bbe-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-401">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="81bbe-401">The scoping system's name.</span></span> <span data-ttu-id="81bbe-402">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="81bbe-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-403">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="81bbe-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-404">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="81bbe-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-405">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-406">Fecha u hora de la última modificación del **EnabledState** del elemento.</span><span class="sxs-lookup"><span data-stu-id="81bbe-406">The date or time when the **EnabledState** of the element last changed.</span></span> <span data-ttu-id="81bbe-407">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="81bbe-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-408">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="81bbe-408">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-409">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81bbe-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-411">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81bbe-411">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="81bbe-412">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81bbe-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81bbe-413">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="81bbe-413">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbe-414">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbe-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bbe-415">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81bbe-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbe-416">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="81bbe-416">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="81bbe-417">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81bbe-417">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="81bbe-418">Value</span><span class="sxs-lookup"><span data-stu-id="81bbe-418">Value</span></span>                                                                         | <span data-ttu-id="81bbe-419">Significado</span><span class="sxs-lookup"><span data-stu-id="81bbe-419">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="81bbe-420"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-420"><dt>12</dt></span></span> </dl> | <span data-ttu-id="81bbe-421">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="81bbe-421">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81bbe-422">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81bbe-422">Remarks</span></span>

<span data-ttu-id="81bbe-423">El acceso a la clase **MSVM \_ VssComponent** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="81bbe-423">Access to the **Msvm\_VssComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="81bbe-424">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="81bbe-424">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="81bbe-425">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81bbe-425">Requirements</span></span>



| <span data-ttu-id="81bbe-426">Requisito</span><span class="sxs-lookup"><span data-stu-id="81bbe-426">Requirement</span></span> | <span data-ttu-id="81bbe-427">Value</span><span class="sxs-lookup"><span data-stu-id="81bbe-427">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81bbe-428">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81bbe-428">Minimum supported client</span></span><br/> | <span data-ttu-id="81bbe-429">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="81bbe-429">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="81bbe-430">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81bbe-430">Minimum supported server</span></span><br/> | <span data-ttu-id="81bbe-431">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="81bbe-431">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="81bbe-432">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="81bbe-432">Namespace</span></span><br/>                | <span data-ttu-id="81bbe-433">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="81bbe-433">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="81bbe-434">MOF</span><span class="sxs-lookup"><span data-stu-id="81bbe-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81bbe-435"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-435"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81bbe-436">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="81bbe-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81bbe-437"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81bbe-437"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81bbe-438">Vea también</span><span class="sxs-lookup"><span data-stu-id="81bbe-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81bbe-439">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="81bbe-439">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="81bbe-440">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="81bbe-440">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

