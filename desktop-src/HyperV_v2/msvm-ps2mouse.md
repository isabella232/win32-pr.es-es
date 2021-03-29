---
description: Representa un dispositivo de mouse PS2.
ms.assetid: 5e02ec15-95e6-4d82-833e-a48ca117a890
title: Msvm_Ps2Mouse (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse
- Msvm_Ps2Mouse.SetPowerState
- Msvm_Ps2Mouse.EnableDevice
- Msvm_Ps2Mouse.OnlineDevice
- Msvm_Ps2Mouse.QuiesceDevice
- Msvm_Ps2Mouse.SaveProperties
- Msvm_Ps2Mouse.RestoreProperties
- Msvm_Ps2Mouse.InstanceID
- Msvm_Ps2Mouse.Caption
- Msvm_Ps2Mouse.Description
- Msvm_Ps2Mouse.ElementName
- Msvm_Ps2Mouse.InstallDate
- Msvm_Ps2Mouse.Name
- Msvm_Ps2Mouse.OperationalStatus
- Msvm_Ps2Mouse.StatusDescriptions
- Msvm_Ps2Mouse.Status
- Msvm_Ps2Mouse.HealthState
- Msvm_Ps2Mouse.CommunicationStatus
- Msvm_Ps2Mouse.DetailedStatus
- Msvm_Ps2Mouse.OperatingStatus
- Msvm_Ps2Mouse.PrimaryStatus
- Msvm_Ps2Mouse.EnabledState
- Msvm_Ps2Mouse.OtherEnabledState
- Msvm_Ps2Mouse.RequestedState
- Msvm_Ps2Mouse.EnabledDefault
- Msvm_Ps2Mouse.TimeOfLastStateChange
- Msvm_Ps2Mouse.AvailableRequestedStates
- Msvm_Ps2Mouse.TransitioningToState
- Msvm_Ps2Mouse.SystemCreationClassName
- Msvm_Ps2Mouse.SystemName
- Msvm_Ps2Mouse.CreationClassName
- Msvm_Ps2Mouse.DeviceID
- Msvm_Ps2Mouse.PowerManagementSupported
- Msvm_Ps2Mouse.PowerManagementCapabilities
- Msvm_Ps2Mouse.Availability
- Msvm_Ps2Mouse.StatusInfo
- Msvm_Ps2Mouse.LastErrorCode
- Msvm_Ps2Mouse.ErrorDescription
- Msvm_Ps2Mouse.ErrorCleared
- Msvm_Ps2Mouse.OtherIdentifyingInfo
- Msvm_Ps2Mouse.PowerOnHours
- Msvm_Ps2Mouse.TotalPowerOnHours
- Msvm_Ps2Mouse.IdentifyingDescriptions
- Msvm_Ps2Mouse.AdditionalAvailability
- Msvm_Ps2Mouse.MaxQuiesceTime
- Msvm_Ps2Mouse.IsLocked
- Msvm_Ps2Mouse.PointingType
- Msvm_Ps2Mouse.NumberOfButtons
- Msvm_Ps2Mouse.Handedness
- Msvm_Ps2Mouse.Resolution
- Msvm_Ps2Mouse.AbsoluteCoordinates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d25d168b85a79c5212afc719ce6ec83ca9780395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360754"
---
# <a name="msvm_ps2mouse-class"></a><span data-ttu-id="85ec9-103">MSVM \_ Ps2Mouse (clase)</span><span class="sxs-lookup"><span data-stu-id="85ec9-103">Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="85ec9-104">Representa un dispositivo de mouse PS2.</span><span class="sxs-lookup"><span data-stu-id="85ec9-104">Represents a PS2 mouse device.</span></span> <span data-ttu-id="85ec9-105">Las instancias de esta clase son dispositivos lógicos que siempre están presentes en una máquina virtual y, por tanto, no se asignan a través de un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="85ec9-105">Instances of this class are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="85ec9-106">Siempre hay una instancia en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="85ec9-106">One instance is always present in a virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="85ec9-107">Esta clase no está disponible para las máquinas virtuales de generación 2.</span><span class="sxs-lookup"><span data-stu-id="85ec9-107">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="85ec9-108">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="85ec9-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="85ec9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85ec9-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Ps2Mouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Emulated Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status;
  uint16   HealthState = 5;
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
  string   CreationClassName = "Msvm_PS2Mouse";
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
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = False;
};
```

## <a name="members"></a><span data-ttu-id="85ec9-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="85ec9-110">Members</span></span>

<span data-ttu-id="85ec9-111">La clase **MSVM \_ Ps2Mouse** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="85ec9-111">The **Msvm\_Ps2Mouse** class has these types of members:</span></span>

-   [<span data-ttu-id="85ec9-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="85ec9-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="85ec9-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85ec9-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="85ec9-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="85ec9-114">Methods</span></span>

<span data-ttu-id="85ec9-115">La clase **MSVM \_ Ps2Mouse** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="85ec9-115">The **Msvm\_Ps2Mouse** class has these methods.</span></span>



| <span data-ttu-id="85ec9-116">Método</span><span class="sxs-lookup"><span data-stu-id="85ec9-116">Method</span></span>                                                           | <span data-ttu-id="85ec9-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="85ec9-117">Description</span></span>                                                                                           |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85ec9-118">**ClickButton**</span><span class="sxs-lookup"><span data-stu-id="85ec9-118">**ClickButton**</span></span>](clickbutton-msvm-ps2mouse.md)                 | <span data-ttu-id="85ec9-119">Simula un clic de botón, una secuencia descendente, en el botón de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="85ec9-119">Simulates a button click, a down-up sequence, on the specified device button.</span></span><br/>              |
| <span data-ttu-id="85ec9-120">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="85ec9-120">**EnableDevice**</span></span>                                                 | <span data-ttu-id="85ec9-121">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="85ec9-121">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="85ec9-122">**GetButtonState**</span><span class="sxs-lookup"><span data-stu-id="85ec9-122">**GetButtonState**</span></span>](getbuttonstate-msvm-ps2mouse.md)           | <span data-ttu-id="85ec9-123">Recupera el estado actual del botón del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="85ec9-123">Retrieves the current state of the specified device button.</span></span><br/>                                |
| <span data-ttu-id="85ec9-124">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="85ec9-124">**OnlineDevice**</span></span>                                                 | <span data-ttu-id="85ec9-125">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="85ec9-125">This method is not supported.</span></span><br/>                                                              |
| <span data-ttu-id="85ec9-126">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="85ec9-126">**QuiesceDevice**</span></span>                                                | <span data-ttu-id="85ec9-127">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="85ec9-127">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="85ec9-128">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="85ec9-128">**RequestStateChange**</span></span>](msvm-ps2mouse-requeststatechange.md)   | <span data-ttu-id="85ec9-129">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="85ec9-129">Requests a state change.</span></span><br/>                                                                   |
| [<span data-ttu-id="85ec9-130">**Reset**</span><span class="sxs-lookup"><span data-stu-id="85ec9-130">**Reset**</span></span>](msvm-ps2mouse-reset.md)                             | <span data-ttu-id="85ec9-131">Restablece el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85ec9-131">Resets the device.</span></span><br/>                                                                         |
| <span data-ttu-id="85ec9-132">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="85ec9-132">**RestoreProperties**</span></span>                                            | <span data-ttu-id="85ec9-133">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="85ec9-133">This method is not supported.</span></span><br/>                                                              |
| <span data-ttu-id="85ec9-134">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="85ec9-134">**SaveProperties**</span></span>                                               | <span data-ttu-id="85ec9-135">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="85ec9-135">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="85ec9-136">**SetButtonState**</span><span class="sxs-lookup"><span data-stu-id="85ec9-136">**SetButtonState**</span></span>](setbuttonstate-msvm-ps2mouse.md)           | <span data-ttu-id="85ec9-137">Establece el estado actual del botón del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="85ec9-137">Sets the current state of the specified device button.</span></span><br/>                                     |
| <span data-ttu-id="85ec9-138">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="85ec9-138">**SetPowerState**</span></span>                                                | <span data-ttu-id="85ec9-139">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="85ec9-139">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="85ec9-140">**SetRelativePosition**</span><span class="sxs-lookup"><span data-stu-id="85ec9-140">**SetRelativePosition**</span></span>](setrelativeposition-msvm-ps2mouse.md) | <span data-ttu-id="85ec9-141">Desplaza la posición del puntero del mouse según las diferencias horizontales y verticales especificadas.</span><span class="sxs-lookup"><span data-stu-id="85ec9-141">Offsets the position of the mouse pointer by the specified horizontal and vertical deltas.</span></span><br/> |
| [<span data-ttu-id="85ec9-142">**SetScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="85ec9-142">**SetScrollPosition**</span></span>](setscrollposition-msvm-ps2mouse.md)     | <span data-ttu-id="85ec9-143">Ajusta la coordenada z del control de rueda del dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="85ec9-143">Adjusts the z-coordinate of the wheel control of the pointing device.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="85ec9-144">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85ec9-144">Properties</span></span>

<span data-ttu-id="85ec9-145">La clase **MSVM \_ Ps2Mouse** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="85ec9-145">The **Msvm\_Ps2Mouse** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85ec9-146">**AbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="85ec9-146">**AbsoluteCoordinates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-147">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85ec9-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-149">Indica si el dispositivo funciona en coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="85ec9-149">Indicates whether the device operates on absolute coordinates.</span></span> <span data-ttu-id="85ec9-150">Si no se establece, las coordenadas del dispositivo son relativas.</span><span class="sxs-lookup"><span data-stu-id="85ec9-150">If not set, the device's coordinates are relative.</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-151">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="85ec9-151">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-152">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-154">Cualquier disponibilidad adicional y estado del dispositivo, más allá de lo especificado en la propiedad **Availability** .</span><span class="sxs-lookup"><span data-stu-id="85ec9-154">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="85ec9-155">La propiedad **Availability** denota el estado principal y la disponibilidad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85ec9-155">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="85ec9-156">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="85ec9-156">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="85ec9-157">Value</span><span class="sxs-lookup"><span data-stu-id="85ec9-157">Value</span></span>                                                                        | <span data-ttu-id="85ec9-158">Significado</span><span class="sxs-lookup"><span data-stu-id="85ec9-158">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="85ec9-159"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="85ec9-159"><dt>6</dt></span></span> </dl> | <span data-ttu-id="85ec9-160">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="85ec9-160">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="85ec9-161">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="85ec9-161">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-162">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-164">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85ec9-164">The primary availability and status of the device.</span></span> <span data-ttu-id="85ec9-165">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="85ec9-165">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="85ec9-166">Value</span><span class="sxs-lookup"><span data-stu-id="85ec9-166">Value</span></span>                                                                        | <span data-ttu-id="85ec9-167">Significado</span><span class="sxs-lookup"><span data-stu-id="85ec9-167">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="85ec9-168"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="85ec9-168"><dt>6</dt></span></span> </dl> | <span data-ttu-id="85ec9-169">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="85ec9-169">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="85ec9-170">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="85ec9-170">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-171">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-171">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-173">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="85ec9-173">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="85ec9-174">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="85ec9-174">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-175">**Caption**</span><span class="sxs-lookup"><span data-stu-id="85ec9-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ec9-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-178">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="85ec9-178">A short description of the object.</span></span> <span data-ttu-id="85ec9-179">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="85ec9-179">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-180">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="85ec9-180">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-181">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-183">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="85ec9-183">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="85ec9-184">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="85ec9-184">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="85ec9-185">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="85ec9-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="85ec9-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="85ec9-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="85ec9-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-188"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="85ec9-188"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-189"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="85ec9-189"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-190"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="85ec9-190"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-191"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="85ec9-191"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-192"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="85ec9-192"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="85ec9-193">)</span><span class="sxs-lookup"><span data-stu-id="85ec9-193">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="85ec9-194">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="85ec9-194">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ec9-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-197">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="85ec9-197">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-198">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="85ec9-198">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="85ec9-199">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="85ec9-199">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="85ec9-200">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="85ec9-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-201">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85ec9-201">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ec9-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-204">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="85ec9-204">A description of the object.</span></span> <span data-ttu-id="85ec9-205">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="85ec9-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-206">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="85ec9-206">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-207">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-209">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="85ec9-209">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="85ec9-210">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="85ec9-210">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="85ec9-211">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="85ec9-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="85ec9-212"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="85ec9-212"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-213"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="85ec9-213"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-214"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="85ec9-214"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-215"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="85ec9-215"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-216"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="85ec9-216"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-217"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="85ec9-217"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="85ec9-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-219"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="85ec9-219"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="85ec9-220">)</span><span class="sxs-lookup"><span data-stu-id="85ec9-220">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="85ec9-221">**ID**</span><span class="sxs-lookup"><span data-stu-id="85ec9-221">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ec9-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-224">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="85ec9-224">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-225">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="85ec9-225">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="85ec9-226">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="85ec9-226">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-227">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="85ec9-227">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-228">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ec9-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-230">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="85ec9-230">A display name for the object.</span></span> <span data-ttu-id="85ec9-231">Esta propiedad permite a cada instancia definir un nombre para mostrar además de las propiedades de clave, los datos de identidad y la información de descripción.</span><span class="sxs-lookup"><span data-stu-id="85ec9-231">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="85ec9-232">La propiedad [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) de la clase del **\_ ManagedSystemElement de CIM** también se define como un nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="85ec9-232">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="85ec9-233">Sin embargo, a menudo se considera una clave.</span><span class="sxs-lookup"><span data-stu-id="85ec9-233">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="85ec9-234">No es razonable que la misma propiedad pueda transmitir tanto la identidad como un nombre para mostrar, sin incoherencias.</span><span class="sxs-lookup"><span data-stu-id="85ec9-234">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="85ec9-235">Donde el [**nombre**](msvm-keyboard.md) existe y no es una clave (por ejemplo, para las instancias del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), la misma información puede estar presente en las propiedades **nombre** y **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="85ec9-235">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="85ec9-236">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "Mouse".</span><span class="sxs-lookup"><span data-stu-id="85ec9-236">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Mouse".</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-237">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="85ec9-237">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-238">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-240">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="85ec9-240">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="85ec9-241">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85ec9-241">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-242">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="85ec9-242">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-243">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-243">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-245">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="85ec9-245">The enabled and disabled states of an element.</span></span> <span data-ttu-id="85ec9-246">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85ec9-246">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-247">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="85ec9-247">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-248">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85ec9-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-250">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="85ec9-250">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="85ec9-251">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ec9-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-252">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="85ec9-252">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-253">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ec9-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-255">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="85ec9-255">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="85ec9-256">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ec9-256">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-257">**Situación**</span><span class="sxs-lookup"><span data-stu-id="85ec9-257">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-258">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-260">La configuración del dispositivo señalador para la operación a la derecha o a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="85ec9-260">The configuration of the pointing device for right-hand or left-hand operation.</span></span> <span data-ttu-id="85ec9-261">Esta propiedad se hereda de [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="85ec9-261">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="85ec9-262">Value</span><span class="sxs-lookup"><span data-stu-id="85ec9-262">Value</span></span>                                                                        | <span data-ttu-id="85ec9-263">Significado</span><span class="sxs-lookup"><span data-stu-id="85ec9-263">Meaning</span></span>                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="85ec9-264"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="85ec9-264"><dt>0</dt></span></span> </dl> | <span data-ttu-id="85ec9-265">Unknown</span><span class="sxs-lookup"><span data-stu-id="85ec9-265">Unknown</span></span><br/>                 |
| <dl> <span data-ttu-id="85ec9-266"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="85ec9-266"><dt>1</dt></span></span> </dl> | <span data-ttu-id="85ec9-267">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="85ec9-267">Not applicable.</span></span><br/>         |
| <dl> <span data-ttu-id="85ec9-268"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="85ec9-268"><dt>2</dt></span></span> </dl> | <span data-ttu-id="85ec9-269">Operación a la derecha.</span><span class="sxs-lookup"><span data-stu-id="85ec9-269">Right handed operation.</span></span><br/> |
| <dl> <span data-ttu-id="85ec9-270"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="85ec9-270"><dt>3</dt></span></span> </dl> | <span data-ttu-id="85ec9-271">Operación de mano izquierda.</span><span class="sxs-lookup"><span data-stu-id="85ec9-271">Left handed operation.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="85ec9-272">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="85ec9-272">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-273">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-273">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-275">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="85ec9-275">The current health of the element.</span></span> <span data-ttu-id="85ec9-276">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="85ec9-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK)</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-277">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="85ec9-277">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-278">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="85ec9-278">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-280">Matriz de cadenas de formato libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz [**OtherIdentifyingInfo**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="85ec9-280">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="85ec9-281">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="85ec9-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-282">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="85ec9-282">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-283">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85ec9-283">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-285">Fecha y hora en que se creó la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="85ec9-285">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="85ec9-286">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="85ec9-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-287">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="85ec9-287">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-288">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ec9-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-290">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="85ec9-290">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-291">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="85ec9-291">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="85ec9-292">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="85ec9-292">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-293">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="85ec9-293">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-294">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85ec9-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-296">Indica si el dispositivo está bloqueado, lo que impide la entrada o salida del usuario.</span><span class="sxs-lookup"><span data-stu-id="85ec9-296">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="85ec9-297">Esta propiedad se hereda de [**\_ UserDevice CIM**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="85ec9-297">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-298">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="85ec9-298">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-299">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85ec9-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-301">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="85ec9-301">The last error code reported by the logical device.</span></span> <span data-ttu-id="85ec9-302">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ec9-302">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-303">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="85ec9-303">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-304">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="85ec9-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-306">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="85ec9-306">This property has been deprecated.</span></span> <span data-ttu-id="85ec9-307">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="85ec9-307">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-308">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="85ec9-308">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-309">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ec9-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-311">Calificadores: **MaxLen** (1024)</span><span class="sxs-lookup"><span data-stu-id="85ec9-311">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-312">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="85ec9-312">The label by which the object is known.</span></span> <span data-ttu-id="85ec9-313">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="85ec9-313">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="85ec9-314">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="85ec9-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-315">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="85ec9-315">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-316">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="85ec9-316">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-318">Número de botones del dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="85ec9-318">The number of buttons on the pointing device.</span></span> <span data-ttu-id="85ec9-319">Esta propiedad se hereda de [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="85ec9-319">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="85ec9-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-321">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-323">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="85ec9-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="85ec9-324">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="85ec9-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="85ec9-325">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="85ec9-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="85ec9-326"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="85ec9-326"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-327"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="85ec9-327"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-328"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="85ec9-328"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-329"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="85ec9-329"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-330"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="85ec9-330"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-331"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="85ec9-331"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-332"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="85ec9-332"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-333"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="85ec9-333"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-334"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="85ec9-334"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-335"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="85ec9-335"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-336"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="85ec9-336"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-337"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="85ec9-337"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-338"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="85ec9-338"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-339"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="85ec9-339"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-340"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="85ec9-340"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-341"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="85ec9-341"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-342"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="85ec9-342"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-343"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="85ec9-343"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-344"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="85ec9-344"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="85ec9-345">)</span><span class="sxs-lookup"><span data-stu-id="85ec9-345">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="85ec9-346">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="85ec9-346">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-347">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-349">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="85ec9-349">The current status of the element.</span></span> <span data-ttu-id="85ec9-350">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 2 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="85ec9-350">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-351">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="85ec9-351">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ec9-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-354">Estado habilitado o deshabilitado del elemento cuando la propiedad [**EnabledState**](msvm-keyboard.md) está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="85ec9-354">The enabled or disabled state of the element when the [**EnabledState**](msvm-keyboard.md) property is set to 1 (Other).</span></span> <span data-ttu-id="85ec9-355">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="85ec9-355">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="85ec9-356">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85ec9-356">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-357">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="85ec9-357">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-358">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="85ec9-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-360">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="85ec9-360">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="85ec9-361">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="85ec9-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-362">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="85ec9-362">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-363">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-363">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-364">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-365">Tipo del dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="85ec9-365">The type of the pointing device.</span></span> <span data-ttu-id="85ec9-366">Esta propiedad se hereda de [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="85ec9-366">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="85ec9-367">Value</span><span class="sxs-lookup"><span data-stu-id="85ec9-367">Value</span></span>                                                                        | <span data-ttu-id="85ec9-368">Significado</span><span class="sxs-lookup"><span data-stu-id="85ec9-368">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="85ec9-369"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="85ec9-369"><dt>3</dt></span></span> </dl> | <span data-ttu-id="85ec9-370">Mouse</span><span class="sxs-lookup"><span data-stu-id="85ec9-370">Mouse</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="85ec9-371">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="85ec9-371">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-372">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-372">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-373">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-374">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85ec9-374">The power management capabilities of the device.</span></span> <span data-ttu-id="85ec9-375">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ec9-375">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-376">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="85ec9-376">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-377">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85ec9-377">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-378">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-379">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="85ec9-379">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="85ec9-380">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ec9-380">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-381">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="85ec9-381">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-382">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="85ec9-382">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-384">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="85ec9-384">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="85ec9-385">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ec9-385">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-386">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="85ec9-386">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-387">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-389">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="85ec9-389">Provides high level status information.</span></span> <span data-ttu-id="85ec9-390">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="85ec9-390">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="85ec9-391">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="85ec9-391">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="85ec9-392">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="85ec9-392">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="85ec9-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="85ec9-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-394"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="85ec9-394"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-395"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="85ec9-395"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-396"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="85ec9-396"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-397"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="85ec9-397"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-398"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="85ec9-398"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="85ec9-399">)</span><span class="sxs-lookup"><span data-stu-id="85ec9-399">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="85ec9-400">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="85ec9-400">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-401">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-403">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="85ec9-403">The last requested or desired state for the element.</span></span> <span data-ttu-id="85ec9-404">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85ec9-404">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="85ec9-405">Value</span><span class="sxs-lookup"><span data-stu-id="85ec9-405">Value</span></span>                                                                         | <span data-ttu-id="85ec9-406">Significado</span><span class="sxs-lookup"><span data-stu-id="85ec9-406">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="85ec9-407"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="85ec9-407"><dt>12</dt></span></span> </dl> | <span data-ttu-id="85ec9-408">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="85ec9-408">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="85ec9-409">**Resolución**</span><span class="sxs-lookup"><span data-stu-id="85ec9-409">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-410">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85ec9-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-411">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-412">La resolución de seguimiento del dispositivo señalador, en recuentos por pulgada.</span><span class="sxs-lookup"><span data-stu-id="85ec9-412">The tracking resolution of the pointing device, in counts per inch.</span></span> <span data-ttu-id="85ec9-413">Esta propiedad se hereda de [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="85ec9-413">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-414">**Estado**</span><span class="sxs-lookup"><span data-stu-id="85ec9-414">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-415">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ec9-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-417">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="85ec9-417">The current status of the object.</span></span> <span data-ttu-id="85ec9-418">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ec9-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-419">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="85ec9-419">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-420">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="85ec9-420">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-422">Cadenas que describen los distintos valores de la matriz [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="85ec9-422">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="85ec9-423">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) y siempre está establecida en "OK".</span><span class="sxs-lookup"><span data-stu-id="85ec9-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-424">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="85ec9-424">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-425">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-425">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-426">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-427">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="85ec9-427">The current state of the logical device.</span></span> <span data-ttu-id="85ec9-428">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ec9-428">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-429">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="85ec9-429">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-430">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ec9-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-431">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-432">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="85ec9-432">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-433">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="85ec9-433">The scoping system's creation class name.</span></span> <span data-ttu-id="85ec9-434">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="85ec9-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-435">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="85ec9-435">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-436">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ec9-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-437">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-438">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="85ec9-438">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-439">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="85ec9-439">The scoping system's name.</span></span> <span data-ttu-id="85ec9-440">Este valor corresponde al valor de la propiedad [**Name**](msvm-computersystem.md) de la clase **MSVM \_ ComputerSystem** para el ámbito de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="85ec9-440">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="85ec9-441">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="85ec9-441">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-442">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="85ec9-442">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-443">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85ec9-443">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-444">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-445">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="85ec9-445">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="85ec9-446">Si el estado del elemento no ha cambiado y se rellena esta propiedad, debe establecerse en un valor de intervalo 0.</span><span class="sxs-lookup"><span data-stu-id="85ec9-446">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="85ec9-447">Si se solicitó un cambio de estado, pero se rechazó o no se procesó todavía, la propiedad no se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="85ec9-447">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="85ec9-448">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85ec9-448">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-449">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="85ec9-449">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-450">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="85ec9-450">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-451">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-452">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85ec9-452">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="85ec9-453">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ec9-453">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ec9-454">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="85ec9-454">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ec9-455">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ec9-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ec9-456">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ec9-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ec9-457">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="85ec9-457">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="85ec9-458">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="85ec9-458">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85ec9-459">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85ec9-459">Remarks</span></span>

<span data-ttu-id="85ec9-460">El acceso a la clase **MSVM \_ Ps2Mouse** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="85ec9-460">Access to the **Msvm\_Ps2Mouse** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="85ec9-461">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="85ec9-461">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="85ec9-462">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85ec9-462">Requirements</span></span>



| <span data-ttu-id="85ec9-463">Requisito</span><span class="sxs-lookup"><span data-stu-id="85ec9-463">Requirement</span></span> | <span data-ttu-id="85ec9-464">Value</span><span class="sxs-lookup"><span data-stu-id="85ec9-464">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85ec9-465">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85ec9-465">Minimum supported client</span></span><br/> | <span data-ttu-id="85ec9-466">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="85ec9-466">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="85ec9-467">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85ec9-467">Minimum supported server</span></span><br/> | <span data-ttu-id="85ec9-468">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="85ec9-468">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="85ec9-469">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="85ec9-469">Namespace</span></span><br/>                | <span data-ttu-id="85ec9-470">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="85ec9-470">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="85ec9-471">MOF</span><span class="sxs-lookup"><span data-stu-id="85ec9-471">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85ec9-472"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85ec9-472"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="85ec9-473">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85ec9-473">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85ec9-474"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="85ec9-474"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="85ec9-475">Vea también</span><span class="sxs-lookup"><span data-stu-id="85ec9-475">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ec9-476">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="85ec9-476">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="85ec9-477">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="85ec9-477">**CIM\_PointingDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[<span data-ttu-id="85ec9-478">Clases de entrada</span><span class="sxs-lookup"><span data-stu-id="85ec9-478">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

