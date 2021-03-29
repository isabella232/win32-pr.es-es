---
description: Representa un dispositivo de mouse sintético.
ms.assetid: c04b7aa1-44fe-41f5-943f-ff49ce64be96
title: Msvm_SyntheticMouse (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse
- Msvm_SyntheticMouse.SetPowerState
- Msvm_SyntheticMouse.EnableDevice
- Msvm_SyntheticMouse.OnlineDevice
- Msvm_SyntheticMouse.QuiesceDevice
- Msvm_SyntheticMouse.SaveProperties
- Msvm_SyntheticMouse.RestoreProperties
- Msvm_SyntheticMouse.InstanceID
- Msvm_SyntheticMouse.Caption
- Msvm_SyntheticMouse.Description
- Msvm_SyntheticMouse.ElementName
- Msvm_SyntheticMouse.InstallDate
- Msvm_SyntheticMouse.Name
- Msvm_SyntheticMouse.OperationalStatus
- Msvm_SyntheticMouse.StatusDescriptions
- Msvm_SyntheticMouse.Status
- Msvm_SyntheticMouse.HealthState
- Msvm_SyntheticMouse.CommunicationStatus
- Msvm_SyntheticMouse.DetailedStatus
- Msvm_SyntheticMouse.OperatingStatus
- Msvm_SyntheticMouse.PrimaryStatus
- Msvm_SyntheticMouse.EnabledState
- Msvm_SyntheticMouse.OtherEnabledState
- Msvm_SyntheticMouse.RequestedState
- Msvm_SyntheticMouse.EnabledDefault
- Msvm_SyntheticMouse.TimeOfLastStateChange
- Msvm_SyntheticMouse.AvailableRequestedStates
- Msvm_SyntheticMouse.TransitioningToState
- Msvm_SyntheticMouse.SystemCreationClassName
- Msvm_SyntheticMouse.SystemName
- Msvm_SyntheticMouse.CreationClassName
- Msvm_SyntheticMouse.DeviceID
- Msvm_SyntheticMouse.PowerManagementSupported
- Msvm_SyntheticMouse.PowerManagementCapabilities
- Msvm_SyntheticMouse.Availability
- Msvm_SyntheticMouse.StatusInfo
- Msvm_SyntheticMouse.LastErrorCode
- Msvm_SyntheticMouse.ErrorDescription
- Msvm_SyntheticMouse.ErrorCleared
- Msvm_SyntheticMouse.OtherIdentifyingInfo
- Msvm_SyntheticMouse.PowerOnHours
- Msvm_SyntheticMouse.TotalPowerOnHours
- Msvm_SyntheticMouse.IdentifyingDescriptions
- Msvm_SyntheticMouse.AdditionalAvailability
- Msvm_SyntheticMouse.MaxQuiesceTime
- Msvm_SyntheticMouse.IsLocked
- Msvm_SyntheticMouse.PointingType
- Msvm_SyntheticMouse.NumberOfButtons
- Msvm_SyntheticMouse.Handedness
- Msvm_SyntheticMouse.Resolution
- Msvm_SyntheticMouse.AbsoluteCoordinates
- Msvm_SyntheticMouse.HorizontalPosition
- Msvm_SyntheticMouse.VerticalPosition
- Msvm_SyntheticMouse.ScrollPosition
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c5be44637c91ebd57867c5062eba6f9e57ee543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808797"
---
# <a name="msvm_syntheticmouse-class"></a><span data-ttu-id="b34f4-103">MSVM \_ SyntheticMouse (clase)</span><span class="sxs-lookup"><span data-stu-id="b34f4-103">Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="b34f4-104">Representa un dispositivo de mouse sintético.</span><span class="sxs-lookup"><span data-stu-id="b34f4-104">Represents a synthetic mouse device.</span></span>

<span data-ttu-id="b34f4-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b34f4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b34f4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b34f4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticMouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Synthetic Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = {
                "OK"
              };
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
  string   CreationClassName = "Msvm_SyntheticMouse";
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
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = True;
  sint32   HorizontalPosition;
  sint32   VerticalPosition;
  sint32   ScrollPosition;
};
```

## <a name="members"></a><span data-ttu-id="b34f4-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b34f4-107">Members</span></span>

<span data-ttu-id="b34f4-108">La clase **MSVM \_ SyntheticMouse** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b34f4-108">The **Msvm\_SyntheticMouse** class has these types of members:</span></span>

-   [<span data-ttu-id="b34f4-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="b34f4-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="b34f4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b34f4-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b34f4-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b34f4-111">Methods</span></span>

<span data-ttu-id="b34f4-112">La clase **MSVM \_ SyntheticMouse** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b34f4-112">The **Msvm\_SyntheticMouse** class has these methods.</span></span>



| <span data-ttu-id="b34f4-113">Método</span><span class="sxs-lookup"><span data-stu-id="b34f4-113">Method</span></span>                                                                 | <span data-ttu-id="b34f4-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b34f4-114">Description</span></span>                                                                   |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="b34f4-115">**ClickButton**</span><span class="sxs-lookup"><span data-stu-id="b34f4-115">**ClickButton**</span></span>](clickbutton-msvm-syntheticmouse.md)                 | <span data-ttu-id="b34f4-116">Simula un clic de botón del botón del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b34f4-116">Simulates a button click of the specified device button.</span></span><br/>           |
| <span data-ttu-id="b34f4-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="b34f4-117">**EnableDevice**</span></span>                                                       | <span data-ttu-id="b34f4-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="b34f4-118">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="b34f4-119">**GetButtonState**</span><span class="sxs-lookup"><span data-stu-id="b34f4-119">**GetButtonState**</span></span>](getbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="b34f4-120">Recupera el estado actual del botón del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b34f4-120">Retrieves the current state of the specified device button.</span></span><br/>        |
| <span data-ttu-id="b34f4-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="b34f4-121">**OnlineDevice**</span></span>                                                       | <span data-ttu-id="b34f4-122">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="b34f4-122">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="b34f4-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="b34f4-123">**QuiesceDevice**</span></span>                                                      | <span data-ttu-id="b34f4-124">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="b34f4-124">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="b34f4-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="b34f4-125">**RequestStateChange**</span></span>](msvm-syntheticmouse-requeststatechange.md)   | <span data-ttu-id="b34f4-126">Solicita un cambio de estado</span><span class="sxs-lookup"><span data-stu-id="b34f4-126">Requests a state change</span></span><br/>                                            |
| [<span data-ttu-id="b34f4-127">**Reset**</span><span class="sxs-lookup"><span data-stu-id="b34f4-127">**Reset**</span></span>](msvm-syntheticmouse-reset.md)                             | <span data-ttu-id="b34f4-128">Restablece el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b34f4-128">Resets the device.</span></span><br/>                                                 |
| <span data-ttu-id="b34f4-129">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="b34f4-129">**RestoreProperties**</span></span>                                                  | <span data-ttu-id="b34f4-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="b34f4-130">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="b34f4-131">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="b34f4-131">**SaveProperties**</span></span>                                                     | <span data-ttu-id="b34f4-132">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="b34f4-132">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="b34f4-133">**SetAbsolutePosition**</span><span class="sxs-lookup"><span data-stu-id="b34f4-133">**SetAbsolutePosition**</span></span>](setabsoluteposition-msvm-syntheticmouse.md) | <span data-ttu-id="b34f4-134">Establece la posición horizontal y vertical del cursor del mouse.</span><span class="sxs-lookup"><span data-stu-id="b34f4-134">Sets the horizontal and vertical position of the mouse cursor.</span></span><br/>     |
| [<span data-ttu-id="b34f4-135">**SetButtonState**</span><span class="sxs-lookup"><span data-stu-id="b34f4-135">**SetButtonState**</span></span>](setbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="b34f4-136">Establece el estado actual del botón del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b34f4-136">Sets the current state of the specified device button.</span></span><br/>             |
| <span data-ttu-id="b34f4-137">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b34f4-137">**SetPowerState**</span></span>                                                      | <span data-ttu-id="b34f4-138">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="b34f4-138">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="b34f4-139">**SetScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="b34f4-139">**SetScrollPosition**</span></span>](setscrollposition-msvm-syntheticmouse.md)     | <span data-ttu-id="b34f4-140">Establece la coordenada z del control de rueda del dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="b34f4-140">Sets the z-coordinate of the wheel control of the pointing device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b34f4-141">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b34f4-141">Properties</span></span>

<span data-ttu-id="b34f4-142">La clase **MSVM \_ SyntheticMouse** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b34f4-142">The **Msvm\_SyntheticMouse** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b34f4-143">**AbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="b34f4-143">**AbsoluteCoordinates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-144">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b34f4-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-146">Indica si el dispositivo funciona en coordenadas absolutas o relativas.</span><span class="sxs-lookup"><span data-stu-id="b34f4-146">Indicates whether the device operates on absolute or relative coordinates.</span></span>



| <span data-ttu-id="b34f4-147">Value</span><span class="sxs-lookup"><span data-stu-id="b34f4-147">Value</span></span>                                                                                | <span data-ttu-id="b34f4-148">Significado</span><span class="sxs-lookup"><span data-stu-id="b34f4-148">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="b34f4-149"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="b34f4-149"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="b34f4-150">Las coordenadas del dispositivo son absolutas.</span><span class="sxs-lookup"><span data-stu-id="b34f4-150">The device's coordinates are absolute.</span></span><br/> |
| <dl> <span data-ttu-id="b34f4-151"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="b34f4-151"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="b34f4-152">Las coordenadas del dispositivo son relativas.</span><span class="sxs-lookup"><span data-stu-id="b34f4-152">The device's coordinates are relative.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b34f4-153">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="b34f4-153">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-154">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-154">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-156">Cualquier disponibilidad adicional y estado del dispositivo, más allá de lo especificado en la propiedad **Availability** .</span><span class="sxs-lookup"><span data-stu-id="b34f4-156">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="b34f4-157">La propiedad **Availability** denota el estado principal y la disponibilidad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b34f4-157">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="b34f4-158">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b34f4-158">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="b34f4-159">Value</span><span class="sxs-lookup"><span data-stu-id="b34f4-159">Value</span></span>                                                                          | <span data-ttu-id="b34f4-160">Significado</span><span class="sxs-lookup"><span data-stu-id="b34f4-160">Meaning</span></span>                   |
|--------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>{6}</dt> </dl> | <span data-ttu-id="b34f4-161">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="b34f4-161">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b34f4-162">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="b34f4-162">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-163">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-165">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b34f4-165">The primary availability and status of the device.</span></span> <span data-ttu-id="b34f4-166">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b34f4-166">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="b34f4-167">Value</span><span class="sxs-lookup"><span data-stu-id="b34f4-167">Value</span></span>                                                                        | <span data-ttu-id="b34f4-168">Significado</span><span class="sxs-lookup"><span data-stu-id="b34f4-168">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="b34f4-169"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b34f4-169"><dt>6</dt></span></span> </dl> | <span data-ttu-id="b34f4-170">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="b34f4-170">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b34f4-171">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="b34f4-171">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-172">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-172">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-174">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="b34f4-174">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="b34f4-175">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="b34f4-175">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-176">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b34f4-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b34f4-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-179">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="b34f4-179">A short description of the object.</span></span> <span data-ttu-id="b34f4-180">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b34f4-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-181">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="b34f4-181">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-182">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-184">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="b34f4-184">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="b34f4-185">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="b34f4-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b34f4-186">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b34f4-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b34f4-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="b34f4-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="b34f4-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="b34f4-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="b34f4-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="b34f4-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b34f4-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="b34f4-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b34f4-194">)</span><span class="sxs-lookup"><span data-stu-id="b34f4-194">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b34f4-195">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b34f4-195">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-196">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b34f4-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-198">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="b34f4-198">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-199">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="b34f4-199">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b34f4-200">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="b34f4-200">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="b34f4-201">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b34f4-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-202">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b34f4-202">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b34f4-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-205">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="b34f4-205">A description of the object.</span></span> <span data-ttu-id="b34f4-206">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b34f4-206">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-207">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="b34f4-207">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-208">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-210">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="b34f4-210">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="b34f4-211">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="b34f4-211">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b34f4-212">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b34f4-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b34f4-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="b34f4-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="b34f4-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="b34f4-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="b34f4-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="b34f4-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="b34f4-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b34f4-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="b34f4-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b34f4-221">)</span><span class="sxs-lookup"><span data-stu-id="b34f4-221">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b34f4-222">**ID**</span><span class="sxs-lookup"><span data-stu-id="b34f4-222">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b34f4-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-225">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="b34f4-225">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-226">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b34f4-226">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="b34f4-227">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="b34f4-227">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-228">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b34f4-228">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-229">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b34f4-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-231">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="b34f4-231">A display name for the object.</span></span> <span data-ttu-id="b34f4-232">Esta propiedad permite a cada instancia definir un nombre para mostrar además de las propiedades de clave, los datos de identidad y la información de descripción.</span><span class="sxs-lookup"><span data-stu-id="b34f4-232">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="b34f4-233">La propiedad [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) de la clase del **\_ ManagedSystemElement de CIM** también se define como un nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="b34f4-233">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="b34f4-234">Sin embargo, a menudo se considera una clave.</span><span class="sxs-lookup"><span data-stu-id="b34f4-234">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="b34f4-235">No es razonable que la misma propiedad pueda transmitir tanto la identidad como un nombre para mostrar, sin incoherencias.</span><span class="sxs-lookup"><span data-stu-id="b34f4-235">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="b34f4-236">Donde [**Name**](msvm-keyboard.md) existe y no es una clave (como en el caso de las instancias de LogicalDevice), la misma información puede estar presente en las propiedades **Name** y **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="b34f4-236">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="b34f4-237">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b34f4-237">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="b34f4-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-239">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-241">Configuración predeterminada o de inicio de un administrador para **EnabledState** de un elemento.</span><span class="sxs-lookup"><span data-stu-id="b34f4-241">An administrator's default or startup configuration for the **EnabledState** of an element.</span></span> <span data-ttu-id="b34f4-242">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b34f4-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-243">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="b34f4-243">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-244">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-246">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="b34f4-246">The enabled and disabled states of an element.</span></span> <span data-ttu-id="b34f4-247">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b34f4-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="b34f4-248">Value</span><span class="sxs-lookup"><span data-stu-id="b34f4-248">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="b34f4-249">Significado</span><span class="sxs-lookup"><span data-stu-id="b34f4-249">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="b34f4-250"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b34f4-250"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="b34f4-251">La máquina virtual invitada admite un mouse sintético.</span><span class="sxs-lookup"><span data-stu-id="b34f4-251">The guest virtual machine supports a synthetic mouse.</span></span><br/>         |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="b34f4-252"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b34f4-252"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="b34f4-253">La máquina virtual invitada no admite un mouse sintético.</span><span class="sxs-lookup"><span data-stu-id="b34f4-253">The guest virtual machine does not support a synthetic mouse.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b34f4-254">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b34f4-254">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-255">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b34f4-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-257">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="b34f4-257">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="b34f4-258">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b34f4-258">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-259">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b34f4-259">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-260">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b34f4-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-262">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="b34f4-262">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="b34f4-263">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b34f4-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-264">**Situación**</span><span class="sxs-lookup"><span data-stu-id="b34f4-264">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-265">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-265">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-266">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-267">La configuración del dispositivo señalador para la operación a la derecha o a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="b34f4-267">The configuration of the pointing device for right-hand or left-hand operation.</span></span> <span data-ttu-id="b34f4-268">Esta propiedad se hereda de [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="b34f4-268">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="b34f4-269">Value</span><span class="sxs-lookup"><span data-stu-id="b34f4-269">Value</span></span>                                                                        | <span data-ttu-id="b34f4-270">Significado</span><span class="sxs-lookup"><span data-stu-id="b34f4-270">Meaning</span></span>                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="b34f4-271"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b34f4-271"><dt>0</dt></span></span> </dl> | <span data-ttu-id="b34f4-272">Unknown</span><span class="sxs-lookup"><span data-stu-id="b34f4-272">Unknown</span></span><br/>                 |
| <dl> <span data-ttu-id="b34f4-273"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b34f4-273"><dt>1</dt></span></span> </dl> | <span data-ttu-id="b34f4-274">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="b34f4-274">Not applicable.</span></span><br/>         |
| <dl> <span data-ttu-id="b34f4-275"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b34f4-275"><dt>2</dt></span></span> </dl> | <span data-ttu-id="b34f4-276">Operación a la derecha.</span><span class="sxs-lookup"><span data-stu-id="b34f4-276">Right handed operation.</span></span><br/> |
| <dl> <span data-ttu-id="b34f4-277"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b34f4-277"><dt>3</dt></span></span> </dl> | <span data-ttu-id="b34f4-278">Operación de mano izquierda.</span><span class="sxs-lookup"><span data-stu-id="b34f4-278">Left handed operation.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="b34f4-279">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="b34f4-279">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-280">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-282">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="b34f4-282">The current health of the element.</span></span> <span data-ttu-id="b34f4-283">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b34f4-283">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-284">**HorizontalPosition**</span><span class="sxs-lookup"><span data-stu-id="b34f4-284">**HorizontalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-285">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34f4-285">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-287">Coordenada x absoluta del dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="b34f4-287">The absolute x-coordinate of the pointing device.</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-288">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b34f4-288">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-289">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="b34f4-289">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-291">Matriz de cadenas de formato libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz [**OtherIdentifyingInfo**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="b34f4-291">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="b34f4-292">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b34f4-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-293">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b34f4-293">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-294">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b34f4-294">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-296">Fecha y hora en que se creó la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b34f4-296">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="b34f4-297">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b34f4-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-298">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b34f4-298">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-299">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b34f4-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-301">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="b34f4-301">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-302">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="b34f4-302">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b34f4-303">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b34f4-303">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-304">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="b34f4-304">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-305">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b34f4-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-307">Indica si el dispositivo está bloqueado, lo que impide la entrada o salida del usuario.</span><span class="sxs-lookup"><span data-stu-id="b34f4-307">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="b34f4-308">Esta propiedad se hereda de [**\_ UserDevice CIM**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="b34f4-308">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-309">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b34f4-309">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-310">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b34f4-310">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-312">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b34f4-312">The last error code reported by the logical device.</span></span> <span data-ttu-id="b34f4-313">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b34f4-313">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-314">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="b34f4-314">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-315">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b34f4-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-317">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="b34f4-317">This property has been deprecated.</span></span> <span data-ttu-id="b34f4-318">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b34f4-318">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-319">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b34f4-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-320">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b34f4-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-322">Calificadores: **MaxLen** (1024)</span><span class="sxs-lookup"><span data-stu-id="b34f4-322">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-323">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="b34f4-323">The label by which the object is known.</span></span> <span data-ttu-id="b34f4-324">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="b34f4-324">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="b34f4-325">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b34f4-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-326">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="b34f4-326">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-327">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b34f4-327">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-329">Número de botones del dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="b34f4-329">The number of buttons on the pointing device.</span></span> <span data-ttu-id="b34f4-330">Esta propiedad se hereda de [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="b34f4-330">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-331">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="b34f4-331">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-332">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-334">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="b34f4-334">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="b34f4-335">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="b34f4-335">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b34f4-336">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b34f4-336">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b34f4-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="b34f4-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="b34f4-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="b34f4-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="b34f4-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="b34f4-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="b34f4-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="b34f4-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="b34f4-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="b34f4-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="b34f4-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="b34f4-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="b34f4-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="b34f4-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="b34f4-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="b34f4-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="b34f4-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="b34f4-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b34f4-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="b34f4-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b34f4-356">)</span><span class="sxs-lookup"><span data-stu-id="b34f4-356">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b34f4-357">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="b34f4-357">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-358">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-360">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="b34f4-360">The current status of the element.</span></span> <span data-ttu-id="b34f4-361">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b34f4-361">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-362">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="b34f4-362">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-363">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b34f4-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-364">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-365">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="b34f4-365">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="b34f4-366">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="b34f4-366">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="b34f4-367">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b34f4-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-368">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="b34f4-368">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-369">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="b34f4-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-371">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b34f4-371">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="b34f4-372">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b34f4-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-373">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="b34f4-373">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-374">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-376">El tipo de dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="b34f4-376">The type of pointing device.</span></span> <span data-ttu-id="b34f4-377">Esta propiedad se hereda de [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="b34f4-377">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="b34f4-378">Value</span><span class="sxs-lookup"><span data-stu-id="b34f4-378">Value</span></span>                                                                        | <span data-ttu-id="b34f4-379">Significado</span><span class="sxs-lookup"><span data-stu-id="b34f4-379">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="b34f4-380"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b34f4-380"><dt>3</dt></span></span> </dl> | <span data-ttu-id="b34f4-381">Mouse</span><span class="sxs-lookup"><span data-stu-id="b34f4-381">Mouse</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b34f4-382">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b34f4-382">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-383">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-383">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-384">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-385">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b34f4-385">The power management capabilities of the device.</span></span> <span data-ttu-id="b34f4-386">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b34f4-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-387">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b34f4-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-388">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b34f4-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-389">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-390">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="b34f4-390">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="b34f4-391">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b34f4-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-392">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="b34f4-392">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-393">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b34f4-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-395">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="b34f4-395">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="b34f4-396">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b34f4-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-397">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="b34f4-397">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-398">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-400">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="b34f4-400">Provides high level status information.</span></span> <span data-ttu-id="b34f4-401">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="b34f4-401">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="b34f4-402">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="b34f4-402">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b34f4-403">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b34f4-403">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b34f4-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="b34f4-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-405"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="b34f4-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="b34f4-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="b34f4-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b34f4-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="b34f4-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b34f4-410">)</span><span class="sxs-lookup"><span data-stu-id="b34f4-410">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b34f4-411">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="b34f4-411">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-412">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-414">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="b34f4-414">The last requested or desired state for the element.</span></span> <span data-ttu-id="b34f4-415">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b34f4-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="b34f4-416">Value</span><span class="sxs-lookup"><span data-stu-id="b34f4-416">Value</span></span>                                                                         | <span data-ttu-id="b34f4-417">Significado</span><span class="sxs-lookup"><span data-stu-id="b34f4-417">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="b34f4-418"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="b34f4-418"><dt>12</dt></span></span> </dl> | <span data-ttu-id="b34f4-419">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="b34f4-419">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b34f4-420">**Resolución**</span><span class="sxs-lookup"><span data-stu-id="b34f4-420">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-421">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b34f4-421">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-423">La resolución de seguimiento del dispositivo señalador, en recuentos por pulgada.</span><span class="sxs-lookup"><span data-stu-id="b34f4-423">The tracking resolution of the pointing device, in counts per inch.</span></span> <span data-ttu-id="b34f4-424">Esta propiedad se hereda de [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="b34f4-424">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-425">**ScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="b34f4-425">**ScrollPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-426">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34f4-426">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-427">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-428">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Mickeys")</span><span class="sxs-lookup"><span data-stu-id="b34f4-428">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-429">Posición de la coordenada z del dispositivo del mouse.</span><span class="sxs-lookup"><span data-stu-id="b34f4-429">The z-coordinate position of the mouse device.</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-430">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b34f4-430">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-431">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b34f4-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-432">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-433">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b34f4-433">The current status of the object.</span></span> <span data-ttu-id="b34f4-434">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b34f4-434">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-435">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b34f4-435">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-436">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="b34f4-436">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-437">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-438">Cadenas que describen los distintos valores de la matriz [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="b34f4-438">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="b34f4-439">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b34f4-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-440">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b34f4-440">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-441">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-442">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-443">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b34f4-443">The current state of the logical device.</span></span> <span data-ttu-id="b34f4-444">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b34f4-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-445">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b34f4-445">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-446">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b34f4-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-447">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-448">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="b34f4-448">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-449">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b34f4-449">The creation class name of the scoping system.</span></span> <span data-ttu-id="b34f4-450">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b34f4-450">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-451">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b34f4-451">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-452">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b34f4-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-453">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-454">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="b34f4-454">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-455">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b34f4-455">The name of the scoping system.</span></span> <span data-ttu-id="b34f4-456">Este valor corresponde al valor de la propiedad [**Name**](msvm-computersystem.md) de la clase **MSVM \_ ComputerSystem** para el ámbito de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b34f4-456">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="b34f4-457">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b34f4-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-458">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="b34f4-458">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-459">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b34f4-459">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-460">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-461">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="b34f4-461">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="b34f4-462">Si el estado del elemento no ha cambiado y se rellena esta propiedad, debe establecerse en un valor de intervalo 0.</span><span class="sxs-lookup"><span data-stu-id="b34f4-462">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="b34f4-463">Si se solicitó un cambio de estado, pero se rechazó o no se procesó todavía, la propiedad no se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="b34f4-463">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="b34f4-464">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="b34f4-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-465">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="b34f4-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-466">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b34f4-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-467">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-468">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b34f4-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="b34f4-469">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="b34f4-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-470">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="b34f4-470">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-471">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f4-471">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-472">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-473">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="b34f4-473">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="b34f4-474">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="b34f4-474">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b34f4-475">**VerticalPosition**</span><span class="sxs-lookup"><span data-stu-id="b34f4-475">**VerticalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f4-476">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34f4-476">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34f4-477">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b34f4-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f4-478">Coordenada y absoluta del dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="b34f4-478">The absolute y-coordinate of the pointing device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b34f4-479">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b34f4-479">Remarks</span></span>

<span data-ttu-id="b34f4-480">El acceso a la clase **MSVM \_ SyntheticMouse** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="b34f4-480">Access to the **Msvm\_SyntheticMouse** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b34f4-481">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b34f4-481">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b34f4-482">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b34f4-482">Requirements</span></span>



| <span data-ttu-id="b34f4-483">Requisito</span><span class="sxs-lookup"><span data-stu-id="b34f4-483">Requirement</span></span> | <span data-ttu-id="b34f4-484">Value</span><span class="sxs-lookup"><span data-stu-id="b34f4-484">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b34f4-485">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b34f4-485">Minimum supported client</span></span><br/> | <span data-ttu-id="b34f4-486">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b34f4-486">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b34f4-487">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b34f4-487">Minimum supported server</span></span><br/> | <span data-ttu-id="b34f4-488">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b34f4-488">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b34f4-489">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b34f4-489">Namespace</span></span><br/>                | <span data-ttu-id="b34f4-490">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b34f4-490">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b34f4-491">MOF</span><span class="sxs-lookup"><span data-stu-id="b34f4-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b34f4-492"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b34f4-492"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b34f4-493">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b34f4-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b34f4-494"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b34f4-494"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b34f4-495">Vea también</span><span class="sxs-lookup"><span data-stu-id="b34f4-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b34f4-496">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b34f4-496">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="b34f4-497">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b34f4-497">**CIM\_PointingDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[<span data-ttu-id="b34f4-498">Clases de entrada</span><span class="sxs-lookup"><span data-stu-id="b34f4-498">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

