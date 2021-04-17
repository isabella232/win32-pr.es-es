---
description: Representa una controladora IDE.
ms.assetid: DFD4D90E-CA91-42B3-AC88-9E9D26089C36
title: Msvm_IDEController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_IDEController
- Msvm_IDEController.SetPowerState
- Msvm_IDEController.EnableDevice
- Msvm_IDEController.OnlineDevice
- Msvm_IDEController.QuiesceDevice
- Msvm_IDEController.SaveProperties
- Msvm_IDEController.RestoreProperties
- Msvm_IDEController.InstanceID
- Msvm_IDEController.Caption
- Msvm_IDEController.Description
- Msvm_IDEController.ElementName
- Msvm_IDEController.InstallDate
- Msvm_IDEController.Name
- Msvm_IDEController.OperationalStatus
- Msvm_IDEController.StatusDescriptions
- Msvm_IDEController.Status
- Msvm_IDEController.HealthState
- Msvm_IDEController.CommunicationStatus
- Msvm_IDEController.DetailedStatus
- Msvm_IDEController.OperatingStatus
- Msvm_IDEController.PrimaryStatus
- Msvm_IDEController.EnabledState
- Msvm_IDEController.OtherEnabledState
- Msvm_IDEController.RequestedState
- Msvm_IDEController.EnabledDefault
- Msvm_IDEController.TimeOfLastStateChange
- Msvm_IDEController.AvailableRequestedStates
- Msvm_IDEController.TransitioningToState
- Msvm_IDEController.SystemCreationClassName
- Msvm_IDEController.SystemName
- Msvm_IDEController.CreationClassName
- Msvm_IDEController.DeviceID
- Msvm_IDEController.PowerManagementSupported
- Msvm_IDEController.PowerManagementCapabilities
- Msvm_IDEController.Availability
- Msvm_IDEController.StatusInfo
- Msvm_IDEController.LastErrorCode
- Msvm_IDEController.ErrorDescription
- Msvm_IDEController.ErrorCleared
- Msvm_IDEController.OtherIdentifyingInfo
- Msvm_IDEController.PowerOnHours
- Msvm_IDEController.TotalPowerOnHours
- Msvm_IDEController.IdentifyingDescriptions
- Msvm_IDEController.AdditionalAvailability
- Msvm_IDEController.MaxQuiesceTime
- Msvm_IDEController.TimeOfLastReset
- Msvm_IDEController.ProtocolSupported
- Msvm_IDEController.MaxNumberControlled
- Msvm_IDEController.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 25da1bddfa029ca5a6892006283e322d91a328a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686943"
---
# <a name="msvm_idecontroller-class"></a><span data-ttu-id="b8ed3-103">MSVM \_ IDEController (clase)</span><span class="sxs-lookup"><span data-stu-id="b8ed3-103">Msvm\_IDEController class</span></span>

<span data-ttu-id="b8ed3-104">Representa una controladora IDE.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-104">Represents an IDE controller.</span></span> <span data-ttu-id="b8ed3-105">Esta clase puede admitir hasta cuatro unidades conectadas al controlador.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-105">This class can support up to four drives attached to the controller.</span></span> <span data-ttu-id="b8ed3-106">La controladora IDE se ha corregido en la máquina virtual y, por tanto, no tiene un grupo de recursos asociado.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-106">The IDE controller is fixed in the virtual machine and therefore does not have a resource pool associated with it.</span></span>

> [!Note]  
> <span data-ttu-id="b8ed3-107">Esta clase no está disponible para las máquinas virtuales de generación 2.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-107">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="b8ed3-108">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8ed3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8ed3-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_IDEController : CIM_IDEController
{
  string   InstanceID;
  string   Caption;
  string   Description = "Microsoft Virtual IDE Controller";
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
  string   CreationClassName = "Msvm_IDEController";
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
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 37;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription = "IDE";
};
```

## <a name="members"></a><span data-ttu-id="b8ed3-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="b8ed3-110">Members</span></span>

<span data-ttu-id="b8ed3-111">La clase **MSVM \_ IDEController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b8ed3-111">The **Msvm\_IDEController** class has these types of members:</span></span>

-   [<span data-ttu-id="b8ed3-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b8ed3-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b8ed3-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b8ed3-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b8ed3-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b8ed3-114">Methods</span></span>

<span data-ttu-id="b8ed3-115">La clase **MSVM \_ IDEController** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-115">The **Msvm\_IDEController** class has these methods.</span></span>



| <span data-ttu-id="b8ed3-116">Método</span><span class="sxs-lookup"><span data-stu-id="b8ed3-116">Method</span></span>                                                              | <span data-ttu-id="b8ed3-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8ed3-117">Description</span></span>                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="b8ed3-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-118">**EnableDevice**</span></span>                                                    | <span data-ttu-id="b8ed3-119">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b8ed3-120">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-120">**OnlineDevice**</span></span>                                                    | <span data-ttu-id="b8ed3-121">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-121">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b8ed3-122">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-122">**QuiesceDevice**</span></span>                                                   | <span data-ttu-id="b8ed3-123">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-123">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="b8ed3-124">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-124">**RequestStateChange**</span></span>](msvm-idecontroller-requeststatechange.md) | <span data-ttu-id="b8ed3-125">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-125">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="b8ed3-126">**Reset**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-126">**Reset**</span></span>](msvm-idecontroller-reset.md)                           | <span data-ttu-id="b8ed3-127">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-127">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="b8ed3-128">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-128">**RestoreProperties**</span></span>                                               | <span data-ttu-id="b8ed3-129">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b8ed3-130">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-130">**SaveProperties**</span></span>                                                  | <span data-ttu-id="b8ed3-131">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b8ed3-132">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-132">**SetPowerState**</span></span>                                                   | <span data-ttu-id="b8ed3-133">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-133">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b8ed3-134">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b8ed3-134">Properties</span></span>

<span data-ttu-id="b8ed3-135">La clase **MSVM \_ IDEController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-135">The **Msvm\_IDEController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8ed3-136">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-136">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-137">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-137">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-139">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-139">Any additional availability and status of the device.</span></span> <span data-ttu-id="b8ed3-140">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-140">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-141">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-142">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-144">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-144">The primary availability and status of the device.</span></span> <span data-ttu-id="b8ed3-145">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-145">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-146">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-146">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-147">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-147">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-149">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-149">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="b8ed3-150">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual del objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b8ed3-150">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="b8ed3-151">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-151">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="b8ed3-152">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-152">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="b8ed3-153">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-153">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-154">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-157">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-157">A short description of the object.</span></span> <span data-ttu-id="b8ed3-158">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>



| <span data-ttu-id="b8ed3-159">Value</span><span class="sxs-lookup"><span data-stu-id="b8ed3-159">Value</span></span>                                                                                         | <span data-ttu-id="b8ed3-160">Significado</span><span class="sxs-lookup"><span data-stu-id="b8ed3-160">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="b8ed3-161"><dt>"Controladora IDE 0"</dt></span><span class="sxs-lookup"><span data-stu-id="b8ed3-161"><dt>"IDE Controller 0"</dt></span></span> </dl> | <span data-ttu-id="b8ed3-162">La instancia representa el controlador principal.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-162">The instance represents the primary controller.</span></span><br/>   |
| <dl> <span data-ttu-id="b8ed3-163"><dt>"Controladora IDE 1"</dt></span><span class="sxs-lookup"><span data-stu-id="b8ed3-163"><dt>"IDE Controller 1"</dt></span></span> </dl> | <span data-ttu-id="b8ed3-164">La instancia representa el controlador secundario.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-164">The instance represents the secondary controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b8ed3-165">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-165">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-166">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-168">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-168">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="b8ed3-169">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b8ed3-170">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-174">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-174">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b8ed3-175">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-176">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-179">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-179">A description of the object.</span></span> <span data-ttu-id="b8ed3-180">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-182">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-184">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-184">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="b8ed3-185">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b8ed3-186">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-187">**ID**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-187">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-188">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-190">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en "Microsoft:*GUID* del \\ *dispositivo-datos específicos*".</span><span class="sxs-lookup"><span data-stu-id="b8ed3-190">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-191">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-191">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-194">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-194">A display name for the object.</span></span> <span data-ttu-id="b8ed3-195">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-195">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>



| <span data-ttu-id="b8ed3-196">Value</span><span class="sxs-lookup"><span data-stu-id="b8ed3-196">Value</span></span>                                                                                         | <span data-ttu-id="b8ed3-197">Significado</span><span class="sxs-lookup"><span data-stu-id="b8ed3-197">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="b8ed3-198"><dt>"Controladora IDE 0"</dt></span><span class="sxs-lookup"><span data-stu-id="b8ed3-198"><dt>"IDE Controller 0"</dt></span></span> </dl> | <span data-ttu-id="b8ed3-199">La instancia representa el controlador principal.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-199">The instance represents the primary controller.</span></span><br/>   |
| <dl> <span data-ttu-id="b8ed3-200"><dt>"Controladora IDE 1"</dt></span><span class="sxs-lookup"><span data-stu-id="b8ed3-200"><dt>"IDE Controller 1"</dt></span></span> </dl> | <span data-ttu-id="b8ed3-201">La instancia representa el controlador secundario.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-201">The instance represents the secondary controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b8ed3-202">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-202">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-203">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-205">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-205">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="b8ed3-206">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-207">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-207">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-208">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-210">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-210">The enabled and disabled states of an element.</span></span> <span data-ttu-id="b8ed3-211">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-211">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="b8ed3-212">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-212">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-213">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-213">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-214">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-216">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-216">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="b8ed3-217">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-218">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-218">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-221">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-221">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="b8ed3-222">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-222">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-223">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-223">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-224">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-226">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-226">The current health of the element.</span></span> <span data-ttu-id="b8ed3-227">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-227">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="b8ed3-228">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-228">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="b8ed3-229">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-229">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-230">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-230">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-231">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-231">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-233">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="b8ed3-233">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="b8ed3-234">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-235">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-235">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-236">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-236">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-238">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-238">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="b8ed3-239">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-239">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-240">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-240">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-241">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-243">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-243">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-244">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-244">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b8ed3-245">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-245">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-246">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-246">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-247">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-249">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-249">The last error code reported by the logical device.</span></span> <span data-ttu-id="b8ed3-250">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-251">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-251">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-252">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-252">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-254">Número máximo de entidades directamente direccionables admitidas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-254">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="b8ed3-255">Se debe utilizar un valor de 0 si el número es desconocido o ilimitado.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-255">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="b8ed3-256">Protocolo usado por el controlador para tener acceso a los dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-256">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="b8ed3-257">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-257">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-258">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-258">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-259">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-259">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-260">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-261">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-261">This property has been deprecated.</span></span> <span data-ttu-id="b8ed3-262">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-262">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-263">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-263">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-266">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-266">The label by which the object is known.</span></span> <span data-ttu-id="b8ed3-267">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y es igual que la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="b8ed3-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-268">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-268">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-269">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-271">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="b8ed3-271">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="b8ed3-272">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-272">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b8ed3-273">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-274">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-274">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-275">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-275">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-277">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-277">The current statuses of the object.</span></span> <span data-ttu-id="b8ed3-278">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-278">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-279">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-279">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-280">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-282">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-282">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="b8ed3-283">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-283">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="b8ed3-284">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-284">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-285">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-285">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-286">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-286">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-288">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-288">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="b8ed3-289">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-289">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-290">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-290">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-291">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-291">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-293">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-293">The power management capabilities of the device.</span></span> <span data-ttu-id="b8ed3-294">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-294">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-295">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-295">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-296">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-298">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-298">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="b8ed3-299">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-299">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-300">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-300">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-301">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-303">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-303">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="b8ed3-304">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-305">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-305">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-306">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-308">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-308">Provides high level status information.</span></span> <span data-ttu-id="b8ed3-309">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-309">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="b8ed3-310">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-310">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b8ed3-311">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-312">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-312">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-313">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-315">Una cadena que proporciona más información relacionada con el protocolo compatible con el controlador.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-315">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="b8ed3-316">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-316">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-317">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-317">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-318">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-318">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-320">Protocolo usado por el controlador para tener acceso a los dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-320">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="b8ed3-321">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-321">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>



| <span data-ttu-id="b8ed3-322">Value</span><span class="sxs-lookup"><span data-stu-id="b8ed3-322">Value</span></span>                                                                         | <span data-ttu-id="b8ed3-323">Significado</span><span class="sxs-lookup"><span data-stu-id="b8ed3-323">Meaning</span></span>        |
|-------------------------------------------------------------------------------|----------------|
| <dl> <span data-ttu-id="b8ed3-324"><dt>37</dt></span><span class="sxs-lookup"><span data-stu-id="b8ed3-324"><dt>37</dt></span></span> </dl> | <span data-ttu-id="b8ed3-325">IDE</span><span class="sxs-lookup"><span data-stu-id="b8ed3-325">IDE</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b8ed3-326">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-326">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-327">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-329">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-329">The last requested or desired state for the element.</span></span> <span data-ttu-id="b8ed3-330">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-330">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="b8ed3-331">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-331">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="b8ed3-332">Una instancia concreta de un elemento lógico habilitado podría no ser compatible con **RequestedStateChange**.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-332">A particular instance of an enabled logical element might not support **RequestedStateChange**.</span></span> <span data-ttu-id="b8ed3-333">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-333">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="b8ed3-334">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-335">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-335">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-336">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-338">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-338">The current status of the object.</span></span> <span data-ttu-id="b8ed3-339">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-340">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-340">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-341">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-343">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="b8ed3-343">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="b8ed3-344">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-344">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-345">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-345">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-346">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-348">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-348">The current state of the logical device.</span></span> <span data-ttu-id="b8ed3-349">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-350">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-350">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-351">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-352">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-353">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-353">The scoping system's creation class name.</span></span> <span data-ttu-id="b8ed3-354">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-354">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-355">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-355">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-356">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-358">Identificador único de la máquina virtual de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-358">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="b8ed3-359">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-359">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-360">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-360">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-361">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-361">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-363">La última vez que se encendió la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-363">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="b8ed3-364">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-364">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-365">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-365">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-366">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-366">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-368">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-368">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="b8ed3-369">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-369">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-370">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-370">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-371">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-371">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-373">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-373">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="b8ed3-374">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-374">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed3-375">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-375">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ed3-376">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8ed3-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8ed3-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8ed3-378">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-378">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="b8ed3-379">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8ed3-380">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8ed3-380">Remarks</span></span>

<span data-ttu-id="b8ed3-381">El acceso a la clase **MSVM \_ IDEController** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="b8ed3-381">Access to the **Msvm\_IDEController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b8ed3-382">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b8ed3-382">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8ed3-383">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8ed3-383">Requirements</span></span>



| <span data-ttu-id="b8ed3-384">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8ed3-384">Requirement</span></span> | <span data-ttu-id="b8ed3-385">Value</span><span class="sxs-lookup"><span data-stu-id="b8ed3-385">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ed3-386">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8ed3-386">Minimum supported client</span></span><br/> | <span data-ttu-id="b8ed3-387">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8ed3-387">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b8ed3-388">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8ed3-388">Minimum supported server</span></span><br/> | <span data-ttu-id="b8ed3-389">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8ed3-389">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8ed3-390">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8ed3-390">Namespace</span></span><br/>                | <span data-ttu-id="b8ed3-391">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b8ed3-391">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b8ed3-392">MOF</span><span class="sxs-lookup"><span data-stu-id="b8ed3-392">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8ed3-393"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8ed3-393"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8ed3-394">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8ed3-394">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8ed3-395"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b8ed3-395"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b8ed3-396">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8ed3-396">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8ed3-397">**\_IDECONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="b8ed3-397">**CIM\_IDEController**</span></span>](cim-idecontroller.md)
</dt> <dt>

<span data-ttu-id="b8ed3-398">[**\_IDECONTROLLER CIM**](/previous-versions//cc136863(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8ed3-398">[**CIM\_IDEController**](/previous-versions//cc136863(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b8ed3-399">Clases de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="b8ed3-399">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

