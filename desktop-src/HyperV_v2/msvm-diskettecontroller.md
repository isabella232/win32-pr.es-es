---
description: Representa el controlador de disquete en la máquina virtual.
ms.assetid: 38A19BF3-0E8F-4DCE-B2DB-B2E3F8100E00
title: Msvm_DisketteController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteController
- Msvm_DisketteController.SetPowerState
- Msvm_DisketteController.EnableDevice
- Msvm_DisketteController.OnlineDevice
- Msvm_DisketteController.QuiesceDevice
- Msvm_DisketteController.SaveProperties
- Msvm_DisketteController.RestoreProperties
- Msvm_DisketteController.InstanceID
- Msvm_DisketteController.Caption
- Msvm_DisketteController.Description
- Msvm_DisketteController.ElementName
- Msvm_DisketteController.InstallDate
- Msvm_DisketteController.Name
- Msvm_DisketteController.OperationalStatus
- Msvm_DisketteController.StatusDescriptions
- Msvm_DisketteController.Status
- Msvm_DisketteController.HealthState
- Msvm_DisketteController.CommunicationStatus
- Msvm_DisketteController.DetailedStatus
- Msvm_DisketteController.OperatingStatus
- Msvm_DisketteController.PrimaryStatus
- Msvm_DisketteController.EnabledState
- Msvm_DisketteController.OtherEnabledState
- Msvm_DisketteController.RequestedState
- Msvm_DisketteController.EnabledDefault
- Msvm_DisketteController.TimeOfLastStateChange
- Msvm_DisketteController.AvailableRequestedStates
- Msvm_DisketteController.TransitioningToState
- Msvm_DisketteController.SystemCreationClassName
- Msvm_DisketteController.SystemName
- Msvm_DisketteController.CreationClassName
- Msvm_DisketteController.DeviceID
- Msvm_DisketteController.PowerManagementSupported
- Msvm_DisketteController.PowerManagementCapabilities
- Msvm_DisketteController.Availability
- Msvm_DisketteController.StatusInfo
- Msvm_DisketteController.LastErrorCode
- Msvm_DisketteController.ErrorDescription
- Msvm_DisketteController.ErrorCleared
- Msvm_DisketteController.OtherIdentifyingInfo
- Msvm_DisketteController.PowerOnHours
- Msvm_DisketteController.TotalPowerOnHours
- Msvm_DisketteController.IdentifyingDescriptions
- Msvm_DisketteController.AdditionalAvailability
- Msvm_DisketteController.MaxQuiesceTime
- Msvm_DisketteController.TimeOfLastReset
- Msvm_DisketteController.ProtocolSupported
- Msvm_DisketteController.MaxNumberControlled
- Msvm_DisketteController.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f1e4e731464e25dc8e871ebd17cdcddd4e262673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809530"
---
# <a name="msvm_diskettecontroller-class"></a><span data-ttu-id="912ee-103">MSVM \_ DisketteController (clase)</span><span class="sxs-lookup"><span data-stu-id="912ee-103">Msvm\_DisketteController class</span></span>

<span data-ttu-id="912ee-104">Representa el controlador de disquete en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="912ee-104">Represents the floppy controller in the virtual machine.</span></span> <span data-ttu-id="912ee-105">El controlador de disquete es fijo, por lo que no hay ningún grupo de recursos asociado a él.</span><span class="sxs-lookup"><span data-stu-id="912ee-105">The floppy controller is fixed, therefore there is no resource pool associated with it.</span></span>

<span data-ttu-id="912ee-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="912ee-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="912ee-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="912ee-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DisketteController : CIM_Controller
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName = "Msvm_DisketteController";
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
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 7;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Diskette Protocol";
};
```

## <a name="members"></a><span data-ttu-id="912ee-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="912ee-108">Members</span></span>

<span data-ttu-id="912ee-109">La clase **MSVM \_ DisketteController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="912ee-109">The **Msvm\_DisketteController** class has these types of members:</span></span>

-   [<span data-ttu-id="912ee-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="912ee-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="912ee-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="912ee-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="912ee-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="912ee-112">Methods</span></span>

<span data-ttu-id="912ee-113">La clase **MSVM \_ DisketteController** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="912ee-113">The **Msvm\_DisketteController** class has these methods.</span></span>



| <span data-ttu-id="912ee-114">Método</span><span class="sxs-lookup"><span data-stu-id="912ee-114">Method</span></span>                                                                   | <span data-ttu-id="912ee-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="912ee-115">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="912ee-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="912ee-116">**EnableDevice**</span></span>                                                         | <span data-ttu-id="912ee-117">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="912ee-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="912ee-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="912ee-118">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="912ee-119">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="912ee-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="912ee-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="912ee-120">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="912ee-121">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="912ee-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="912ee-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="912ee-122">**RequestStateChange**</span></span>](msvm-diskettecontroller-requeststatechange.md) | <span data-ttu-id="912ee-123">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="912ee-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="912ee-124">**Reset**</span><span class="sxs-lookup"><span data-stu-id="912ee-124">**Reset**</span></span>](msvm-diskettecontroller-reset.md)                           | <span data-ttu-id="912ee-125">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="912ee-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="912ee-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="912ee-126">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="912ee-127">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="912ee-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="912ee-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="912ee-128">**SaveProperties**</span></span>                                                       | <span data-ttu-id="912ee-129">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="912ee-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="912ee-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="912ee-130">**SetPowerState**</span></span>                                                        | <span data-ttu-id="912ee-131">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="912ee-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="912ee-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="912ee-132">Properties</span></span>

<span data-ttu-id="912ee-133">La clase **MSVM \_ DisketteController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="912ee-133">The **Msvm\_DisketteController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="912ee-134">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="912ee-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-135">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="912ee-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-137">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en 6 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="912ee-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-138">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="912ee-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-141">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en 6 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="912ee-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-142">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="912ee-142">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-143">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-143">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="912ee-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-145">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="912ee-145">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="912ee-146">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="912ee-146">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-147">**Caption**</span><span class="sxs-lookup"><span data-stu-id="912ee-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="912ee-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-150">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="912ee-150">A short description of the object.</span></span> <span data-ttu-id="912ee-151">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="912ee-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-152">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="912ee-152">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-153">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-155">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="912ee-155">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="912ee-156">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="912ee-156">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="912ee-157">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="912ee-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="912ee-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="912ee-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-159"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="912ee-159"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-160"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="912ee-160"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-161"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="912ee-161"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-162"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="912ee-162"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-163"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="912ee-163"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-164"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="912ee-164"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="912ee-165">)</span><span class="sxs-lookup"><span data-stu-id="912ee-165">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="912ee-166">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="912ee-166">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="912ee-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-169">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="912ee-169">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="912ee-170">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y se establece en "MSVM \_ DisketteController".</span><span class="sxs-lookup"><span data-stu-id="912ee-170">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Msvm\_DisketteController".</span></span>

</dd> <dt>

<span data-ttu-id="912ee-171">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="912ee-171">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="912ee-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-174">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="912ee-174">A description of the object.</span></span> <span data-ttu-id="912ee-175">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="912ee-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-176">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="912ee-176">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-177">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-179">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="912ee-179">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="912ee-180">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="912ee-180">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="912ee-181">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="912ee-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="912ee-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="912ee-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="912ee-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="912ee-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="912ee-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="912ee-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="912ee-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="912ee-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="912ee-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="912ee-190">)</span><span class="sxs-lookup"><span data-stu-id="912ee-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="912ee-191">**ID**</span><span class="sxs-lookup"><span data-stu-id="912ee-191">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="912ee-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-194">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="912ee-194">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="912ee-195">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="912ee-195">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-196">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="912ee-196">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="912ee-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-199">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="912ee-199">A display name for the object.</span></span> <span data-ttu-id="912ee-200">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="912ee-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-201">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="912ee-201">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-202">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-204">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="912ee-204">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="912ee-205">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="912ee-205">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-206">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="912ee-206">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-207">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-209">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="912ee-209">The enabled and disabled states of an element.</span></span> <span data-ttu-id="912ee-210">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="912ee-210">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="912ee-211">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="912ee-211">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="912ee-212">Value</span><span class="sxs-lookup"><span data-stu-id="912ee-212">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="912ee-213">Significado</span><span class="sxs-lookup"><span data-stu-id="912ee-213">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="912ee-214"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="912ee-214"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="912ee-215">No se pudo determinar el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="912ee-215">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="912ee-216"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="912ee-216"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="912ee-217"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="912ee-217"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="912ee-218">El elemento se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="912ee-218">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="912ee-219"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="912ee-219"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="912ee-220">El elemento está desactivado.</span><span class="sxs-lookup"><span data-stu-id="912ee-220">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="912ee-221"><dt>**Cerrando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="912ee-221"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="912ee-222">El elemento está en el proceso de pasar a un Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="912ee-222">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="912ee-223"><dt>**No aplicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="912ee-223"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="912ee-224">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="912ee-224">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="912ee-225"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="912ee-225"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="912ee-226">Es posible que el elemento esté completando comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="912ee-226">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="912ee-227"><dt>**En la prueba**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="912ee-227"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="912ee-228">El elemento está en un estado de prueba.</span><span class="sxs-lookup"><span data-stu-id="912ee-228">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="912ee-229"><dt>**Aplazado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="912ee-229"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="912ee-230">Es posible que el elemento esté completando los comandos, pero pondrá en cola todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="912ee-230">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="912ee-231">Modo <dt>**inactivo**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="912ee-231"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="912ee-232">El elemento está habilitado, pero está en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="912ee-232">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="912ee-233">El comportamiento del elemento es similar al estado habilitado (2), pero solo procesa un conjunto restringido de comandos.</span><span class="sxs-lookup"><span data-stu-id="912ee-233">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="912ee-234">Todas las demás solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="912ee-234">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="912ee-235"><dt>**Inicio**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="912ee-235"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="912ee-236">El elemento está en proceso de pasar a un estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="912ee-236">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="912ee-237">Las nuevas solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="912ee-237">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="912ee-238">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="912ee-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-239">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="912ee-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-241">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="912ee-241">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="912ee-242">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="912ee-242">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="912ee-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-245">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="912ee-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="912ee-246">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="912ee-246">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-247">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-249">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="912ee-249">The current health of the element.</span></span> <span data-ttu-id="912ee-250">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="912ee-250">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="912ee-251">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="912ee-251">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="912ee-252">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="912ee-252">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-253">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="912ee-253">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-254">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="912ee-254">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="912ee-255">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-256">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="912ee-256">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="912ee-257">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="912ee-257">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-258">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="912ee-258">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-260">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="912ee-260">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="912ee-261">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="912ee-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-262">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="912ee-262">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-263">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="912ee-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="912ee-265">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="912ee-265">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="912ee-266">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="912ee-266">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="912ee-267">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="912ee-267">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-268">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="912ee-268">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-269">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="912ee-269">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-271">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="912ee-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="912ee-272">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="912ee-272">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-273">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="912ee-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-275">Número máximo de entidades directamente direccionables admitidas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="912ee-275">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="912ee-276">Se debe utilizar un valor de 0 si el número es desconocido o ilimitado.</span><span class="sxs-lookup"><span data-stu-id="912ee-276">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="912ee-277">Protocolo usado por el controlador para tener acceso a los dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="912ee-277">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="912ee-278">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller)y está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="912ee-278">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="912ee-279">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="912ee-279">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-280">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="912ee-280">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-282">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="912ee-282">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="912ee-283">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="912ee-283">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-284">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="912ee-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-286">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="912ee-286">The label by which the object is known.</span></span> <span data-ttu-id="912ee-287">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="912ee-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-288">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="912ee-288">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-289">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-291">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="912ee-291">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="912ee-292">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="912ee-292">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="912ee-293">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="912ee-293">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="912ee-294"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="912ee-294"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-295"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="912ee-295"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-296"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="912ee-296"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-297"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="912ee-297"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-298"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="912ee-298"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-299"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="912ee-299"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-300"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="912ee-300"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-301"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="912ee-301"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-302"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="912ee-302"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-303"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="912ee-303"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-304"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="912ee-304"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-305"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="912ee-305"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-306"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="912ee-306"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-307"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="912ee-307"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-308"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="912ee-308"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-309"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="912ee-309"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-310"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="912ee-310"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-311"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="912ee-311"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-312"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="912ee-312"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="912ee-313">)</span><span class="sxs-lookup"><span data-stu-id="912ee-313">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="912ee-314">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="912ee-314">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-315">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-315">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="912ee-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-317">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="912ee-317">The current statuses of the object.</span></span> <span data-ttu-id="912ee-318">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="912ee-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-319">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="912ee-319">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-320">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="912ee-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-322">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="912ee-322">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="912ee-323">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="912ee-323">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="912ee-324">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="912ee-324">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="912ee-325">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="912ee-325">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-326">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="912ee-326">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="912ee-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-328">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="912ee-328">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="912ee-329">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="912ee-329">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-330">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-330">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="912ee-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-332">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="912ee-332">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="912ee-333">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="912ee-333">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-334">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="912ee-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-336">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="912ee-336">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="912ee-337">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="912ee-337">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-338">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="912ee-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-340">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="912ee-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="912ee-341">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="912ee-341">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-342">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-342">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-344">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="912ee-344">Provides high level status information.</span></span> <span data-ttu-id="912ee-345">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="912ee-345">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="912ee-346">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="912ee-346">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="912ee-347">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="912ee-347">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="912ee-348"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="912ee-348"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-349"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="912ee-349"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-350"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="912ee-350"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-351"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="912ee-351"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-352"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="912ee-352"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="912ee-353"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="912ee-353"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="912ee-354">)</span><span class="sxs-lookup"><span data-stu-id="912ee-354">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="912ee-355">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="912ee-355">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-356">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="912ee-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-358">Una cadena que proporciona más información relacionada con el protocolo compatible con el controlador.</span><span class="sxs-lookup"><span data-stu-id="912ee-358">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="912ee-359">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller)y está establecida en "Protocolo de disquete".</span><span class="sxs-lookup"><span data-stu-id="912ee-359">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to "Diskette Protocol".</span></span>

</dd> <dt>

<span data-ttu-id="912ee-360">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="912ee-360">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-361">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-361">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-363">Protocolo usado por el controlador para tener acceso a los dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="912ee-363">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="912ee-364">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller)y está establecida en 7 (disco flexible).</span><span class="sxs-lookup"><span data-stu-id="912ee-364">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to 7 (Flexible Diskette).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-365">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="912ee-365">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-366">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-368">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="912ee-368">The last requested or desired state for the element.</span></span> <span data-ttu-id="912ee-369">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="912ee-369">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="912ee-370">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="912ee-370">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="912ee-371">Una instancia concreta de un elemento lógico habilitado podría no ser compatible con **RequestedStateChange**.</span><span class="sxs-lookup"><span data-stu-id="912ee-371">A particular instance of an enabled logical element might not support **RequestedStateChange**.</span></span> <span data-ttu-id="912ee-372">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="912ee-372">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="912ee-373">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="912ee-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-374">**Estado**</span><span class="sxs-lookup"><span data-stu-id="912ee-374">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-375">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="912ee-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-376">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-377">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="912ee-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="912ee-378">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="912ee-378">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-379">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="912ee-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="912ee-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-381">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="912ee-381">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="912ee-382">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="912ee-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="912ee-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-384">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-385">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-386">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="912ee-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="912ee-387">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="912ee-387">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-388">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="912ee-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-389">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-390">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="912ee-390">The scoping system's creation class name.</span></span> <span data-ttu-id="912ee-391">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="912ee-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-392">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="912ee-392">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-393">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="912ee-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-395">Identificador único de la máquina virtual de ámbito.</span><span class="sxs-lookup"><span data-stu-id="912ee-395">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="912ee-396">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="912ee-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-397">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="912ee-397">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-398">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="912ee-398">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-400">La última vez que se encendió la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="912ee-400">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="912ee-401">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="912ee-401">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="912ee-402">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="912ee-402">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-403">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="912ee-403">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-405">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="912ee-405">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="912ee-406">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="912ee-406">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="912ee-407">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="912ee-407">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-408">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="912ee-408">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-409">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-410">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="912ee-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="912ee-411">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="912ee-411">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="912ee-412">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="912ee-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="912ee-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="912ee-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="912ee-414">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="912ee-414">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="912ee-415">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="912ee-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="912ee-416">Observaciones</span><span class="sxs-lookup"><span data-stu-id="912ee-416">Remarks</span></span>

<span data-ttu-id="912ee-417">El acceso a la clase **MSVM \_ DisketteController** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="912ee-417">Access to the **Msvm\_DisketteController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="912ee-418">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="912ee-418">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="912ee-419">Requisitos</span><span class="sxs-lookup"><span data-stu-id="912ee-419">Requirements</span></span>



| <span data-ttu-id="912ee-420">Requisito</span><span class="sxs-lookup"><span data-stu-id="912ee-420">Requirement</span></span> | <span data-ttu-id="912ee-421">Value</span><span class="sxs-lookup"><span data-stu-id="912ee-421">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="912ee-422">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="912ee-422">Minimum supported client</span></span><br/> | <span data-ttu-id="912ee-423">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="912ee-423">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="912ee-424">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="912ee-424">Minimum supported server</span></span><br/> | <span data-ttu-id="912ee-425">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="912ee-425">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="912ee-426">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="912ee-426">Namespace</span></span><br/>                | <span data-ttu-id="912ee-427">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="912ee-427">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="912ee-428">MOF</span><span class="sxs-lookup"><span data-stu-id="912ee-428">MOF</span></span><br/>                      | <dl> <span data-ttu-id="912ee-429"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="912ee-429"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="912ee-430">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="912ee-430">DLL</span></span><br/>                      | <dl> <span data-ttu-id="912ee-431"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="912ee-431"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="912ee-432">Vea también</span><span class="sxs-lookup"><span data-stu-id="912ee-432">See also</span></span>

<dl> <dt>

[<span data-ttu-id="912ee-433">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="912ee-433">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dt>

[<span data-ttu-id="912ee-434">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="912ee-434">**CIM\_Controller**</span></span>](/windows/desktop/CIMWin32Prov/cim-controller)
</dt> <dt>

[<span data-ttu-id="912ee-435">Clases de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="912ee-435">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

