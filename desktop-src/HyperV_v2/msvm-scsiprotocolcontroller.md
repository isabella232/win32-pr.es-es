---
description: Representa una controladora SCSI sintética.
ms.assetid: 4ABAB4C8-F922-4AA3-8FEE-5F5AA969E8B4
title: Msvm_SCSIProtocolController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SCSIProtocolController
- Msvm_SCSIProtocolController.SetPowerState
- Msvm_SCSIProtocolController.EnableDevice
- Msvm_SCSIProtocolController.OnlineDevice
- Msvm_SCSIProtocolController.QuiesceDevice
- Msvm_SCSIProtocolController.SaveProperties
- Msvm_SCSIProtocolController.RestoreProperties
- Msvm_SCSIProtocolController.InstanceID
- Msvm_SCSIProtocolController.Caption
- Msvm_SCSIProtocolController.Description
- Msvm_SCSIProtocolController.ElementName
- Msvm_SCSIProtocolController.InstallDate
- Msvm_SCSIProtocolController.Name
- Msvm_SCSIProtocolController.OperationalStatus
- Msvm_SCSIProtocolController.StatusDescriptions
- Msvm_SCSIProtocolController.Status
- Msvm_SCSIProtocolController.HealthState
- Msvm_SCSIProtocolController.CommunicationStatus
- Msvm_SCSIProtocolController.DetailedStatus
- Msvm_SCSIProtocolController.OperatingStatus
- Msvm_SCSIProtocolController.PrimaryStatus
- Msvm_SCSIProtocolController.EnabledState
- Msvm_SCSIProtocolController.OtherEnabledState
- Msvm_SCSIProtocolController.RequestedState
- Msvm_SCSIProtocolController.EnabledDefault
- Msvm_SCSIProtocolController.TimeOfLastStateChange
- Msvm_SCSIProtocolController.AvailableRequestedStates
- Msvm_SCSIProtocolController.TransitioningToState
- Msvm_SCSIProtocolController.SystemCreationClassName
- Msvm_SCSIProtocolController.SystemName
- Msvm_SCSIProtocolController.CreationClassName
- Msvm_SCSIProtocolController.DeviceID
- Msvm_SCSIProtocolController.PowerManagementSupported
- Msvm_SCSIProtocolController.PowerManagementCapabilities
- Msvm_SCSIProtocolController.Availability
- Msvm_SCSIProtocolController.StatusInfo
- Msvm_SCSIProtocolController.LastErrorCode
- Msvm_SCSIProtocolController.ErrorDescription
- Msvm_SCSIProtocolController.ErrorCleared
- Msvm_SCSIProtocolController.OtherIdentifyingInfo
- Msvm_SCSIProtocolController.PowerOnHours
- Msvm_SCSIProtocolController.TotalPowerOnHours
- Msvm_SCSIProtocolController.IdentifyingDescriptions
- Msvm_SCSIProtocolController.AdditionalAvailability
- Msvm_SCSIProtocolController.MaxQuiesceTime
- Msvm_SCSIProtocolController.MaxUnitsControlled
- Msvm_SCSIProtocolController.NameFormat
- Msvm_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b65390c7cb03f195e9de39aedc3629688717e0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547206"
---
# <a name="msvm_scsiprotocolcontroller-class"></a><span data-ttu-id="9916f-103">MSVM \_ SCSIProtocolController (clase)</span><span class="sxs-lookup"><span data-stu-id="9916f-103">Msvm\_SCSIProtocolController class</span></span>

<span data-ttu-id="9916f-104">Representa una controladora SCSI sintética.</span><span class="sxs-lookup"><span data-stu-id="9916f-104">Represents a synthetic SCSI controller.</span></span> <span data-ttu-id="9916f-105">Una controladora SCSI sintética puede admitir hasta 256 unidades.</span><span class="sxs-lookup"><span data-stu-id="9916f-105">A synthetic SCSI controller can support up to 256 drives.</span></span>

<span data-ttu-id="9916f-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9916f-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9916f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9916f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SCSIProtocolController : CIM_SCSIProtocolController
{
  string   InstanceID;
  string   Caption = "SCSI Controller";
  string   Description = "Microsoft Virtual SCSI Controller";
  string   ElementName = "SCSI Controller";
  datetime InstallDate;
  string   Name = "SCSI Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_SCSIProtocolController";
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
  uint32   MaxUnitsControlled = 256;
  uint16   NameFormat = 0;
  string   OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="9916f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9916f-108">Members</span></span>

<span data-ttu-id="9916f-109">La clase **MSVM \_ SCSIProtocolController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9916f-109">The **Msvm\_SCSIProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="9916f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9916f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9916f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9916f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9916f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9916f-112">Methods</span></span>

<span data-ttu-id="9916f-113">La clase **MSVM \_ SCSIProtocolController** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9916f-113">The **Msvm\_SCSIProtocolController** class has these methods.</span></span>



| <span data-ttu-id="9916f-114">Método</span><span class="sxs-lookup"><span data-stu-id="9916f-114">Method</span></span>                                                                       | <span data-ttu-id="9916f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9916f-115">Description</span></span>                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="9916f-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="9916f-116">**EnableDevice**</span></span>                                                             | <span data-ttu-id="9916f-117">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="9916f-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9916f-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="9916f-118">**OnlineDevice**</span></span>                                                             | <span data-ttu-id="9916f-119">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="9916f-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9916f-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="9916f-120">**QuiesceDevice**</span></span>                                                            | <span data-ttu-id="9916f-121">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="9916f-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="9916f-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="9916f-122">**RequestStateChange**</span></span>](msvm-scsiprotocolcontroller-requeststatechange.md) | <span data-ttu-id="9916f-123">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="9916f-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="9916f-124">**Reset**</span><span class="sxs-lookup"><span data-stu-id="9916f-124">**Reset**</span></span>](msvm-scsiprotocolcontroller-reset.md)                           | <span data-ttu-id="9916f-125">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="9916f-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="9916f-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="9916f-126">**RestoreProperties**</span></span>                                                        | <span data-ttu-id="9916f-127">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="9916f-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9916f-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="9916f-128">**SaveProperties**</span></span>                                                           | <span data-ttu-id="9916f-129">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="9916f-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9916f-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9916f-130">**SetPowerState**</span></span>                                                            | <span data-ttu-id="9916f-131">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="9916f-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9916f-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9916f-132">Properties</span></span>

<span data-ttu-id="9916f-133">La clase **MSVM \_ SCSIProtocolController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9916f-133">The **Msvm\_SCSIProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9916f-134">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="9916f-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-135">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9916f-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-137">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9916f-137">Any additional availability and status of the device.</span></span> <span data-ttu-id="9916f-138">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="9916f-138">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="9916f-139">Value</span><span class="sxs-lookup"><span data-stu-id="9916f-139">Value</span></span>                                                                            | <span data-ttu-id="9916f-140">Significado</span><span class="sxs-lookup"><span data-stu-id="9916f-140">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="9916f-141"><dt>1,8</dt></span><span class="sxs-lookup"><span data-stu-id="9916f-141"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="9916f-142"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9916f-142"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="9916f-143">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="9916f-143">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9916f-144">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="9916f-144">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-145">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-147">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9916f-147">The primary availability and status of the device.</span></span> <span data-ttu-id="9916f-148">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="9916f-148">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="9916f-149">Value</span><span class="sxs-lookup"><span data-stu-id="9916f-149">Value</span></span>                                                                        | <span data-ttu-id="9916f-150">Significado</span><span class="sxs-lookup"><span data-stu-id="9916f-150">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="9916f-151"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9916f-151"><dt>6</dt></span></span> </dl> | <span data-ttu-id="9916f-152">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="9916f-152">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9916f-153">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="9916f-153">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-154">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-154">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9916f-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-156">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="9916f-156">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="9916f-157">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="9916f-157">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9916f-158">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9916f-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9916f-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-161">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="9916f-161">A short description of the object.</span></span> <span data-ttu-id="9916f-162">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9916f-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9916f-163">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="9916f-163">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-164">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-166">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="9916f-166">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9916f-167">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="9916f-167">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9916f-168">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9916f-168">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9916f-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9916f-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="9916f-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="9916f-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="9916f-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="9916f-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9916f-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="9916f-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9916f-176">)</span><span class="sxs-lookup"><span data-stu-id="9916f-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9916f-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9916f-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9916f-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-180">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="9916f-180">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9916f-181">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="9916f-181">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9916f-182">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9916f-182">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9916f-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-185">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="9916f-185">A description of the object.</span></span> <span data-ttu-id="9916f-186">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9916f-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9916f-187">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9916f-187">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-188">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-190">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="9916f-190">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9916f-191">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="9916f-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9916f-192">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9916f-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9916f-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="9916f-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="9916f-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="9916f-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="9916f-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="9916f-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="9916f-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9916f-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="9916f-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9916f-201">)</span><span class="sxs-lookup"><span data-stu-id="9916f-201">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9916f-202">**ID**</span><span class="sxs-lookup"><span data-stu-id="9916f-202">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9916f-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-205">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en "Microsoft:*GUID* del \\ *dispositivo-datos específicos*".</span><span class="sxs-lookup"><span data-stu-id="9916f-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="9916f-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9916f-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9916f-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-209">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="9916f-209">A display name for the object.</span></span> <span data-ttu-id="9916f-210">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9916f-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9916f-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="9916f-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-212">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-214">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="9916f-214">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="9916f-215">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9916f-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="9916f-216">Value</span><span class="sxs-lookup"><span data-stu-id="9916f-216">Value</span></span>                                                                        | <span data-ttu-id="9916f-217">Significado</span><span class="sxs-lookup"><span data-stu-id="9916f-217">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="9916f-218"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9916f-218"><dt>2</dt></span></span> </dl> | <span data-ttu-id="9916f-219">habilitado</span><span class="sxs-lookup"><span data-stu-id="9916f-219">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9916f-220">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9916f-220">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-221">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-223">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="9916f-223">The enabled and disabled states of an element.</span></span> <span data-ttu-id="9916f-224">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="9916f-224">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="9916f-225">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9916f-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="9916f-226">Value</span><span class="sxs-lookup"><span data-stu-id="9916f-226">Value</span></span>                                                                        | <span data-ttu-id="9916f-227">Significado</span><span class="sxs-lookup"><span data-stu-id="9916f-227">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="9916f-228"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9916f-228"><dt>5</dt></span></span> </dl> | <span data-ttu-id="9916f-229">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="9916f-229">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9916f-230">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9916f-230">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-231">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9916f-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-233">Indica si el error comunicado en la propiedad **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="9916f-233">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="9916f-234">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="9916f-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9916f-235">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9916f-235">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-236">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9916f-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-238">Una cadena que proporciona más información sobre el error registrado en la propiedad **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="9916f-238">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="9916f-239">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="9916f-239">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9916f-240">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9916f-240">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-241">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-243">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="9916f-243">The current health of the element.</span></span> <span data-ttu-id="9916f-244">Esto expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="9916f-244">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="9916f-245">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="9916f-245">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="9916f-246">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9916f-246">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9916f-247">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9916f-247">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-248">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="9916f-248">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9916f-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-250">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="9916f-250">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="9916f-251">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="9916f-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9916f-252">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9916f-252">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-253">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9916f-253">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-255">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9916f-255">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="9916f-256">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9916f-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9916f-257">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9916f-257">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9916f-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9916f-260">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="9916f-260">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9916f-261">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="9916f-261">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9916f-262">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9916f-262">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9916f-263">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9916f-263">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-264">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9916f-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-266">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9916f-266">The last error code reported by the logical device.</span></span> <span data-ttu-id="9916f-267">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="9916f-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9916f-268">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="9916f-268">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-269">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9916f-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-271">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="9916f-271">This property has been deprecated.</span></span> <span data-ttu-id="9916f-272">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="9916f-272">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9916f-273">**MaxUnitsControlled**</span><span class="sxs-lookup"><span data-stu-id="9916f-273">**MaxUnitsControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-274">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9916f-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-276">Número máximo de unidades que puede controlar o a la que se tiene acceso a través de este controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="9916f-276">The maximum number of units that can be controlled by or accessed through this protocol controller.</span></span> <span data-ttu-id="9916f-277">Esta propiedad se hereda de [**\_ ProtocolController CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span><span class="sxs-lookup"><span data-stu-id="9916f-277">This property is inherited from [**CIM\_ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="9916f-278">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="9916f-278">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-279">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9916f-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-281">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="9916f-281">The label by which the object is known.</span></span> <span data-ttu-id="9916f-282">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9916f-282">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9916f-283">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="9916f-283">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-284">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-286">Identifica cómo se selecciona el nombre del controlador de protocolo SCSI.</span><span class="sxs-lookup"><span data-stu-id="9916f-286">Identifies how the name of the SCSI protocol controller is selected.</span></span> <span data-ttu-id="9916f-287">Esta propiedad se hereda de [**\_ SCSIProtocolController CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span><span class="sxs-lookup"><span data-stu-id="9916f-287">This property is inherited from [**CIM\_SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>



| <span data-ttu-id="9916f-288">Value</span><span class="sxs-lookup"><span data-stu-id="9916f-288">Value</span></span>                                                                        | <span data-ttu-id="9916f-289">Significado</span><span class="sxs-lookup"><span data-stu-id="9916f-289">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="9916f-290"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9916f-290"><dt>0</dt></span></span> </dl> | <span data-ttu-id="9916f-291">Unknown</span><span class="sxs-lookup"><span data-stu-id="9916f-291">Unknown</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9916f-292">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="9916f-292">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-293">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-293">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-295">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="9916f-295">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9916f-296">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="9916f-296">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9916f-297">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9916f-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9916f-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9916f-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-299"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="9916f-299"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-300"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="9916f-300"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-301"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="9916f-301"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-302"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="9916f-302"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-303"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="9916f-303"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-304"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="9916f-304"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-305"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="9916f-305"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-306"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="9916f-306"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-307"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="9916f-307"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-308"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="9916f-308"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-309"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="9916f-309"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-310"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="9916f-310"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-311"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="9916f-311"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-312"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="9916f-312"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-313"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="9916f-313"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-314"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="9916f-314"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9916f-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="9916f-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9916f-317">)</span><span class="sxs-lookup"><span data-stu-id="9916f-317">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9916f-318">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9916f-318">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-319">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-319">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9916f-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-321">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9916f-321">The current status of the object.</span></span> <span data-ttu-id="9916f-322">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9916f-322">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="9916f-323">Value</span><span class="sxs-lookup"><span data-stu-id="9916f-323">Value</span></span>                                                                            | <span data-ttu-id="9916f-324">Significado</span><span class="sxs-lookup"><span data-stu-id="9916f-324">Meaning</span></span>       |
|----------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="9916f-325"><dt>dos</dt></span><span class="sxs-lookup"><span data-stu-id="9916f-325"><dt>{ 2 }</dt></span></span> </dl> |               |
| <dl> <span data-ttu-id="9916f-326"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9916f-326"><dt>2</dt></span></span> </dl>     | <span data-ttu-id="9916f-327">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9916f-327">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9916f-328">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="9916f-328">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-329">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9916f-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-331">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="9916f-331">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="9916f-332">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="9916f-332">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="9916f-333">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9916f-333">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9916f-334">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9916f-334">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-335">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="9916f-335">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9916f-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-337">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9916f-337">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="9916f-338">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="9916f-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9916f-339">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="9916f-339">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9916f-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-342">Cadena que describe cómo se identifica el controlador de protocolo cuando **NameFormat** es 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="9916f-342">A string that describes how the protocol controller is identified when the **NameFormat** is 1 (Other).</span></span> <span data-ttu-id="9916f-343">Esta propiedad se hereda de [**\_ SCSIProtocolController CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span><span class="sxs-lookup"><span data-stu-id="9916f-343">This property is inherited from [**CIM\_SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="9916f-344">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9916f-344">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-345">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9916f-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-347">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9916f-347">The power management capabilities of the device.</span></span> <span data-ttu-id="9916f-348">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="9916f-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9916f-349">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9916f-349">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-350">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9916f-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-352">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="9916f-352">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="9916f-353">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="9916f-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9916f-354">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="9916f-354">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-355">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9916f-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-357">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="9916f-357">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="9916f-358">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="9916f-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9916f-359">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="9916f-359">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-360">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-362">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="9916f-362">Provides high level status information.</span></span> <span data-ttu-id="9916f-363">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="9916f-363">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="9916f-364">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="9916f-364">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9916f-365">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9916f-365">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9916f-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9916f-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-367"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="9916f-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="9916f-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="9916f-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9916f-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9916f-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="9916f-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9916f-372">)</span><span class="sxs-lookup"><span data-stu-id="9916f-372">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9916f-373">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9916f-373">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-374">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-376">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="9916f-376">The last requested or desired state for the element.</span></span> <span data-ttu-id="9916f-377">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="9916f-377">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="9916f-378">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="9916f-378">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="9916f-379">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9916f-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="9916f-380">Value</span><span class="sxs-lookup"><span data-stu-id="9916f-380">Value</span></span>                                                                         | <span data-ttu-id="9916f-381">Significado</span><span class="sxs-lookup"><span data-stu-id="9916f-381">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="9916f-382"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="9916f-382"><dt>12</dt></span></span> </dl> | <span data-ttu-id="9916f-383">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="9916f-383">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9916f-384">**Estado**</span><span class="sxs-lookup"><span data-stu-id="9916f-384">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-385">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9916f-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-386">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-387">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9916f-387">The current status of the object.</span></span> <span data-ttu-id="9916f-388">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="9916f-388">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9916f-389">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9916f-389">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-390">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="9916f-390">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9916f-391">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-392">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="9916f-392">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9916f-393">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "OK".</span><span class="sxs-lookup"><span data-stu-id="9916f-393">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="9916f-394">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9916f-394">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-395">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-396">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-397">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9916f-397">The current state of the logical device.</span></span> <span data-ttu-id="9916f-398">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="9916f-398">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9916f-399">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9916f-399">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-400">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9916f-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-401">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-402">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="9916f-402">The scoping system's creation class name.</span></span> <span data-ttu-id="9916f-403">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="9916f-403">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9916f-404">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9916f-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-405">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9916f-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-406">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-407">Identificador único de la máquina virtual de ámbito.</span><span class="sxs-lookup"><span data-stu-id="9916f-407">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="9916f-408">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="9916f-408">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9916f-409">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="9916f-409">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-410">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9916f-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-411">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-412">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="9916f-412">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="9916f-413">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9916f-413">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9916f-414">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="9916f-414">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-415">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9916f-415">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-417">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9916f-417">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="9916f-418">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="9916f-418">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9916f-419">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="9916f-419">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9916f-420">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9916f-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9916f-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9916f-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9916f-422">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="9916f-422">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9916f-423">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="9916f-423">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9916f-424">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9916f-424">Remarks</span></span>

<span data-ttu-id="9916f-425">El acceso a la clase **MSVM \_ SCSIProtocolController** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="9916f-425">Access to the **Msvm\_SCSIProtocolController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9916f-426">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9916f-426">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9916f-427">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9916f-427">Requirements</span></span>



| <span data-ttu-id="9916f-428">Requisito</span><span class="sxs-lookup"><span data-stu-id="9916f-428">Requirement</span></span> | <span data-ttu-id="9916f-429">Value</span><span class="sxs-lookup"><span data-stu-id="9916f-429">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9916f-430">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9916f-430">Minimum supported client</span></span><br/> | <span data-ttu-id="9916f-431">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="9916f-431">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9916f-432">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9916f-432">Minimum supported server</span></span><br/> | <span data-ttu-id="9916f-433">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9916f-433">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9916f-434">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9916f-434">Namespace</span></span><br/>                | <span data-ttu-id="9916f-435">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9916f-435">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9916f-436">MOF</span><span class="sxs-lookup"><span data-stu-id="9916f-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9916f-437"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9916f-437"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9916f-438">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9916f-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9916f-439"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9916f-439"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9916f-440">Vea también</span><span class="sxs-lookup"><span data-stu-id="9916f-440">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9916f-441">**\_SCSIPROTOCOLCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="9916f-441">**CIM\_SCSIProtocolController**</span></span>](cim-scsiprotocolcontroller.md)
</dt> <dt>

[<span data-ttu-id="9916f-442">**\_SCSIPROTOCOLCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="9916f-442">**CIM\_SCSIProtocolController**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)
</dt> <dt>

[<span data-ttu-id="9916f-443">Clases de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="9916f-443">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

