---
description: Representa el estado del componente RDV, que es responsable de proporcionar un transporte para el elemento primario al invitado con fines de configuración.
ms.assetid: 240d2659-01ec-4300-a17e-0b1ec90483df
title: Msvm_RdvComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent
- Msvm_RdvComponent.RequestStateChange
- Msvm_RdvComponent.SetPowerState
- Msvm_RdvComponent.Reset
- Msvm_RdvComponent.EnableDevice
- Msvm_RdvComponent.OnlineDevice
- Msvm_RdvComponent.QuiesceDevice
- Msvm_RdvComponent.SaveProperties
- Msvm_RdvComponent.RestoreProperties
- Msvm_RdvComponent.InstanceID
- Msvm_RdvComponent.Caption
- Msvm_RdvComponent.Description
- Msvm_RdvComponent.ElementName
- Msvm_RdvComponent.InstallDate
- Msvm_RdvComponent.Name
- Msvm_RdvComponent.OperationalStatus
- Msvm_RdvComponent.StatusDescriptions
- Msvm_RdvComponent.Status
- Msvm_RdvComponent.HealthState
- Msvm_RdvComponent.CommunicationStatus
- Msvm_RdvComponent.DetailedStatus
- Msvm_RdvComponent.OperatingStatus
- Msvm_RdvComponent.PrimaryStatus
- Msvm_RdvComponent.EnabledState
- Msvm_RdvComponent.OtherEnabledState
- Msvm_RdvComponent.RequestedState
- Msvm_RdvComponent.EnabledDefault
- Msvm_RdvComponent.TimeOfLastStateChange
- Msvm_RdvComponent.AvailableRequestedStates
- Msvm_RdvComponent.TransitioningToState
- Msvm_RdvComponent.SystemCreationClassName
- Msvm_RdvComponent.SystemName
- Msvm_RdvComponent.CreationClassName
- Msvm_RdvComponent.DeviceID
- Msvm_RdvComponent.PowerManagementSupported
- Msvm_RdvComponent.PowerManagementCapabilities
- Msvm_RdvComponent.Availability
- Msvm_RdvComponent.StatusInfo
- Msvm_RdvComponent.LastErrorCode
- Msvm_RdvComponent.ErrorDescription
- Msvm_RdvComponent.ErrorCleared
- Msvm_RdvComponent.OtherIdentifyingInfo
- Msvm_RdvComponent.PowerOnHours
- Msvm_RdvComponent.TotalPowerOnHours
- Msvm_RdvComponent.IdentifyingDescriptions
- Msvm_RdvComponent.AdditionalAvailability
- Msvm_RdvComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e1dbffb7db18ef2441d4c8e06cff23af2648e5a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277051"
---
# <a name="msvm_rdvcomponent-class"></a><span data-ttu-id="ca49f-103">MSVM \_ RdvComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="ca49f-103">Msvm\_RdvComponent class</span></span>

<span data-ttu-id="ca49f-104">Representa el estado del componente RDV, que es responsable de proporcionar un transporte para el elemento primario al invitado con fines de configuración.</span><span class="sxs-lookup"><span data-stu-id="ca49f-104">Represents the state of the RDV component, which is responsible for providing a transport for the parent to the guest for configuration purposes.</span></span>

<span data-ttu-id="ca49f-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ca49f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca49f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca49f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "RDV";
  string   Description = "Remote Desktop Virtualization Service";
  string   ElementName = "RDV";
  datetime InstallDate;
  string   Name = "RDV";
  uint16   OperationalStatus[] = {2};
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
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_RdvComponent";
  string   DeviceID;
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
};
```

## <a name="members"></a><span data-ttu-id="ca49f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ca49f-107">Members</span></span>

<span data-ttu-id="ca49f-108">La clase **MSVM \_ RdvComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ca49f-108">The **Msvm\_RdvComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="ca49f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="ca49f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="ca49f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ca49f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ca49f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="ca49f-111">Methods</span></span>

<span data-ttu-id="ca49f-112">La clase **MSVM \_ RdvComponent** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ca49f-112">The **Msvm\_RdvComponent** class has these methods.</span></span>



| <span data-ttu-id="ca49f-113">Método</span><span class="sxs-lookup"><span data-stu-id="ca49f-113">Method</span></span>                                                       | <span data-ttu-id="ca49f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca49f-114">Description</span></span>                                                                                                                                                                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca49f-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="ca49f-115">**EnableDevice**</span></span>                                             | <span data-ttu-id="ca49f-116">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ca49f-116">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="ca49f-117">**EnableEndPoints**</span><span class="sxs-lookup"><span data-stu-id="ca49f-117">**EnableEndPoints**</span></span>](enableendpoints-msvm-rdvcomponent.md) | <span data-ttu-id="ca49f-118">Solicita el Servicios de Escritorio remoto dispositivo virtual para iniciar una conexión de canalización con la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ca49f-118">Requests the Remote Desktop Services virtual device to start a pipe connection with the virtual machine.</span></span> <span data-ttu-id="ca49f-119">Si se devuelve cero (0), la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ca49f-119">If zero (0) is returned, then the operation was successful.</span></span> <span data-ttu-id="ca49f-120">Cualquier otro código de retorno indica una condición de error.</span><span class="sxs-lookup"><span data-stu-id="ca49f-120">Any other return code indicates an error condition.</span></span><br/> |
| <span data-ttu-id="ca49f-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="ca49f-121">**OnlineDevice**</span></span>                                             | <span data-ttu-id="ca49f-122">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ca49f-122">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="ca49f-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="ca49f-123">**QuiesceDevice**</span></span>                                            | <span data-ttu-id="ca49f-124">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ca49f-124">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="ca49f-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="ca49f-125">**RequestStateChange**</span></span>                                       | <span data-ttu-id="ca49f-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ca49f-126">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="ca49f-127">**Reset**</span><span class="sxs-lookup"><span data-stu-id="ca49f-127">**Reset**</span></span>                                                    | <span data-ttu-id="ca49f-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ca49f-128">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="ca49f-129">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="ca49f-129">**RestoreProperties**</span></span>                                        | <span data-ttu-id="ca49f-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ca49f-130">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="ca49f-131">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="ca49f-131">**SaveProperties**</span></span>                                           | <span data-ttu-id="ca49f-132">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ca49f-132">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="ca49f-133">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ca49f-133">**SetPowerState**</span></span>                                            | <span data-ttu-id="ca49f-134">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ca49f-134">This method is not supported.</span></span><br/>                                                                                                                                                                                            |



 

### <a name="properties"></a><span data-ttu-id="ca49f-135">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ca49f-135">Properties</span></span>

<span data-ttu-id="ca49f-136">La clase **MSVM \_ RdvComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ca49f-136">The **Msvm\_RdvComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca49f-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="ca49f-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-138">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca49f-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-140">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca49f-140">Any additional availability and status of the device.</span></span> <span data-ttu-id="ca49f-141">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ca49f-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-142">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="ca49f-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-143">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca49f-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-145">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca49f-145">The primary availability and status of the device.</span></span> <span data-ttu-id="ca49f-146">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ca49f-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="ca49f-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-148">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca49f-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-150">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="ca49f-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="ca49f-151">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="ca49f-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-152">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ca49f-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca49f-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-155">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ca49f-155">A short description of the object.</span></span> <span data-ttu-id="ca49f-156">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ca49f-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="ca49f-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-158">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca49f-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-160">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="ca49f-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="ca49f-161">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="ca49f-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ca49f-162">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ca49f-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ca49f-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="ca49f-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="ca49f-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="ca49f-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="ca49f-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="ca49f-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ca49f-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="ca49f-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ca49f-170">)</span><span class="sxs-lookup"><span data-stu-id="ca49f-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ca49f-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ca49f-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca49f-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-174">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="ca49f-174">The scoping system's creation class name.</span></span> <span data-ttu-id="ca49f-175">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ca49f-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-176">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ca49f-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca49f-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-179">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ca49f-179">A description of the object.</span></span> <span data-ttu-id="ca49f-180">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ca49f-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="ca49f-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-182">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca49f-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-184">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="ca49f-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="ca49f-185">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="ca49f-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ca49f-186">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ca49f-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ca49f-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="ca49f-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="ca49f-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="ca49f-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="ca49f-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="ca49f-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="ca49f-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ca49f-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="ca49f-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ca49f-195">)</span><span class="sxs-lookup"><span data-stu-id="ca49f-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ca49f-196">**ID**</span><span class="sxs-lookup"><span data-stu-id="ca49f-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca49f-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-199">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ca49f-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="ca49f-200">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ca49f-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ca49f-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca49f-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-204">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="ca49f-204">A display name for the object.</span></span> <span data-ttu-id="ca49f-205">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ca49f-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-206">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="ca49f-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-207">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca49f-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-209">Configuración predeterminada o de inicio de un administrador para la propiedad **EnabledState** de un elemento.</span><span class="sxs-lookup"><span data-stu-id="ca49f-209">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="ca49f-210">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ca49f-210">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-211">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ca49f-211">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-212">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca49f-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-214">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="ca49f-214">The enabled and disabled states of an element.</span></span> <span data-ttu-id="ca49f-215">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ca49f-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="ca49f-216">Value</span><span class="sxs-lookup"><span data-stu-id="ca49f-216">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="ca49f-217">Significado</span><span class="sxs-lookup"><span data-stu-id="ca49f-217">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="ca49f-218"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ca49f-218"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="ca49f-219">No se pudo determinar el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="ca49f-219">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="ca49f-220"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ca49f-220"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="ca49f-221"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ca49f-221"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="ca49f-222">El elemento se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="ca49f-222">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="ca49f-223"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ca49f-223"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="ca49f-224">El elemento está desactivado.</span><span class="sxs-lookup"><span data-stu-id="ca49f-224">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="ca49f-225"><dt>**Cerrando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ca49f-225"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="ca49f-226">El elemento está en el proceso de pasar a un Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="ca49f-226">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="ca49f-227"><dt>**No aplicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ca49f-227"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="ca49f-228">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="ca49f-228">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="ca49f-229"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ca49f-229"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="ca49f-230">Es posible que el elemento esté completando comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="ca49f-230">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="ca49f-231"><dt>**En la prueba**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="ca49f-231"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="ca49f-232">El elemento está en un estado de prueba.</span><span class="sxs-lookup"><span data-stu-id="ca49f-232">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="ca49f-233"><dt>**Aplazado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="ca49f-233"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="ca49f-234">Es posible que el elemento esté completando los comandos, pero pondrá en cola todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="ca49f-234">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="ca49f-235">Modo <dt>**inactivo**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="ca49f-235"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="ca49f-236">El elemento está habilitado pero en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="ca49f-236">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="ca49f-237">El comportamiento del elemento es similar al estado habilitado (2), pero solo procesa un conjunto restringido de comandos.</span><span class="sxs-lookup"><span data-stu-id="ca49f-237">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="ca49f-238">Todas las demás solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="ca49f-238">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="ca49f-239"><dt>**Inicio**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="ca49f-239"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="ca49f-240">El elemento está en proceso de pasar a un estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="ca49f-240">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="ca49f-241">Las nuevas solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="ca49f-241">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="ca49f-242">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="ca49f-242">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-243">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ca49f-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-245">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="ca49f-245">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="ca49f-246">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ca49f-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-247">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ca49f-247">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-248">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca49f-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-250">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="ca49f-250">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="ca49f-251">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ca49f-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ca49f-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-253">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca49f-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-255">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="ca49f-255">The current health of the element.</span></span> <span data-ttu-id="ca49f-256">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ca49f-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-257">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ca49f-257">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-258">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ca49f-258">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-260">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="ca49f-260">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="ca49f-261">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ca49f-261">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-262">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ca49f-262">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-263">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ca49f-263">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-265">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="ca49f-265">The date and time when the object was installed.</span></span> <span data-ttu-id="ca49f-266">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="ca49f-266">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="ca49f-267">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ca49f-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-268">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ca49f-268">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-269">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca49f-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-271">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="ca49f-271">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-272">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="ca49f-272">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ca49f-273">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ca49f-273">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-274">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ca49f-274">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-275">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca49f-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-277">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ca49f-277">The last error code reported by the logical device.</span></span> <span data-ttu-id="ca49f-278">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ca49f-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-279">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="ca49f-279">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-280">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ca49f-280">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-282">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="ca49f-282">This property has been deprecated.</span></span> <span data-ttu-id="ca49f-283">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ca49f-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-284">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="ca49f-284">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-285">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca49f-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-287">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="ca49f-287">The label by which the object is known.</span></span> <span data-ttu-id="ca49f-288">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ca49f-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-289">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="ca49f-289">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-290">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca49f-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-292">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="ca49f-292">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="ca49f-293">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="ca49f-293">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ca49f-294">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ca49f-294">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ca49f-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="ca49f-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-296"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="ca49f-296"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-297"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="ca49f-297"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-298"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="ca49f-298"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-299"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="ca49f-299"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-300"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="ca49f-300"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-301"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="ca49f-301"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-302"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="ca49f-302"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-303"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="ca49f-303"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-304"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="ca49f-304"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-305"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="ca49f-305"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-306"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="ca49f-306"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-307"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="ca49f-307"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-308"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="ca49f-308"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-309"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="ca49f-309"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-310"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="ca49f-310"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-311"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="ca49f-311"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-312"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ca49f-312"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-313"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="ca49f-313"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ca49f-314">)</span><span class="sxs-lookup"><span data-stu-id="ca49f-314">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ca49f-315">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ca49f-315">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-316">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca49f-316">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-318">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="ca49f-318">The current statuses of the object.</span></span> <span data-ttu-id="ca49f-319">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ca49f-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-320">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="ca49f-320">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-321">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca49f-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-323">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="ca49f-323">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="ca49f-324">Esta propiedad debe establecerse en **null** cuando la propiedad **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="ca49f-324">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="ca49f-325">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="ca49f-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-326">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ca49f-326">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-327">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ca49f-327">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-329">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ca49f-329">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="ca49f-330">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ca49f-330">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-331">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ca49f-331">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-332">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca49f-332">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-334">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca49f-334">The power management capabilities of the device.</span></span> <span data-ttu-id="ca49f-335">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ca49f-335">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-336">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="ca49f-336">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-337">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ca49f-337">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-339">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="ca49f-339">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="ca49f-340">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ca49f-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-341">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ca49f-341">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-342">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ca49f-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-344">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="ca49f-344">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="ca49f-345">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ca49f-345">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-346">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="ca49f-346">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-347">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca49f-347">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-349">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="ca49f-349">Provides high level status information.</span></span> <span data-ttu-id="ca49f-350">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="ca49f-350">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="ca49f-351">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="ca49f-351">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ca49f-352">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ca49f-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ca49f-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="ca49f-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-354"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="ca49f-354"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-355"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="ca49f-355"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-356"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="ca49f-356"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ca49f-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="ca49f-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ca49f-359">)</span><span class="sxs-lookup"><span data-stu-id="ca49f-359">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ca49f-360">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="ca49f-360">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-361">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca49f-361">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-363">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="ca49f-363">The last requested or desired state for the element.</span></span> <span data-ttu-id="ca49f-364">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="ca49f-364">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-365">**Estado**</span><span class="sxs-lookup"><span data-stu-id="ca49f-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-366">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca49f-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-368">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="ca49f-368">The current status of the object.</span></span> <span data-ttu-id="ca49f-369">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ca49f-369">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-370">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ca49f-370">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-371">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ca49f-371">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-373">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="ca49f-373">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="ca49f-374">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ca49f-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-375">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ca49f-375">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-376">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca49f-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-378">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ca49f-378">The current state of the logical device.</span></span> <span data-ttu-id="ca49f-379">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ca49f-379">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-380">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ca49f-380">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-381">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca49f-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-383">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="ca49f-383">The scoping system's creation class name.</span></span> <span data-ttu-id="ca49f-384">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ca49f-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-385">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ca49f-385">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-386">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca49f-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-388">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="ca49f-388">The scoping system's name.</span></span> <span data-ttu-id="ca49f-389">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ca49f-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-390">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="ca49f-390">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-391">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ca49f-391">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-392">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-393">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="ca49f-393">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="ca49f-394">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="ca49f-394">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-395">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ca49f-395">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-396">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ca49f-396">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-398">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca49f-398">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="ca49f-399">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ca49f-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ca49f-400">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="ca49f-400">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49f-401">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca49f-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca49f-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca49f-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49f-403">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="ca49f-403">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="ca49f-404">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="ca49f-404">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca49f-405">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca49f-405">Requirements</span></span>



| <span data-ttu-id="ca49f-406">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca49f-406">Requirement</span></span> | <span data-ttu-id="ca49f-407">Value</span><span class="sxs-lookup"><span data-stu-id="ca49f-407">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca49f-408">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca49f-408">Minimum supported client</span></span><br/> | <span data-ttu-id="ca49f-409">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ca49f-409">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ca49f-410">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca49f-410">Minimum supported server</span></span><br/> | <span data-ttu-id="ca49f-411">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ca49f-411">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca49f-412">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ca49f-412">Namespace</span></span><br/>                | <span data-ttu-id="ca49f-413">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ca49f-413">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ca49f-414">MOF</span><span class="sxs-lookup"><span data-stu-id="ca49f-414">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca49f-415"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca49f-415"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca49f-416">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ca49f-416">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca49f-417"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ca49f-417"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

