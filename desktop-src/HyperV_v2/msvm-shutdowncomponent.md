---
description: Representa el estado del servicio de cierre, que proporciona un mecanismo para apagar el sistema operativo de la máquina virtual desde las interfaces de administración en el sistema host.
ms.assetid: E9BBB08C-A3FE-4226-A2CF-458706E759D6
title: Msvm_ShutdownComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent
- Msvm_ShutdownComponent.EnableDevice
- Msvm_ShutdownComponent.OnlineDevice
- Msvm_ShutdownComponent.QuiesceDevice
- Msvm_ShutdownComponent.RestoreProperties
- Msvm_ShutdownComponent.SaveProperties
- Msvm_ShutdownComponent.SetPowerState
- Msvm_ShutdownComponent.InstanceID
- Msvm_ShutdownComponent.Caption
- Msvm_ShutdownComponent.Description
- Msvm_ShutdownComponent.ElementName
- Msvm_ShutdownComponent.InstallDate
- Msvm_ShutdownComponent.Name
- Msvm_ShutdownComponent.OperationalStatus
- Msvm_ShutdownComponent.StatusDescriptions
- Msvm_ShutdownComponent.Status
- Msvm_ShutdownComponent.HealthState
- Msvm_ShutdownComponent.CommunicationStatus
- Msvm_ShutdownComponent.DetailedStatus
- Msvm_ShutdownComponent.OperatingStatus
- Msvm_ShutdownComponent.PrimaryStatus
- Msvm_ShutdownComponent.EnabledState
- Msvm_ShutdownComponent.OtherEnabledState
- Msvm_ShutdownComponent.RequestedState
- Msvm_ShutdownComponent.EnabledDefault
- Msvm_ShutdownComponent.TimeOfLastStateChange
- Msvm_ShutdownComponent.AvailableRequestedStates
- Msvm_ShutdownComponent.TransitioningToState
- Msvm_ShutdownComponent.SystemCreationClassName
- Msvm_ShutdownComponent.SystemName
- Msvm_ShutdownComponent.CreationClassName
- Msvm_ShutdownComponent.DeviceID
- Msvm_ShutdownComponent.PowerManagementSupported
- Msvm_ShutdownComponent.PowerManagementCapabilities
- Msvm_ShutdownComponent.Availability
- Msvm_ShutdownComponent.StatusInfo
- Msvm_ShutdownComponent.LastErrorCode
- Msvm_ShutdownComponent.ErrorDescription
- Msvm_ShutdownComponent.ErrorCleared
- Msvm_ShutdownComponent.OtherIdentifyingInfo
- Msvm_ShutdownComponent.PowerOnHours
- Msvm_ShutdownComponent.TotalPowerOnHours
- Msvm_ShutdownComponent.IdentifyingDescriptions
- Msvm_ShutdownComponent.AdditionalAvailability
- Msvm_ShutdownComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 49729568a1625b3df723b1b5b88cc1044b41e715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082340"
---
# <a name="msvm_shutdowncomponent-class"></a><span data-ttu-id="2359d-103">MSVM \_ ShutdownComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="2359d-103">Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="2359d-104">Representa el estado del servicio de cierre, que proporciona un mecanismo para apagar el sistema operativo de la máquina virtual desde las interfaces de administración en el sistema host.</span><span class="sxs-lookup"><span data-stu-id="2359d-104">Represents the state of the shutdown service, which provides a mechanism to shut down the operating system of the virtual machine from the management interfaces on the host system.</span></span>

<span data-ttu-id="2359d-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2359d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2359d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2359d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ShutdownComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Shutdown";
  string   Description = "Microsoft Shutdown Service";
  string   ElementName = "Shutdown";
  datetime InstallDate;
  string   Name = "Shutdown";
  uint16   OperationalStatus[];
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
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ShutdownComponent";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="2359d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2359d-107">Members</span></span>

<span data-ttu-id="2359d-108">La clase **MSVM \_ ShutdownComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2359d-108">The **Msvm\_ShutdownComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="2359d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2359d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2359d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2359d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2359d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2359d-111">Methods</span></span>

<span data-ttu-id="2359d-112">La clase **MSVM \_ ShutdownComponent** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2359d-112">The **Msvm\_ShutdownComponent** class has these methods.</span></span>



| <span data-ttu-id="2359d-113">Método</span><span class="sxs-lookup"><span data-stu-id="2359d-113">Method</span></span>                                                                  | <span data-ttu-id="2359d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2359d-114">Description</span></span>                                                                                        |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2359d-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="2359d-115">**EnableDevice**</span></span>                                                        | <span data-ttu-id="2359d-116">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="2359d-116">This method is not supported.</span></span><br/>                                                           |
| [<span data-ttu-id="2359d-117">**InitiateReboot**</span><span class="sxs-lookup"><span data-stu-id="2359d-117">**InitiateReboot**</span></span>](msvm-shutdowncomponent-initiatereboot.md)         | <span data-ttu-id="2359d-118">Inicia una operación de reinicio del sistema operativo en la máquina virtual secundaria asociada.</span><span class="sxs-lookup"><span data-stu-id="2359d-118">Initiates an operating system reboot operation on the associated child virtual machine.</span></span><br/> |
| [<span data-ttu-id="2359d-119">**InitiateShutdown**</span><span class="sxs-lookup"><span data-stu-id="2359d-119">**InitiateShutdown**</span></span>](msvm-shutdowncomponent-initiateshutdown.md)     | <span data-ttu-id="2359d-120">Inicia una operación de apagado del sistema operativo en la máquina virtual secundaria asociada.</span><span class="sxs-lookup"><span data-stu-id="2359d-120">Initiates an operating system shutdown operation on associated child virtual machine.</span></span><br/>   |
| <span data-ttu-id="2359d-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="2359d-121">**OnlineDevice**</span></span>                                                        | <span data-ttu-id="2359d-122">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="2359d-122">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="2359d-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="2359d-123">**QuiesceDevice**</span></span>                                                       | <span data-ttu-id="2359d-124">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="2359d-124">This method is not supported.</span></span><br/>                                                           |
| [<span data-ttu-id="2359d-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="2359d-125">**RequestStateChange**</span></span>](msvm-shutdowncomponent-requeststatechange.md) | <span data-ttu-id="2359d-126">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="2359d-126">Requests a state change.</span></span><br/>                                                                |
| [<span data-ttu-id="2359d-127">**Reset**</span><span class="sxs-lookup"><span data-stu-id="2359d-127">**Reset**</span></span>](msvm-shutdowncomponent-reset.md)                           | <span data-ttu-id="2359d-128">Restablece el componente.</span><span class="sxs-lookup"><span data-stu-id="2359d-128">Resets the component.</span></span><br/>                                                                   |
| <span data-ttu-id="2359d-129">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="2359d-129">**RestoreProperties**</span></span>                                                   | <span data-ttu-id="2359d-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="2359d-130">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="2359d-131">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="2359d-131">**SaveProperties**</span></span>                                                      | <span data-ttu-id="2359d-132">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="2359d-132">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="2359d-133">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2359d-133">**SetPowerState**</span></span>                                                       | <span data-ttu-id="2359d-134">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="2359d-134">This method is not supported.</span></span><br/>                                                           |



 

### <a name="properties"></a><span data-ttu-id="2359d-135">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2359d-135">Properties</span></span>

<span data-ttu-id="2359d-136">La clase **MSVM \_ ShutdownComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2359d-136">The **Msvm\_ShutdownComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2359d-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="2359d-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-138">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2359d-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2359d-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-140">Disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2359d-140">Additional availability and status of the device.</span></span> <span data-ttu-id="2359d-141">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2359d-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="2359d-142">Value</span><span class="sxs-lookup"><span data-stu-id="2359d-142">Value</span></span>                                                                        | <span data-ttu-id="2359d-143">Significado</span><span class="sxs-lookup"><span data-stu-id="2359d-143">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="2359d-144"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2359d-144"><dt>6</dt></span></span> </dl> | <span data-ttu-id="2359d-145">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="2359d-145">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2359d-146">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="2359d-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-147">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2359d-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-149">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2359d-149">The primary availability and status of the device.</span></span> <span data-ttu-id="2359d-150">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="2359d-150">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>



| <span data-ttu-id="2359d-151">Value</span><span class="sxs-lookup"><span data-stu-id="2359d-151">Value</span></span>                                                                        | <span data-ttu-id="2359d-152">Significado</span><span class="sxs-lookup"><span data-stu-id="2359d-152">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="2359d-153"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2359d-153"><dt>6</dt></span></span> </dl> | <span data-ttu-id="2359d-154">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="2359d-154">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2359d-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="2359d-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-156">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2359d-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2359d-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-158">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="2359d-158">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="2359d-159">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="2359d-159">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2359d-160">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2359d-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2359d-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-163">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="2359d-163">A short description of the object.</span></span> <span data-ttu-id="2359d-164">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2359d-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2359d-165">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="2359d-165">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-166">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2359d-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-168">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="2359d-168">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="2359d-169">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="2359d-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2359d-170">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2359d-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2359d-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2359d-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="2359d-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-173"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="2359d-173"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-174"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="2359d-174"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-175"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="2359d-175"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2359d-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="2359d-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2359d-178">)</span><span class="sxs-lookup"><span data-stu-id="2359d-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2359d-179">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2359d-179">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2359d-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-182">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="2359d-182">The scoping system's creation class name.</span></span> <span data-ttu-id="2359d-183">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2359d-183">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2359d-184">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2359d-184">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2359d-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-187">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="2359d-187">A description of the object.</span></span> <span data-ttu-id="2359d-188">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2359d-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2359d-189">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="2359d-189">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-190">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2359d-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-192">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="2359d-192">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="2359d-193">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="2359d-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2359d-194">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2359d-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2359d-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="2359d-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="2359d-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="2359d-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="2359d-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="2359d-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="2359d-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2359d-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="2359d-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2359d-203">)</span><span class="sxs-lookup"><span data-stu-id="2359d-203">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2359d-204">**ID**</span><span class="sxs-lookup"><span data-stu-id="2359d-204">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-205">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2359d-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-207">Una dirección u otra información de identificación para asignar un nombre único al LogicalDevice.</span><span class="sxs-lookup"><span data-stu-id="2359d-207">An address or other identifying information to uniquely name the LogicalDevice.</span></span> <span data-ttu-id="2359d-208">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "Microsoft:*VMGUID* \\ *GUID*", donde *VMGUID* es la propiedad **Name** de la instancia de [**MSVM \_ ComputerSystem**](msvm-computersystem.md) asociada con este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2359d-208">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) instance associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="2359d-209">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2359d-209">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2359d-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-212">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="2359d-212">A display name for the object.</span></span> <span data-ttu-id="2359d-213">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2359d-213">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2359d-214">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="2359d-214">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-215">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2359d-215">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-217">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2359d-217">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="2359d-218">Value</span><span class="sxs-lookup"><span data-stu-id="2359d-218">Value</span></span>                                                                        | <span data-ttu-id="2359d-219">Significado</span><span class="sxs-lookup"><span data-stu-id="2359d-219">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="2359d-220"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="2359d-220"><dt>7</dt></span></span> </dl> | <span data-ttu-id="2359d-221">Sin valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2359d-221">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2359d-222">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2359d-222">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-223">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2359d-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-225">Estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="2359d-225">The enabled state of the element.</span></span> <span data-ttu-id="2359d-226">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) y está establecida en 2 (habilitado) o 3 (deshabilitada).</span><span class="sxs-lookup"><span data-stu-id="2359d-226">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is either set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="2359d-227">Value</span><span class="sxs-lookup"><span data-stu-id="2359d-227">Value</span></span>                                                                        | <span data-ttu-id="2359d-228">Significado</span><span class="sxs-lookup"><span data-stu-id="2359d-228">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="2359d-229"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2359d-229"><dt>2</dt></span></span> </dl> | <span data-ttu-id="2359d-230">habilitado</span><span class="sxs-lookup"><span data-stu-id="2359d-230">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="2359d-231"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2359d-231"><dt>3</dt></span></span> </dl> | <span data-ttu-id="2359d-232">Disabled</span><span class="sxs-lookup"><span data-stu-id="2359d-232">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2359d-233">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2359d-233">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-234">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2359d-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-236">Indica si el error comunicado en la propiedad **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="2359d-236">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="2359d-237">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="2359d-237">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2359d-238">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2359d-238">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-239">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2359d-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-241">Una cadena que proporciona más información sobre el error registrado en la propiedad **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="2359d-241">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="2359d-242">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="2359d-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2359d-243">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="2359d-243">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-244">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2359d-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-246">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="2359d-246">The current health of the element.</span></span> <span data-ttu-id="2359d-247">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="2359d-247">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="2359d-248">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2359d-248">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2359d-249">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2359d-249">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-250">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2359d-250">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2359d-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-252">Matriz de cadenas de formato libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="2359d-252">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="2359d-253">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="2359d-253">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2359d-254">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2359d-254">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-255">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2359d-255">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-257">Fecha y hora en que se instaló el servicio de integración en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2359d-257">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="2359d-258">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2359d-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2359d-259">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2359d-259">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-260">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2359d-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2359d-262">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="2359d-262">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2359d-263">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="2359d-263">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2359d-264">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2359d-264">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2359d-265">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2359d-265">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-266">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2359d-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-268">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2359d-268">The last error code reported by the logical device.</span></span> <span data-ttu-id="2359d-269">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="2359d-269">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2359d-270">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="2359d-270">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-271">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2359d-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-273">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="2359d-273">This property has been deprecated.</span></span> <span data-ttu-id="2359d-274">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2359d-274">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2359d-275">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2359d-275">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-276">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2359d-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-277">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-278">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="2359d-278">The label by which the object is known.</span></span> <span data-ttu-id="2359d-279">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2359d-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2359d-280">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="2359d-280">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-281">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2359d-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-283">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="2359d-283">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="2359d-284">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="2359d-284">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2359d-285">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2359d-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2359d-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2359d-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-287"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="2359d-287"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-288"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="2359d-288"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-289"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="2359d-289"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-290"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="2359d-290"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-291"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="2359d-291"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-292"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="2359d-292"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-293"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="2359d-293"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-294"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="2359d-294"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-295"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="2359d-295"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-296"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="2359d-296"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-297"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="2359d-297"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-298"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="2359d-298"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-299"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="2359d-299"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-300"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="2359d-300"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-301"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="2359d-301"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-302"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="2359d-302"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-303"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2359d-303"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-304"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="2359d-304"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2359d-305">)</span><span class="sxs-lookup"><span data-stu-id="2359d-305">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2359d-306">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="2359d-306">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-307">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2359d-307">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2359d-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-309">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="2359d-309">The current status of the element.</span></span> <span data-ttu-id="2359d-310">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2359d-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="2359d-311">A continuación se muestran los posibles valores para el valor de la propiedad **OperationalStatus** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="2359d-311">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="2359d-312">Value</span><span class="sxs-lookup"><span data-stu-id="2359d-312">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="2359d-313">Significado</span><span class="sxs-lookup"><span data-stu-id="2359d-313">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="2359d-314"><dt>**Aceptar**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2359d-314"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="2359d-315">El servicio está funcionando con normalidad.</span><span class="sxs-lookup"><span data-stu-id="2359d-315">The service is operating normally.</span></span> <span data-ttu-id="2359d-316">Los valores de la propiedad **OperationalStatus** \[ 1 \] y **StatusDescriptions** \[ 1 \] pueden contener más información.</span><span class="sxs-lookup"><span data-stu-id="2359d-316">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="2359d-317"><dt>**Degradado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2359d-317"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="2359d-318">El servicio está funcionando con normalidad, pero el servicio invitado negoció una versión del Protocolo de comunicaciones compatible.</span><span class="sxs-lookup"><span data-stu-id="2359d-318">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="2359d-319">Los valores de la propiedad **OperationalStatus** \[ 1 \] y **StatusDescriptions** \[ 1 \] pueden contener más información.</span><span class="sxs-lookup"><span data-stu-id="2359d-319">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="2359d-320"><dt>**Error no recuperable**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="2359d-320"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="2359d-321">El invitado no es compatible con una versión de protocolo compatible.</span><span class="sxs-lookup"><span data-stu-id="2359d-321">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="2359d-322">Los valores de la propiedad **OperationalStatus** \[ 1 \] y **StatusDescriptions** \[ 1 \] pueden contener más información.</span><span class="sxs-lookup"><span data-stu-id="2359d-322">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="2359d-323"><dt>**No Contact**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="2359d-323"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="2359d-324">El servicio invitado no está instalado o no se ha conectado todavía.</span><span class="sxs-lookup"><span data-stu-id="2359d-324">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="2359d-325"><dt>**Comunicación perdida**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="2359d-325"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="2359d-326">El servicio invitado ya no responde normalmente.</span><span class="sxs-lookup"><span data-stu-id="2359d-326">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="2359d-327">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="2359d-327">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-328">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2359d-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-330">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="2359d-330">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="2359d-331">Esta propiedad debe establecerse en **null** cuando la propiedad **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="2359d-331">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="2359d-332">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2359d-332">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2359d-333">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="2359d-333">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-334">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2359d-334">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2359d-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-336">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2359d-336">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="2359d-337">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="2359d-337">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2359d-338">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2359d-338">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-339">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2359d-339">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2359d-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-341">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2359d-341">The power management capabilities of the device.</span></span> <span data-ttu-id="2359d-342">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="2359d-342">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2359d-343">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2359d-343">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-344">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2359d-344">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-346">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="2359d-346">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="2359d-347">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="2359d-347">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2359d-348">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2359d-348">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-349">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2359d-349">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-351">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="2359d-351">The number of consecutive hours that this Device has been powered on since its last power cycle.</span></span> <span data-ttu-id="2359d-352">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="2359d-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2359d-353">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="2359d-353">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-354">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2359d-354">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-356">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="2359d-356">Provides high level status information.</span></span> <span data-ttu-id="2359d-357">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="2359d-357">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="2359d-358">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="2359d-358">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2359d-359">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2359d-359">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2359d-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2359d-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-361"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="2359d-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="2359d-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="2359d-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2359d-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2359d-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="2359d-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2359d-366">)</span><span class="sxs-lookup"><span data-stu-id="2359d-366">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2359d-367">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="2359d-367">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-368">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2359d-368">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-370">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="2359d-370">The last requested or desired state for the element.</span></span> <span data-ttu-id="2359d-371">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="2359d-371">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="2359d-372">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="2359d-372">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="2359d-373">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="2359d-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="2359d-374">Value</span><span class="sxs-lookup"><span data-stu-id="2359d-374">Value</span></span>                                                                         | <span data-ttu-id="2359d-375">Significado</span><span class="sxs-lookup"><span data-stu-id="2359d-375">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="2359d-376"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="2359d-376"><dt>12</dt></span></span> </dl> | <span data-ttu-id="2359d-377">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="2359d-377">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2359d-378">**Estado**</span><span class="sxs-lookup"><span data-stu-id="2359d-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-379">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2359d-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-381">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2359d-381">The current status of the object.</span></span> <span data-ttu-id="2359d-382">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="2359d-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2359d-383">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2359d-383">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-384">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2359d-384">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2359d-385">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-386">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="2359d-386">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="2359d-387">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2359d-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2359d-388">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2359d-388">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-389">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2359d-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-391">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2359d-391">The current state of the logical device.</span></span> <span data-ttu-id="2359d-392">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="2359d-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2359d-393">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2359d-393">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-394">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2359d-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-395">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-396">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="2359d-396">The scoping system's creation class name.</span></span> <span data-ttu-id="2359d-397">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2359d-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2359d-398">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2359d-398">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-399">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2359d-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-401">Identificador único de la máquina virtual de ámbito.</span><span class="sxs-lookup"><span data-stu-id="2359d-401">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="2359d-402">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2359d-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2359d-403">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="2359d-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-404">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2359d-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-405">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-406">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="2359d-406">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="2359d-407">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2359d-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2359d-408">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2359d-408">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-409">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2359d-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-411">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2359d-411">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="2359d-412">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="2359d-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2359d-413">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="2359d-413">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2359d-414">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2359d-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2359d-415">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2359d-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2359d-416">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="2359d-416">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="2359d-417">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="2359d-417">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2359d-418">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2359d-418">Remarks</span></span>

<span data-ttu-id="2359d-419">El acceso a la clase **MSVM \_ ShutdownComponent** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="2359d-419">Access to the **Msvm\_ShutdownComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2359d-420">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2359d-420">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2359d-421">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2359d-421">Requirements</span></span>



| <span data-ttu-id="2359d-422">Requisito</span><span class="sxs-lookup"><span data-stu-id="2359d-422">Requirement</span></span> | <span data-ttu-id="2359d-423">Value</span><span class="sxs-lookup"><span data-stu-id="2359d-423">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2359d-424">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2359d-424">Minimum supported client</span></span><br/> | <span data-ttu-id="2359d-425">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2359d-425">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2359d-426">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2359d-426">Minimum supported server</span></span><br/> | <span data-ttu-id="2359d-427">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="2359d-427">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2359d-428">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2359d-428">Namespace</span></span><br/>                | <span data-ttu-id="2359d-429">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2359d-429">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2359d-430">MOF</span><span class="sxs-lookup"><span data-stu-id="2359d-430">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2359d-431"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2359d-431"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2359d-432">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2359d-432">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2359d-433"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2359d-433"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2359d-434">Vea también</span><span class="sxs-lookup"><span data-stu-id="2359d-434">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2359d-435">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2359d-435">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="2359d-436">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2359d-436">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

