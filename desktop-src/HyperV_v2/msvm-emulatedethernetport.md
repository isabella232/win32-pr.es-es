---
description: Representa un adaptador Ethernet emulado.
ms.assetid: 8E990C76-7D48-42B0-BB4D-C4C07B1C482A
title: Clase Msvm_EmulatedEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPort
- Msvm_EmulatedEthernetPort.SetPowerState
- Msvm_EmulatedEthernetPort.EnableDevice
- Msvm_EmulatedEthernetPort.OnlineDevice
- Msvm_EmulatedEthernetPort.QuiesceDevice
- Msvm_EmulatedEthernetPort.SaveProperties
- Msvm_EmulatedEthernetPort.RestoreProperties
- Msvm_EmulatedEthernetPort.InstanceID
- Msvm_EmulatedEthernetPort.Caption
- Msvm_EmulatedEthernetPort.Description
- Msvm_EmulatedEthernetPort.ElementName
- Msvm_EmulatedEthernetPort.InstallDate
- Msvm_EmulatedEthernetPort.Name
- Msvm_EmulatedEthernetPort.OperationalStatus
- Msvm_EmulatedEthernetPort.StatusDescriptions
- Msvm_EmulatedEthernetPort.Status
- Msvm_EmulatedEthernetPort.HealthState
- Msvm_EmulatedEthernetPort.CommunicationStatus
- Msvm_EmulatedEthernetPort.DetailedStatus
- Msvm_EmulatedEthernetPort.OperatingStatus
- Msvm_EmulatedEthernetPort.PrimaryStatus
- Msvm_EmulatedEthernetPort.EnabledState
- Msvm_EmulatedEthernetPort.OtherEnabledState
- Msvm_EmulatedEthernetPort.RequestedState
- Msvm_EmulatedEthernetPort.EnabledDefault
- Msvm_EmulatedEthernetPort.TimeOfLastStateChange
- Msvm_EmulatedEthernetPort.AvailableRequestedStates
- Msvm_EmulatedEthernetPort.TransitioningToState
- Msvm_EmulatedEthernetPort.SystemCreationClassName
- Msvm_EmulatedEthernetPort.SystemName
- Msvm_EmulatedEthernetPort.CreationClassName
- Msvm_EmulatedEthernetPort.DeviceID
- Msvm_EmulatedEthernetPort.PowerManagementSupported
- Msvm_EmulatedEthernetPort.PowerManagementCapabilities
- Msvm_EmulatedEthernetPort.Availability
- Msvm_EmulatedEthernetPort.StatusInfo
- Msvm_EmulatedEthernetPort.LastErrorCode
- Msvm_EmulatedEthernetPort.ErrorDescription
- Msvm_EmulatedEthernetPort.ErrorCleared
- Msvm_EmulatedEthernetPort.OtherIdentifyingInfo
- Msvm_EmulatedEthernetPort.PowerOnHours
- Msvm_EmulatedEthernetPort.TotalPowerOnHours
- Msvm_EmulatedEthernetPort.IdentifyingDescriptions
- Msvm_EmulatedEthernetPort.AdditionalAvailability
- Msvm_EmulatedEthernetPort.MaxQuiesceTime
- Msvm_EmulatedEthernetPort.Speed
- Msvm_EmulatedEthernetPort.MaxSpeed
- Msvm_EmulatedEthernetPort.RequestedSpeed
- Msvm_EmulatedEthernetPort.UsageRestriction
- Msvm_EmulatedEthernetPort.PortType
- Msvm_EmulatedEthernetPort.OtherPortType
- Msvm_EmulatedEthernetPort.OtherNetworkPortType
- Msvm_EmulatedEthernetPort.PortNumber
- Msvm_EmulatedEthernetPort.LinkTechnology
- Msvm_EmulatedEthernetPort.OtherLinkTechnology
- Msvm_EmulatedEthernetPort.PermanentAddress
- Msvm_EmulatedEthernetPort.NetworkAddresses
- Msvm_EmulatedEthernetPort.FullDuplex
- Msvm_EmulatedEthernetPort.AutoSense
- Msvm_EmulatedEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.MaxDataSize
- Msvm_EmulatedEthernetPort.Capabilities
- Msvm_EmulatedEthernetPort.CapabilityDescriptions
- Msvm_EmulatedEthernetPort.EnabledCapabilities
- Msvm_EmulatedEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ec13ae369f6d5e3d884f74c96d7df27c2f5fa97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666811"
---
# <a name="msvm_emulatedethernetport-class"></a><span data-ttu-id="ac1b0-103">MSVM \_ EmulatedEthernetPort (clase)</span><span class="sxs-lookup"><span data-stu-id="ac1b0-103">Msvm\_EmulatedEthernetPort class</span></span>

<span data-ttu-id="ac1b0-104">Representa un adaptador Ethernet emulado.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-104">Represents an emulated Ethernet adapter.</span></span> <span data-ttu-id="ac1b0-105">Este adaptador se usa cuando una máquina virtual no es capaz de ejecutar el puerto Ethernet sintético cuando no hay circuitos integrados instalados en el invitado.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-105">This adapter is used when a virtual machine is not capable of running the synthetic Ethernet port when no integrated circuits are installed in the guest.</span></span>

> [!Note]  
> <span data-ttu-id="ac1b0-106">Esta clase no está disponible para las máquinas virtuales de generación 2.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-106">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="ac1b0-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac1b0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac1b0-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Emulated Ethernet Port";
  string   ElementName = "Legacy Network Adapter";
  datetime InstallDate;
  string   Name = "Ethernet Port";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
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
  string   CreationClassName = "Msvm_EmulatedEthernetPort";
  string   DeviceID = "Microsoft:GUID\device-specific data";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   Speed = 1000000000;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Virtual Ethernet";
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  string   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="ac1b0-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="ac1b0-109">Members</span></span>

<span data-ttu-id="ac1b0-110">La clase **MSVM \_ EmulatedEthernetPort** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ac1b0-110">The **Msvm\_EmulatedEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="ac1b0-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="ac1b0-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ac1b0-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ac1b0-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ac1b0-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ac1b0-113">Methods</span></span>

<span data-ttu-id="ac1b0-114">La clase **MSVM \_ EmulatedEthernetPort** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-114">The **Msvm\_EmulatedEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="ac1b0-115">Método</span><span class="sxs-lookup"><span data-stu-id="ac1b0-115">Method</span></span>                                                                     | <span data-ttu-id="ac1b0-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac1b0-116">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="ac1b0-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-117">**EnableDevice**</span></span>                                                           | <span data-ttu-id="ac1b0-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ac1b0-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-119">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="ac1b0-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ac1b0-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-121">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="ac1b0-122">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="ac1b0-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-123">**RequestStateChange**</span></span>](msvm-emulatedethernetport-requeststatechange.md) | <span data-ttu-id="ac1b0-124">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="ac1b0-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-125">**Reset**</span></span>](msvm-emulatedethernetport-reset.md)                           | <span data-ttu-id="ac1b0-126">Restablece el dispositivo emulado.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-126">Resets the emulated device.</span></span><br/>   |
| <span data-ttu-id="ac1b0-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-127">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="ac1b0-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ac1b0-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-129">**SaveProperties**</span></span>                                                         | <span data-ttu-id="ac1b0-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ac1b0-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-131">**SetPowerState**</span></span>                                                          | <span data-ttu-id="ac1b0-132">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ac1b0-133">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ac1b0-133">Properties</span></span>

<span data-ttu-id="ac1b0-134">La clase **MSVM \_ EmulatedEthernetPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-134">The **Msvm\_EmulatedEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac1b0-135">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-135">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-136">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-138">La unidad de transmisión máxima (MTU) activa o negociada que se puede admitir.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="ac1b0-139">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)y siempre se establece en 1500.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-141">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-143">Cualquier disponibilidad adicional y estado del dispositivo, más allá de lo especificado en la propiedad **Availability** .</span><span class="sxs-lookup"><span data-stu-id="ac1b0-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="ac1b0-144">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre está establecida en 6 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="ac1b0-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-145">**Percepción automática**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-146">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-148">Indica si el puerto de red es capaz de determinar automáticamente la velocidad u otras características de comunicación de los medios de red conectados.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="ac1b0-149">Esta propiedad se hereda de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-150">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-151">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-153">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-153">The primary availability and status of the device.</span></span> <span data-ttu-id="ac1b0-154">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-156">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-158">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="ac1b0-159">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ac1b0-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="ac1b0-160">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="ac1b0-161">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="ac1b0-162">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ac1b0-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="ac1b0-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="ac1b0-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="ac1b0-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="ac1b0-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="ac1b0-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="ac1b0-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="ac1b0-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="ac1b0-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="ac1b0-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="ac1b0-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="ac1b0-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="ac1b0-173">)</span><span class="sxs-lookup"><span data-stu-id="ac1b0-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac1b0-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-175">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-177">Capacidades del puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-177">Capabilities of the Ethernet port.</span></span> <span data-ttu-id="ac1b0-178">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-178">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-179">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-179">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-180">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-180">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-182">Una matriz de cadenas de forma libre que proporciona explicaciones más detalladas para cualquiera de las características de puerto Ethernet que se indican en la matriz de **capacidades** .</span><span class="sxs-lookup"><span data-stu-id="ac1b0-182">An array of free-form strings that provides more detailed explanations for any of the Ethernet port features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="ac1b0-183">Tenga en cuenta que cada entrada de esta matriz está relacionada con la entrada de la matriz de **capacidades** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-183">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="ac1b0-184">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-184">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-185">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-185">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-188">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-188">A short description of the object.</span></span> <span data-ttu-id="ac1b0-189">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "puerto Ethernet".</span><span class="sxs-lookup"><span data-stu-id="ac1b0-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-190">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-190">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-191">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-193">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-193">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="ac1b0-194">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-194">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ac1b0-195">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ac1b0-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-199">El nombre de la clase o la subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-199">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="ac1b0-200">Cuando se usa con las otras propiedades de clave de esta clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-200">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="ac1b0-201">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "MSVM \_ EmulatedEthernetPort".</span><span class="sxs-lookup"><span data-stu-id="ac1b0-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_EmulatedEthernetPort".</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-202">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-202">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-205">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-205">A description of the object.</span></span> <span data-ttu-id="ac1b0-206">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "puerto Ethernet emulado de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="ac1b0-206">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-207">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-207">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-208">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-210">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-210">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="ac1b0-211">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-211">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ac1b0-212">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ac1b0-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-213">**ID**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-213">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-214">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-216">Una dirección u otra información de identificación utilizada para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-216">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="ac1b0-217">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "Microsoft:*GUID* \\ *específico del dispositivo*".</span><span class="sxs-lookup"><span data-stu-id="ac1b0-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-218">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-218">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-221">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-221">A display name for the object.</span></span> <span data-ttu-id="ac1b0-222">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "adaptador de red heredado".</span><span class="sxs-lookup"><span data-stu-id="ac1b0-222">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Legacy Network Adapter".</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-223">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-223">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-224">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-224">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-226">Las funciones que se habilitan en la lista de todos los admitidos, que se definen en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="ac1b0-226">The capabilities that are enabled from the list of all supported ones, which are defined in the **Capabilities** array.</span></span> <span data-ttu-id="ac1b0-227">Esta propiedad se hereda de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-227">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-228">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-228">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-229">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-231">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-231">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="ac1b0-232">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) y siempre está establecida en 2 ("habilitado").</span><span class="sxs-lookup"><span data-stu-id="ac1b0-232">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to 2 ("Enabled").</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-233">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-233">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-234">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-234">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-236">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-236">The enabled and disabled states of an element.</span></span> <span data-ttu-id="ac1b0-237">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="ac1b0-237">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-238">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-239">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-241">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-241">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="ac1b0-242">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-244">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-246">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-246">A string that provides more information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span> <span data-ttu-id="ac1b0-247">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-247">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-248">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-248">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-249">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-251">Indica si el puerto está funcionando en modo dúplex completo.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-251">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="ac1b0-252">Esta propiedad se hereda de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-252">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-253">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-253">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-254">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-255">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-256">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-256">The current health of the element.</span></span> <span data-ttu-id="ac1b0-257">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-257">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="ac1b0-258">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 ("correcto").</span><span class="sxs-lookup"><span data-stu-id="ac1b0-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-259">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-259">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-260">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-262">Matriz de cadenas de formato libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="ac1b0-262">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="ac1b0-263">Cada entrada de esta matriz está relacionada con la entrada de **OtherIdentifyingInfo** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-263">Each entry of this array is related to the entry in **OtherIdentifyingInfo** that is located at the same index.</span></span> <span data-ttu-id="ac1b0-264">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-264">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-265">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-265">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-266">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-268">Un valor de **fecha y hora** que indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-268">A **datetime** value that indicates when the object was installed.</span></span> <span data-ttu-id="ac1b0-269">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-269">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="ac1b0-270">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ac1b0-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-272">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-273">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-274">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-275">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ac1b0-276">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ac1b0-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-278">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-280">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="ac1b0-281">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-282">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-282">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-283">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-285">Tipos de vínculos.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-285">The types of links.</span></span> <span data-ttu-id="ac1b0-286">Cuando se establece en 1 ("otro"), la propiedad relacionada **OtherLinkTechnology** contiene una descripción de cadena del tipo de vínculo.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-286">When set to 1 ("Other"), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="ac1b0-287">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) y siempre está establecida en 2 ("Ethernet").</span><span class="sxs-lookup"><span data-stu-id="ac1b0-287">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is always set to 2 ("Ethernet").</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-288">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-288">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-289">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-289">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-291">El tamaño máximo del campo de información (no MAC) que se recibirá o transmitirá.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-291">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="ac1b0-292">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)y siempre se establece en 1500.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-292">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-293">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-293">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-294">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-294">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-296">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-297">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-297">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-298">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-300">Ancho de banda máximo del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-300">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="ac1b0-301">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85))y siempre se establece en 1 mil millones.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-301">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-302">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-302">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-305">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-305">The label by which the object is known.</span></span> <span data-ttu-id="ac1b0-306">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-306">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="ac1b0-307">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre se establece en "puerto Ethernet".</span><span class="sxs-lookup"><span data-stu-id="ac1b0-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-308">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-308">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-309">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-309">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-311">Las direcciones MAC Ethernet/802.3, con formato de doce dígitos hexadecimales (por ejemplo, "010203040506"), con cada par que representa uno de los seis octetos de la dirección MAC en orden de bits canónico (el bit de dirección de grupo se encuentra en el bit de orden inferior del primer carácter de la cadena).</span><span class="sxs-lookup"><span data-stu-id="ac1b0-311">The Ethernet/802.3 MAC addresses, formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the group address bit is found in the low order bit of the first character of the string).</span></span> <span data-ttu-id="ac1b0-312">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-312">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-313">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-313">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-314">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-314">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-316">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="ac1b0-316">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="ac1b0-317">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-317">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ac1b0-318">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ac1b0-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-319">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-319">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-320">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-322">Estados actuales del elemento.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-322">The current statuses of the element.</span></span> <span data-ttu-id="ac1b0-323">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 2 ("correcto").</span><span class="sxs-lookup"><span data-stu-id="ac1b0-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-324">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-324">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-325">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-325">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-327">Matriz de cadenas de formato libre que proporciona explicaciones más detalladas para cualquiera de las funciones habilitadas que se especifican como "otro".</span><span class="sxs-lookup"><span data-stu-id="ac1b0-327">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as "Other".</span></span> <span data-ttu-id="ac1b0-328">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-328">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-329">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-329">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-330">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-332">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="ac1b0-332">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="ac1b0-333">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-333">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="ac1b0-334">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-335">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-335">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-336">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-336">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-338">Los datos, además de la información de identificador de dispositivo, que se pueden usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-338">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="ac1b0-339">Por ejemplo, puede usar esta propiedad para contener el nombre para mostrar del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-339">For example, you could use this property to hold the operating system's display name for the device.</span></span> <span data-ttu-id="ac1b0-340">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-341">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-341">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-342">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-344">Un valor de cadena que describe **LinkTechnology** cuando se establece en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="ac1b0-344">A string value that describes **LinkTechnology** when it is set to 1 ("Other").</span></span> <span data-ttu-id="ac1b0-345">Esta propiedad se hereda de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-346">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-346">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-347">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-349">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-349">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-350">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-350">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-351">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-352">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-353">El tipo de módulo, cuando **portType** está establecido en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="ac1b0-353">The type of module, when **PortType** is set to 1 ("Other").</span></span> <span data-ttu-id="ac1b0-354">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)) y siempre se establece en "Ethernet virtual".</span><span class="sxs-lookup"><span data-stu-id="ac1b0-354">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) and is always set to "Virtual Ethernet".</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-355">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-355">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-356">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-358">La dirección de red que está codificada en un puerto.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-358">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="ac1b0-359">Esta dirección se puede cambiar mediante una actualización de firmware o una configuración de software.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-359">This address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="ac1b0-360">Cuando se realiza este cambio, el campo debe actualizarse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-360">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="ac1b0-361">Debe dejarse en blanco si no existe ninguna dirección codificada para el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-361">This should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="ac1b0-362">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ac1b0-362">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-363">**NúmeroDePuerto**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-363">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-364">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-366">Los puertos de red suelen numerarse con respecto a un módulo lógico o a un elemento de red.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-366">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="ac1b0-367">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ac1b0-367">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="ac1b0-368">Value</span><span class="sxs-lookup"><span data-stu-id="ac1b0-368">Value</span></span>                                                                        | <span data-ttu-id="ac1b0-369">Significado</span><span class="sxs-lookup"><span data-stu-id="ac1b0-369">Meaning</span></span>                             |
|------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="ac1b0-370"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ac1b0-370"><dt>0</dt></span></span> </dl> | <span data-ttu-id="ac1b0-371">La NIC no está emulada.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-371">The NIC is not emulated.</span></span><br/> |
| <dl> <span data-ttu-id="ac1b0-372"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ac1b0-372"><dt>1</dt></span></span> </dl> | <span data-ttu-id="ac1b0-373">La NIC está emulada.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-373">The NIC is emulated.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="ac1b0-374">**PortType**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-374">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-375">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-375">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-376">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-377">Modo específico que está habilitado actualmente para el puerto.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-377">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="ac1b0-378">Cuando se establece en 1 ("otro"), la propiedad relacionada **OtherPortType** contiene una descripción de cadena del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-378">When set to 1 ("Other"), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="ac1b0-379">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)y siempre está establecida en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="ac1b0-379">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1 ("Other").</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-380">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-380">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-381">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-381">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-383">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-383">The power management capabilities of the device.</span></span> <span data-ttu-id="ac1b0-384">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-385">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-386">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-388">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-388">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="ac1b0-389">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-390">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-390">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-391">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-391">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-392">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-393">El número de horas consecutivas que este dispositivo ha estado encendido desde su último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-393">The number of consecutive hours that this device has been powered, since its last power cycle.</span></span> <span data-ttu-id="ac1b0-394">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-395">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-395">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-396">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-398">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-398">Provides high level status information.</span></span> <span data-ttu-id="ac1b0-399">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-399">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="ac1b0-400">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-400">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ac1b0-401">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ac1b0-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-402">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-402">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-403">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-405">Ancho de banda solicitado del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-405">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="ac1b0-406">El ancho de banda real se registra en LogicalPort. Speed.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-406">The actual bandwidth is reported in LogicalPort.Speed.</span></span> <span data-ttu-id="ac1b0-407">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85))y siempre se establece en 1 mil millones.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-407">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-408">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-408">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-409">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-411">Último estado solicitado o deseado para el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-411">The last requested or desired state for the management service.</span></span> <span data-ttu-id="ac1b0-412">Cuando **EnabledState** está establecido en 5 ("no aplicable"), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-412">When **EnabledState** is set to 5 ("Not Applicable"), then this property has no meaning.</span></span> <span data-ttu-id="ac1b0-413">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 12 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="ac1b0-413">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-414">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-414">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-415">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-415">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-417">El ancho de banda actual del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-417">The current bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="ac1b0-418">En el caso de los puertos que varían en ancho de banda o en aquellos casos en los que no se puede realizar una estimación precisa, esta propiedad debe contener el ancho de banda nominal.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-418">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="ac1b0-419">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)y siempre se establece en 1 mil millones.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-419">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-420">**Estado**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-420">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-421">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-423">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-424">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-424">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-425">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-425">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-426">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-427">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="ac1b0-427">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="ac1b0-428">Las entradas de esta matriz se correlacionan con las del mismo índice de matriz en **OperationalStatus**.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-428">Entries in this array are correlated with those at the same array index in **OperationalStatus**.</span></span> <span data-ttu-id="ac1b0-429">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en "OK".</span><span class="sxs-lookup"><span data-stu-id="ac1b0-429">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-430">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-430">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-431">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-431">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-432">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-433">El estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-433">The state of the logical device.</span></span> <span data-ttu-id="ac1b0-434">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-435">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-435">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-436">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-437">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-438">Calificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="ac1b0-438">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-439">La unidad de transmisión máxima (MTU) que se puede admitir, en bytes.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-439">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="ac1b0-440">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)y siempre se establece en 1500.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-440">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-441">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-441">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-442">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-443">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-444">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-444">The creation class name of the scoping system.</span></span> <span data-ttu-id="ac1b0-445">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="ac1b0-445">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-446">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-446">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-447">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-448">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-449">El identificador de la máquina virtual en forma de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="ac1b0-449">The virtual machine ID in **GUID** form.</span></span> <span data-ttu-id="ac1b0-450">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ac1b0-450">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-451">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-451">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-452">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-452">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-453">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-454">Fecha u hora de la última modificación del **EnabledState** del elemento.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-454">The date or time when the **EnabledState** of the element last changed.</span></span> <span data-ttu-id="ac1b0-455">Si el estado del elemento no ha cambiado y se rellena esta propiedad, debe establecerse en un valor de intervalo 0.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-455">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="ac1b0-456">Si se solicitó un cambio de estado, pero se rechazó o no se procesó todavía, la propiedad no se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-456">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="ac1b0-457">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-457">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-458">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-458">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-459">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-460">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-461">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-461">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="ac1b0-462">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-463">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-463">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-464">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-465">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-466">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-466">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="ac1b0-467">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-467">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac1b0-468">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-468">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1b0-469">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac1b0-470">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac1b0-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac1b0-471">En algunas circunstancias, un puerto lógico puede identificarse como un puerto de front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-471">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="ac1b0-472">Si no hay ninguna restricción sobre el uso del puerto, el valor debe establecerse en 4 ("no restringido").</span><span class="sxs-lookup"><span data-stu-id="ac1b0-472">If there is no restriction on the use of the port, then the value should be set to 4 ("Not Restricted").</span></span> <span data-ttu-id="ac1b0-473">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)) y siempre está establecida en 4 ("no restringido").</span><span class="sxs-lookup"><span data-stu-id="ac1b0-473">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) and is always set to 4 ("Not Restricted").</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac1b0-474">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac1b0-474">Remarks</span></span>

<span data-ttu-id="ac1b0-475">El acceso a la clase **MSVM \_ EmulatedEthernetPort** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="ac1b0-475">Access to the **Msvm\_EmulatedEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ac1b0-476">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ac1b0-476">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="ac1b0-477">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ac1b0-477">Examples</span></span>

<span data-ttu-id="ac1b0-478">Consulte [consultar objetos de red](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ac1b0-478">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac1b0-479">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac1b0-479">Requirements</span></span>



| <span data-ttu-id="ac1b0-480">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac1b0-480">Requirement</span></span> | <span data-ttu-id="ac1b0-481">Value</span><span class="sxs-lookup"><span data-stu-id="ac1b0-481">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac1b0-482">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac1b0-482">Minimum supported client</span></span><br/> | <span data-ttu-id="ac1b0-483">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac1b0-483">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ac1b0-484">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac1b0-484">Minimum supported server</span></span><br/> | <span data-ttu-id="ac1b0-485">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac1b0-485">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ac1b0-486">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ac1b0-486">Namespace</span></span><br/>                | <span data-ttu-id="ac1b0-487">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ac1b0-487">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ac1b0-488">MOF</span><span class="sxs-lookup"><span data-stu-id="ac1b0-488">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac1b0-489"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac1b0-489"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac1b0-490">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ac1b0-490">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac1b0-491"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ac1b0-491"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ac1b0-492">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac1b0-492">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac1b0-493">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-493">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="ac1b0-494">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="ac1b0-494">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

