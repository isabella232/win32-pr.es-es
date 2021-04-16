---
description: Representa un puerto en el modificador.
ms.assetid: a2637e53-6b28-41ad-bef9-d3a14b6cf727
title: Clase Msvm_EthernetSwitchPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPort
- Msvm_EthernetSwitchPort.SetPowerState
- Msvm_EthernetSwitchPort.EnableDevice
- Msvm_EthernetSwitchPort.OnlineDevice
- Msvm_EthernetSwitchPort.QuiesceDevice
- Msvm_EthernetSwitchPort.SaveProperties
- Msvm_EthernetSwitchPort.RestoreProperties
- Msvm_EthernetSwitchPort.InstanceID
- Msvm_EthernetSwitchPort.Caption
- Msvm_EthernetSwitchPort.Description
- Msvm_EthernetSwitchPort.ElementName
- Msvm_EthernetSwitchPort.InstallDate
- Msvm_EthernetSwitchPort.Name
- Msvm_EthernetSwitchPort.OperationalStatus
- Msvm_EthernetSwitchPort.StatusDescriptions
- Msvm_EthernetSwitchPort.Status
- Msvm_EthernetSwitchPort.HealthState
- Msvm_EthernetSwitchPort.CommunicationStatus
- Msvm_EthernetSwitchPort.DetailedStatus
- Msvm_EthernetSwitchPort.OperatingStatus
- Msvm_EthernetSwitchPort.PrimaryStatus
- Msvm_EthernetSwitchPort.EnabledState
- Msvm_EthernetSwitchPort.OtherEnabledState
- Msvm_EthernetSwitchPort.RequestedState
- Msvm_EthernetSwitchPort.EnabledDefault
- Msvm_EthernetSwitchPort.TimeOfLastStateChange
- Msvm_EthernetSwitchPort.AvailableRequestedStates
- Msvm_EthernetSwitchPort.TransitioningToState
- Msvm_EthernetSwitchPort.SystemCreationClassName
- Msvm_EthernetSwitchPort.SystemName
- Msvm_EthernetSwitchPort.CreationClassName
- Msvm_EthernetSwitchPort.DeviceID
- Msvm_EthernetSwitchPort.PowerManagementSupported
- Msvm_EthernetSwitchPort.PowerManagementCapabilities
- Msvm_EthernetSwitchPort.Availability
- Msvm_EthernetSwitchPort.StatusInfo
- Msvm_EthernetSwitchPort.LastErrorCode
- Msvm_EthernetSwitchPort.ErrorDescription
- Msvm_EthernetSwitchPort.ErrorCleared
- Msvm_EthernetSwitchPort.OtherIdentifyingInfo
- Msvm_EthernetSwitchPort.PowerOnHours
- Msvm_EthernetSwitchPort.TotalPowerOnHours
- Msvm_EthernetSwitchPort.IdentifyingDescriptions
- Msvm_EthernetSwitchPort.AdditionalAvailability
- Msvm_EthernetSwitchPort.MaxQuiesceTime
- Msvm_EthernetSwitchPort.Speed
- Msvm_EthernetSwitchPort.MaxSpeed
- Msvm_EthernetSwitchPort.RequestedSpeed
- Msvm_EthernetSwitchPort.UsageRestriction
- Msvm_EthernetSwitchPort.PortType
- Msvm_EthernetSwitchPort.OtherPortType
- Msvm_EthernetSwitchPort.OtherNetworkPortType
- Msvm_EthernetSwitchPort.PortNumber
- Msvm_EthernetSwitchPort.LinkTechnology
- Msvm_EthernetSwitchPort.OtherLinkTechnology
- Msvm_EthernetSwitchPort.PermanentAddress
- Msvm_EthernetSwitchPort.NetworkAddresses
- Msvm_EthernetSwitchPort.FullDuplex
- Msvm_EthernetSwitchPort.AutoSense
- Msvm_EthernetSwitchPort.SupportedMaximumTransmissionUnit
- Msvm_EthernetSwitchPort.ActiveMaximumTransmissionUnit
- Msvm_EthernetSwitchPort.MaxDataSize
- Msvm_EthernetSwitchPort.Capabilities
- Msvm_EthernetSwitchPort.CapabilityDescriptions
- Msvm_EthernetSwitchPort.EnabledCapabilities
- Msvm_EthernetSwitchPort.OtherEnabledCapabilities
- Msvm_EthernetSwitchPort.VMQOffloadUsage
- Msvm_EthernetSwitchPort.IOVOffloadUsage
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76c43cbe8dd053808085346b1874781f354b20dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670027"
---
# <a name="msvm_ethernetswitchport-class"></a><span data-ttu-id="81d3c-103">MSVM \_ EthernetSwitchPort (clase)</span><span class="sxs-lookup"><span data-stu-id="81d3c-103">Msvm\_EthernetSwitchPort class</span></span>

<span data-ttu-id="81d3c-104">Representa un puerto en el modificador.</span><span class="sxs-lookup"><span data-stu-id="81d3c-104">Represents a port on the switch.</span></span>

<span data-ttu-id="81d3c-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="81d3c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="81d3c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81d3c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Switch Port";
  string   Description = "Microsoft Virtual Ethernet Switch Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[];
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
  string   SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string   SystemName;
  string   CreationClassName = "Msvm_EthernetSwitchPort";
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
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint32   MaxDataSize;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
  uint32   VMQOffloadUsage;
  uint32   IOVOffloadUsage;
};
```

## <a name="members"></a><span data-ttu-id="81d3c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="81d3c-107">Members</span></span>

<span data-ttu-id="81d3c-108">La clase **MSVM \_ EthernetSwitchPort** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="81d3c-108">The **Msvm\_EthernetSwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="81d3c-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="81d3c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="81d3c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81d3c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="81d3c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="81d3c-111">Methods</span></span>

<span data-ttu-id="81d3c-112">La clase **MSVM \_ EthernetSwitchPort** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="81d3c-112">The **Msvm\_EthernetSwitchPort** class has these methods.</span></span>



| <span data-ttu-id="81d3c-113">Método</span><span class="sxs-lookup"><span data-stu-id="81d3c-113">Method</span></span>                                                                   | <span data-ttu-id="81d3c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="81d3c-114">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="81d3c-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="81d3c-115">**EnableDevice**</span></span>                                                         | <span data-ttu-id="81d3c-116">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="81d3c-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="81d3c-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="81d3c-117">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="81d3c-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="81d3c-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="81d3c-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="81d3c-119">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="81d3c-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="81d3c-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="81d3c-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="81d3c-121">**RequestStateChange**</span></span>](msvm-ethernetswitchport-requeststatechange.md) | <span data-ttu-id="81d3c-122">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="81d3c-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="81d3c-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="81d3c-123">**Reset**</span></span>](msvm-ethernetswitchport-reset.md)                           | <span data-ttu-id="81d3c-124">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="81d3c-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="81d3c-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="81d3c-125">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="81d3c-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="81d3c-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="81d3c-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="81d3c-127">**SaveProperties**</span></span>                                                       | <span data-ttu-id="81d3c-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="81d3c-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="81d3c-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="81d3c-129">**SetPowerState**</span></span>                                                        | <span data-ttu-id="81d3c-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="81d3c-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="81d3c-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81d3c-131">Properties</span></span>

<span data-ttu-id="81d3c-132">La clase **MSVM \_ EthernetSwitchPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="81d3c-132">The **Msvm\_EthernetSwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81d3c-133">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="81d3c-133">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-134">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81d3c-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-136">Calificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="81d3c-136">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-137">La unidad de transmisión máxima (MTU) activa o negociada que se puede admitir, en bytes.</span><span class="sxs-lookup"><span data-stu-id="81d3c-137">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="81d3c-138">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="81d3c-138">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="81d3c-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-140">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-142">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81d3c-142">Any additional availability and status of the device.</span></span> <span data-ttu-id="81d3c-143">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81d3c-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-144">**Percepción automática**</span><span class="sxs-lookup"><span data-stu-id="81d3c-144">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-145">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="81d3c-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-147">Indica si el puerto es capaz de determinar automáticamente la velocidad u otras características de comunicación de los medios de red conectados.</span><span class="sxs-lookup"><span data-stu-id="81d3c-147">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="81d3c-148">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="81d3c-148">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-149">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="81d3c-149">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-150">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-152">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81d3c-152">The primary availability and status of the device.</span></span> <span data-ttu-id="81d3c-153">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81d3c-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="81d3c-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-155">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-157">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="81d3c-157">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="81d3c-158">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81d3c-158">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="81d3c-159">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="81d3c-159">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="81d3c-160">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="81d3c-160">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="81d3c-161">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81d3c-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="81d3c-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="81d3c-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="81d3c-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="81d3c-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="81d3c-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="81d3c-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="81d3c-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="81d3c-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="81d3c-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="81d3c-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="81d3c-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="81d3c-172">)</span><span class="sxs-lookup"><span data-stu-id="81d3c-172">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81d3c-173">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="81d3c-173">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-174">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-174">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-176">Matriz que especifica las funciones del puerto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-176">An array that specifies the capabilities of the port.</span></span> <span data-ttu-id="81d3c-177">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="81d3c-177">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="81d3c-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="81d3c-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="81d3c-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-180"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="81d3c-180"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-181"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="81d3c-181"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-182"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Conmutación por error** (4)</span><span class="sxs-lookup"><span data-stu-id="81d3c-182"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-183"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**Equilibrio** (5)</span><span class="sxs-lookup"><span data-stu-id="81d3c-183"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81d3c-184">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="81d3c-184">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-185">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="81d3c-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-187">Matriz de cadenas de forma libre que proporciona explicaciones más detalladas para las características de Puerto incluidas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="81d3c-187">An array of free-form strings that provides more detailed explanations for the port features that are contained in the **Capabilities** array.</span></span> <span data-ttu-id="81d3c-188">Cada entrada de esta matriz está relacionada con la entrada correspondiente en la matriz de **capacidades** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="81d3c-188">Each entry of this array is related to the corresponding entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="81d3c-189">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="81d3c-189">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-190">**Caption**</span><span class="sxs-lookup"><span data-stu-id="81d3c-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-193">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-193">A short description of the object.</span></span> <span data-ttu-id="81d3c-194">Esta propiedad se hereda de la clase [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) y siempre se establece en "Puerto de conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="81d3c-194">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class, and it is always set to "Ethernet Switch Port".</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-195">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="81d3c-195">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-196">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-198">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="81d3c-198">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="81d3c-199">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="81d3c-199">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="81d3c-200">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81d3c-200">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-201">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="81d3c-201">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-204">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="81d3c-204">The scoping system's creation class name.</span></span> <span data-ttu-id="81d3c-205">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "MSVM \_ EthernetSwitchPort".</span><span class="sxs-lookup"><span data-stu-id="81d3c-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-206">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="81d3c-206">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-209">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-209">A description of the object.</span></span> <span data-ttu-id="81d3c-210">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "Puerto de conmutador Ethernet Virtual de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="81d3c-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Ethernet Switch Port".</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-211">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="81d3c-211">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-212">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-214">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="81d3c-214">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="81d3c-215">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="81d3c-215">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="81d3c-216">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81d3c-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-217">**ID**</span><span class="sxs-lookup"><span data-stu-id="81d3c-217">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-218">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-220">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81d3c-220">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="81d3c-221">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="81d3c-221">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-222">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="81d3c-222">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-225">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-225">A display name for the object.</span></span> <span data-ttu-id="81d3c-226">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="81d3c-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-227">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="81d3c-227">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-228">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-228">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-230">Especifica las funcionalidades que se habilitan en la lista de todas las funcionalidades admitidas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="81d3c-230">Specifies which capabilities are enabled from the list of all supported capabilities in the **Capabilities** array.</span></span> <span data-ttu-id="81d3c-231">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="81d3c-231">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="81d3c-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="81d3c-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="81d3c-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-234"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="81d3c-234"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-235"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="81d3c-235"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-236"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Conmutación por error** (4)</span><span class="sxs-lookup"><span data-stu-id="81d3c-236"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-237"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**Equilibrio** (5)</span><span class="sxs-lookup"><span data-stu-id="81d3c-237"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81d3c-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="81d3c-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-239">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-241">Configuración predeterminada o de inicio de un administrador para la propiedad **EnabledState** de un elemento.</span><span class="sxs-lookup"><span data-stu-id="81d3c-241">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="81d3c-242">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="81d3c-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-243">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="81d3c-243">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-244">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-246">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="81d3c-246">The enabled and disabled states of an element.</span></span> <span data-ttu-id="81d3c-247">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="81d3c-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="81d3c-248">Value</span><span class="sxs-lookup"><span data-stu-id="81d3c-248">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="81d3c-249">Significado</span><span class="sxs-lookup"><span data-stu-id="81d3c-249">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="81d3c-250"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="81d3c-250"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="81d3c-251">El elemento se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="81d3c-251">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="81d3c-252"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="81d3c-252"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="81d3c-253">El elemento está desactivado.</span><span class="sxs-lookup"><span data-stu-id="81d3c-253">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="81d3c-254">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="81d3c-254">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-255">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="81d3c-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-257">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="81d3c-257">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="81d3c-258">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81d3c-258">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-259">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="81d3c-259">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-260">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-262">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="81d3c-262">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="81d3c-263">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81d3c-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-264">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="81d3c-264">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-265">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="81d3c-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-266">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-267">Indica si el puerto está funcionando en modo dúplex completo.</span><span class="sxs-lookup"><span data-stu-id="81d3c-267">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="81d3c-268">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="81d3c-268">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-269">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="81d3c-269">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-270">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-270">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-271">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-272">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="81d3c-272">The current health of the element.</span></span> <span data-ttu-id="81d3c-273">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="81d3c-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-274">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="81d3c-274">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-275">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="81d3c-275">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-277">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="81d3c-277">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="81d3c-278">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81d3c-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-279">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="81d3c-279">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-280">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="81d3c-280">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-282">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-282">The date and time when the object was installed.</span></span> <span data-ttu-id="81d3c-283">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="81d3c-283">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="81d3c-284">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81d3c-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-285">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="81d3c-285">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-288">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="81d3c-288">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-289">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="81d3c-289">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="81d3c-290">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="81d3c-290">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-291">**IOVOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="81d3c-291">**IOVOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-292">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81d3c-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-294">El uso de la descarga actual de la virtualización de e/s (IOV) en este puerto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-294">The current I/O virtualization (IOV) offload usage on this port.</span></span> <span data-ttu-id="81d3c-295">El uso es la cantidad de recursos de IOV en uso en el puerto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-295">The usage is the amount of IOV resources in use on the port.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-296">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="81d3c-296">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-297">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81d3c-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-299">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81d3c-299">The last error code reported by the logical device.</span></span> <span data-ttu-id="81d3c-300">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81d3c-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-301">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="81d3c-301">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-302">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-304">Especifica el tipo de tecnología de vínculo para el puerto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-304">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="81d3c-305">Cuando se establece en 1 (otro), la propiedad **OtherLinkTechnology** contiene una descripción de cadena del tipo de vínculo.</span><span class="sxs-lookup"><span data-stu-id="81d3c-305">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="81d3c-306">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="81d3c-306">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="81d3c-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="81d3c-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-308"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="81d3c-308"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-309"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="81d3c-309"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-310"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="81d3c-310"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-311"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="81d3c-311"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-312"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="81d3c-312"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-313"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="81d3c-313"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-314"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="81d3c-314"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-315"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="81d3c-315"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-316"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarrojos** (9)</span><span class="sxs-lookup"><span data-stu-id="81d3c-316"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-317"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="81d3c-317"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-318"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**LAN inalámbrica** (11)</span><span class="sxs-lookup"><span data-stu-id="81d3c-318"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81d3c-319">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="81d3c-319">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-320">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81d3c-320">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-322">El tamaño máximo del campo de información (no MAC) que se recibirá o transmitirá.</span><span class="sxs-lookup"><span data-stu-id="81d3c-322">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="81d3c-323">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)y siempre se establece en 1500.</span><span class="sxs-lookup"><span data-stu-id="81d3c-323">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-324">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="81d3c-324">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-325">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81d3c-325">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-327">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="81d3c-327">This property has been deprecated.</span></span> <span data-ttu-id="81d3c-328">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81d3c-328">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-329">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="81d3c-329">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-330">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81d3c-330">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-332">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="81d3c-332">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-333">Ancho de banda máximo del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="81d3c-333">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="81d3c-334">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81d3c-334">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-335">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="81d3c-335">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-336">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-338">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-338">The label by which the object is known.</span></span> <span data-ttu-id="81d3c-339">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81d3c-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-340">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="81d3c-340">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-341">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="81d3c-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-343">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="81d3c-343">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-344">Una matriz de cadenas que contienen las direcciones MAC para el puerto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-344">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="81d3c-345">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="81d3c-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-346">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="81d3c-346">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-347">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-347">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-349">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="81d3c-349">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="81d3c-350">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="81d3c-350">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="81d3c-351">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81d3c-351">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-352">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="81d3c-352">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-353">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-353">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-355">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-355">The current statuses of the object.</span></span> <span data-ttu-id="81d3c-356">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="81d3c-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-357">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="81d3c-357">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-358">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="81d3c-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-360">Matriz de cadenas de forma libre que proporciona explicaciones más detalladas para cualquiera de las capacidades habilitadas que se especifican como 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="81d3c-360">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other).</span></span> <span data-ttu-id="81d3c-361">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="81d3c-361">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-362">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="81d3c-362">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-363">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-364">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-365">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="81d3c-365">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="81d3c-366">Esta propiedad debe establecerse en **null** cuando la propiedad **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="81d3c-366">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="81d3c-367">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="81d3c-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-368">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="81d3c-368">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-369">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="81d3c-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-371">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81d3c-371">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="81d3c-372">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81d3c-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-373">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="81d3c-373">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-374">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-376">Un valor de cadena que describe **LinkTechnology** cuando se establece en 1, (otro).</span><span class="sxs-lookup"><span data-stu-id="81d3c-376">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="81d3c-377">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="81d3c-377">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-378">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="81d3c-378">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-379">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-381">El uso de esta propiedad está en desuso en lugar de la propiedad **portType** .</span><span class="sxs-lookup"><span data-stu-id="81d3c-381">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="81d3c-382">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="81d3c-382">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-383">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="81d3c-383">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-384">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-385">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-386">Describe el tipo de módulo, cuando **portType** está establecido en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="81d3c-386">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="81d3c-387">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81d3c-387">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-388">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="81d3c-388">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-389">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-391">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="81d3c-391">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-392">La dirección de red que está codificada en un puerto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-392">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="81d3c-393">Esta dirección codificada se puede cambiar mediante una actualización de firmware o una configuración de software.</span><span class="sxs-lookup"><span data-stu-id="81d3c-393">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="81d3c-394">Cuando se realiza este cambio, el campo debe actualizarse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="81d3c-394">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="81d3c-395">Esta propiedad debe ser **null** si no existe ninguna dirección codificada para el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="81d3c-395">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="81d3c-396">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="81d3c-396">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-397">**NúmeroDePuerto**</span><span class="sxs-lookup"><span data-stu-id="81d3c-397">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-398">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-400">El número de puerto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-400">The port number.</span></span> <span data-ttu-id="81d3c-401">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="81d3c-401">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-402">**PortType**</span><span class="sxs-lookup"><span data-stu-id="81d3c-402">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-403">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-405">Modo específico que está habilitado actualmente para el puerto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-405">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="81d3c-406">Cuando se establece en 1 (otro), la propiedad **OtherPortType** relacionada contiene una descripción de cadena del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-406">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="81d3c-407">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81d3c-407">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="81d3c-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="81d3c-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-409"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="81d3c-409"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-410"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 cobre 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="81d3c-410"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-411"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="81d3c-411"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-412"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="81d3c-412"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-413"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="81d3c-413"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-414"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="81d3c-414"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-415"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="81d3c-415"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-416"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="81d3c-416"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-417"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 fibra 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="81d3c-417"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-418"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="81d3c-418"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-419"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="81d3c-419"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-420"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="81d3c-420"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-421"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="81d3c-421"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-422"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="81d3c-422"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-423"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="81d3c-423"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-424"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="81d3c-424"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-425"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="81d3c-425"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-426"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="81d3c-426"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-427"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="81d3c-427"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-428"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-uevo** (111)</span><span class="sxs-lookup"><span data-stu-id="81d3c-428"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-429"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="81d3c-429"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81d3c-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="81d3c-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-431">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-432">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-433">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81d3c-433">The power management capabilities of the device.</span></span> <span data-ttu-id="81d3c-434">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81d3c-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-435">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="81d3c-435">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-436">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="81d3c-436">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-437">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-438">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="81d3c-438">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="81d3c-439">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81d3c-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-440">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="81d3c-440">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-441">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81d3c-441">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-442">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-443">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="81d3c-443">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="81d3c-444">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81d3c-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-445">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="81d3c-445">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-446">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-447">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-448">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="81d3c-448">Provides high level status information.</span></span> <span data-ttu-id="81d3c-449">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="81d3c-449">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="81d3c-450">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="81d3c-450">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="81d3c-451">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81d3c-451">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-452">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="81d3c-452">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-453">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81d3c-453">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-454">Tipo de acceso: solo escritura</span><span class="sxs-lookup"><span data-stu-id="81d3c-454">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-455">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="81d3c-455">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-456">Ancho de banda solicitado del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="81d3c-456">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="81d3c-457">El ancho de banda real se registra en la propiedad **Speed** .</span><span class="sxs-lookup"><span data-stu-id="81d3c-457">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="81d3c-458">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81d3c-458">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-459">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="81d3c-459">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-460">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-460">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-461">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-462">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="81d3c-462">The last requested or desired state for the element.</span></span> <span data-ttu-id="81d3c-463">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="81d3c-463">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-464">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="81d3c-464">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-465">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81d3c-465">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-466">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-467">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="81d3c-467">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-468">Ancho de banda del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="81d3c-468">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="81d3c-469">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81d3c-469">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-470">**Estado**</span><span class="sxs-lookup"><span data-stu-id="81d3c-470">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-471">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-472">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-473">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-473">The current status of the object.</span></span> <span data-ttu-id="81d3c-474">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81d3c-474">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-475">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="81d3c-475">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-476">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="81d3c-476">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-477">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-478">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="81d3c-478">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="81d3c-479">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="81d3c-479">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-480">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="81d3c-480">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-481">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-481">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-482">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-483">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81d3c-483">The current state of the logical device.</span></span> <span data-ttu-id="81d3c-484">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81d3c-484">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-485">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="81d3c-485">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-486">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81d3c-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-487">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-488">Calificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="81d3c-488">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-489">La unidad de transmisión máxima (MTU) que se puede admitir, en bytes.</span><span class="sxs-lookup"><span data-stu-id="81d3c-489">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="81d3c-490">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="81d3c-490">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-491">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="81d3c-491">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-492">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-493">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-494">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="81d3c-494">The scoping system's creation class name.</span></span> <span data-ttu-id="81d3c-495">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "MSVM \_ VirtualEthernetSwitch".</span><span class="sxs-lookup"><span data-stu-id="81d3c-495">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-496">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="81d3c-496">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-497">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81d3c-497">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-498">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-498">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-499">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="81d3c-499">The scoping system's name.</span></span> <span data-ttu-id="81d3c-500">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="81d3c-500">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-501">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="81d3c-501">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-502">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="81d3c-502">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-503">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-504">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="81d3c-504">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="81d3c-505">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="81d3c-505">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-506">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="81d3c-506">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-507">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81d3c-507">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-508">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-509">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81d3c-509">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="81d3c-510">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81d3c-510">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-511">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="81d3c-511">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-512">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-512">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-513">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-514">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="81d3c-514">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="81d3c-515">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="81d3c-515">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81d3c-516">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="81d3c-516">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-517">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d3c-517">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-518">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-519">En algunas circunstancias, un puerto lógico puede identificarse como un puerto de front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="81d3c-519">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="81d3c-520">Un ejemplo de esta situación sería una matriz de almacenamiento que podría tener puertos back-end para comunicarse con las unidades de disco y los puertos front-end para comunicarse con los hosts.</span><span class="sxs-lookup"><span data-stu-id="81d3c-520">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="81d3c-521">Si no hay ninguna restricción sobre el uso del puerto, el valor debe establecerse en 4 (no restringido).</span><span class="sxs-lookup"><span data-stu-id="81d3c-521">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="81d3c-522">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81d3c-522">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="81d3c-523"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="81d3c-523"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-524"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Solo front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="81d3c-524"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-525"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Solo back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="81d3c-525"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-526"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**No restringido** (4)</span><span class="sxs-lookup"><span data-stu-id="81d3c-526"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81d3c-527">**VMQOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="81d3c-527">**VMQOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d3c-528">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81d3c-528">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81d3c-529">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81d3c-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81d3c-530">El uso actual de la cola de máquinas virtuales (VMQ) en este puerto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-530">The current virtual machine queue (VMQ) offloading usage on this port.</span></span> <span data-ttu-id="81d3c-531">El uso es la cantidad de recursos VMQ en uso en el puerto.</span><span class="sxs-lookup"><span data-stu-id="81d3c-531">The usage is the amount of VMQ resources in use on the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81d3c-532">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81d3c-532">Requirements</span></span>



| <span data-ttu-id="81d3c-533">Requisito</span><span class="sxs-lookup"><span data-stu-id="81d3c-533">Requirement</span></span> | <span data-ttu-id="81d3c-534">Value</span><span class="sxs-lookup"><span data-stu-id="81d3c-534">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81d3c-535">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81d3c-535">Minimum supported client</span></span><br/> | <span data-ttu-id="81d3c-536">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="81d3c-536">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="81d3c-537">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81d3c-537">Minimum supported server</span></span><br/> | <span data-ttu-id="81d3c-538">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="81d3c-538">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="81d3c-539">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="81d3c-539">Namespace</span></span><br/>                | <span data-ttu-id="81d3c-540">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="81d3c-540">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="81d3c-541">MOF</span><span class="sxs-lookup"><span data-stu-id="81d3c-541">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81d3c-542"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81d3c-542"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81d3c-543">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="81d3c-543">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81d3c-544"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81d3c-544"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

