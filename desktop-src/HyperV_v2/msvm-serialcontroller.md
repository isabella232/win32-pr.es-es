---
description: Representa las capacidades y la administración del controlador serie.
ms.assetid: 0F4DCF98-8EE4-4005-ADD5-BA23CB4CBE82
title: Clase Msvm_SerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialController
- Msvm_SerialController.SetPowerState
- Msvm_SerialController.EnableDevice
- Msvm_SerialController.OnlineDevice
- Msvm_SerialController.QuiesceDevice
- Msvm_SerialController.SaveProperties
- Msvm_SerialController.RestoreProperties
- Msvm_SerialController.InstanceID
- Msvm_SerialController.Caption
- Msvm_SerialController.Description
- Msvm_SerialController.ElementName
- Msvm_SerialController.InstallDate
- Msvm_SerialController.Name
- Msvm_SerialController.OperationalStatus
- Msvm_SerialController.StatusDescriptions
- Msvm_SerialController.Status
- Msvm_SerialController.HealthState
- Msvm_SerialController.CommunicationStatus
- Msvm_SerialController.DetailedStatus
- Msvm_SerialController.OperatingStatus
- Msvm_SerialController.PrimaryStatus
- Msvm_SerialController.EnabledState
- Msvm_SerialController.OtherEnabledState
- Msvm_SerialController.RequestedState
- Msvm_SerialController.EnabledDefault
- Msvm_SerialController.TimeOfLastStateChange
- Msvm_SerialController.AvailableRequestedStates
- Msvm_SerialController.TransitioningToState
- Msvm_SerialController.SystemCreationClassName
- Msvm_SerialController.SystemName
- Msvm_SerialController.CreationClassName
- Msvm_SerialController.DeviceID
- Msvm_SerialController.PowerManagementSupported
- Msvm_SerialController.PowerManagementCapabilities
- Msvm_SerialController.Availability
- Msvm_SerialController.StatusInfo
- Msvm_SerialController.LastErrorCode
- Msvm_SerialController.ErrorDescription
- Msvm_SerialController.ErrorCleared
- Msvm_SerialController.OtherIdentifyingInfo
- Msvm_SerialController.PowerOnHours
- Msvm_SerialController.TotalPowerOnHours
- Msvm_SerialController.IdentifyingDescriptions
- Msvm_SerialController.AdditionalAvailability
- Msvm_SerialController.MaxQuiesceTime
- Msvm_SerialController.TimeOfLastReset
- Msvm_SerialController.ProtocolSupported
- Msvm_SerialController.MaxNumberControlled
- Msvm_SerialController.ProtocolDescription
- Msvm_SerialController.Capabilities
- Msvm_SerialController.CapabilityDescriptions
- Msvm_SerialController.MaxBaudRate
- Msvm_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3f1bbc9dabe078751d58875745a789895cb4c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652473"
---
# <a name="msvm_serialcontroller-class"></a><span data-ttu-id="448d3-103">MSVM \_ SerialController (clase)</span><span class="sxs-lookup"><span data-stu-id="448d3-103">Msvm\_SerialController class</span></span>

<span data-ttu-id="448d3-104">Representa las capacidades y la administración del controlador serie.</span><span class="sxs-lookup"><span data-stu-id="448d3-104">Represents the capabilities and management of the serial controller.</span></span> <span data-ttu-id="448d3-105">Los controladores serie son dispositivos lógicos que siempre están presentes en una máquina virtual y, por tanto, no se asignan a través de un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="448d3-105">Serial controllers are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="448d3-106">Siempre hay una instancia de controlador de serie en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="448d3-106">One serial controller instance is always present in a virtual machine.</span></span> <span data-ttu-id="448d3-107">Los controladores serie tienen un número fijo de instancias de puerto.</span><span class="sxs-lookup"><span data-stu-id="448d3-107">Serial controllers have a fixed number of port instances.</span></span> <span data-ttu-id="448d3-108">Esta implementación admite dos puertos por controlador.</span><span class="sxs-lookup"><span data-stu-id="448d3-108">This implementation supports two ports per controller.</span></span>

> [!Note]  
> <span data-ttu-id="448d3-109">Los controladores serie son opcionales en las [máquinas virtuales de generación 2](virtualization-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="448d3-109">Serial controllers are optional in [generation 2 virtual machines](virtualization-glossary.md).</span></span>

 

<span data-ttu-id="448d3-110">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="448d3-110">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="448d3-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="448d3-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialController : CIM_SerialController
{
  string   InstanceID;
  string   Caption = "Serial Controller";
  string   Description = "Microsoft Virtual Serial Controller";
  string   ElementName = "Serial Controller";
  datetime InstallDate;
  string   Name = "Serial Controller";
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
  string   CreationClassName = "Msvm_SerialController";
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
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 26;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription;
  uint16   Capabilities[] = { 5 };
  string   CapabilityDescriptions[] = { "16550 compatible" };
  uint32   MaxBaudRate = 115200;
  uint16   Security = 3;
};
```

## <a name="members"></a><span data-ttu-id="448d3-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="448d3-112">Members</span></span>

<span data-ttu-id="448d3-113">La clase **MSVM \_ SerialController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="448d3-113">The **Msvm\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="448d3-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="448d3-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="448d3-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="448d3-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="448d3-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="448d3-116">Methods</span></span>

<span data-ttu-id="448d3-117">La clase **MSVM \_ SerialController** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="448d3-117">The **Msvm\_SerialController** class has these methods.</span></span>



| <span data-ttu-id="448d3-118">Método</span><span class="sxs-lookup"><span data-stu-id="448d3-118">Method</span></span>                                                                 | <span data-ttu-id="448d3-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="448d3-119">Description</span></span>                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="448d3-120">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="448d3-120">**EnableDevice**</span></span>                                                       | <span data-ttu-id="448d3-121">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="448d3-121">This method is not supported.</span></span><br/> |
| <span data-ttu-id="448d3-122">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="448d3-122">**OnlineDevice**</span></span>                                                       | <span data-ttu-id="448d3-123">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="448d3-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="448d3-124">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="448d3-124">**QuiesceDevice**</span></span>                                                      | <span data-ttu-id="448d3-125">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="448d3-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="448d3-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="448d3-126">**RequestStateChange**</span></span>](msvm-serialcontroller-requeststatechange.md) | <span data-ttu-id="448d3-127">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="448d3-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="448d3-128">**Reset**</span><span class="sxs-lookup"><span data-stu-id="448d3-128">**Reset**</span></span>](msvm-serialcontroller-reset.md)                           | <span data-ttu-id="448d3-129">Restablece el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="448d3-129">Resets the device.</span></span><br/>            |
| <span data-ttu-id="448d3-130">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="448d3-130">**RestoreProperties**</span></span>                                                  | <span data-ttu-id="448d3-131">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="448d3-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="448d3-132">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="448d3-132">**SaveProperties**</span></span>                                                     | <span data-ttu-id="448d3-133">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="448d3-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="448d3-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="448d3-134">**SetPowerState**</span></span>                                                      | <span data-ttu-id="448d3-135">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="448d3-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="448d3-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="448d3-136">Properties</span></span>

<span data-ttu-id="448d3-137">La clase **MSVM \_ SerialController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="448d3-137">The **Msvm\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="448d3-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="448d3-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-139">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="448d3-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-141">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="448d3-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="448d3-142">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="448d3-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="448d3-143">Value</span><span class="sxs-lookup"><span data-stu-id="448d3-143">Value</span></span>                                                                            | <span data-ttu-id="448d3-144">Significado</span><span class="sxs-lookup"><span data-stu-id="448d3-144">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="448d3-145"><dt>1,8</dt></span><span class="sxs-lookup"><span data-stu-id="448d3-145"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="448d3-146"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="448d3-146"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="448d3-147">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="448d3-147">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="448d3-148">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="448d3-148">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-149">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-151">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="448d3-151">The primary availability and status of the device.</span></span> <span data-ttu-id="448d3-152">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="448d3-152">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="448d3-153">Value</span><span class="sxs-lookup"><span data-stu-id="448d3-153">Value</span></span>                                                                        | <span data-ttu-id="448d3-154">Significado</span><span class="sxs-lookup"><span data-stu-id="448d3-154">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="448d3-155"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="448d3-155"><dt>6</dt></span></span> </dl> | <span data-ttu-id="448d3-156">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="448d3-156">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="448d3-157">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="448d3-157">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-158">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="448d3-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-160">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="448d3-160">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="448d3-161">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="448d3-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="448d3-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="448d3-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-163">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="448d3-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-165">El almacenamiento en búfer y otras funciones del controlador serie que podrían ser inherentes en el hardware del chip.</span><span class="sxs-lookup"><span data-stu-id="448d3-165">The buffering and other capabilities of the serial controller that might be inherent in the chip hardware.</span></span> <span data-ttu-id="448d3-166">Esta propiedad se hereda de [**\_ SerialController CIM**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="448d3-166">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-167">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="448d3-167">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-168">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="448d3-168">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="448d3-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-170">Una matriz de cadenas de forma libre que proporciona explicaciones más detalladas para cualquiera de las características del controlador serie que se indican en la matriz de **capacidades** .</span><span class="sxs-lookup"><span data-stu-id="448d3-170">An array of free-form strings that provides more detailed explanations for any of the serial controller features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="448d3-171">Esta propiedad se hereda de [**\_ SerialController CIM**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="448d3-171">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-172">**Caption**</span><span class="sxs-lookup"><span data-stu-id="448d3-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="448d3-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-175">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="448d3-175">A short description of the object.</span></span> <span data-ttu-id="448d3-176">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="448d3-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-177">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="448d3-177">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-178">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-180">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="448d3-180">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="448d3-181">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="448d3-181">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="448d3-182">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="448d3-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="448d3-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="448d3-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="448d3-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="448d3-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="448d3-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="448d3-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="448d3-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="448d3-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="448d3-190">)</span><span class="sxs-lookup"><span data-stu-id="448d3-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="448d3-191">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="448d3-191">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="448d3-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-194">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="448d3-194">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="448d3-195">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="448d3-195">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-196">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="448d3-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="448d3-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-199">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="448d3-199">A description of the object.</span></span> <span data-ttu-id="448d3-200">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="448d3-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="448d3-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-202">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-204">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="448d3-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="448d3-205">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="448d3-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="448d3-206">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="448d3-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="448d3-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="448d3-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="448d3-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="448d3-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="448d3-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="448d3-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="448d3-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="448d3-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="448d3-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="448d3-215">)</span><span class="sxs-lookup"><span data-stu-id="448d3-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="448d3-216">**ID**</span><span class="sxs-lookup"><span data-stu-id="448d3-216">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="448d3-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-219">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "Microsoft: *<GUID>* ".</span><span class="sxs-lookup"><span data-stu-id="448d3-219">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*<GUID>*".</span></span>

</dd> <dt>

<span data-ttu-id="448d3-220">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="448d3-220">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-221">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="448d3-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-223">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="448d3-223">A display name for the object.</span></span> <span data-ttu-id="448d3-224">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="448d3-224">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-225">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="448d3-225">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-226">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-227">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-228">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="448d3-228">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="448d3-229">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="448d3-229">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="448d3-230">Value</span><span class="sxs-lookup"><span data-stu-id="448d3-230">Value</span></span>                                                                        | <span data-ttu-id="448d3-231">Significado</span><span class="sxs-lookup"><span data-stu-id="448d3-231">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="448d3-232"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="448d3-232"><dt>2</dt></span></span> </dl> | <span data-ttu-id="448d3-233">habilitado</span><span class="sxs-lookup"><span data-stu-id="448d3-233">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="448d3-234">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="448d3-234">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-235">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-237">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="448d3-237">The enabled and disabled states of an element.</span></span> <span data-ttu-id="448d3-238">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="448d3-238">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="448d3-239">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="448d3-239">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="448d3-240">Value</span><span class="sxs-lookup"><span data-stu-id="448d3-240">Value</span></span>                                                                        | <span data-ttu-id="448d3-241">Significado</span><span class="sxs-lookup"><span data-stu-id="448d3-241">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="448d3-242"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="448d3-242"><dt>5</dt></span></span> </dl> | <span data-ttu-id="448d3-243">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="448d3-243">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="448d3-244">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="448d3-244">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-245">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="448d3-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-247">Indica si el error comunicado en la propiedad **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="448d3-247">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="448d3-248">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="448d3-248">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="448d3-249">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="448d3-249">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-250">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="448d3-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-252">Una cadena que proporciona más información sobre el error registrado en la propiedad **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="448d3-252">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="448d3-253">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="448d3-253">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="448d3-254">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="448d3-254">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-255">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-257">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="448d3-257">The current health of the element.</span></span> <span data-ttu-id="448d3-258">Esto expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="448d3-258">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="448d3-259">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="448d3-259">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="448d3-260">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="448d3-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-261">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="448d3-261">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-262">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="448d3-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="448d3-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-264">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="448d3-264">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="448d3-265">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="448d3-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="448d3-266">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="448d3-266">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-267">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="448d3-267">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-269">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="448d3-269">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="448d3-270">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="448d3-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="448d3-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-272">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="448d3-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-273">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="448d3-274">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="448d3-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="448d3-275">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="448d3-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="448d3-276">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="448d3-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="448d3-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-278">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="448d3-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-280">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="448d3-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="448d3-281">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="448d3-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="448d3-282">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="448d3-282">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-283">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="448d3-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-285">La velocidad máxima en baudios, en bits por segundo, que admite el controlador serie.</span><span class="sxs-lookup"><span data-stu-id="448d3-285">The maximum baud rate, in bits per second, that is supported by the serial controller.</span></span> <span data-ttu-id="448d3-286">Esta propiedad se hereda de [**\_ SerialController CIM**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="448d3-286">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-287">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="448d3-287">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-288">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="448d3-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-290">Número máximo de entidades directamente direccionables admitidas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="448d3-290">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="448d3-291">Se debe utilizar un valor de 0 si el número es desconocido o ilimitado.</span><span class="sxs-lookup"><span data-stu-id="448d3-291">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="448d3-292">Protocolo usado por el controlador para tener acceso a los dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="448d3-292">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="448d3-293">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="448d3-293">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-294">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="448d3-294">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-295">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="448d3-295">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-297">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="448d3-297">This property has been deprecated.</span></span> <span data-ttu-id="448d3-298">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="448d3-298">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="448d3-299">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="448d3-299">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="448d3-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-302">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="448d3-302">The label by which the object is known.</span></span> <span data-ttu-id="448d3-303">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y es igual que la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="448d3-303">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="448d3-304">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="448d3-304">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-305">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-307">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="448d3-307">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="448d3-308">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="448d3-308">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="448d3-309">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="448d3-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="448d3-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="448d3-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-311"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="448d3-311"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-312"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="448d3-312"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-313"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="448d3-313"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-314"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="448d3-314"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-315"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="448d3-315"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-316"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="448d3-316"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-317"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="448d3-317"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-318"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="448d3-318"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-319"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="448d3-319"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-320"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="448d3-320"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-321"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="448d3-321"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-322"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="448d3-322"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-323"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="448d3-323"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-324"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="448d3-324"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-325"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="448d3-325"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-326"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="448d3-326"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-327"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="448d3-327"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-328"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="448d3-328"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="448d3-329">)</span><span class="sxs-lookup"><span data-stu-id="448d3-329">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="448d3-330">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="448d3-330">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-331">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-331">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="448d3-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-333">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="448d3-333">The current statuses of the object.</span></span> <span data-ttu-id="448d3-334">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="448d3-334">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-335">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="448d3-335">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-336">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="448d3-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-338">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="448d3-338">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="448d3-339">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="448d3-339">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="448d3-340">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="448d3-340">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="448d3-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-342">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="448d3-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="448d3-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-344">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="448d3-344">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="448d3-345">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="448d3-345">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="448d3-346">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="448d3-346">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-347">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="448d3-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-349">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="448d3-349">The power management capabilities of the device.</span></span> <span data-ttu-id="448d3-350">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="448d3-350">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="448d3-351">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="448d3-351">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-352">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="448d3-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-354">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="448d3-354">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="448d3-355">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="448d3-355">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="448d3-356">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="448d3-356">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-357">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="448d3-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-359">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="448d3-359">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="448d3-360">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="448d3-360">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="448d3-361">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="448d3-361">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-362">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-364">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="448d3-364">Provides high level status information.</span></span> <span data-ttu-id="448d3-365">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="448d3-365">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="448d3-366">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="448d3-366">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="448d3-367">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="448d3-367">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="448d3-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="448d3-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-369"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="448d3-369"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-370"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="448d3-370"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-371"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="448d3-371"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-372"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="448d3-372"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="448d3-373"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="448d3-373"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="448d3-374">)</span><span class="sxs-lookup"><span data-stu-id="448d3-374">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="448d3-375">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="448d3-375">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-376">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="448d3-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-378">Una cadena que proporciona más información relacionada con el protocolo compatible con el controlador.</span><span class="sxs-lookup"><span data-stu-id="448d3-378">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="448d3-379">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="448d3-379">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-380">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="448d3-380">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-381">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-381">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-383">Protocolo usado por el controlador para tener acceso a los dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="448d3-383">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="448d3-384">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="448d3-384">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>



| <span data-ttu-id="448d3-385">Value</span><span class="sxs-lookup"><span data-stu-id="448d3-385">Value</span></span>                                                                         | <span data-ttu-id="448d3-386">Significado</span><span class="sxs-lookup"><span data-stu-id="448d3-386">Meaning</span></span>             |
|-------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="448d3-387"><dt>26</dt></span><span class="sxs-lookup"><span data-stu-id="448d3-387"><dt>26</dt></span></span> </dl> | <span data-ttu-id="448d3-388">IEEE-488</span><span class="sxs-lookup"><span data-stu-id="448d3-388">IEEE-488</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="448d3-389">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="448d3-389">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-390">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-391">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-392">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="448d3-392">The last requested or desired state for the element.</span></span> <span data-ttu-id="448d3-393">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="448d3-393">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="448d3-394">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="448d3-394">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="448d3-395">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="448d3-395">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="448d3-396">Value</span><span class="sxs-lookup"><span data-stu-id="448d3-396">Value</span></span>                                                                         | <span data-ttu-id="448d3-397">Significado</span><span class="sxs-lookup"><span data-stu-id="448d3-397">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="448d3-398"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="448d3-398"><dt>12</dt></span></span> </dl> | <span data-ttu-id="448d3-399">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="448d3-399">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="448d3-400">**Seguridad**</span><span class="sxs-lookup"><span data-stu-id="448d3-400">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-401">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-403">La seguridad operativa del controlador.</span><span class="sxs-lookup"><span data-stu-id="448d3-403">The operational security for the controller.</span></span> <span data-ttu-id="448d3-404">Esta propiedad se hereda de [**\_ SerialController CIM**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="448d3-404">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>



| <span data-ttu-id="448d3-405">Value</span><span class="sxs-lookup"><span data-stu-id="448d3-405">Value</span></span>                                                                        | <span data-ttu-id="448d3-406">Significado</span><span class="sxs-lookup"><span data-stu-id="448d3-406">Meaning</span></span>         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <span data-ttu-id="448d3-407"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="448d3-407"><dt>3</dt></span></span> </dl> | <span data-ttu-id="448d3-408">None</span><span class="sxs-lookup"><span data-stu-id="448d3-408">None</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="448d3-409">**Estado**</span><span class="sxs-lookup"><span data-stu-id="448d3-409">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-410">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="448d3-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-411">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-412">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="448d3-412">The current status of the object.</span></span> <span data-ttu-id="448d3-413">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="448d3-413">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="448d3-414">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="448d3-414">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-415">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="448d3-415">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="448d3-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-417">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="448d3-417">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="448d3-418">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="448d3-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-419">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="448d3-419">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-420">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-422">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="448d3-422">The current state of the logical device.</span></span> <span data-ttu-id="448d3-423">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="448d3-423">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="448d3-424">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="448d3-424">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-425">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="448d3-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-426">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-427">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="448d3-427">The scoping system's creation class name.</span></span> <span data-ttu-id="448d3-428">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="448d3-428">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-429">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="448d3-429">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-430">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="448d3-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-431">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-432">Identificador único de la máquina virtual de ámbito.</span><span class="sxs-lookup"><span data-stu-id="448d3-432">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="448d3-433">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="448d3-433">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-434">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="448d3-434">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-435">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="448d3-435">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-436">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-437">La última vez que se encendió el controlador.</span><span class="sxs-lookup"><span data-stu-id="448d3-437">The last time the controller was powered on.</span></span> <span data-ttu-id="448d3-438">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="448d3-438">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="448d3-439">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="448d3-439">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-440">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="448d3-440">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-441">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-442">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="448d3-442">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="448d3-443">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="448d3-443">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="448d3-444">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="448d3-444">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-445">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="448d3-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-446">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-447">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="448d3-447">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="448d3-448">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="448d3-448">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="448d3-449">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="448d3-449">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="448d3-450">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="448d3-450">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="448d3-451">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="448d3-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="448d3-452">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="448d3-452">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="448d3-453">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="448d3-453">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="448d3-454">Observaciones</span><span class="sxs-lookup"><span data-stu-id="448d3-454">Remarks</span></span>

<span data-ttu-id="448d3-455">El acceso a la clase **MSVM \_ SerialController** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="448d3-455">Access to the **Msvm\_SerialController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="448d3-456">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="448d3-456">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="448d3-457">Requisitos</span><span class="sxs-lookup"><span data-stu-id="448d3-457">Requirements</span></span>



| <span data-ttu-id="448d3-458">Requisito</span><span class="sxs-lookup"><span data-stu-id="448d3-458">Requirement</span></span> | <span data-ttu-id="448d3-459">Value</span><span class="sxs-lookup"><span data-stu-id="448d3-459">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="448d3-460">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="448d3-460">Minimum supported client</span></span><br/> | <span data-ttu-id="448d3-461">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="448d3-461">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="448d3-462">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="448d3-462">Minimum supported server</span></span><br/> | <span data-ttu-id="448d3-463">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="448d3-463">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="448d3-464">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="448d3-464">Namespace</span></span><br/>                | <span data-ttu-id="448d3-465">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="448d3-465">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="448d3-466">MOF</span><span class="sxs-lookup"><span data-stu-id="448d3-466">MOF</span></span><br/>                      | <dl> <span data-ttu-id="448d3-467"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="448d3-467"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="448d3-468">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="448d3-468">DLL</span></span><br/>                      | <dl> <span data-ttu-id="448d3-469"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="448d3-469"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="448d3-470">Vea también</span><span class="sxs-lookup"><span data-stu-id="448d3-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="448d3-471">**\_SERIALCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="448d3-471">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dt>

[<span data-ttu-id="448d3-472">**\_SERIALCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="448d3-472">**CIM\_SerialController**</span></span>](/windows/desktop/CIMWin32Prov/cim-serialcontroller)
</dt> <dt>

[<span data-ttu-id="448d3-473">Clases de dispositivos serie</span><span class="sxs-lookup"><span data-stu-id="448d3-473">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

