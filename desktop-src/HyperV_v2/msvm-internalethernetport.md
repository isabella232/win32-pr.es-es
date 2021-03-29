---
description: Representa un puerto Ethernet interno (adaptador de red).
ms.assetid: 43277FA7-E040-49F2-A086-AF19B29D4F75
title: Clase Msvm_InternalEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InternalEthernetPort
- Msvm_InternalEthernetPort.SetPowerState
- Msvm_InternalEthernetPort.EnableDevice
- Msvm_InternalEthernetPort.OnlineDevice
- Msvm_InternalEthernetPort.QuiesceDevice
- Msvm_InternalEthernetPort.SaveProperties
- Msvm_InternalEthernetPort.RestoreProperties
- Msvm_InternalEthernetPort.InstanceID
- Msvm_InternalEthernetPort.Caption
- Msvm_InternalEthernetPort.Description
- Msvm_InternalEthernetPort.ElementName
- Msvm_InternalEthernetPort.InstallDate
- Msvm_InternalEthernetPort.Name
- Msvm_InternalEthernetPort.OperationalStatus
- Msvm_InternalEthernetPort.StatusDescriptions
- Msvm_InternalEthernetPort.Status
- Msvm_InternalEthernetPort.HealthState
- Msvm_InternalEthernetPort.CommunicationStatus
- Msvm_InternalEthernetPort.DetailedStatus
- Msvm_InternalEthernetPort.OperatingStatus
- Msvm_InternalEthernetPort.PrimaryStatus
- Msvm_InternalEthernetPort.EnabledState
- Msvm_InternalEthernetPort.OtherEnabledState
- Msvm_InternalEthernetPort.RequestedState
- Msvm_InternalEthernetPort.EnabledDefault
- Msvm_InternalEthernetPort.TimeOfLastStateChange
- Msvm_InternalEthernetPort.AvailableRequestedStates
- Msvm_InternalEthernetPort.TransitioningToState
- Msvm_InternalEthernetPort.SystemCreationClassName
- Msvm_InternalEthernetPort.SystemName
- Msvm_InternalEthernetPort.CreationClassName
- Msvm_InternalEthernetPort.DeviceID
- Msvm_InternalEthernetPort.PowerManagementSupported
- Msvm_InternalEthernetPort.PowerManagementCapabilities
- Msvm_InternalEthernetPort.Availability
- Msvm_InternalEthernetPort.StatusInfo
- Msvm_InternalEthernetPort.LastErrorCode
- Msvm_InternalEthernetPort.ErrorDescription
- Msvm_InternalEthernetPort.ErrorCleared
- Msvm_InternalEthernetPort.OtherIdentifyingInfo
- Msvm_InternalEthernetPort.PowerOnHours
- Msvm_InternalEthernetPort.TotalPowerOnHours
- Msvm_InternalEthernetPort.IdentifyingDescriptions
- Msvm_InternalEthernetPort.AdditionalAvailability
- Msvm_InternalEthernetPort.MaxQuiesceTime
- Msvm_InternalEthernetPort.MaxSpeed
- Msvm_InternalEthernetPort.RequestedSpeed
- Msvm_InternalEthernetPort.UsageRestriction
- Msvm_InternalEthernetPort.OtherPortType
- Msvm_InternalEthernetPort.Speed
- Msvm_InternalEthernetPort.OtherNetworkPortType
- Msvm_InternalEthernetPort.PortNumber
- Msvm_InternalEthernetPort.LinkTechnology
- Msvm_InternalEthernetPort.OtherLinkTechnology
- Msvm_InternalEthernetPort.PermanentAddress
- Msvm_InternalEthernetPort.FullDuplex
- Msvm_InternalEthernetPort.AutoSense
- Msvm_InternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_InternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_InternalEthernetPort.PortType
- Msvm_InternalEthernetPort.NetworkAddresses
- Msvm_InternalEthernetPort.MaxDataSize
- Msvm_InternalEthernetPort.Capabilities
- Msvm_InternalEthernetPort.CapabilityDescriptions
- Msvm_InternalEthernetPort.EnabledCapabilities
- Msvm_InternalEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a1441055fc7b86b97c69a40758236261b20f75c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810424"
---
# <a name="msvm_internalethernetport-class"></a><span data-ttu-id="4f4c4-103">MSVM \_ InternalEthernetPort (clase)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-103">Msvm\_InternalEthernetPort class</span></span>

<span data-ttu-id="4f4c4-104">Representa un puerto Ethernet interno (adaptador de red).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-104">Represents an internal Ethernet port (network adapter).</span></span> <span data-ttu-id="4f4c4-105">Este tipo de puerto Ethernet proporciona a las máquinas virtuales acceso al servidor de virtualización que ejecuta el software de red.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-105">This type of Ethernet port gives virtual machines access to the virtualization server running the networking software.</span></span> <span data-ttu-id="4f4c4-106">Los adaptadores de red internos permiten enrutar o filtrar el tráfico de red de las máquinas virtuales antes de dejar el sistema físico.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-106">The internal network adapters allow the virtual machines network traffic to be routed or filtered before leaving the physical system.</span></span>

<span data-ttu-id="4f4c4-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f4c4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f4c4-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Internal Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
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
  string   CreationClassName = "Msvm_InternalEthernetPort";
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
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  string   OtherPortType;
  uint64   Speed;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  uint64   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint16   PortType;
  string   NetworkAddresses[];
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="4f4c4-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4f4c4-109">Members</span></span>

<span data-ttu-id="4f4c4-110">La clase **MSVM \_ InternalEthernetPort** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4f4c4-110">The **Msvm\_InternalEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="4f4c4-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4f4c4-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4f4c4-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4f4c4-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4f4c4-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4f4c4-113">Methods</span></span>

<span data-ttu-id="4f4c4-114">La clase **MSVM \_ InternalEthernetPort** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-114">The **Msvm\_InternalEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="4f4c4-115">Método</span><span class="sxs-lookup"><span data-stu-id="4f4c4-115">Method</span></span>                                                                     | <span data-ttu-id="4f4c4-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f4c4-116">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="4f4c4-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-117">**EnableDevice**</span></span>                                                           | <span data-ttu-id="4f4c4-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4f4c4-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-119">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="4f4c4-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4f4c4-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-121">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="4f4c4-122">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="4f4c4-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-123">**RequestStateChange**</span></span>](msvm-internalethernetport-requeststatechange.md) | <span data-ttu-id="4f4c4-124">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="4f4c4-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-125">**Reset**</span></span>](msvm-internalethernetport-reset.md)                           | <span data-ttu-id="4f4c4-126">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="4f4c4-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-127">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="4f4c4-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4f4c4-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-129">**SaveProperties**</span></span>                                                         | <span data-ttu-id="4f4c4-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4f4c4-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-131">**SetPowerState**</span></span>                                                          | <span data-ttu-id="4f4c4-132">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4f4c4-133">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4f4c4-133">Properties</span></span>

<span data-ttu-id="4f4c4-134">La clase **MSVM \_ InternalEthernetPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-134">The **Msvm\_InternalEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f4c4-135">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-135">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-136">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-138">La unidad de transmisión máxima (MTU) activa o negociada que se puede admitir.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="4f4c4-139">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-141">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-143">Cualquier disponibilidad adicional y estado del dispositivo, más allá de lo especificado en la propiedad **Availability** .</span><span class="sxs-lookup"><span data-stu-id="4f4c4-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="4f4c4-144">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-145">**Percepción automática**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-146">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-148">Indica si el puerto de red es capaz de determinar automáticamente la velocidad u otras características de comunicación de los medios de red conectados.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="4f4c4-149">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-150">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-151">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-153">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-153">The primary availability and status of the device.</span></span> <span data-ttu-id="4f4c4-154">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-156">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-158">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="4f4c4-159">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual del objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4f4c4-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="4f4c4-160">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="4f4c4-161">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="4f4c4-162">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-164">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-166">Capacidades del puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-166">Capabilities of the Ethernet port.</span></span> <span data-ttu-id="4f4c4-167">Si se enumeran las funcionalidades de conmutación por error o de equilibrio de carga, también se debe definir una [**\_ SpareGroup CIM**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (conmutación por error) o un [**\_ ExtraCapacityGroup CIM**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (equilibrio de carga) para describir completamente la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-167">If failover or load balancing capabilities are listed, a [**CIM\_SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) or [**CIM\_ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="4f4c4-168">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-168">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="4f4c4-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Conmutación por error** (4)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Equilibrio** (5)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4f4c4-175">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-176">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-178">Una matriz de cadenas de forma libre que proporciona explicaciones más detalladas para cualquiera de las características de puerto Ethernet que se indican en la matriz de **capacidades** .</span><span class="sxs-lookup"><span data-stu-id="4f4c4-178">An array of free-form strings that provides more detailed explanations for any of the Ethernet port features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="4f4c4-179">Tenga en cuenta que cada entrada de esta matriz está relacionada con la entrada de la matriz de **capacidades** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-179">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="4f4c4-180">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-181">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-181">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-184">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-184">A short description of the object.</span></span> <span data-ttu-id="4f4c4-185">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-186">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-186">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-187">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-189">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-189">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="4f4c4-190">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4f4c4-191">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-192">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-192">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-193">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-195">El nombre de la clase o la subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-195">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="4f4c4-196">Cuando se usa con las otras propiedades de clave de esta clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-196">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="4f4c4-197">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-197">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-198">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-201">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-201">A description of the object.</span></span> <span data-ttu-id="4f4c4-202">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-203">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-203">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-204">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-206">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-206">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="4f4c4-207">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-207">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4f4c4-208">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-209">**ID**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-212">Una dirección u otra información de identificación utilizada para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-212">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="4f4c4-213">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y se establece en "Microsoft:*GUID* \\ *específico del dispositivo*".</span><span class="sxs-lookup"><span data-stu-id="4f4c4-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-215">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-216">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-217">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-217">A display name for the object.</span></span> <span data-ttu-id="4f4c4-218">Esta propiedad permite a cada instancia definir un nombre para mostrar además de las propiedades de clave, los datos de identidad y la información de descripción.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-218">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="4f4c4-219">Esta propiedad se hereda de [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) y se genera en función de la NIC presente en el host.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-219">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) and is generated based on the NIC present in the host.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-220">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-220">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-221">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-223">Especifica las funcionalidades que se habilitan en la lista de todos los admitidos, que se definen en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="4f4c4-223">Specifies which capabilities are enabled from the list of all supported ones, which are defined in the **Capabilities** array.</span></span> <span data-ttu-id="4f4c4-224">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-224">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="4f4c4-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Conmutación por error** (4)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Equilibrio** (5)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4f4c4-231">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-231">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-232">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-234">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-234">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="4f4c4-235">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-236">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-236">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-237">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-239">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-239">The enabled and disabled states of an element.</span></span> <span data-ttu-id="4f4c4-240">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-240">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-241">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-241">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-242">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-244">Indica si el error comunicado en la propiedad **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-244">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="4f4c4-245">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-246">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-246">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-249">Una cadena que proporciona más información sobre el error registrado en la propiedad **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-249">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="4f4c4-250">Esta propiedad se hereda de la propiedad de [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) property and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-251">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-251">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-252">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-254">Indica si el puerto está funcionando en modo dúplex completo.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-254">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="4f4c4-255">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-255">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-256">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-256">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-257">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-259">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-259">The current health of the element.</span></span> <span data-ttu-id="4f4c4-260">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-260">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="4f4c4-261">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-262">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-262">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-263">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-263">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-265">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="4f4c4-265">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="4f4c4-266">Cada entrada de esta matriz está relacionada con la entrada de la matriz de propiedades **OtherIdentifyingInfo** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-266">Each entry of this array is related to the entry in the **OtherIdentifyingInfo** property array that is located at the same index.</span></span> <span data-ttu-id="4f4c4-267">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-269">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-271">Un valor de **fecha y hora** que indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-271">A **datetime** value that indicates when the object was installed.</span></span> <span data-ttu-id="4f4c4-272">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-272">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="4f4c4-273">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-274">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-274">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-275">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-277">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-277">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-278">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-278">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4f4c4-279">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-279">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-280">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-280">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-281">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-281">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-283">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-283">The last error code reported by the logical device.</span></span> <span data-ttu-id="4f4c4-284">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-284">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-285">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-285">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-286">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-288">Tipos de vínculos.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-288">The types of links.</span></span> <span data-ttu-id="4f4c4-289">Cuando se establece en 1 (otro), la propiedad relacionada **OtherLinkTechnology** contiene una descripción de cadena del tipo de vínculo.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-289">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="4f4c4-290">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-290">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="4f4c4-291">Value</span><span class="sxs-lookup"><span data-stu-id="4f4c4-291">Value</span></span>                                                                        | <span data-ttu-id="4f4c4-292">Significado</span><span class="sxs-lookup"><span data-stu-id="4f4c4-292">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="4f4c4-293"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4f4c4-293"><dt>2</dt></span></span> </dl> | <span data-ttu-id="4f4c4-294">Ethernet</span><span class="sxs-lookup"><span data-stu-id="4f4c4-294">Ethernet</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4f4c4-295">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-295">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-296">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-298">El tamaño máximo del campo de información (no MAC) que se recibirá o transmitirá.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-298">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="4f4c4-299">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-299">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-300">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-300">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-301">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-303">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-303">This property has been deprecated.</span></span> <span data-ttu-id="4f4c4-304">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-305">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-305">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-306">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-306">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-308">Ancho de banda máximo del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-308">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="4f4c4-309">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-309">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-310">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-310">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-311">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-313">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-313">The label by which the object is known.</span></span> <span data-ttu-id="4f4c4-314">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-314">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="4f4c4-315">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-316">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-316">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-317">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-319">Las direcciones MAC Ethernet/802.3 formateadas como doce dígitos hexadecimales (por ejemplo, "010203040506"), donde cada par representa uno de los seis octetos de la dirección MAC en orden de bits canónico (el bit de dirección de grupo se encuentra en el bit de orden inferior del primer carácter de la cadena). Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-319">The Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string.) This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-321">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-323">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="4f4c4-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="4f4c4-324">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4f4c4-325">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-326">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-326">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-327">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-327">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-329">Estados actuales del elemento.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-329">The current statuses of the element.</span></span> <span data-ttu-id="4f4c4-330">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-330">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-331">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-331">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-332">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-332">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-334">Matriz de cadenas de forma libre que proporciona explicaciones más detalladas para cualquiera de las capacidades habilitadas que se especifican como 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-334">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other).</span></span> <span data-ttu-id="4f4c4-335">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-335">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-336">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-336">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-337">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-339">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro). Esta propiedad debe establecerse en **null** cuando la propiedad **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-339">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other.) This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="4f4c4-340">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-340">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-342">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-344">Los datos, además de la información de identificador de dispositivo, que se pueden usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-344">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="4f4c4-345">Por ejemplo, puede usar esta propiedad para contener el nombre para mostrar del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-345">For example, you could use this property to hold the operating system's display name for the device.</span></span> <span data-ttu-id="4f4c4-346">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-347">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-347">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-348">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-350">Valor de cadena que describe la propiedad **LinkTechnology** cuando se establece en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-350">A string value that describes the **LinkTechnology** property when it is set to 1 (Other).</span></span> <span data-ttu-id="4f4c4-351">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-351">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-352">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-352">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-353">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-355">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-355">This property is deprecated.</span></span> <span data-ttu-id="4f4c4-356">Use la propiedad **portType** .</span><span class="sxs-lookup"><span data-stu-id="4f4c4-356">Use the **PortType** property.</span></span> <span data-ttu-id="4f4c4-357">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-357">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<span data-ttu-id="4f4c4-358">Descripción desusada: el tipo de módulo, cuando la propiedad **portType** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-358">Deprecated description: The type of module, when the **PortType** property is set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-359">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-359">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-360">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-362">El tipo de módulo, cuando la propiedad **portType** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-362">The type of module, when the **PortType** property is set to 1 (Other).</span></span> <span data-ttu-id="4f4c4-363">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4f4c4-363">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) .</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-364">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-364">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-365">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-367">La dirección de red que está codificada en un puerto.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-367">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="4f4c4-368">Esta dirección se puede cambiar mediante una actualización de firmware o una configuración de software.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-368">This address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="4f4c4-369">Cuando se realiza este cambio, el campo debe actualizarse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-369">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="4f4c4-370">Debe dejarse en blanco si no existe ninguna dirección codificada para el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-370">This should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="4f4c4-371">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-371">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-372">**NúmeroDePuerto**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-372">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-373">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-374">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-375">Los puertos de red suelen numerarse con respecto a un módulo lógico o a un elemento de red.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-375">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="4f4c4-376">Este valor es 1 para las NIC emuladas, 0 para todas las demás.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-376">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="4f4c4-377">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-377">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-378">**PortType**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-378">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-379">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-381">Modo específico que está habilitado actualmente para el puerto.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-381">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="4f4c4-382">Cuando se establece en 1 (otro), la propiedad relacionada **OtherPortType** contiene una descripción de cadena del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-382">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="4f4c4-383">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-383">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="4f4c4-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 cobre 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 fibra 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-uevo** (111)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (16000 65535)</span><span class="sxs-lookup"><span data-stu-id="4f4c4-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4f4c4-406">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-406">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-407">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-407">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-409">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-409">The power management capabilities of the device.</span></span> <span data-ttu-id="4f4c4-410">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-411">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-411">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-412">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-414">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-414">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="4f4c4-415">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-415">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-416">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-416">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-417">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-417">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-418">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-419">El número de horas consecutivas que este dispositivo ha estado encendido desde su último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-419">The number of consecutive hours that this device has been powered, since its last power cycle.</span></span> <span data-ttu-id="4f4c4-420">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-421">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-421">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-422">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-423">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-424">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-424">Provides high level status information.</span></span> <span data-ttu-id="4f4c4-425">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-425">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="4f4c4-426">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-426">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4f4c4-427">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-428">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-428">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-429">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-429">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-430">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-431">Ancho de banda solicitado del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-431">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="4f4c4-432">El ancho de banda real se registra en la propiedad **Speed** .</span><span class="sxs-lookup"><span data-stu-id="4f4c4-432">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="4f4c4-433">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-434">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-434">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-435">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-436">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-437">Último estado solicitado o deseado para el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-437">The last requested or desired state for the management service.</span></span> <span data-ttu-id="4f4c4-438">Cuando la propiedad **EnabledState** está establecida en 5 (no es aplicable), esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-438">When the **EnabledState** property is set to 5 (Not Applicable), then this property has no meaning.</span></span> <span data-ttu-id="4f4c4-439">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-439">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-440">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-440">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-441">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-441">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-442">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-442">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-443">Calificadores: **invalidación**, **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="4f4c4-443">Qualifiers: **Override**, **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-444">El ancho de banda actual del puerto en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-444">The current bandwidth of the port in bits per second.</span></span> <span data-ttu-id="4f4c4-445">En el caso de los puertos que varían en ancho de banda o en aquellos casos en los que no se puede realizar una estimación precisa, esta propiedad debe contener el ancho de banda nominal.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-445">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="4f4c4-446">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-446">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-447">**Estado**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-447">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-448">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-449">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-450">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-450">The current status of the object.</span></span> <span data-ttu-id="4f4c4-451">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-451">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-452">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-452">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-453">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-453">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-454">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-455">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="4f4c4-455">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="4f4c4-456">Las entradas de esta matriz se correlacionan con las del mismo índice de matriz en **OperationalStatus**.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-456">Entries in this array are correlated with those at the same array index in **OperationalStatus**.</span></span> <span data-ttu-id="4f4c4-457">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-457">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-458">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-458">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-459">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-460">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-461">El estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-461">The state of the logical device.</span></span> <span data-ttu-id="4f4c4-462">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-463">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-463">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-464">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-464">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-465">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-466">La unidad de transmisión máxima (MTU) que se puede admitir.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-466">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="4f4c4-467">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-467">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-468">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-468">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-469">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-470">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-471">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-471">The scoping system's creation class name.</span></span> <span data-ttu-id="4f4c4-472">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se admite</span><span class="sxs-lookup"><span data-stu-id="4f4c4-472">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not supported</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-474">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-475">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-476">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-476">The name of the scoping system.</span></span> <span data-ttu-id="4f4c4-477">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-477">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-478">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-478">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-479">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-479">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-480">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-481">Fecha u hora en que se cambió por última vez la propiedad **EnabledState** del elemento.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-481">The date or time when the **EnabledState** property of the element last changed.</span></span> <span data-ttu-id="4f4c4-482">Si el estado del elemento no ha cambiado y se rellena esta propiedad, debe establecerse en un valor de intervalo 0.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-482">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="4f4c4-483">Si se solicitó un cambio de estado, pero se rechazó o no se procesó todavía, la propiedad no se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-483">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="4f4c4-484">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-484">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-485">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-485">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-486">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-487">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-488">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-488">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="4f4c4-489">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-489">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-490">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-490">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-491">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-491">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-492">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-493">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-493">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="4f4c4-494">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-494">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c4-495">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-495">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4c4-496">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-496">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4c4-497">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4c4-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4c4-498">En algunas circunstancias, un puerto lógico puede identificarse como un puerto de front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-498">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="4f4c4-499">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-499">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="4f4c4-500">Value</span><span class="sxs-lookup"><span data-stu-id="4f4c4-500">Value</span></span>                                                                        | <span data-ttu-id="4f4c4-501">Significado</span><span class="sxs-lookup"><span data-stu-id="4f4c4-501">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="4f4c4-502"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4f4c4-502"><dt>4</dt></span></span> </dl> | <span data-ttu-id="4f4c4-503">No restringido</span><span class="sxs-lookup"><span data-stu-id="4f4c4-503">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f4c4-504">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f4c4-504">Remarks</span></span>

<span data-ttu-id="4f4c4-505">El acceso a la clase **MSVM \_ InternalEthernetPort** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="4f4c4-505">Access to the **Msvm\_InternalEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4f4c4-506">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-506">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="4f4c4-507">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4f4c4-507">Examples</span></span>

<span data-ttu-id="4f4c4-508">Consulte [consultar objetos de red](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4f4c4-508">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f4c4-509">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f4c4-509">Requirements</span></span>



| <span data-ttu-id="4f4c4-510">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f4c4-510">Requirement</span></span> | <span data-ttu-id="4f4c4-511">Value</span><span class="sxs-lookup"><span data-stu-id="4f4c4-511">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f4c4-512">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f4c4-512">Minimum supported client</span></span><br/> | <span data-ttu-id="4f4c4-513">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f4c4-513">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4f4c4-514">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f4c4-514">Minimum supported server</span></span><br/> | <span data-ttu-id="4f4c4-515">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f4c4-515">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f4c4-516">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4f4c4-516">Namespace</span></span><br/>                | <span data-ttu-id="4f4c4-517">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4f4c4-517">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4f4c4-518">MOF</span><span class="sxs-lookup"><span data-stu-id="4f4c4-518">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f4c4-519"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f4c4-519"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f4c4-520">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f4c4-520">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f4c4-521"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4f4c4-521"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4f4c4-522">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f4c4-522">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f4c4-523">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-523">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="4f4c4-524">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="4f4c4-524">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

