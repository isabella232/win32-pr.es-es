---
description: Representa un adaptador de red físico Wi-Fi (802,11) que se puede enlazar a un conmutador virtual para proporcionar conectividad de red externa a las máquinas virtuales.
ms.assetid: c6dae491-607c-4f17-aea9-162d910120c2
title: Clase Msvm_WiFiPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiPort
- Msvm_WiFiPort.RequestStateChange
- Msvm_WiFiPort.SetPowerState
- Msvm_WiFiPort.Reset
- Msvm_WiFiPort.EnableDevice
- Msvm_WiFiPort.OnlineDevice
- Msvm_WiFiPort.QuiesceDevice
- Msvm_WiFiPort.SaveProperties
- Msvm_WiFiPort.RestoreProperties
- Msvm_WiFiPort.InstanceID
- Msvm_WiFiPort.Caption
- Msvm_WiFiPort.Description
- Msvm_WiFiPort.ElementName
- Msvm_WiFiPort.InstallDate
- Msvm_WiFiPort.Name
- Msvm_WiFiPort.OperationalStatus
- Msvm_WiFiPort.StatusDescriptions
- Msvm_WiFiPort.Status
- Msvm_WiFiPort.HealthState
- Msvm_WiFiPort.CommunicationStatus
- Msvm_WiFiPort.DetailedStatus
- Msvm_WiFiPort.OperatingStatus
- Msvm_WiFiPort.PrimaryStatus
- Msvm_WiFiPort.EnabledState
- Msvm_WiFiPort.OtherEnabledState
- Msvm_WiFiPort.RequestedState
- Msvm_WiFiPort.EnabledDefault
- Msvm_WiFiPort.TimeOfLastStateChange
- Msvm_WiFiPort.AvailableRequestedStates
- Msvm_WiFiPort.TransitioningToState
- Msvm_WiFiPort.SystemCreationClassName
- Msvm_WiFiPort.SystemName
- Msvm_WiFiPort.CreationClassName
- Msvm_WiFiPort.DeviceID
- Msvm_WiFiPort.PowerManagementSupported
- Msvm_WiFiPort.PowerManagementCapabilities
- Msvm_WiFiPort.Availability
- Msvm_WiFiPort.StatusInfo
- Msvm_WiFiPort.LastErrorCode
- Msvm_WiFiPort.ErrorDescription
- Msvm_WiFiPort.ErrorCleared
- Msvm_WiFiPort.OtherIdentifyingInfo
- Msvm_WiFiPort.PowerOnHours
- Msvm_WiFiPort.TotalPowerOnHours
- Msvm_WiFiPort.IdentifyingDescriptions
- Msvm_WiFiPort.AdditionalAvailability
- Msvm_WiFiPort.MaxQuiesceTime
- Msvm_WiFiPort.Speed
- Msvm_WiFiPort.MaxSpeed
- Msvm_WiFiPort.RequestedSpeed
- Msvm_WiFiPort.UsageRestriction
- Msvm_WiFiPort.PortType
- Msvm_WiFiPort.OtherPortType
- Msvm_WiFiPort.OtherNetworkPortType
- Msvm_WiFiPort.PortNumber
- Msvm_WiFiPort.LinkTechnology
- Msvm_WiFiPort.OtherLinkTechnology
- Msvm_WiFiPort.PermanentAddress
- Msvm_WiFiPort.NetworkAddresses
- Msvm_WiFiPort.FullDuplex
- Msvm_WiFiPort.AutoSense
- Msvm_WiFiPort.SupportedMaximumTransmissionUnit
- Msvm_WiFiPort.ActiveMaximumTransmissionUnit
- Msvm_WiFiPort.IsBound
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47ec33236c55d281755b50449a8f33a56152a07a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003146"
---
# <a name="msvm_wifiport-class"></a><span data-ttu-id="c313e-103">MSVM \_ WiFiPort (clase)</span><span class="sxs-lookup"><span data-stu-id="c313e-103">Msvm\_WiFiPort class</span></span>

<span data-ttu-id="c313e-104">Representa un adaptador de red físico Wi-Fi (802,11) que se puede enlazar a un conmutador virtual para proporcionar conectividad de red externa a las máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="c313e-104">Represents a physical Wi-Fi (802.11) network adapter that can be bound to a virtual switch to provide external network connectivity to virtual machines.</span></span>

<span data-ttu-id="c313e-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c313e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c313e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c313e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiPort : CIM_WiFiPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
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
  boolean  IsBound;
};
```

## <a name="members"></a><span data-ttu-id="c313e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c313e-107">Members</span></span>

<span data-ttu-id="c313e-108">La clase **MSVM \_ WiFiPort** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c313e-108">The **Msvm\_WiFiPort** class has these types of members:</span></span>

-   [<span data-ttu-id="c313e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c313e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c313e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c313e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c313e-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c313e-111">Methods</span></span>

<span data-ttu-id="c313e-112">La clase **MSVM \_ WiFiPort** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c313e-112">The **Msvm\_WiFiPort** class has these methods.</span></span>



| <span data-ttu-id="c313e-113">Método</span><span class="sxs-lookup"><span data-stu-id="c313e-113">Method</span></span>                 | <span data-ttu-id="c313e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c313e-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="c313e-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="c313e-115">**EnableDevice**</span></span>       | <span data-ttu-id="c313e-116">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="c313e-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c313e-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="c313e-117">**OnlineDevice**</span></span>       | <span data-ttu-id="c313e-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="c313e-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c313e-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="c313e-119">**QuiesceDevice**</span></span>      | <span data-ttu-id="c313e-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="c313e-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c313e-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="c313e-121">**RequestStateChange**</span></span> | <span data-ttu-id="c313e-122">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="c313e-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c313e-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="c313e-123">**Reset**</span></span>              | <span data-ttu-id="c313e-124">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="c313e-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c313e-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="c313e-125">**RestoreProperties**</span></span>  | <span data-ttu-id="c313e-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="c313e-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c313e-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="c313e-127">**SaveProperties**</span></span>     | <span data-ttu-id="c313e-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="c313e-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c313e-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c313e-129">**SetPowerState**</span></span>      | <span data-ttu-id="c313e-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="c313e-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c313e-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c313e-131">Properties</span></span>

<span data-ttu-id="c313e-132">La clase **MSVM \_ WiFiPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c313e-132">The **Msvm\_WiFiPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c313e-133">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="c313e-133">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-134">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c313e-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c313e-136">Calificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="c313e-136">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c313e-137">La unidad de transmisión máxima (MTU) activa o negociada que se puede admitir, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c313e-137">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="c313e-138">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c313e-138">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="c313e-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-140">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c313e-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-142">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c313e-142">Any additional availability and status of the device.</span></span> <span data-ttu-id="c313e-143">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-144">**Percepción automática**</span><span class="sxs-lookup"><span data-stu-id="c313e-144">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-145">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c313e-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-147">Indica si el puerto es capaz de determinar automáticamente la velocidad u otras características de comunicación de los medios de red conectados.</span><span class="sxs-lookup"><span data-stu-id="c313e-147">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="c313e-148">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c313e-148">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-149">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="c313e-149">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-150">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-152">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c313e-152">The primary availability and status of the device.</span></span> <span data-ttu-id="c313e-153">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="c313e-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-155">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c313e-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-157">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="c313e-157">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="c313e-158">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c313e-158">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="c313e-159">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="c313e-159">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="c313e-160">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="c313e-160">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="c313e-161">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c313e-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="c313e-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="c313e-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c313e-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="c313e-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="c313e-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="c313e-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="c313e-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="c313e-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="c313e-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="c313e-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="c313e-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="c313e-172">)</span><span class="sxs-lookup"><span data-stu-id="c313e-172">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c313e-173">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c313e-173">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-176">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c313e-176">A short description of the object.</span></span> <span data-ttu-id="c313e-177">Esta propiedad se hereda de la clase [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .</span><span class="sxs-lookup"><span data-stu-id="c313e-177">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="c313e-178">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="c313e-178">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-179">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-181">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="c313e-181">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c313e-182">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="c313e-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c313e-183">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c313e-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c313e-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-187">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="c313e-187">The scoping system's creation class name.</span></span> <span data-ttu-id="c313e-188">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-189">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c313e-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-192">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c313e-192">A description of the object.</span></span> <span data-ttu-id="c313e-193">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c313e-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c313e-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-195">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-197">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="c313e-197">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c313e-198">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="c313e-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c313e-199">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c313e-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-200">**ID**</span><span class="sxs-lookup"><span data-stu-id="c313e-200">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-203">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c313e-203">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="c313e-204">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-204">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-205">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c313e-205">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-206">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-208">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="c313e-208">A display name for the object.</span></span> <span data-ttu-id="c313e-209">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c313e-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-210">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="c313e-210">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-211">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-213">Configuración predeterminada o de inicio de un administrador para la propiedad **EnabledState** de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c313e-213">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="c313e-214">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c313e-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-215">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c313e-215">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-216">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-218">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c313e-218">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c313e-219">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c313e-219">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="c313e-220">Value</span><span class="sxs-lookup"><span data-stu-id="c313e-220">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="c313e-221">Significado</span><span class="sxs-lookup"><span data-stu-id="c313e-221">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="c313e-222"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c313e-222"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="c313e-223">El elemento se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="c313e-223">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="c313e-224"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c313e-224"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="c313e-225">El elemento está desactivado.</span><span class="sxs-lookup"><span data-stu-id="c313e-225">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c313e-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c313e-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-227">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c313e-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-229">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="c313e-229">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="c313e-230">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c313e-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-232">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-234">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="c313e-234">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="c313e-235">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-236">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="c313e-236">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-237">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c313e-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-239">Indica si el puerto está funcionando en modo dúplex completo.</span><span class="sxs-lookup"><span data-stu-id="c313e-239">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="c313e-240">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c313e-240">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-241">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c313e-241">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-242">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-242">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-244">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="c313e-244">The current health of the element.</span></span> <span data-ttu-id="c313e-245">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c313e-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-246">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c313e-246">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-247">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c313e-247">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c313e-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-249">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="c313e-249">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="c313e-250">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-251">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c313e-251">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-252">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c313e-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-254">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="c313e-254">The date and time when the object was installed.</span></span> <span data-ttu-id="c313e-255">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="c313e-255">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="c313e-256">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c313e-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-257">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c313e-257">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c313e-260">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="c313e-260">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c313e-261">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="c313e-261">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c313e-262">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c313e-262">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-263">**IsBound**</span><span class="sxs-lookup"><span data-stu-id="c313e-263">**IsBound**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-264">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c313e-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-266">Especifica si el puerto de Wi-Fi se enlaza a la arquitectura de red de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c313e-266">Specifies if the Wi-Fi port is bound to the virtual machine networking architecture.</span></span> <span data-ttu-id="c313e-267">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c313e-267">This will be one of the following values.</span></span>



| <span data-ttu-id="c313e-268">Value</span><span class="sxs-lookup"><span data-stu-id="c313e-268">Value</span></span>                                                                                                                                                        | <span data-ttu-id="c313e-269">Significado</span><span class="sxs-lookup"><span data-stu-id="c313e-269">Meaning</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="True"></span><span id="true"></span><span id="TRUE"></span><dl> <span data-ttu-id="c313e-270"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="c313e-270"><dt>**True**</dt></span></span> </dl>     | <span data-ttu-id="c313e-271">El puerto Wi-Fi se enlaza a la arquitectura de red de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c313e-271">The Wi-Fi port is bound to the virtual machine networking architecture.</span></span> <br/>     |
| <span id="False"></span><span id="false"></span><span id="FALSE"></span><dl> <span data-ttu-id="c313e-272"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="c313e-272"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="c313e-273">El puerto Wi-Fi no está enlazado a la arquitectura de red de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c313e-273">The Wi-Fi port is not bound to the virtual machine networking architecture.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="c313e-274">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c313e-274">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-275">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c313e-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-277">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c313e-277">The last error code reported by the logical device.</span></span> <span data-ttu-id="c313e-278">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-279">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="c313e-279">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-280">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-282">Especifica el tipo de tecnología de vínculo para el puerto.</span><span class="sxs-lookup"><span data-stu-id="c313e-282">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="c313e-283">Cuando se establece en 1 (otro), la propiedad **OtherLinkTechnology** contiene una descripción de cadena del tipo de vínculo.</span><span class="sxs-lookup"><span data-stu-id="c313e-283">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="c313e-284">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c313e-284">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="c313e-285"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="c313e-285"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-286"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="c313e-286"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-287"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="c313e-287"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-288"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="c313e-288"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-289"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="c313e-289"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-290"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="c313e-290"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-291"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="c313e-291"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-292"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="c313e-292"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-293"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="c313e-293"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-294"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarrojos** (9)</span><span class="sxs-lookup"><span data-stu-id="c313e-294"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-295"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="c313e-295"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-296"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**LAN inalámbrica** (11)</span><span class="sxs-lookup"><span data-stu-id="c313e-296"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c313e-297">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="c313e-297">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-298">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c313e-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-300">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="c313e-300">This property has been deprecated.</span></span> <span data-ttu-id="c313e-301">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-302">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="c313e-302">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-303">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c313e-303">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c313e-305">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="c313e-305">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="c313e-306">Ancho de banda máximo del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="c313e-306">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="c313e-307">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c313e-307">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-308">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c313e-308">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-309">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-311">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="c313e-311">The label by which the object is known.</span></span> <span data-ttu-id="c313e-312">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c313e-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-313">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="c313e-313">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-314">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c313e-314">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c313e-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c313e-316">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="c313e-316">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="c313e-317">Una matriz de cadenas que contienen las direcciones MAC para el puerto.</span><span class="sxs-lookup"><span data-stu-id="c313e-317">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="c313e-318">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c313e-318">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-319">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="c313e-319">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-320">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-320">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-322">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="c313e-322">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c313e-323">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="c313e-323">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c313e-324">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c313e-324">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-325">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c313e-325">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-326">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-326">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c313e-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-328">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="c313e-328">The current statuses of the object.</span></span> <span data-ttu-id="c313e-329">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c313e-329">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-330">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="c313e-330">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-331">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-333">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="c313e-333">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="c313e-334">Esta propiedad debe establecerse en **null** cuando la propiedad **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="c313e-334">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="c313e-335">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c313e-335">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-336">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="c313e-336">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-337">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c313e-337">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c313e-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-339">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c313e-339">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="c313e-340">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-341">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="c313e-341">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-342">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-344">Un valor de cadena que describe **LinkTechnology** cuando se establece en 1, (otro).</span><span class="sxs-lookup"><span data-stu-id="c313e-344">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="c313e-345">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c313e-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-346">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="c313e-346">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-347">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-349">El uso de esta propiedad está en desuso en lugar de la propiedad **portType** .</span><span class="sxs-lookup"><span data-stu-id="c313e-349">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="c313e-350">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c313e-350">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-351">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="c313e-351">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-354">Describe el tipo de módulo, cuando **portType** está establecido en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="c313e-354">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="c313e-355">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c313e-355">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-356">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="c313e-356">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-357">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c313e-359">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="c313e-359">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="c313e-360">La dirección de red que está codificada en un puerto.</span><span class="sxs-lookup"><span data-stu-id="c313e-360">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="c313e-361">Esta dirección codificada se puede cambiar mediante una actualización de firmware o una configuración de software.</span><span class="sxs-lookup"><span data-stu-id="c313e-361">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="c313e-362">Cuando se realiza este cambio, el campo debe actualizarse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="c313e-362">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="c313e-363">Esta propiedad debe ser **null** si no existe ninguna dirección codificada para el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="c313e-363">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="c313e-364">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c313e-364">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-365">**NúmeroDePuerto**</span><span class="sxs-lookup"><span data-stu-id="c313e-365">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-366">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-368">El número de puerto.</span><span class="sxs-lookup"><span data-stu-id="c313e-368">The port number.</span></span> <span data-ttu-id="c313e-369">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c313e-369">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-370">**PortType**</span><span class="sxs-lookup"><span data-stu-id="c313e-370">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-371">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-373">Modo específico que está habilitado actualmente para el puerto.</span><span class="sxs-lookup"><span data-stu-id="c313e-373">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="c313e-374">Cuando se establece en 1 (otro), la propiedad **OtherPortType** relacionada contiene una descripción de cadena del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="c313e-374">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="c313e-375">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c313e-375">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="c313e-376"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="c313e-376"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-377"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="c313e-377"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-378"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 cobre 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="c313e-378"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-379"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="c313e-379"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-380"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="c313e-380"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-381"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="c313e-381"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-382"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="c313e-382"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-383"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="c313e-383"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-384"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="c313e-384"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-385"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 fibra 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="c313e-385"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-386"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="c313e-386"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-387"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="c313e-387"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-388"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="c313e-388"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-389"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="c313e-389"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-390"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="c313e-390"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-391"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="c313e-391"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-392"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="c313e-392"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-393"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="c313e-393"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-394"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="c313e-394"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-395"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="c313e-395"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-396"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-uevo** (111)</span><span class="sxs-lookup"><span data-stu-id="c313e-396"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-397"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="c313e-397"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c313e-398">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c313e-398">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-399">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-399">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c313e-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-401">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c313e-401">The power management capabilities of the device.</span></span> <span data-ttu-id="c313e-402">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-403">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c313e-403">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-404">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c313e-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-405">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-406">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="c313e-406">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="c313e-407">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-408">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="c313e-408">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-409">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c313e-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-411">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="c313e-411">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="c313e-412">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-413">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="c313e-413">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-414">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-415">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-416">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="c313e-416">Provides high level status information.</span></span> <span data-ttu-id="c313e-417">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="c313e-417">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="c313e-418">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="c313e-418">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c313e-419">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c313e-419">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-420">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="c313e-420">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-421">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c313e-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-422">Tipo de acceso: solo escritura</span><span class="sxs-lookup"><span data-stu-id="c313e-422">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="c313e-423">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="c313e-423">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="c313e-424">Ancho de banda solicitado del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="c313e-424">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="c313e-425">El ancho de banda real se registra en la propiedad **Speed** .</span><span class="sxs-lookup"><span data-stu-id="c313e-425">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="c313e-426">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c313e-426">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-427">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c313e-427">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-428">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-430">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="c313e-430">The last requested or desired state for the element.</span></span> <span data-ttu-id="c313e-431">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c313e-431">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-432">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="c313e-432">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-433">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c313e-433">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-434">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c313e-435">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="c313e-435">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="c313e-436">Ancho de banda del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="c313e-436">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="c313e-437">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c313e-437">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-438">**Estado**</span><span class="sxs-lookup"><span data-stu-id="c313e-438">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-439">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-441">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c313e-441">The current status of the object.</span></span> <span data-ttu-id="c313e-442">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c313e-442">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-443">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c313e-443">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-444">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c313e-444">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c313e-445">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-446">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="c313e-446">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c313e-447">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c313e-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-448">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c313e-448">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-449">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-450">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-451">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c313e-451">The current state of the logical device.</span></span> <span data-ttu-id="c313e-452">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-452">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-453">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="c313e-453">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-454">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c313e-454">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-455">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c313e-456">Calificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="c313e-456">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c313e-457">La unidad de transmisión máxima (MTU) que se puede admitir, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c313e-457">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="c313e-458">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c313e-458">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-459">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c313e-459">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-460">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-461">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-462">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="c313e-462">The scoping system's creation class name.</span></span> <span data-ttu-id="c313e-463">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-463">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-464">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c313e-464">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-465">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c313e-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-466">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-467">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="c313e-467">The scoping system's name.</span></span> <span data-ttu-id="c313e-468">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-468">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-469">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="c313e-469">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-470">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c313e-470">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-471">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-471">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-472">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="c313e-472">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="c313e-473">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c313e-473">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-474">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="c313e-474">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-475">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c313e-475">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-476">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-477">El número total de horas que se ha encendido este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c313e-477">The total number of hours that this device has been powered on.</span></span> <span data-ttu-id="c313e-478">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c313e-478">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c313e-479">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="c313e-479">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-480">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-481">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-482">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="c313e-482">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c313e-483">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="c313e-483">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c313e-484">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="c313e-484">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c313e-485">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c313e-485">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c313e-486">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c313e-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c313e-487">En algunas circunstancias, un puerto lógico puede identificarse como un puerto de front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="c313e-487">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="c313e-488">Un ejemplo de esta situación sería una matriz de almacenamiento que podría tener puertos back-end para comunicarse con las unidades de disco y los puertos front-end para comunicarse con los hosts.</span><span class="sxs-lookup"><span data-stu-id="c313e-488">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="c313e-489">Si no hay ninguna restricción sobre el uso del puerto, el valor debe establecerse en 4 (no restringido).</span><span class="sxs-lookup"><span data-stu-id="c313e-489">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="c313e-490">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c313e-490">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="c313e-491"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="c313e-491"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-492"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Solo front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="c313e-492"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-493"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Solo back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="c313e-493"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c313e-494"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**No restringido** (4)</span><span class="sxs-lookup"><span data-stu-id="c313e-494"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c313e-495">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c313e-495">Requirements</span></span>



| <span data-ttu-id="c313e-496">Requisito</span><span class="sxs-lookup"><span data-stu-id="c313e-496">Requirement</span></span> | <span data-ttu-id="c313e-497">Value</span><span class="sxs-lookup"><span data-stu-id="c313e-497">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c313e-498">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c313e-498">Minimum supported client</span></span><br/> | <span data-ttu-id="c313e-499">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c313e-499">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c313e-500">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c313e-500">Minimum supported server</span></span><br/> | <span data-ttu-id="c313e-501">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c313e-501">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c313e-502">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c313e-502">Namespace</span></span><br/>                | <span data-ttu-id="c313e-503">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c313e-503">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c313e-504">MOF</span><span class="sxs-lookup"><span data-stu-id="c313e-504">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c313e-505"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c313e-505"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c313e-506">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c313e-506">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c313e-507"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c313e-507"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

