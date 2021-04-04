---
description: Representa un adaptador Ethernet sintético.
ms.assetid: B5CB86A9-015B-42E8-ADF4-2F61970D8437
title: Clase Msvm_SyntheticEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPort
- Msvm_SyntheticEthernetPort.SetPowerState
- Msvm_SyntheticEthernetPort.EnableDevice
- Msvm_SyntheticEthernetPort.OnlineDevice
- Msvm_SyntheticEthernetPort.QuiesceDevice
- Msvm_SyntheticEthernetPort.SaveProperties
- Msvm_SyntheticEthernetPort.RestoreProperties
- Msvm_SyntheticEthernetPort.InstanceID
- Msvm_SyntheticEthernetPort.Caption
- Msvm_SyntheticEthernetPort.Description
- Msvm_SyntheticEthernetPort.ElementName
- Msvm_SyntheticEthernetPort.InstallDate
- Msvm_SyntheticEthernetPort.Name
- Msvm_SyntheticEthernetPort.OperationalStatus
- Msvm_SyntheticEthernetPort.StatusDescriptions
- Msvm_SyntheticEthernetPort.Status
- Msvm_SyntheticEthernetPort.HealthState
- Msvm_SyntheticEthernetPort.CommunicationStatus
- Msvm_SyntheticEthernetPort.DetailedStatus
- Msvm_SyntheticEthernetPort.OperatingStatus
- Msvm_SyntheticEthernetPort.PrimaryStatus
- Msvm_SyntheticEthernetPort.EnabledState
- Msvm_SyntheticEthernetPort.OtherEnabledState
- Msvm_SyntheticEthernetPort.RequestedState
- Msvm_SyntheticEthernetPort.EnabledDefault
- Msvm_SyntheticEthernetPort.TimeOfLastStateChange
- Msvm_SyntheticEthernetPort.AvailableRequestedStates
- Msvm_SyntheticEthernetPort.TransitioningToState
- Msvm_SyntheticEthernetPort.SystemCreationClassName
- Msvm_SyntheticEthernetPort.SystemName
- Msvm_SyntheticEthernetPort.CreationClassName
- Msvm_SyntheticEthernetPort.DeviceID
- Msvm_SyntheticEthernetPort.PowerManagementSupported
- Msvm_SyntheticEthernetPort.PowerManagementCapabilities
- Msvm_SyntheticEthernetPort.Availability
- Msvm_SyntheticEthernetPort.StatusInfo
- Msvm_SyntheticEthernetPort.LastErrorCode
- Msvm_SyntheticEthernetPort.ErrorDescription
- Msvm_SyntheticEthernetPort.ErrorCleared
- Msvm_SyntheticEthernetPort.OtherIdentifyingInfo
- Msvm_SyntheticEthernetPort.PowerOnHours
- Msvm_SyntheticEthernetPort.TotalPowerOnHours
- Msvm_SyntheticEthernetPort.IdentifyingDescriptions
- Msvm_SyntheticEthernetPort.AdditionalAvailability
- Msvm_SyntheticEthernetPort.MaxQuiesceTime
- Msvm_SyntheticEthernetPort.Speed
- Msvm_SyntheticEthernetPort.MaxSpeed
- Msvm_SyntheticEthernetPort.RequestedSpeed
- Msvm_SyntheticEthernetPort.UsageRestriction
- Msvm_SyntheticEthernetPort.PortType
- Msvm_SyntheticEthernetPort.OtherPortType
- Msvm_SyntheticEthernetPort.OtherNetworkPortType
- Msvm_SyntheticEthernetPort.PortNumber
- Msvm_SyntheticEthernetPort.LinkTechnology
- Msvm_SyntheticEthernetPort.OtherLinkTechnology
- Msvm_SyntheticEthernetPort.PermanentAddress
- Msvm_SyntheticEthernetPort.NetworkAddresses
- Msvm_SyntheticEthernetPort.FullDuplex
- Msvm_SyntheticEthernetPort.AutoSense
- Msvm_SyntheticEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.MaxDataSize
- Msvm_SyntheticEthernetPort.Capabilities
- Msvm_SyntheticEthernetPort.CapabilityDescriptions
- Msvm_SyntheticEthernetPort.EnabledCapabilities
- Msvm_SyntheticEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8e2a8c2207e410878a4f5c498ea71a1ce67cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908603"
---
# <a name="msvm_syntheticethernetport-class"></a><span data-ttu-id="d2ad7-103">MSVM \_ SyntheticEthernetPort (clase)</span><span class="sxs-lookup"><span data-stu-id="d2ad7-103">Msvm\_SyntheticEthernetPort class</span></span>

<span data-ttu-id="d2ad7-104">Representa un adaptador Ethernet sintético.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-104">Represents a synthetic Ethernet adapter.</span></span> <span data-ttu-id="d2ad7-105">Este adaptador es el adaptador de red preferido debido a su rendimiento, y dado que los cambios en él pueden surtir efecto inmediatamente, mientras está en uso (capacidad de configuracion activa).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-105">This adapter is the preferred network adapter because of its performance and because changes to it can take effect right away, while it is in use (hot configurability).</span></span>

<span data-ttu-id="d2ad7-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ad7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2ad7-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
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
  uint16   AdditionalAvailability[] = 6;
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
};
```

## <a name="members"></a><span data-ttu-id="d2ad7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d2ad7-108">Members</span></span>

<span data-ttu-id="d2ad7-109">La clase **MSVM \_ SyntheticEthernetPort** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d2ad7-109">The **Msvm\_SyntheticEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="d2ad7-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d2ad7-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="d2ad7-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2ad7-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d2ad7-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d2ad7-112">Methods</span></span>

<span data-ttu-id="d2ad7-113">La clase **MSVM \_ SyntheticEthernetPort** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-113">The **Msvm\_SyntheticEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="d2ad7-114">Método</span><span class="sxs-lookup"><span data-stu-id="d2ad7-114">Method</span></span>                                                                      | <span data-ttu-id="d2ad7-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2ad7-115">Description</span></span>                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="d2ad7-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-116">**EnableDevice**</span></span>                                                            | <span data-ttu-id="d2ad7-117">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d2ad7-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-118">**OnlineDevice**</span></span>                                                            | <span data-ttu-id="d2ad7-119">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d2ad7-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-120">**QuiesceDevice**</span></span>                                                           | <span data-ttu-id="d2ad7-121">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="d2ad7-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-122">**RequestStateChange**</span></span>](msvm-syntheticethernetport-requeststatechange.md) | <span data-ttu-id="d2ad7-123">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="d2ad7-124">**Reset**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-124">**Reset**</span></span>](msvm-syntheticethernetport-reset.md)                           | <span data-ttu-id="d2ad7-125">Restablece el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-125">Resets the device.</span></span><br/>            |
| <span data-ttu-id="d2ad7-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-126">**RestoreProperties**</span></span>                                                       | <span data-ttu-id="d2ad7-127">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d2ad7-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-128">**SaveProperties**</span></span>                                                          | <span data-ttu-id="d2ad7-129">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d2ad7-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-130">**SetPowerState**</span></span>                                                           | <span data-ttu-id="d2ad7-131">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d2ad7-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2ad7-132">Properties</span></span>

<span data-ttu-id="d2ad7-133">La clase **MSVM \_ SyntheticEthernetPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-133">The **Msvm\_SyntheticEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2ad7-134">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-134">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-135">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-137">Calificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="d2ad7-137">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-138">La unidad de transmisión máxima (MTU) activa o negociada que se puede admitir.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="d2ad7-139">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-141">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-143">Disponibilidad adicional y estado del dispositivo, más allá de lo especificado en la propiedad **Availability** .</span><span class="sxs-lookup"><span data-stu-id="d2ad7-143">Additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="d2ad7-144">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre está establecida en 6 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-145">**Percepción automática**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-146">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-148">Indica si el puerto de red es capaz de determinar automáticamente la velocidad u otras características de comunicación de los medios de red conectados.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="d2ad7-149">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-150">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-151">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-153">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-153">The primary availability and status of the device.</span></span> <span data-ttu-id="d2ad7-154">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-156">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-158">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="d2ad7-159">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="d2ad7-160">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="d2ad7-161">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="d2ad7-162">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="d2ad7-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="d2ad7-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d2ad7-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="d2ad7-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="d2ad7-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="d2ad7-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="d2ad7-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="d2ad7-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="d2ad7-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="d2ad7-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="d2ad7-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="d2ad7-173">)</span><span class="sxs-lookup"><span data-stu-id="d2ad7-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2ad7-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-175">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-177">Las capacidades del puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-177">The capabilities of the Ethernet port.</span></span> <span data-ttu-id="d2ad7-178">Por ejemplo, el dispositivo podría admitir AlertOnLan, WakeOnLan, equilibrio de carga o conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-178">For example, the device might support AlertOnLan, WakeOnLan, Load Balancing, or FailOver.</span></span> <span data-ttu-id="d2ad7-179">Si se enumeran las funcionalidades de conmutación por error o de equilibrio de carga, también se debe definir una SpareGroup (conmutación por error) o ExtraCapacityGroup (equilibrio de carga) para describir completamente la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-179">If failover or load balancing capabilities are listed, a SpareGroup (failover) or ExtraCapacityGroup (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="d2ad7-180">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-181">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-181">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-182">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-182">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-184">Una matriz de cadenas de forma libre que proporciona explicaciones más detalladas para cualquiera de las características de EthernetPort que se indican en la matriz de propiedades **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="d2ad7-184">An array of free-form strings that provides more detailed explanations for any of the EthernetPort features that are indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="d2ad7-185">Tenga en cuenta que cada entrada de esta matriz está relacionada con la entrada de la matriz de propiedades **Capabilities** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-185">Note, each entry of this array is related to the entry in the **Capabilities** property array that is located at the same index.</span></span> <span data-ttu-id="d2ad7-186">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-186">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-187">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-187">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-188">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-190">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-190">A short description of the object.</span></span> <span data-ttu-id="d2ad7-191">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-191">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-192">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-192">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-193">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-195">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-195">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d2ad7-196">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-196">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2ad7-197">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-198">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-198">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-201">El nombre de la clase o la subclase que se usa en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-201">The name of the class or the subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="d2ad7-202">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-202">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-203">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-203">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-206">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-206">A description of the object.</span></span> <span data-ttu-id="d2ad7-207">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-207">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-208">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-208">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-209">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-211">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-211">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d2ad7-212">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-212">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2ad7-213">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-213">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-214">**ID**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-214">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-215">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-217">Una dirección u otra información de identificación utilizada para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-217">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="d2ad7-218">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-218">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-219">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-219">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-220">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-222">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-222">A display name for the object.</span></span> <span data-ttu-id="d2ad7-223">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-223">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-224">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-224">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-225">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-225">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-227">Las funciones que se habilitan en la lista de todos los admitidos, que se definen en la matriz de propiedades **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="d2ad7-227">The capabilities that are enabled from the list of all supported ones, which are defined in the **Capabilities** property array.</span></span> <span data-ttu-id="d2ad7-228">Esta propiedad se hereda de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-228">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-229">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-229">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-230">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-232">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-232">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d2ad7-233">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-233">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-234">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-234">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-235">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-237">Estados habilitados y deshabilitados de este elemento.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-237">The enabled and disabled states of this element.</span></span> <span data-ttu-id="d2ad7-238">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-238">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-239">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-239">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-240">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-242">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-244">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-246">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-247">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-247">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-248">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-250">Indica si el puerto está funcionando en modo dúplex completo.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-250">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="d2ad7-251">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-251">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-253">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-255">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-255">The current health of the element.</span></span> <span data-ttu-id="d2ad7-256">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-257">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-257">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-258">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-258">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-260">Matriz de cadenas de formato libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="d2ad7-260">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="d2ad7-261">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-261">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-262">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-262">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-263">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-263">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-265">Fecha en que se agregó el puerto Ethernet a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-265">The date the Ethernet port was added to the virtual machine.</span></span> <span data-ttu-id="d2ad7-266">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-267">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-267">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-268">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-270">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-270">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-271">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-271">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d2ad7-272">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-272">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-273">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-273">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-274">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-276">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-276">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-277">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-277">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-278">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-278">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-280">Una enumeración de los tipos de vínculos.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-280">An enumeration of the types of links.</span></span> <span data-ttu-id="d2ad7-281">Cuando se establece en 1 (otro), la propiedad relacionada **OtherLinkTechnology** contiene una descripción de cadena del tipo de vínculo.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-281">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="d2ad7-282">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-282">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="d2ad7-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="d2ad7-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2ad7-284">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-284">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-285">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-287">El tamaño máximo del campo de información (no MAC) que se recibirá o transmitirá.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-287">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="d2ad7-288">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-288">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-289">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-289">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-290">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-292">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-293">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-293">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-294">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-294">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-296">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="d2ad7-296">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-297">Ancho de banda máximo del puerto en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-297">The maximum bandwidth of the port in bits per second.</span></span> <span data-ttu-id="d2ad7-298">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-298">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-299">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-299">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-302">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-302">A display name for the object.</span></span> <span data-ttu-id="d2ad7-303">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-303">This property is inherited from [**CIM\_ManagedSystemElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-304">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-304">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-305">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-307">Direcciones MAC Ethernet/802.3 con formato de doce dígitos hexadecimales (por ejemplo, "010203040506"), donde cada par representa uno de los seis octetos de la dirección MAC en orden de bits canónico (el bit de dirección de grupo se encuentra en el bit de orden inferior del primer carácter de la cadena).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-307">Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string).</span></span> <span data-ttu-id="d2ad7-308">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-308">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-309">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-309">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-310">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-312">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="d2ad7-312">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d2ad7-313">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-313">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2ad7-314">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-315">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-315">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-316">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-316">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-318">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-318">The current status of the element.</span></span> <span data-ttu-id="d2ad7-319">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 2 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-320">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-320">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-321">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-321">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-323">Matriz de cadenas de formato libre que proporciona explicaciones más detalladas para cualquiera de las funciones habilitadas que se especifican como "otro".</span><span class="sxs-lookup"><span data-stu-id="d2ad7-323">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as "Other".</span></span> <span data-ttu-id="d2ad7-324">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-324">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-325">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-325">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-326">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-328">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-328">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d2ad7-329">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-330">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-330">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-331">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-331">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-333">Los datos, además de la información de identificador de dispositivo, que se pueden usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-333">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="d2ad7-334">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-334">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-335">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-335">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-336">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-338">Un valor de cadena que describe **LinkTechnology** cuando se establece en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-338">A string value that describes **LinkTechnology** when it is set to 1 (Other).</span></span> <span data-ttu-id="d2ad7-339">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-339">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-340">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-340">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-341">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-343">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-343">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-344">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-344">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-345">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-347">El tipo de módulo, cuando **portType** está establecido en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-347">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="d2ad7-348">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-348">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-349">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-349">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-350">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-352">La dirección de red que está codificada en el puerto.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-352">The network address that is hardcoded into the port.</span></span> <span data-ttu-id="d2ad7-353">Esta dirección codificada se puede cambiar mediante una actualización de firmware o una configuración de software.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-353">This hardcoded address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="d2ad7-354">Cuando se realiza este cambio, el campo debe actualizarse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-354">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="d2ad7-355">La propiedad **PermanentAddress** debe dejarse en blanco si no existe ninguna dirección codificada para el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-355">The **PermanentAddress** property should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="d2ad7-356">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-356">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-357">**NúmeroDePuerto**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-357">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-358">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-358">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-360">Los puertos de red suelen numerarse con respecto a un módulo lógico o a un elemento de red.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-360">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="d2ad7-361">Este valor es 1 para las NIC emuladas, 0 para todas las demás.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-361">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="d2ad7-362">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-362">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-363">**PortType**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-363">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-364">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-366">Modo específico que está habilitado actualmente para el puerto.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-366">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="d2ad7-367">Cuando se establece en 1 (otro), la propiedad relacionada **OtherPortType** contiene una descripción de cadena del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-367">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="d2ad7-368">Esta propiedad se hereda de [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-368">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-369">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-370">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-372">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-373">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-373">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-374">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-374">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-376">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-376">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-377">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-377">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-378">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-378">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-379">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-380">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-380">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-381">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-381">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-382">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-384">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-384">Provides high level status information.</span></span> <span data-ttu-id="d2ad7-385">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-385">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="d2ad7-386">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-386">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2ad7-387">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-388">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-388">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-389">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-391">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="d2ad7-391">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-392">Ancho de banda solicitado del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-392">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="d2ad7-393">El ancho de banda real se registra en la propiedad **Speed** .</span><span class="sxs-lookup"><span data-stu-id="d2ad7-393">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="d2ad7-394">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-394">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-395">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-395">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-396">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-398">Último estado solicitado o deseado para el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-398">The last requested or desired state for the management service.</span></span> <span data-ttu-id="d2ad7-399">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-399">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-400">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-400">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-401">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-403">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="d2ad7-403">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-404">El ancho de banda actual del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-404">The current bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="d2ad7-405">En el caso de los puertos que varían en ancho de banda o en aquellos casos en los que no se puede realizar una estimación precisa, esta propiedad debe contener el ancho de banda nominal.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-405">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="d2ad7-406">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-406">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-407">**Estado**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-407">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-408">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-409">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-410">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-410">The current status of the element.</span></span> <span data-ttu-id="d2ad7-411">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-411">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-412">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-412">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-413">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-413">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-414">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-415">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d2ad7-415">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d2ad7-416">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-416">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-417">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-417">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-418">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-418">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-419">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-420">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-421">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-421">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-422">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-422">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-423">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-424">Calificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="d2ad7-424">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-425">La unidad de transmisión máxima (MTU) que se puede admitir.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-425">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="d2ad7-426">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-426">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-428">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-430">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-430">The creation class name of the scoping system.</span></span> <span data-ttu-id="d2ad7-431">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-431">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-432">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-432">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-433">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-434">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-435">Nombre NetBIOS del sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-435">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="d2ad7-436">Esta propiedad contendrá el identificador de la máquina virtual en forma de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="d2ad7-436">This property will contain the virtual machine ID in **GUID** form.</span></span> <span data-ttu-id="d2ad7-437">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-438">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-438">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-439">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-441">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-441">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d2ad7-442">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-442">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-443">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-443">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-444">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-444">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-445">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-446">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-446">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-447">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-447">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-448">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-448">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-449">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-450">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-450">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d2ad7-451">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-451">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2ad7-452">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-452">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ad7-453">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-453">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ad7-454">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2ad7-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ad7-455">En algunas circunstancias, un puerto lógico puede identificarse como un puerto de front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-455">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="d2ad7-456">Si no hay ninguna restricción sobre el uso del puerto, el valor debe establecerse en 4 (no restringido).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-456">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="d2ad7-457">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-457">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2ad7-458">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2ad7-458">Remarks</span></span>

<span data-ttu-id="d2ad7-459">El acceso a la clase **MSVM \_ SyntheticEthernetPort** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-459">Access to the **Msvm\_SyntheticEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d2ad7-460">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-460">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d2ad7-461">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2ad7-461">Examples</span></span>

<span data-ttu-id="d2ad7-462">Consulte [consultar objetos de red](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-462">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2ad7-463">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2ad7-463">Requirements</span></span>



| <span data-ttu-id="d2ad7-464">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2ad7-464">Requirement</span></span> | <span data-ttu-id="d2ad7-465">Value</span><span class="sxs-lookup"><span data-stu-id="d2ad7-465">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ad7-466">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2ad7-466">Minimum supported client</span></span><br/> | <span data-ttu-id="d2ad7-467">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d2ad7-467">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d2ad7-468">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2ad7-468">Minimum supported server</span></span><br/> | <span data-ttu-id="d2ad7-469">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d2ad7-469">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2ad7-470">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d2ad7-470">Namespace</span></span><br/>                | <span data-ttu-id="d2ad7-471">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d2ad7-471">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d2ad7-472">MOF</span><span class="sxs-lookup"><span data-stu-id="d2ad7-472">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2ad7-473"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2ad7-473"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2ad7-474">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d2ad7-474">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2ad7-475"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d2ad7-475"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d2ad7-476">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2ad7-476">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ad7-477">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-477">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="d2ad7-478">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="d2ad7-478">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

