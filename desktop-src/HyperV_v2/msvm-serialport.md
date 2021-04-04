---
description: Representa un puerto serie asociado al controlador serie.
ms.assetid: 856823A5-7481-453A-8476-1CDAB1D84123
title: Msvm_SerialPort (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPort
- Msvm_SerialPort.SetPowerState
- Msvm_SerialPort.EnableDevice
- Msvm_SerialPort.OnlineDevice
- Msvm_SerialPort.QuiesceDevice
- Msvm_SerialPort.SaveProperties
- Msvm_SerialPort.RestoreProperties
- Msvm_SerialPort.InstanceID
- Msvm_SerialPort.Caption
- Msvm_SerialPort.Description
- Msvm_SerialPort.ElementName
- Msvm_SerialPort.InstallDate
- Msvm_SerialPort.Name
- Msvm_SerialPort.OperationalStatus
- Msvm_SerialPort.StatusDescriptions
- Msvm_SerialPort.Status
- Msvm_SerialPort.HealthState
- Msvm_SerialPort.CommunicationStatus
- Msvm_SerialPort.DetailedStatus
- Msvm_SerialPort.OperatingStatus
- Msvm_SerialPort.PrimaryStatus
- Msvm_SerialPort.EnabledState
- Msvm_SerialPort.OtherEnabledState
- Msvm_SerialPort.RequestedState
- Msvm_SerialPort.EnabledDefault
- Msvm_SerialPort.TimeOfLastStateChange
- Msvm_SerialPort.AvailableRequestedStates
- Msvm_SerialPort.TransitioningToState
- Msvm_SerialPort.SystemCreationClassName
- Msvm_SerialPort.SystemName
- Msvm_SerialPort.CreationClassName
- Msvm_SerialPort.DeviceID
- Msvm_SerialPort.PowerManagementSupported
- Msvm_SerialPort.PowerManagementCapabilities
- Msvm_SerialPort.Availability
- Msvm_SerialPort.StatusInfo
- Msvm_SerialPort.LastErrorCode
- Msvm_SerialPort.ErrorDescription
- Msvm_SerialPort.ErrorCleared
- Msvm_SerialPort.OtherIdentifyingInfo
- Msvm_SerialPort.PowerOnHours
- Msvm_SerialPort.TotalPowerOnHours
- Msvm_SerialPort.IdentifyingDescriptions
- Msvm_SerialPort.AdditionalAvailability
- Msvm_SerialPort.MaxQuiesceTime
- Msvm_SerialPort.Speed
- Msvm_SerialPort.MaxSpeed
- Msvm_SerialPort.RequestedSpeed
- Msvm_SerialPort.UsageRestriction
- Msvm_SerialPort.PortType
- Msvm_SerialPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bc9ff5e1ce4b0a750866a9957c0cffc4bc8501e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910133"
---
# <a name="msvm_serialport-class"></a><span data-ttu-id="ae78c-103">MSVM \_ SerialPort (clase)</span><span class="sxs-lookup"><span data-stu-id="ae78c-103">Msvm\_SerialPort class</span></span>

<span data-ttu-id="ae78c-104">Representa un puerto serie asociado al controlador serie.</span><span class="sxs-lookup"><span data-stu-id="ae78c-104">Represents a serial port associated with the serial controller.</span></span>

<span data-ttu-id="ae78c-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ae78c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae78c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae78c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPort : CIM_LogicalPort
{
  string   InstanceID;
  string   Caption;
  string   Description = "Microsoft Virtual Serial Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
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
  string   CreationClassName = "Msvm_SerialPort";
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
  uint64   Speed = 115200;
  uint32   MaxSpeed = 115200;
  uint64   RequestedSpeed = 115200;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Serial Port";
};
```

## <a name="members"></a><span data-ttu-id="ae78c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ae78c-107">Members</span></span>

<span data-ttu-id="ae78c-108">La clase **MSVM \_ SerialPort** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ae78c-108">The **Msvm\_SerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="ae78c-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="ae78c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="ae78c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ae78c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ae78c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="ae78c-111">Methods</span></span>

<span data-ttu-id="ae78c-112">La **clase \_ SerialPort MSVM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ae78c-112">The **Msvm\_SerialPort** class has these methods.</span></span>



| <span data-ttu-id="ae78c-113">Método</span><span class="sxs-lookup"><span data-stu-id="ae78c-113">Method</span></span>                                                           | <span data-ttu-id="ae78c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae78c-114">Description</span></span>                              |
|:-----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="ae78c-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="ae78c-115">**EnableDevice**</span></span>                                                 | <span data-ttu-id="ae78c-116">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ae78c-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ae78c-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="ae78c-117">**OnlineDevice**</span></span>                                                 | <span data-ttu-id="ae78c-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ae78c-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ae78c-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="ae78c-119">**QuiesceDevice**</span></span>                                                | <span data-ttu-id="ae78c-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ae78c-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="ae78c-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="ae78c-121">**RequestStateChange**</span></span>](msvm-serialport-requeststatechange.md) | <span data-ttu-id="ae78c-122">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="ae78c-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="ae78c-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="ae78c-123">**Reset**</span></span>](msvm-serialport-reset.md)                           | <span data-ttu-id="ae78c-124">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="ae78c-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="ae78c-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="ae78c-125">**RestoreProperties**</span></span>                                            | <span data-ttu-id="ae78c-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ae78c-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ae78c-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="ae78c-127">**SaveProperties**</span></span>                                               | <span data-ttu-id="ae78c-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ae78c-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ae78c-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ae78c-129">**SetPowerState**</span></span>                                                | <span data-ttu-id="ae78c-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ae78c-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ae78c-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ae78c-131">Properties</span></span>

<span data-ttu-id="ae78c-132">La **clase \_ SerialPort MSVM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ae78c-132">The **Msvm\_SerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae78c-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="ae78c-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-134">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-136">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae78c-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="ae78c-137">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ae78c-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="ae78c-138">Value</span><span class="sxs-lookup"><span data-stu-id="ae78c-138">Value</span></span>                                                                            | <span data-ttu-id="ae78c-139">Significado</span><span class="sxs-lookup"><span data-stu-id="ae78c-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="ae78c-140"><dt>1,8</dt></span><span class="sxs-lookup"><span data-stu-id="ae78c-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="ae78c-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ae78c-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="ae78c-142">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="ae78c-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ae78c-143">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="ae78c-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-144">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-146">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae78c-146">The primary availability and status of the device.</span></span> <span data-ttu-id="ae78c-147">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ae78c-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="ae78c-148">Value</span><span class="sxs-lookup"><span data-stu-id="ae78c-148">Value</span></span>                                                                        | <span data-ttu-id="ae78c-149">Significado</span><span class="sxs-lookup"><span data-stu-id="ae78c-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="ae78c-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ae78c-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="ae78c-151">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="ae78c-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ae78c-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="ae78c-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-153">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-155">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="ae78c-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="ae78c-156">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae78c-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-157">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ae78c-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae78c-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-160">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ae78c-160">A short description of the object.</span></span> <span data-ttu-id="ae78c-161">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ae78c-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="ae78c-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-163">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-165">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="ae78c-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="ae78c-166">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="ae78c-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ae78c-167">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ae78c-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ae78c-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="ae78c-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="ae78c-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="ae78c-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="ae78c-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="ae78c-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ae78c-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="ae78c-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ae78c-175">)</span><span class="sxs-lookup"><span data-stu-id="ae78c-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ae78c-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ae78c-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae78c-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-179">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="ae78c-179">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ae78c-180">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ae78c-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-181">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae78c-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae78c-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-184">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ae78c-184">A description of the object.</span></span> <span data-ttu-id="ae78c-185">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ae78c-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="ae78c-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-187">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-189">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="ae78c-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="ae78c-190">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="ae78c-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ae78c-191">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ae78c-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ae78c-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="ae78c-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="ae78c-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="ae78c-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="ae78c-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="ae78c-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="ae78c-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ae78c-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="ae78c-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ae78c-200">)</span><span class="sxs-lookup"><span data-stu-id="ae78c-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ae78c-201">**ID**</span><span class="sxs-lookup"><span data-stu-id="ae78c-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae78c-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-204">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en "Microsoft:*GUID* del \\ *dispositivo-datos específicos*", donde los *datos específicos del dispositivo* son opcionales.</span><span class="sxs-lookup"><span data-stu-id="ae78c-204">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*", where *device-specific-data* is optional.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-205">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ae78c-205">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-206">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae78c-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-208">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="ae78c-208">A display name for the object.</span></span> <span data-ttu-id="ae78c-209">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ae78c-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-210">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="ae78c-210">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-211">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-213">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="ae78c-213">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="ae78c-214">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae78c-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="ae78c-215">Value</span><span class="sxs-lookup"><span data-stu-id="ae78c-215">Value</span></span>                                                                        | <span data-ttu-id="ae78c-216">Significado</span><span class="sxs-lookup"><span data-stu-id="ae78c-216">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="ae78c-217"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ae78c-217"><dt>2</dt></span></span> </dl> | <span data-ttu-id="ae78c-218">habilitado</span><span class="sxs-lookup"><span data-stu-id="ae78c-218">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ae78c-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ae78c-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-220">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-222">Estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="ae78c-222">The enabled state of the element.</span></span> <span data-ttu-id="ae78c-223">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="ae78c-223">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="ae78c-224">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae78c-224">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="ae78c-225">Value</span><span class="sxs-lookup"><span data-stu-id="ae78c-225">Value</span></span>                                                                        | <span data-ttu-id="ae78c-226">Significado</span><span class="sxs-lookup"><span data-stu-id="ae78c-226">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="ae78c-227"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ae78c-227"><dt>5</dt></span></span> </dl> | <span data-ttu-id="ae78c-228">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="ae78c-228">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ae78c-229">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="ae78c-229">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-230">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ae78c-230">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-232">Indica si el error comunicado en la propiedad **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="ae78c-232">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="ae78c-233">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae78c-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ae78c-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-235">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae78c-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-237">Una cadena que proporciona más información sobre el error registrado en la propiedad **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="ae78c-237">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="ae78c-238">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae78c-238">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-239">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ae78c-239">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-240">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-240">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-242">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="ae78c-242">The current health of the element.</span></span> <span data-ttu-id="ae78c-243">Esto expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="ae78c-243">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="ae78c-244">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="ae78c-244">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="ae78c-245">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ae78c-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-246">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ae78c-246">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-247">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ae78c-247">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-249">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="ae78c-249">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="ae78c-250">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="ae78c-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-251">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ae78c-251">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-252">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ae78c-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-254">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ae78c-254">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="ae78c-255">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ae78c-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-256">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ae78c-256">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae78c-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-259">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="ae78c-259">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-260">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="ae78c-260">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ae78c-261">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ae78c-261">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-262">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ae78c-262">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-263">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae78c-263">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-265">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ae78c-265">The last error code reported by the logical device.</span></span> <span data-ttu-id="ae78c-266">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae78c-266">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-267">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="ae78c-267">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-268">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ae78c-268">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-270">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="ae78c-270">This property has been deprecated.</span></span> <span data-ttu-id="ae78c-271">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ae78c-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-272">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="ae78c-272">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-273">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae78c-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-275">El ancho de banda máximo del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ae78c-275">The maximum bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="ae78c-276">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae78c-276">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-277">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="ae78c-277">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-278">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae78c-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-280">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="ae78c-280">The label by which the object is known.</span></span> <span data-ttu-id="ae78c-281">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y es igual que la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="ae78c-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-282">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="ae78c-282">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-283">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-285">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="ae78c-285">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="ae78c-286">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="ae78c-286">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ae78c-287">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ae78c-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ae78c-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="ae78c-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="ae78c-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="ae78c-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="ae78c-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="ae78c-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="ae78c-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="ae78c-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="ae78c-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="ae78c-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="ae78c-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="ae78c-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="ae78c-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="ae78c-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="ae78c-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="ae78c-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="ae78c-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="ae78c-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ae78c-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="ae78c-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ae78c-307">)</span><span class="sxs-lookup"><span data-stu-id="ae78c-307">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ae78c-308">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ae78c-308">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-309">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-311">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="ae78c-311">The current statuses of the object.</span></span> <span data-ttu-id="ae78c-312">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ae78c-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-313">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="ae78c-313">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-314">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae78c-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-316">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="ae78c-316">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="ae78c-317">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="ae78c-317">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="ae78c-318">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae78c-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-319">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ae78c-319">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-320">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ae78c-320">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-322">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ae78c-322">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="ae78c-323">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="ae78c-323">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-324">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="ae78c-324">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-325">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae78c-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-327">El tipo de módulo, cuando **portType** está establecido en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="ae78c-327">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="ae78c-328">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae78c-328">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-329">**PortType**</span><span class="sxs-lookup"><span data-stu-id="ae78c-329">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-330">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-330">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-332">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae78c-332">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="ae78c-333">Value</span><span class="sxs-lookup"><span data-stu-id="ae78c-333">Value</span></span>                                                                        | <span data-ttu-id="ae78c-334">Significado</span><span class="sxs-lookup"><span data-stu-id="ae78c-334">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="ae78c-335"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ae78c-335"><dt>1</dt></span></span> </dl> | <span data-ttu-id="ae78c-336">Otros</span><span class="sxs-lookup"><span data-stu-id="ae78c-336">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ae78c-337">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ae78c-337">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-338">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-340">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae78c-340">The power management capabilities of the device.</span></span> <span data-ttu-id="ae78c-341">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae78c-341">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-342">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="ae78c-342">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-343">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ae78c-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-345">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="ae78c-345">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="ae78c-346">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae78c-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-347">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ae78c-347">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-348">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ae78c-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-350">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="ae78c-350">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="ae78c-351">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae78c-351">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-352">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="ae78c-352">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-353">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-353">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-355">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="ae78c-355">Provides high level status information.</span></span> <span data-ttu-id="ae78c-356">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="ae78c-356">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="ae78c-357">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="ae78c-357">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ae78c-358">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ae78c-358">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ae78c-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="ae78c-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-360"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="ae78c-360"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="ae78c-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="ae78c-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ae78c-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="ae78c-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ae78c-365">)</span><span class="sxs-lookup"><span data-stu-id="ae78c-365">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ae78c-366">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="ae78c-366">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-367">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ae78c-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-369">Ancho de banda solicitado del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ae78c-369">The requested bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="ae78c-370">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae78c-370">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-371">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="ae78c-371">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-372">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-372">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-373">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-374">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="ae78c-374">The last requested or desired state for the element.</span></span> <span data-ttu-id="ae78c-375">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="ae78c-375">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="ae78c-376">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="ae78c-376">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="ae78c-377">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae78c-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="ae78c-378">Value</span><span class="sxs-lookup"><span data-stu-id="ae78c-378">Value</span></span>                                                                         | <span data-ttu-id="ae78c-379">Significado</span><span class="sxs-lookup"><span data-stu-id="ae78c-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="ae78c-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="ae78c-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="ae78c-381">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="ae78c-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ae78c-382">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="ae78c-382">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-383">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ae78c-383">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-384">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-385">Ancho de banda del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ae78c-385">The bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="ae78c-386">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae78c-386">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-387">**Estado**</span><span class="sxs-lookup"><span data-stu-id="ae78c-387">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-388">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae78c-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-389">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-390">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="ae78c-390">The current status of the object.</span></span> <span data-ttu-id="ae78c-391">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae78c-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-392">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ae78c-392">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-393">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ae78c-393">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-395">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="ae78c-395">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="ae78c-396">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ae78c-396">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-397">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ae78c-397">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-398">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-400">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ae78c-400">The current state of the logical device.</span></span> <span data-ttu-id="ae78c-401">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae78c-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-402">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ae78c-402">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-403">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae78c-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-405">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="ae78c-405">The scoping system's creation class name.</span></span> <span data-ttu-id="ae78c-406">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ae78c-406">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-407">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ae78c-407">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-408">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae78c-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-409">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-410">Identificador único de la máquina virtual de ámbito.</span><span class="sxs-lookup"><span data-stu-id="ae78c-410">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="ae78c-411">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ae78c-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-412">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="ae78c-412">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-413">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ae78c-413">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-414">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-415">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="ae78c-415">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="ae78c-416">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="ae78c-416">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-417">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ae78c-417">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-418">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ae78c-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-419">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-420">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae78c-420">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="ae78c-421">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae78c-421">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-422">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="ae78c-422">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-423">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-423">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-424">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-425">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="ae78c-425">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="ae78c-426">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae78c-426">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae78c-427">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="ae78c-427">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae78c-428">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae78c-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae78c-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae78c-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae78c-430">En algunas circunstancias, un puerto lógico puede identificarse como un puerto de front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="ae78c-430">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="ae78c-431">Un ejemplo de esta situación sería una matriz de almacenamiento que podría tener puertos back-end para comunicarse con las unidades de disco y los puertos front-end para comunicarse con los hosts.</span><span class="sxs-lookup"><span data-stu-id="ae78c-431">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="ae78c-432">Si no hay ninguna restricción sobre el uso del puerto, el valor debe establecerse en 4 (no restringido).</span><span class="sxs-lookup"><span data-stu-id="ae78c-432">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="ae78c-433">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae78c-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="ae78c-434">Value</span><span class="sxs-lookup"><span data-stu-id="ae78c-434">Value</span></span>                                                                        | <span data-ttu-id="ae78c-435">Significado</span><span class="sxs-lookup"><span data-stu-id="ae78c-435">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="ae78c-436"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ae78c-436"><dt>4</dt></span></span> </dl> | <span data-ttu-id="ae78c-437">No restringido</span><span class="sxs-lookup"><span data-stu-id="ae78c-437">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae78c-438">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae78c-438">Remarks</span></span>

<span data-ttu-id="ae78c-439">El acceso a la clase **MSVM \_ SerialPort** podría estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="ae78c-439">Access to the **Msvm\_SerialPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ae78c-440">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ae78c-440">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae78c-441">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae78c-441">Requirements</span></span>



| <span data-ttu-id="ae78c-442">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae78c-442">Requirement</span></span> | <span data-ttu-id="ae78c-443">Value</span><span class="sxs-lookup"><span data-stu-id="ae78c-443">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae78c-444">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae78c-444">Minimum supported client</span></span><br/> | <span data-ttu-id="ae78c-445">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae78c-445">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ae78c-446">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae78c-446">Minimum supported server</span></span><br/> | <span data-ttu-id="ae78c-447">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae78c-447">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ae78c-448">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ae78c-448">Namespace</span></span><br/>                | <span data-ttu-id="ae78c-449">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ae78c-449">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ae78c-450">MOF</span><span class="sxs-lookup"><span data-stu-id="ae78c-450">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae78c-451"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae78c-451"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae78c-452">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae78c-452">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae78c-453"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ae78c-453"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ae78c-454">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae78c-454">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae78c-455">**\_LOGICALPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="ae78c-455">**CIM\_LogicalPort**</span></span>](cim-logicalport.md)
</dt> <dt>

<span data-ttu-id="ae78c-456">[**\_LOGICALPORT CIM**](/previous-versions//cc136869(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ae78c-456">[**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ae78c-457">Clases de dispositivos serie</span><span class="sxs-lookup"><span data-stu-id="ae78c-457">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

