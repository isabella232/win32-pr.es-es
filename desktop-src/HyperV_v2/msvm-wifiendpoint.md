---
description: Representa el punto de conexión lógico para un adaptador de red. Cuando el extremo de Wi-Fi está conectado a un puerto de conmutador, el adaptador de red conectado al punto de conexión de Wi-Fi tiene conectividad de red.
ms.assetid: 66ed1503-9c11-4a51-a3a5-21e5d7021197
title: Msvm_WiFiEndpoint (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiEndpoint
- Msvm_WiFiEndpoint.RequestStateChange
- Msvm_WiFiEndpoint.InstanceID
- Msvm_WiFiEndpoint.Caption
- Msvm_WiFiEndpoint.Description
- Msvm_WiFiEndpoint.ElementName
- Msvm_WiFiEndpoint.InstallDate
- Msvm_WiFiEndpoint.Name
- Msvm_WiFiEndpoint.OperationalStatus
- Msvm_WiFiEndpoint.StatusDescriptions
- Msvm_WiFiEndpoint.Status
- Msvm_WiFiEndpoint.HealthState
- Msvm_WiFiEndpoint.CommunicationStatus
- Msvm_WiFiEndpoint.DetailedStatus
- Msvm_WiFiEndpoint.OperatingStatus
- Msvm_WiFiEndpoint.PrimaryStatus
- Msvm_WiFiEndpoint.EnabledState
- Msvm_WiFiEndpoint.OtherEnabledState
- Msvm_WiFiEndpoint.RequestedState
- Msvm_WiFiEndpoint.EnabledDefault
- Msvm_WiFiEndpoint.TimeOfLastStateChange
- Msvm_WiFiEndpoint.AvailableRequestedStates
- Msvm_WiFiEndpoint.TransitioningToState
- Msvm_WiFiEndpoint.SystemCreationClassName
- Msvm_WiFiEndpoint.SystemName
- Msvm_WiFiEndpoint.CreationClassName
- Msvm_WiFiEndpoint.NameFormat
- Msvm_WiFiEndpoint.ProtocolType
- Msvm_WiFiEndpoint.ProtocolIFType
- Msvm_WiFiEndpoint.OtherTypeDescription
- Msvm_WiFiEndpoint.LANID
- Msvm_WiFiEndpoint.LANType
- Msvm_WiFiEndpoint.OtherLANType
- Msvm_WiFiEndpoint.MACAddress
- Msvm_WiFiEndpoint.AliasAddresses
- Msvm_WiFiEndpoint.GroupAddresses
- Msvm_WiFiEndpoint.MaxDataSize
- Msvm_WiFiEndpoint.Connected
- Msvm_WiFiEndpoint.EncryptionMethod
- Msvm_WiFiEndpoint.OtherEncryptionMethod
- Msvm_WiFiEndpoint.AuthenticationMethod
- Msvm_WiFiEndpoint.OtherAuthenticationMethod
- Msvm_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- Msvm_WiFiEndpoint.AccessPointAddress
- Msvm_WiFiEndpoint.BSSType
- Msvm_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f4a0a287d85b7a229b0e8e50a10c402fca734429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001103"
---
# <a name="msvm_wifiendpoint-class"></a><span data-ttu-id="88353-104">MSVM \_ WiFiEndpoint (clase)</span><span class="sxs-lookup"><span data-stu-id="88353-104">Msvm\_WiFiEndpoint class</span></span>

<span data-ttu-id="88353-105">Representa el punto de conexión lógico para un adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="88353-105">Represents the logical connection point for a network adapter.</span></span> <span data-ttu-id="88353-106">Cuando el extremo de Wi-Fi está conectado a un puerto de conmutador, el adaptador de red conectado al punto de conexión de Wi-Fi tiene conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="88353-106">When the Wi-Fi endpoint is connected to a switch port, the network adapter connected to the Wi-Fi endpoint has network connectivity.</span></span>

<span data-ttu-id="88353-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="88353-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="88353-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88353-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiEndpoint : CIM_WiFiEndpoint
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
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 71;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
  uint16   EncryptionMethod;
  string   OtherEncryptionMethod;
  uint16   AuthenticationMethod;
  string   OtherAuthenticationMethod;
  uint16   IEEE8021xAuthenticationProtocol;
  string   AccessPointAddress;
  uint16   BSSType;
  boolean  Associated;
};
```

## <a name="members"></a><span data-ttu-id="88353-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="88353-109">Members</span></span>

<span data-ttu-id="88353-110">La clase **MSVM \_ WiFiEndpoint** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="88353-110">The **Msvm\_WiFiEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="88353-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="88353-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="88353-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88353-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="88353-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="88353-113">Methods</span></span>

<span data-ttu-id="88353-114">La clase **MSVM \_ WiFiEndpoint** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="88353-114">The **Msvm\_WiFiEndpoint** class has these methods.</span></span>



| <span data-ttu-id="88353-115">Método</span><span class="sxs-lookup"><span data-stu-id="88353-115">Method</span></span>                 | <span data-ttu-id="88353-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="88353-116">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="88353-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="88353-117">**RequestStateChange**</span></span> | <span data-ttu-id="88353-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="88353-118">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="88353-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88353-119">Properties</span></span>

<span data-ttu-id="88353-120">La clase **MSVM \_ WiFiEndpoint** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="88353-120">The **Msvm\_WiFiEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88353-121">**AccessPointAddress**</span><span class="sxs-lookup"><span data-stu-id="88353-121">**AccessPointAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-124">Contiene la dirección MAC del punto de acceso con el que está asociado actualmente el punto de conexión de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="88353-124">Contains the MAC address of the access point with which the Wi-Fi endpoint is currently associated.</span></span> <span data-ttu-id="88353-125">Si el extremo de Wi-Fi no está asociado actualmente, **AccessPointAddress** debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="88353-125">If the Wi-Fi endpoint is not currently associated, then **AccessPointAddress** should be **Null**.</span></span> <span data-ttu-id="88353-126">Se debe dar formato a la dirección MAC como doce dígitos hexadecimales (por ejemplo, "010203040506"), donde cada par representa uno de los seis octetos de la dirección MAC en orden de bits canónico (por ejemplo, el bit de dirección de grupo se encuentra en el bit de orden inferior del primer carácter de la cadena).</span><span class="sxs-lookup"><span data-stu-id="88353-126">The MAC address should be formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (for example, the Group address bit is found in the low order bit of the first character of the string).</span></span>

</dd> <dt>

<span data-ttu-id="88353-127">**AliasAddresses**</span><span class="sxs-lookup"><span data-stu-id="88353-127">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-128">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="88353-128">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="88353-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-130">Otras direcciones de unidifusión que se pueden usar para comunicarse con el punto de conexión de LAN.</span><span class="sxs-lookup"><span data-stu-id="88353-130">Other unicast addresses that may be used to communicate with the LAN endpoint.</span></span> <span data-ttu-id="88353-131">Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88353-131">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="88353-132">**Asociado**</span><span class="sxs-lookup"><span data-stu-id="88353-132">**Associated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-133">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="88353-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88353-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-135">Indica si el extremo Wi-Fi está asociado actualmente a un punto de acceso o a una estación de cliente.</span><span class="sxs-lookup"><span data-stu-id="88353-135">Indicates whether the Wi-Fi endpoint is currently associated to an access point or client station.</span></span>

<span data-ttu-id="88353-136">Contiene **true** si el extremo Wi-Fi está asociado a un punto de acceso o a una estación de cliente; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="88353-136">Contains **True** if the Wi-Fi endpoint is associated to an access point or client station; otherwise, **False**.</span></span>

</dd> <dt>

<span data-ttu-id="88353-137">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="88353-137">**AuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-138">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-140">Especifica el método utilizado para autenticar el Wi-Fi punto de conexión y la red entre sí.</span><span class="sxs-lookup"><span data-stu-id="88353-140">Specifies the method used to authenticate the Wi-Fi endpoint and the network to one another.</span></span>

<dl> <dt>

<span data-ttu-id="88353-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="88353-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="88353-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="88353-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="88353-143"><span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**Abrir sistema** (2)</span><span class="sxs-lookup"><span data-stu-id="88353-143"><span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**Open System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="88353-144"><span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**Clave compartida** (3)</span><span class="sxs-lookup"><span data-stu-id="88353-144"><span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**Shared Key** (3)</span></span>
</dt> <dt>

<span data-ttu-id="88353-145"><span id="WPA_PSK"></span><span id="wpa_psk"></span>**WPA PSK** (4)</span><span class="sxs-lookup"><span data-stu-id="88353-145"><span id="WPA_PSK"></span><span id="wpa_psk"></span>**WPA PSK** (4)</span></span>
</dt> <dt>

<span data-ttu-id="88353-146"><span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1 x** (5)</span><span class="sxs-lookup"><span data-stu-id="88353-146"><span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1x** (5)</span></span>
</dt> <dt>

<span data-ttu-id="88353-147"><span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**PSK de WPA2** (6)</span><span class="sxs-lookup"><span data-stu-id="88353-147"><span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**WPA2 PSK** (6)</span></span>
</dt> <dt>

<span data-ttu-id="88353-148"><span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**IEEE 802.1 de WPA2 x** (7)</span><span class="sxs-lookup"><span data-stu-id="88353-148"><span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**WPA2 IEEE 802.1x** (7)</span></span>
</dt> <dt>

<span data-ttu-id="88353-149"><span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**CCKM IEEE 802.1 x** (8)</span><span class="sxs-lookup"><span data-stu-id="88353-149"><span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**CCKM IEEE 802.1x** (8)</span></span>
</dt> <dt>

<span data-ttu-id="88353-150"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (9..</span><span class="sxs-lookup"><span data-stu-id="88353-150"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (9..</span></span> <span data-ttu-id="88353-151">)</span><span class="sxs-lookup"><span data-stu-id="88353-151">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="88353-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="88353-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-153">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="88353-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-155">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="88353-155">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="88353-156">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88353-156">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="88353-157">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="88353-157">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="88353-158">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="88353-158">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="88353-159">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88353-159">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="88353-160"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="88353-160"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="88353-161"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="88353-161"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="88353-162"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="88353-162"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="88353-163"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="88353-163"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="88353-164"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="88353-164"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="88353-165"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="88353-165"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="88353-166"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="88353-166"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="88353-167"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="88353-167"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="88353-168"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="88353-168"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="88353-169"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="88353-169"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="88353-170">)</span><span class="sxs-lookup"><span data-stu-id="88353-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="88353-171">**BSSType**</span><span class="sxs-lookup"><span data-stu-id="88353-171">**BSSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-172">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-174">Indica el tipo básico de Service Set (BSS) de la red que corresponde a la instancia de.</span><span class="sxs-lookup"><span data-stu-id="88353-174">Indicates the Basic Service Set (BSS) type of the network that corresponds to the instance.</span></span> <span data-ttu-id="88353-175">Un conjunto de servicios básico es un conjunto de estaciones controlado por una única función de coordinación.</span><span class="sxs-lookup"><span data-stu-id="88353-175">A Basic Service Set is a set of stations controlled by a single coordination function.</span></span>



| <span data-ttu-id="88353-176">Value</span><span class="sxs-lookup"><span data-stu-id="88353-176">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="88353-177">Significado</span><span class="sxs-lookup"><span data-stu-id="88353-177">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="88353-178"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="88353-178"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                |                                                                                    |
| <span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span><dl> <span data-ttu-id="88353-179"><dt>**Independiente**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="88353-179"><dt>**Independent**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="88353-180">El extremo Wi-Fi está asociado directamente a otra estación cliente.</span><span class="sxs-lookup"><span data-stu-id="88353-180">The Wi-Fi endpoint is associated directly to another client station.</span></span><br/>    |
| <span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span><dl> <span data-ttu-id="88353-181"><dt>**Infraestructura**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="88353-181"><dt>**Infrastructure**</dt> <dt>3</dt></span></span> </dl>    | <span data-ttu-id="88353-182">El extremo Wi-Fi está asociado a una red mediante un punto de acceso.</span><span class="sxs-lookup"><span data-stu-id="88353-182">The Wi-Fi endpoint is associated to a network by using an access point.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="88353-183"><dt> **Reservado para DMTF**</dt> <dt>4..</dt></span><span class="sxs-lookup"><span data-stu-id="88353-183"><dt>**DMTF Reserved** </dt> <dt>4.. </dt></span></span> </dl> |                                                                                    |



 

</dd> <dt>

<span data-ttu-id="88353-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="88353-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-187">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="88353-187">A short description of the object.</span></span> <span data-ttu-id="88353-188">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="88353-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="88353-189">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="88353-189">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-190">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-192">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="88353-192">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="88353-193">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="88353-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="88353-194">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="88353-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="88353-195">**Conectada**</span><span class="sxs-lookup"><span data-stu-id="88353-195">**Connected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-196">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="88353-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88353-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-198">Esta propiedad se establece en **true** si el extremo Wi-Fi está conectado a un puerto de conmutador.</span><span class="sxs-lookup"><span data-stu-id="88353-198">This property is set to **True** if the Wi-Fi endpoint is connected to a switch port.</span></span>

</dd> <dt>

<span data-ttu-id="88353-199">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="88353-199">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-200">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88353-202">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="88353-202">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="88353-203">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="88353-203">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="88353-204">Esta propiedad se hereda de [**\_ punto CIM**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="88353-204">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="88353-205">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="88353-205">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-206">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-208">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="88353-208">A description of the object.</span></span> <span data-ttu-id="88353-209">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="88353-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="88353-210">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="88353-210">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-211">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-213">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="88353-213">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="88353-214">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="88353-214">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="88353-215">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="88353-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="88353-216">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="88353-216">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-219">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="88353-219">A display name for the object.</span></span> <span data-ttu-id="88353-220">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="88353-220">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="88353-221">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="88353-221">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-222">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-224">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="88353-224">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="88353-225">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) y tendrá uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="88353-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="88353-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="88353-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="88353-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="88353-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="88353-228"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitada pero sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="88353-228"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="88353-229">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="88353-229">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-230">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-232">Especifica el estado habilitado del sistema planeado.</span><span class="sxs-lookup"><span data-stu-id="88353-232">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="88353-233">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="88353-233">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="88353-234">Value</span><span class="sxs-lookup"><span data-stu-id="88353-234">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="88353-235">Significado</span><span class="sxs-lookup"><span data-stu-id="88353-235">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="88353-236"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="88353-236"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="88353-237">El sistema está desactivado.</span><span class="sxs-lookup"><span data-stu-id="88353-237">The system is turned off.</span></span><br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="88353-238"><dt>**No aplicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="88353-238"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="88353-239">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="88353-239">The element does not support being enabled or disabled.</span></span><br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="88353-240"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="88353-240"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="88353-241">El sistema está habilitado, pero sin conexión.</span><span class="sxs-lookup"><span data-stu-id="88353-241">The system is enabled, but offline.</span></span> <span data-ttu-id="88353-242">Se quitarán las nuevas solicitudes.</span><span class="sxs-lookup"><span data-stu-id="88353-242">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="88353-243">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="88353-243">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-244">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-246">Especifica el método de cifrado que se usa para proteger la confidencialidad de los datos enviados y recibidos por el punto de conexión de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="88353-246">Specifies the encryption method in use to protect the confidentiality of data sent and received by the Wi-Fi endpoint.</span></span>

<dl> <dt>

<span data-ttu-id="88353-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="88353-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="88353-248"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="88353-248"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="88353-249"><span id="WEP"></span><span id="wep"></span>**WEP** (2)</span><span class="sxs-lookup"><span data-stu-id="88353-249"><span id="WEP"></span><span id="wep"></span>**WEP** (2)</span></span>
</dt> <dt>

<span data-ttu-id="88353-250"><span id="TKIP"></span><span id="tkip"></span>**TKIP** (3)</span><span class="sxs-lookup"><span data-stu-id="88353-250"><span id="TKIP"></span><span id="tkip"></span>**TKIP** (3)</span></span>
</dt> <dt>

<span data-ttu-id="88353-251"><span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4)</span><span class="sxs-lookup"><span data-stu-id="88353-251"><span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4)</span></span>
</dt> <dt>

<span data-ttu-id="88353-252"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno** (5)</span><span class="sxs-lookup"><span data-stu-id="88353-252"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (5)</span></span>
</dt> <dt>

<span data-ttu-id="88353-253"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (6..</span><span class="sxs-lookup"><span data-stu-id="88353-253"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (6..</span></span> <span data-ttu-id="88353-254">)</span><span class="sxs-lookup"><span data-stu-id="88353-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="88353-255">**GroupAddresses**</span><span class="sxs-lookup"><span data-stu-id="88353-255">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-256">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="88353-256">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="88353-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-258">Direcciones de multidifusión a las que el punto de conexión de LAN realiza escuchas.</span><span class="sxs-lookup"><span data-stu-id="88353-258">Multicast addresses to which the LAN endpoint listens.</span></span> <span data-ttu-id="88353-259">Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88353-259">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="88353-260">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="88353-260">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-261">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-263">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="88353-263">The current health of the element.</span></span> <span data-ttu-id="88353-264">Esta propiedad expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="88353-264">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="88353-265">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="88353-265">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="88353-266">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="88353-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="88353-267">**IEEE8021xAuthenticationProtocol**</span><span class="sxs-lookup"><span data-stu-id="88353-267">**IEEE8021xAuthenticationProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-268">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-270">Contiene el tipo de protocolo de autenticación extensible (EAP) si el **AuthenticationMethod** contiene 5 (WPA IEEE 802.1 x), 7 (WPA2 IEEE 802.1 x) o 8 (CCKM IEEE 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="88353-270">Contains the Extensible Authentication Protocol (EAP) type if and only if **AuthenticationMethod** contains 5 (WPA IEEE 802.1x), 7 (WPA2 IEEE 802.1x), or 8 (CCKM IEEE 802.1x).</span></span>

<dl> <dt>

<span data-ttu-id="88353-271"><span id="EAP-TLS"></span><span id="eap-tls"></span>**EAP-TLS** (0)</span><span class="sxs-lookup"><span data-stu-id="88353-271"><span id="EAP-TLS"></span><span id="eap-tls"></span>**EAP-TLS** (0)</span></span>
</dt> <dt>

<span data-ttu-id="88353-272"><span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/MSCHAPv2** (1)</span><span class="sxs-lookup"><span data-stu-id="88353-272"><span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/MSCHAPv2** (1)</span></span>
</dt> <dt>

<span data-ttu-id="88353-273"><span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-MSCHAPv2** (2)</span><span class="sxs-lookup"><span data-stu-id="88353-273"><span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-MSCHAPv2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="88353-274"><span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3)</span><span class="sxs-lookup"><span data-stu-id="88353-274"><span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3)</span></span>
</dt> <dt>

<span data-ttu-id="88353-275"><span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**EAP-FAST/MSCHAPv2** (4)</span><span class="sxs-lookup"><span data-stu-id="88353-275"><span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**EAP-FAST/MSCHAPv2** (4)</span></span>
</dt> <dt>

<span data-ttu-id="88353-276"><span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**EAP-FAST/GTC** (5)</span><span class="sxs-lookup"><span data-stu-id="88353-276"><span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**EAP-FAST/GTC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="88353-277"><span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6)</span><span class="sxs-lookup"><span data-stu-id="88353-277"><span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6)</span></span>
</dt> <dt>

<span data-ttu-id="88353-278"><span id="EAP-PSK"></span><span id="eap-psk"></span>**EAP-PSK** (7)</span><span class="sxs-lookup"><span data-stu-id="88353-278"><span id="EAP-PSK"></span><span id="eap-psk"></span>**EAP-PSK** (7)</span></span>
</dt> <dt>

<span data-ttu-id="88353-279"><span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8)</span><span class="sxs-lookup"><span data-stu-id="88353-279"><span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8)</span></span>
</dt> <dt>

<span data-ttu-id="88353-280"><span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-AKA** (9)</span><span class="sxs-lookup"><span data-stu-id="88353-280"><span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-AKA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="88353-281"><span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**EAP-FAST/TLS** (10)</span><span class="sxs-lookup"><span data-stu-id="88353-281"><span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**EAP-FAST/TLS** (10)</span></span>
</dt> <dt>

<span data-ttu-id="88353-282"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (11..</span><span class="sxs-lookup"><span data-stu-id="88353-282"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (11..</span></span> <span data-ttu-id="88353-283">)</span><span class="sxs-lookup"><span data-stu-id="88353-283">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="88353-284">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="88353-284">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-285">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="88353-285">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88353-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-287">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="88353-287">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="88353-288">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="88353-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="88353-289">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="88353-289">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-290">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88353-292">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="88353-292">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="88353-293">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="88353-293">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="88353-294">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="88353-294">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="88353-295">**LANID**</span><span class="sxs-lookup"><span data-stu-id="88353-295">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-296">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-298">Etiqueta o identificador del segmento de LAN al que está conectado el extremo.</span><span class="sxs-lookup"><span data-stu-id="88353-298">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="88353-299">Si el extremo no está activo o conectado actualmente, o no se conoce esta información, esta propiedad será **null**.</span><span class="sxs-lookup"><span data-stu-id="88353-299">If the endpoint is not currently active/connected, or this information is not known, then this property will be **Null**.</span></span> <span data-ttu-id="88353-300">Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88353-300">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="88353-301">**LANType**</span><span class="sxs-lookup"><span data-stu-id="88353-301">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-302">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-304">Esta propiedad está en desuso en lugar de la propiedad **protocolType** .</span><span class="sxs-lookup"><span data-stu-id="88353-304">This property is deprecated in lieu of the **ProtocolType** property.</span></span> <span data-ttu-id="88353-305">Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88353-305">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="88353-306">**Mac**</span><span class="sxs-lookup"><span data-stu-id="88353-306">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88353-309">Calificadores: **MaxLen** (12)</span><span class="sxs-lookup"><span data-stu-id="88353-309">Qualifiers: **MaxLen** ( 12 )</span></span>
</dt> </dl>

<span data-ttu-id="88353-310">Dirección MAC que se usa en la comunicación con el punto de conexión de LAN.</span><span class="sxs-lookup"><span data-stu-id="88353-310">The MAC address used in communication with the LAN endpoint.</span></span> <span data-ttu-id="88353-311">La dirección MAC tiene el formato de doce dígitos hexadecimales (por ejemplo, "010203040506"), donde cada par representa uno de los seis octetos de la dirección MAC en orden de bits canónico según RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="88353-311">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span> <span data-ttu-id="88353-312">Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88353-312">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="88353-313">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="88353-313">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-314">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88353-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88353-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88353-316">Calificadores: **unidades** ("bits")</span><span class="sxs-lookup"><span data-stu-id="88353-316">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="88353-317">Tamaño máximo, en número de bits, del campo de información que puede ser enviado o recibido por el punto de conexión de LAN.</span><span class="sxs-lookup"><span data-stu-id="88353-317">The largest size, in number of bits, of the information field that may be sent or received by the LAN endpoint.</span></span> <span data-ttu-id="88353-318">Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88353-318">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="88353-319">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="88353-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-320">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-322">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="88353-322">The label by which the object is known.</span></span> <span data-ttu-id="88353-323">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="88353-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="88353-324">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="88353-324">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-325">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88353-327">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="88353-327">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="88353-328">Contiene la heurística de nomenclatura que se selecciona para asegurarse de que el valor de la propiedad **Name** es único.</span><span class="sxs-lookup"><span data-stu-id="88353-328">Contains the naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="88353-329">Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="88353-329">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="88353-330">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="88353-330">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-331">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-333">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="88353-333">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="88353-334">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="88353-334">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="88353-335">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="88353-335">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="88353-336">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="88353-336">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-337">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="88353-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-339">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="88353-339">The current statuses of the object.</span></span> <span data-ttu-id="88353-340">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="88353-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="88353-341">**OtherAuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="88353-341">**OtherAuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-342">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-344">Especifica el método de autenticación 802,11 solo si **AuthenticationMethod** contiene 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="88353-344">Specifies the 802.11 authentication method if and only if **AuthenticationMethod** contains 1 (Other).</span></span> <span data-ttu-id="88353-345">El formato de esta cadena es específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="88353-345">The format of this string is vendor specific.</span></span>

</dd> <dt>

<span data-ttu-id="88353-346">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="88353-346">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-347">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-349">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="88353-349">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="88353-350">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="88353-350">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="88353-351">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88353-351">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="88353-352">**OtherEncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="88353-352">**OtherEncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-353">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-355">Especifica el método de cifrado 802,11 si y solo si **EncryptionMethod** contiene 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="88353-355">Specifies the 802.11 encryption method if and only if **EncryptionMethod** contains 1 (Other).</span></span> <span data-ttu-id="88353-356">El formato de esta cadena es específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="88353-356">The format of this string is vendor specific.</span></span>

</dd> <dt>

<span data-ttu-id="88353-357">**OtherLANType**</span><span class="sxs-lookup"><span data-stu-id="88353-357">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-358">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-360">Esta propiedad está en desuso en lugar de la propiedad **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="88353-360">This property is deprecated in lieu of the **OtherTypeDescription** property.</span></span> <span data-ttu-id="88353-361">Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88353-361">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="88353-362">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="88353-362">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-363">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-364">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88353-365">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="88353-365">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="88353-366">Una cadena que describe el tipo de extremo de protocolo cuando la propiedad **ProtocolIFType** de esta clase (o cualquiera de sus subclases) está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="88353-366">A string that describes the type of protocol endpoint when the **ProtocolIFType** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="88353-367">Esta propiedad debe establecerse en **null** cuando la propiedad **ProtocolIFType** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="88353-367">This property should be set to **Null** when the **ProtocolIFType** property is any value other than 1.</span></span> <span data-ttu-id="88353-368">Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="88353-368">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="88353-369">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="88353-369">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-370">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-372">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="88353-372">Provides high level status information.</span></span> <span data-ttu-id="88353-373">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="88353-373">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="88353-374">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="88353-374">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="88353-375">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="88353-375">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="88353-376">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="88353-376">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-377">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-378">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-379">La propiedad se utiliza para categorizar y clasificar las instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="88353-379">The property is used to categorize and classify instances of this class.</span></span> <span data-ttu-id="88353-380">Si **ProtocolIFType** se establece en 1 (otro), se debe proporcionar la información de tipo en la propiedad **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="88353-380">If the **ProtocolIFType** is set to 1 (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span> <span data-ttu-id="88353-381">Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="88353-381">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

> [!Note]  
> <span data-ttu-id="88353-382">**ProtocolIFType** es una enumeración que está sincronizada con la [MIB de ifType de IANA](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="88353-382">**ProtocolIFType** is an enumeration that is synchronized with the [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="88353-383">También se incluyen los valores adicionales definidos por DMTF.</span><span class="sxs-lookup"><span data-stu-id="88353-383">Additional values defined by the DMTF are also included.</span></span>

 

<dl> <dt>

<span data-ttu-id="88353-384"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="88353-384"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="88353-385"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="88353-385"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)</span></span>
</dt> <dt>

<span data-ttu-id="88353-386"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA reservado** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="88353-386"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)</span></span>
</dt> <dt>

<span data-ttu-id="88353-387"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (4301.. 32767)</span><span class="sxs-lookup"><span data-stu-id="88353-387"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (4301..32767)</span></span>
</dt> <dt>

<span data-ttu-id="88353-388"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (32768..</span><span class="sxs-lookup"><span data-stu-id="88353-388"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768..</span></span> <span data-ttu-id="88353-389">)</span><span class="sxs-lookup"><span data-stu-id="88353-389">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="88353-390">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="88353-390">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-391">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-392">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-393">Esta propiedad está en desuso en lugar de la propiedad **ProtocolIFType** .</span><span class="sxs-lookup"><span data-stu-id="88353-393">This property is deprecated in lieu of the **ProtocolIFType** property.</span></span> <span data-ttu-id="88353-394">Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="88353-394">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="88353-395">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="88353-395">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-396">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-398">Último estado solicitado o deseado para el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="88353-398">The last requested or desired state for the management service.</span></span> <span data-ttu-id="88353-399">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88353-399">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="88353-400">**Estado**</span><span class="sxs-lookup"><span data-stu-id="88353-400">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-401">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-403">Describe el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="88353-403">Describes the status of the element.</span></span> <span data-ttu-id="88353-404">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="88353-404">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="88353-405">ACEPTAR</span><span class="sxs-lookup"><span data-stu-id="88353-405">"OK"</span></span>

<span data-ttu-id="88353-406">Error</span><span class="sxs-lookup"><span data-stu-id="88353-406">"Error"</span></span>

<span data-ttu-id="88353-407">Degradado</span><span class="sxs-lookup"><span data-stu-id="88353-407">"Degraded"</span></span>

<span data-ttu-id="88353-408">Unknown</span><span class="sxs-lookup"><span data-stu-id="88353-408">"Unknown"</span></span>

<span data-ttu-id="88353-409">"Pred FAIL"</span><span class="sxs-lookup"><span data-stu-id="88353-409">"Pred Fail"</span></span>

<span data-ttu-id="88353-410">Comenzar</span><span class="sxs-lookup"><span data-stu-id="88353-410">"Starting"</span></span>

<span data-ttu-id="88353-411">Bloqueo</span><span class="sxs-lookup"><span data-stu-id="88353-411">"Stopping"</span></span>

<span data-ttu-id="88353-412">Servicio</span><span class="sxs-lookup"><span data-stu-id="88353-412">"Service"</span></span>

<span data-ttu-id="88353-413">Calca</span><span class="sxs-lookup"><span data-stu-id="88353-413">"Stressed"</span></span>

<span data-ttu-id="88353-414">"Recover"</span><span class="sxs-lookup"><span data-stu-id="88353-414">"NonRecover"</span></span>

<span data-ttu-id="88353-415">"Sin contacto"</span><span class="sxs-lookup"><span data-stu-id="88353-415">"No Contact"</span></span>

<span data-ttu-id="88353-416">"Pérdida de comunicación"</span><span class="sxs-lookup"><span data-stu-id="88353-416">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="88353-417">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="88353-417">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-418">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="88353-418">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="88353-419">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-420">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="88353-420">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="88353-421">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="88353-421">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="88353-422">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="88353-422">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-423">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-424">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-425">Nombre de la clase de creación del sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="88353-425">The hosting system's creation class name.</span></span> <span data-ttu-id="88353-426">Esta propiedad se hereda de [**\_ punto CIM**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="88353-426">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="88353-427">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="88353-427">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-428">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88353-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88353-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88353-430">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="88353-430">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="88353-431">Nombre del sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="88353-431">The name of the hosting system.</span></span> <span data-ttu-id="88353-432">Esta propiedad se hereda de [**\_ punto CIM**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="88353-432">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="88353-433">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="88353-433">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-434">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="88353-434">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88353-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-436">Fecha y hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="88353-436">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="88353-437">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88353-437">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="88353-438">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="88353-438">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88353-439">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88353-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88353-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88353-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88353-441">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="88353-441">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="88353-442">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88353-442">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88353-443">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88353-443">Requirements</span></span>



| <span data-ttu-id="88353-444">Requisito</span><span class="sxs-lookup"><span data-stu-id="88353-444">Requirement</span></span> | <span data-ttu-id="88353-445">Value</span><span class="sxs-lookup"><span data-stu-id="88353-445">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88353-446">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88353-446">Minimum supported client</span></span><br/> | <span data-ttu-id="88353-447">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="88353-447">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="88353-448">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88353-448">Minimum supported server</span></span><br/> | <span data-ttu-id="88353-449">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="88353-449">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="88353-450">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="88353-450">Namespace</span></span><br/>                | <span data-ttu-id="88353-451">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="88353-451">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="88353-452">MOF</span><span class="sxs-lookup"><span data-stu-id="88353-452">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88353-453"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88353-453"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="88353-454">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88353-454">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88353-455"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="88353-455"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

