---
description: Representa un puerto Ethernet externo (adaptador de red).
ms.assetid: 70901587-641D-46F5-8A35-FEA483D336DE
title: Clase Msvm_ExternalEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPort
- Msvm_ExternalEthernetPort.SetPowerState
- Msvm_ExternalEthernetPort.EnableDevice
- Msvm_ExternalEthernetPort.OnlineDevice
- Msvm_ExternalEthernetPort.QuiesceDevice
- Msvm_ExternalEthernetPort.SaveProperties
- Msvm_ExternalEthernetPort.RestoreProperties
- Msvm_ExternalEthernetPort.InstanceID
- Msvm_ExternalEthernetPort.Caption
- Msvm_ExternalEthernetPort.Description
- Msvm_ExternalEthernetPort.ElementName
- Msvm_ExternalEthernetPort.InstallDate
- Msvm_ExternalEthernetPort.Name
- Msvm_ExternalEthernetPort.OperationalStatus
- Msvm_ExternalEthernetPort.StatusDescriptions
- Msvm_ExternalEthernetPort.Status
- Msvm_ExternalEthernetPort.HealthState
- Msvm_ExternalEthernetPort.CommunicationStatus
- Msvm_ExternalEthernetPort.DetailedStatus
- Msvm_ExternalEthernetPort.OperatingStatus
- Msvm_ExternalEthernetPort.PrimaryStatus
- Msvm_ExternalEthernetPort.EnabledState
- Msvm_ExternalEthernetPort.OtherEnabledState
- Msvm_ExternalEthernetPort.RequestedState
- Msvm_ExternalEthernetPort.EnabledDefault
- Msvm_ExternalEthernetPort.TimeOfLastStateChange
- Msvm_ExternalEthernetPort.AvailableRequestedStates
- Msvm_ExternalEthernetPort.TransitioningToState
- Msvm_ExternalEthernetPort.SystemCreationClassName
- Msvm_ExternalEthernetPort.SystemName
- Msvm_ExternalEthernetPort.CreationClassName
- Msvm_ExternalEthernetPort.DeviceID
- Msvm_ExternalEthernetPort.PowerManagementSupported
- Msvm_ExternalEthernetPort.PowerManagementCapabilities
- Msvm_ExternalEthernetPort.Availability
- Msvm_ExternalEthernetPort.StatusInfo
- Msvm_ExternalEthernetPort.LastErrorCode
- Msvm_ExternalEthernetPort.ErrorDescription
- Msvm_ExternalEthernetPort.ErrorCleared
- Msvm_ExternalEthernetPort.OtherIdentifyingInfo
- Msvm_ExternalEthernetPort.PowerOnHours
- Msvm_ExternalEthernetPort.TotalPowerOnHours
- Msvm_ExternalEthernetPort.IdentifyingDescriptions
- Msvm_ExternalEthernetPort.AdditionalAvailability
- Msvm_ExternalEthernetPort.MaxQuiesceTime
- Msvm_ExternalEthernetPort.Speed
- Msvm_ExternalEthernetPort.MaxSpeed
- Msvm_ExternalEthernetPort.RequestedSpeed
- Msvm_ExternalEthernetPort.UsageRestriction
- Msvm_ExternalEthernetPort.PortType
- Msvm_ExternalEthernetPort.OtherPortType
- Msvm_ExternalEthernetPort.OtherNetworkPortType
- Msvm_ExternalEthernetPort.PortNumber
- Msvm_ExternalEthernetPort.LinkTechnology
- Msvm_ExternalEthernetPort.OtherLinkTechnology
- Msvm_ExternalEthernetPort.PermanentAddress
- Msvm_ExternalEthernetPort.NetworkAddresses
- Msvm_ExternalEthernetPort.FullDuplex
- Msvm_ExternalEthernetPort.AutoSense
- Msvm_ExternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_ExternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_ExternalEthernetPort.MaxDataSize
- Msvm_ExternalEthernetPort.Capabilities
- Msvm_ExternalEthernetPort.CapabilityDescriptions
- Msvm_ExternalEthernetPort.EnabledCapabilities
- Msvm_ExternalEthernetPort.OtherEnabledCapabilities
- Msvm_ExternalEthernetPort.IsBound
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 507c2235c1fda5f43ba025172e276b30e2f0aa85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542494"
---
# <a name="msvm_externalethernetport-class"></a><span data-ttu-id="e4077-103">MSVM \_ ExternalEthernetPort (clase)</span><span class="sxs-lookup"><span data-stu-id="e4077-103">Msvm\_ExternalEthernetPort class</span></span>

<span data-ttu-id="e4077-104">Representa un puerto Ethernet externo (adaptador de red).</span><span class="sxs-lookup"><span data-stu-id="e4077-104">Represents an external Ethernet port (network adapter).</span></span> <span data-ttu-id="e4077-105">Estos tipos de puertos Ethernet proporcionan acceso a las máquinas virtuales a la red externa.</span><span class="sxs-lookup"><span data-stu-id="e4077-105">These types of Ethernet ports give virtual machines access to the external network.</span></span>

<span data-ttu-id="e4077-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e4077-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4077-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4077-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft External Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
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
  string   CreationClassName = "Msvm_ExternalEthernetPort";
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
  string   AdditionalAvailability[];
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
  boolean  IsBound;
};
```

## <a name="members"></a><span data-ttu-id="e4077-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e4077-108">Members</span></span>

<span data-ttu-id="e4077-109">La clase **MSVM \_ ExternalEthernetPort** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e4077-109">The **Msvm\_ExternalEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="e4077-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e4077-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e4077-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4077-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e4077-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e4077-112">Methods</span></span>

<span data-ttu-id="e4077-113">La clase **MSVM \_ ExternalEthernetPort** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e4077-113">The **Msvm\_ExternalEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="e4077-114">Método</span><span class="sxs-lookup"><span data-stu-id="e4077-114">Method</span></span>                                                                     | <span data-ttu-id="e4077-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4077-115">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="e4077-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="e4077-116">**EnableDevice**</span></span>                                                           | <span data-ttu-id="e4077-117">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e4077-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e4077-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="e4077-118">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="e4077-119">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e4077-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e4077-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="e4077-120">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="e4077-121">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e4077-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="e4077-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e4077-122">**RequestStateChange**</span></span>](msvm-externalethernetport-requeststatechange.md) | <span data-ttu-id="e4077-123">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="e4077-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="e4077-124">**Reset**</span><span class="sxs-lookup"><span data-stu-id="e4077-124">**Reset**</span></span>](msvm-externalethernetport-reset.md)                           | <span data-ttu-id="e4077-125">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="e4077-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="e4077-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="e4077-126">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="e4077-127">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e4077-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e4077-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="e4077-128">**SaveProperties**</span></span>                                                         | <span data-ttu-id="e4077-129">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e4077-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e4077-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e4077-130">**SetPowerState**</span></span>                                                          | <span data-ttu-id="e4077-131">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e4077-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e4077-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4077-132">Properties</span></span>

<span data-ttu-id="e4077-133">La clase **MSVM \_ ExternalEthernetPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e4077-133">The **Msvm\_ExternalEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4077-134">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="e4077-134">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-135">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4077-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4077-137">Calificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="e4077-137">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e4077-138">La unidad de transmisión máxima (MTU) activa o negociada que se puede admitir, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e4077-138">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="e4077-139">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e4077-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="e4077-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-141">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e4077-141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e4077-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-143">Cualquier disponibilidad adicional y estado del dispositivo, más allá de lo especificado en la propiedad **Availability** .</span><span class="sxs-lookup"><span data-stu-id="e4077-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="e4077-144">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e4077-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-145">**Percepción automática**</span><span class="sxs-lookup"><span data-stu-id="e4077-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-146">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e4077-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-148">Indica si el puerto de red es capaz de determinar automáticamente la velocidad u otras características de comunicación de los medios de red conectados.</span><span class="sxs-lookup"><span data-stu-id="e4077-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="e4077-149">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e4077-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-150">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="e4077-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-151">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-153">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4077-153">The primary availability and status of the device.</span></span> <span data-ttu-id="e4077-154">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e4077-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="e4077-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-156">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e4077-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-158">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="e4077-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="e4077-159">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4077-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="e4077-160">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="e4077-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="e4077-161">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="e4077-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="e4077-162">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4077-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="e4077-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="e4077-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e4077-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="e4077-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="e4077-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="e4077-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="e4077-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="e4077-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="e4077-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="e4077-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="e4077-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="e4077-173">)</span><span class="sxs-lookup"><span data-stu-id="e4077-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e4077-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="e4077-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-175">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e4077-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-177">Matriz que especifica las funciones del puerto.</span><span class="sxs-lookup"><span data-stu-id="e4077-177">An array that specifies the capabilities of the port.</span></span> <span data-ttu-id="e4077-178">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="e4077-178">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="e4077-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e4077-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="e4077-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-181"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="e4077-181"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-182"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="e4077-182"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-183"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Conmutación por error** (4)</span><span class="sxs-lookup"><span data-stu-id="e4077-183"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-184"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Equilibrio** (5)</span><span class="sxs-lookup"><span data-stu-id="e4077-184"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e4077-185">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e4077-185">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-186">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e4077-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e4077-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-188">Matriz de cadenas de forma libre que proporciona explicaciones más detalladas para las características de Puerto incluidas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="e4077-188">An array of free-form strings that provides more detailed explanations for the port features that are contained in the **Capabilities** array.</span></span> <span data-ttu-id="e4077-189">Cada entrada de esta matriz está relacionada con la entrada correspondiente en la matriz de **capacidades** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="e4077-189">Each entry of this array is related to the corresponding entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="e4077-190">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="e4077-190">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-191">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e4077-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4077-194">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="e4077-194">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="e4077-195">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e4077-195">A short description of the object.</span></span> <span data-ttu-id="e4077-196">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "puerto Ethernet".</span><span class="sxs-lookup"><span data-stu-id="e4077-196">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="e4077-197">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="e4077-197">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-198">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-200">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="e4077-200">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e4077-201">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e4077-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e4077-202">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e4077-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-203">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e4077-203">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-206">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e4077-206">The scoping system's creation class name.</span></span> <span data-ttu-id="e4077-207">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "MSVM \_ ExternalEthernetPort".</span><span class="sxs-lookup"><span data-stu-id="e4077-207">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ExternalEthernetPort".</span></span>

</dd> <dt>

<span data-ttu-id="e4077-208">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e4077-208">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-209">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-211">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e4077-211">A description of the object.</span></span> <span data-ttu-id="e4077-212">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "puerto Ethernet externo de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="e4077-212">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft External Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="e4077-213">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e4077-213">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-214">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-216">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="e4077-216">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e4077-217">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e4077-217">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e4077-218">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e4077-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-219">**ID**</span><span class="sxs-lookup"><span data-stu-id="e4077-219">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-220">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-222">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e4077-222">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="e4077-223">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e4077-223">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-224">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e4077-224">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-227">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="e4077-227">A display name for the object.</span></span> <span data-ttu-id="e4077-228">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e4077-228">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-229">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e4077-229">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-230">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-230">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e4077-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-232">Especifica las funcionalidades que se habilitan en la lista de todas las funcionalidades admitidas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="e4077-232">Specifies which capabilities are enabled from the list of all supported capabilities in the **Capabilities** array.</span></span> <span data-ttu-id="e4077-233">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="e4077-233">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="e4077-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e4077-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-235"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="e4077-235"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-236"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="e4077-236"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-237"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="e4077-237"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-238"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Conmutación por error** (4)</span><span class="sxs-lookup"><span data-stu-id="e4077-238"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-239"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Equilibrio** (5)</span><span class="sxs-lookup"><span data-stu-id="e4077-239"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e4077-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="e4077-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-241">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-243">Configuración predeterminada o de inicio de un administrador para la propiedad **EnabledState** de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e4077-243">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="e4077-244">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="e4077-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e4077-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-246">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-248">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e4077-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e4077-249">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="e4077-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="e4077-250">Por ejemplo, apagar (4) e iniciar (10) son Estados transitorios entre habilitado y deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="e4077-250">For example, shutting down (4) and starting (10) are transient states between enabled and disabled.</span></span> <span data-ttu-id="e4077-251">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4077-251">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="e4077-252">Value</span><span class="sxs-lookup"><span data-stu-id="e4077-252">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="e4077-253">Significado</span><span class="sxs-lookup"><span data-stu-id="e4077-253">Meaning</span></span>                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="e4077-254"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e4077-254"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 |                                                                                                                                                                                                             |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="e4077-255"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e4077-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                             |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="e4077-256"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e4077-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="e4077-257">El elemento es o puede ejecutar comandos, procesará cualquier comando en cola y pondrá en cola nuevas solicitudes.</span><span class="sxs-lookup"><span data-stu-id="e4077-257">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                        |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="e4077-258"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e4077-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="e4077-259">El elemento no ejecutará comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="e4077-259">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                            |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="e4077-260"><dt>**Cerrando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e4077-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="e4077-261">El elemento está en el proceso de pasar a un Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="e4077-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                      |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="e4077-262"><dt>**No aplicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e4077-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="e4077-263">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="e4077-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                          |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="e4077-264"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e4077-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="e4077-265">Es posible que el elemento esté completando comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="e4077-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                     |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="e4077-266"><dt>**En la prueba**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e4077-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="e4077-267">El elemento está en un estado de prueba.</span><span class="sxs-lookup"><span data-stu-id="e4077-267">The element is in a test state.</span></span><br/>                                                                                                                                                                  |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="e4077-268"><dt>**Aplazado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e4077-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="e4077-269">Es posible que el elemento esté completando los comandos, pero pondrá en cola todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="e4077-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                    |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="e4077-270">Modo <dt>**inactivo**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e4077-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="e4077-271">El elemento está habilitado pero en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="e4077-271">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="e4077-272">El comportamiento del elemento es similar al estado habilitado, pero solo procesa un conjunto restringido de comandos.</span><span class="sxs-lookup"><span data-stu-id="e4077-272">The behavior of the element is similar to the Enabled state, but it processes only a restricted set of commands.</span></span> <span data-ttu-id="e4077-273">Todas las demás solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="e4077-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="e4077-274"><dt>**Inicio**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="e4077-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="e4077-275">El elemento está en proceso de pasar a un estado habilitado.</span><span class="sxs-lookup"><span data-stu-id="e4077-275">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="e4077-276">Las nuevas solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="e4077-276">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="e4077-277"><dt>**DMTF reservado**</dt> <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="e4077-277"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="e4077-278">Reservado.</span><span class="sxs-lookup"><span data-stu-id="e4077-278">Reserved.</span></span><br/>                                                                                                                                                                                        |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="e4077-279"><dt>**Proveedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="e4077-279"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="e4077-280">Reservado.</span><span class="sxs-lookup"><span data-stu-id="e4077-280">Reserved.</span></span><br/>                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="e4077-281">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e4077-281">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-282">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e4077-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-284">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="e4077-284">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="e4077-285">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e4077-285">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-286">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e4077-286">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-287">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-289">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="e4077-289">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="e4077-290">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e4077-290">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-291">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="e4077-291">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-292">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e4077-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-294">Indica si el puerto está funcionando en modo dúplex completo.</span><span class="sxs-lookup"><span data-stu-id="e4077-294">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="e4077-295">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e4077-295">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-296">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e4077-296">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-297">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-297">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-299">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="e4077-299">The current health of the element.</span></span> <span data-ttu-id="e4077-300">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="e4077-300">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="e4077-301">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="e4077-301">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="e4077-302">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="e4077-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-303">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e4077-303">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-304">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e4077-304">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e4077-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-306">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="e4077-306">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="e4077-307">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e4077-307">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e4077-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-309">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e4077-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-311">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="e4077-311">The date and time when the object was installed.</span></span> <span data-ttu-id="e4077-312">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="e4077-312">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="e4077-313">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e4077-313">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-314">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e4077-314">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-315">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4077-317">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="e4077-317">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e4077-318">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="e4077-318">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e4077-319">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e4077-319">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-320">**IsBound**</span><span class="sxs-lookup"><span data-stu-id="e4077-320">**IsBound**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-321">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e4077-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-323">Si esta propiedad es **true**, este puerto Ethernet puede estar conectado a los conmutadores y, por tanto, puede proporcionar conectividad a una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e4077-323">If this property is **True**, then this Ethernet port can be connected to the switches and thus can provide connectivity to a virtual machine.</span></span> <span data-ttu-id="e4077-324">Si esta propiedad es **false**, la arquitectura de red de la máquina virtual no utiliza este puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="e4077-324">If this property is **False**, then this Ethernet port is not being used by the virtual machine networking architecture.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-325">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e4077-325">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-326">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4077-326">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-328">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e4077-328">The last error code reported by the logical device.</span></span> <span data-ttu-id="e4077-329">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e4077-329">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-330">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="e4077-330">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-331">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-333">Especifica el tipo de tecnología de vínculo para el puerto.</span><span class="sxs-lookup"><span data-stu-id="e4077-333">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="e4077-334">Cuando se establece en 1 (otro), la propiedad **OtherLinkTechnology** contiene una descripción de cadena del tipo de vínculo.</span><span class="sxs-lookup"><span data-stu-id="e4077-334">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="e4077-335">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e4077-335">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="e4077-336"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e4077-336"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-337"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="e4077-337"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-338"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="e4077-338"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-339"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="e4077-339"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-340"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="e4077-340"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-341"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="e4077-341"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-342"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="e4077-342"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-343"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="e4077-343"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-344"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="e4077-344"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-345"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarrojos** (9)</span><span class="sxs-lookup"><span data-stu-id="e4077-345"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-346"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="e4077-346"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-347"><span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>**LAN inalámbrica** (11)</span><span class="sxs-lookup"><span data-stu-id="e4077-347"><span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>**Wireless LAN** (11)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e4077-348">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="e4077-348">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-349">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4077-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-351">El tamaño máximo del campo de información (no MAC) que se recibirá o transmitirá.</span><span class="sxs-lookup"><span data-stu-id="e4077-351">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="e4077-352">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)y siempre se establece en 1500.</span><span class="sxs-lookup"><span data-stu-id="e4077-352">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-353">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="e4077-353">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-354">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4077-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-356">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="e4077-356">This property has been deprecated.</span></span> <span data-ttu-id="e4077-357">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e4077-357">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-358">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="e4077-358">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-359">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4077-359">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-360">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4077-361">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="e4077-361">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="e4077-362">Ancho de banda máximo del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="e4077-362">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="e4077-363">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4077-363">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-364">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="e4077-364">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-365">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-367">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="e4077-367">The label by which the object is known.</span></span> <span data-ttu-id="e4077-368">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e4077-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-369">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="e4077-369">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-370">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e4077-370">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e4077-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4077-372">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="e4077-372">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="e4077-373">Una matriz de cadenas que contienen las direcciones MAC para el puerto.</span><span class="sxs-lookup"><span data-stu-id="e4077-373">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="e4077-374">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e4077-374">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-375">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="e4077-375">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-376">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-378">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="e4077-378">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e4077-379">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e4077-379">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e4077-380">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e4077-380">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-381">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e4077-381">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-382">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-382">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e4077-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-384">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="e4077-384">The current statuses of the object.</span></span> <span data-ttu-id="e4077-385">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="e4077-385">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-386">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e4077-386">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-387">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e4077-387">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e4077-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-389">Matriz de cadenas de formato libre que proporciona explicaciones más detalladas para cualquiera de las capacidades habilitadas que se especifican como 1 (otro). Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="e4077-389">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other.) This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-390">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="e4077-390">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-391">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-392">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-393">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="e4077-393">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="e4077-394">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="e4077-394">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="e4077-395">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4077-395">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-396">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e4077-396">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-397">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e4077-397">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e4077-398">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-399">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e4077-399">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="e4077-400">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e4077-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-401">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="e4077-401">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-402">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-404">Un valor de cadena que describe **LinkTechnology** cuando se establece en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="e4077-404">A string value that describes **LinkTechnology** when it is set to 1 (Other).</span></span> <span data-ttu-id="e4077-405">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e4077-405">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-406">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="e4077-406">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-407">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-409">El uso de esta propiedad está en desuso en lugar de la propiedad **portType** .</span><span class="sxs-lookup"><span data-stu-id="e4077-409">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="e4077-410">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e4077-410">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-411">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="e4077-411">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-412">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-414">El tipo de módulo, cuando **portType** está establecido en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="e4077-414">The type of module, when **PortType** is set to 1 ("Other").</span></span> <span data-ttu-id="e4077-415">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4077-415">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-416">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="e4077-416">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-417">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-418">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4077-419">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="e4077-419">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="e4077-420">La dirección de red que está codificada en un puerto.</span><span class="sxs-lookup"><span data-stu-id="e4077-420">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="e4077-421">Esta dirección codificada se puede cambiar mediante una actualización de firmware o una configuración de software.</span><span class="sxs-lookup"><span data-stu-id="e4077-421">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="e4077-422">Cuando se realiza este cambio, el campo debe actualizarse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="e4077-422">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="e4077-423">Esta propiedad debe ser **null** si no existe ninguna dirección codificada para el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="e4077-423">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="e4077-424">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e4077-424">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-425">**NúmeroDePuerto**</span><span class="sxs-lookup"><span data-stu-id="e4077-425">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-426">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-426">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-427">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-428">El número de puerto.</span><span class="sxs-lookup"><span data-stu-id="e4077-428">The port number.</span></span> <span data-ttu-id="e4077-429">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e4077-429">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-430">**PortType**</span><span class="sxs-lookup"><span data-stu-id="e4077-430">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-431">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-431">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-432">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-433">Modo específico que está habilitado actualmente para el puerto.</span><span class="sxs-lookup"><span data-stu-id="e4077-433">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="e4077-434">Cuando se establece en 1 ("otro"), la propiedad relacionada **OtherPortType** contiene una descripción de cadena del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="e4077-434">When set to 1 ("Other"), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="e4077-435">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4077-435">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="e4077-436"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e4077-436"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-437"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="e4077-437"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-438"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 cobre 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="e4077-438"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-439"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="e4077-439"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-440"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="e4077-440"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-441"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="e4077-441"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-442"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="e4077-442"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-443"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="e4077-443"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-444"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="e4077-444"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-445"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 fibra 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="e4077-445"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-446"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="e4077-446"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-447"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="e4077-447"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-448"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="e4077-448"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-449"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="e4077-449"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-450"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="e4077-450"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-451"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="e4077-451"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-452"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="e4077-452"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-453"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="e4077-453"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-454"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="e4077-454"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-455"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="e4077-455"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-456"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-uevo** (111)</span><span class="sxs-lookup"><span data-stu-id="e4077-456"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-457"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (16000 65535)</span><span class="sxs-lookup"><span data-stu-id="e4077-457"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e4077-458">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e4077-458">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-459">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-459">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e4077-460">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-461">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4077-461">The power management capabilities of the device.</span></span> <span data-ttu-id="e4077-462">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e4077-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-463">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e4077-463">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-464">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e4077-464">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-465">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-466">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="e4077-466">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="e4077-467">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e4077-467">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-468">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e4077-468">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-469">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4077-469">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-470">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-471">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="e4077-471">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="e4077-472">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e4077-472">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-473">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="e4077-473">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-474">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-474">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-475">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-476">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="e4077-476">Provides high level status information.</span></span> <span data-ttu-id="e4077-477">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="e4077-477">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="e4077-478">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e4077-478">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e4077-479">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e4077-479">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-480">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="e4077-480">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-481">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4077-481">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-482">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4077-483">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="e4077-483">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="e4077-484">Ancho de banda solicitado del puerto en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="e4077-484">The requested bandwidth of the port in bits per second.</span></span> <span data-ttu-id="e4077-485">El ancho de banda real se registra en la propiedad **Speed** .</span><span class="sxs-lookup"><span data-stu-id="e4077-485">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="e4077-486">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4077-486">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-487">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e4077-487">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-488">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-488">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-489">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-490">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="e4077-490">The last requested or desired state for the element.</span></span> <span data-ttu-id="e4077-491">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="e4077-491">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-492">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="e4077-492">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-493">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4077-493">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-494">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4077-495">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="e4077-495">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="e4077-496">Ancho de banda del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="e4077-496">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="e4077-497">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4077-497">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-498">**Estado**</span><span class="sxs-lookup"><span data-stu-id="e4077-498">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-499">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-500">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-501">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="e4077-501">The current status of the object.</span></span> <span data-ttu-id="e4077-502">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e4077-502">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e4077-503">ACEPTAR</span><span class="sxs-lookup"><span data-stu-id="e4077-503">"OK"</span></span>
</dt> <dt>

<span data-ttu-id="e4077-504"><span id="OK"></span><span id="ok"></span>**Vale**</span><span class="sxs-lookup"><span data-stu-id="e4077-504"><span id="OK"></span><span id="ok"></span>**OK**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-505"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span><span class="sxs-lookup"><span data-stu-id="e4077-505"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-506"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado**</span><span class="sxs-lookup"><span data-stu-id="e4077-506"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-507"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span><span class="sxs-lookup"><span data-stu-id="e4077-507"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-508"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred error**</span><span class="sxs-lookup"><span data-stu-id="e4077-508"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred Fail**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-509"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Comenzar**</span><span class="sxs-lookup"><span data-stu-id="e4077-509"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-510"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Bloqueo**</span><span class="sxs-lookup"><span data-stu-id="e4077-510"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-511"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio**</span><span class="sxs-lookup"><span data-stu-id="e4077-511"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-512"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Calca**</span><span class="sxs-lookup"><span data-stu-id="e4077-512"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-513"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**No recuperable**</span><span class="sxs-lookup"><span data-stu-id="e4077-513"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-514"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto**</span><span class="sxs-lookup"><span data-stu-id="e4077-514"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-515"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Comunicación perdida**</span><span class="sxs-lookup"><span data-stu-id="e4077-515"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Lost Comm**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e4077-516">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e4077-516">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-517">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e4077-517">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e4077-518">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-519">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e4077-519">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e4077-520">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "OK".</span><span class="sxs-lookup"><span data-stu-id="e4077-520">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="e4077-521">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e4077-521">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-522">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-522">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-523">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-523">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-524">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e4077-524">The current state of the logical device.</span></span> <span data-ttu-id="e4077-525">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e4077-525">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-526">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="e4077-526">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-527">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4077-527">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-528">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4077-529">Calificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="e4077-529">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e4077-530">La unidad de transmisión máxima (MTU) que se puede admitir, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e4077-530">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="e4077-531">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e4077-531">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-532">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e4077-532">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-533">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-534">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-535">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e4077-535">The scoping system's creation class name.</span></span> <span data-ttu-id="e4077-536">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="e4077-536">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="e4077-537">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e4077-537">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-538">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4077-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-539">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-539">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-540">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e4077-540">The name of the scoping system.</span></span> <span data-ttu-id="e4077-541">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e4077-541">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e4077-542">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="e4077-542">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-543">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e4077-543">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-544">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-545">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="e4077-545">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e4077-546">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="e4077-546">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-547">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e4077-547">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-548">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4077-548">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-549">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-550">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4077-550">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="e4077-551">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e4077-551">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-552">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="e4077-552">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-553">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-553">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-554">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-554">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-555">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="e4077-555">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e4077-556">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e4077-556">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e4077-557">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="e4077-557">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4077-558">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4077-558">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4077-559">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4077-559">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4077-560">En algunas circunstancias, un puerto lógico puede identificarse como un puerto de front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="e4077-560">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="e4077-561">Un ejemplo de esta situación sería una matriz de almacenamiento que podría tener puertos back-end para comunicarse con las unidades de disco y los puertos front-end para comunicarse con los hosts.</span><span class="sxs-lookup"><span data-stu-id="e4077-561">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="e4077-562">Si no hay ninguna restricción sobre el uso del puerto, el valor se debe establecer en "no restringido".</span><span class="sxs-lookup"><span data-stu-id="e4077-562">If there is no restriction on the use of the port, then the value should be set to "Not restricted".</span></span> <span data-ttu-id="e4077-563">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4077-563">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="e4077-564"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e4077-564"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-565"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Solo front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="e4077-565"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-566"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Solo back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="e4077-566"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e4077-567"><span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>**No restringido** (4)</span><span class="sxs-lookup"><span data-stu-id="e4077-567"><span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>**Not restricted** (4)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4077-568">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4077-568">Remarks</span></span>

<span data-ttu-id="e4077-569">El acceso a la clase **MSVM \_ ExternalEthernetPort** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="e4077-569">Access to the **Msvm\_ExternalEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e4077-570">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e4077-570">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="e4077-571">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e4077-571">Examples</span></span>

<span data-ttu-id="e4077-572">Consulte [consultar objetos de red](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e4077-572">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4077-573">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4077-573">Requirements</span></span>



| <span data-ttu-id="e4077-574">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4077-574">Requirement</span></span> | <span data-ttu-id="e4077-575">Value</span><span class="sxs-lookup"><span data-stu-id="e4077-575">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4077-576">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4077-576">Minimum supported client</span></span><br/> | <span data-ttu-id="e4077-577">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4077-577">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e4077-578">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4077-578">Minimum supported server</span></span><br/> | <span data-ttu-id="e4077-579">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4077-579">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e4077-580">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e4077-580">Namespace</span></span><br/>                | <span data-ttu-id="e4077-581">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e4077-581">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e4077-582">MOF</span><span class="sxs-lookup"><span data-stu-id="e4077-582">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4077-583"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4077-583"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4077-584">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e4077-584">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4077-585"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e4077-585"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e4077-586">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4077-586">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4077-587">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="e4077-587">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="e4077-588">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="e4077-588">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

