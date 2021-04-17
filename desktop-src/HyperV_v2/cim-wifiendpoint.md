---
description: Representa un punto de conexión de comunicación inalámbrica, que puede enviar y recibir tramas de datos cuando su dispositivo de interfaz asociado está conectado con una LAN inalámbrica IEEE 802,11.
ms.assetid: 61743402-f333-4501-ba17-e676d85f72f3
title: CIM_WiFiEndpoint (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiEndpoint
- CIM_WiFiEndpoint.LANID
- CIM_WiFiEndpoint.ProtocolIFType
- CIM_WiFiEndpoint.EncryptionMethod
- CIM_WiFiEndpoint.OtherEncryptionMethod
- CIM_WiFiEndpoint.AuthenticationMethod
- CIM_WiFiEndpoint.OtherAuthenticationMethod
- CIM_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- CIM_WiFiEndpoint.AccessPointAddress
- CIM_WiFiEndpoint.BSSType
- CIM_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e09d040f9d4530bee4347528d704cfe2e9403b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688121"
---
# <a name="cim_wifiendpoint-class"></a><span data-ttu-id="60b26-103">\_Clase WiFiEndpoint de CIM</span><span class="sxs-lookup"><span data-stu-id="60b26-103">CIM\_WiFiEndpoint class</span></span>

<span data-ttu-id="60b26-104">Representa un punto de conexión de comunicación inalámbrica, que puede enviar y recibir tramas de datos cuando su dispositivo de interfaz asociado está conectado con una LAN inalámbrica IEEE 802,11.</span><span class="sxs-lookup"><span data-stu-id="60b26-104">Represents a wireless communication endpoint, which can send and receive data frames when its associated interface device is connected with an IEEE 802.11 wireless LAN.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b26-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60b26-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Network::Wireless"), AMENDMENT]
class CIM_WiFiEndpoint : CIM_LANEndpoint
{
  string  LANID;
  uint16  ProtocolIFType = 71;
  uint16  EncryptionMethod;
  string  OtherEncryptionMethod;
  uint16  AuthenticationMethod;
  string  OtherAuthenticationMethod;
  uint16  IEEE8021xAuthenticationProtocol;
  string  AccessPointAddress;
  uint16  BSSType;
  boolean Associated;
};
```

## <a name="members"></a><span data-ttu-id="60b26-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="60b26-106">Members</span></span>

<span data-ttu-id="60b26-107">La clase **CIM \_ WiFiEndpoint** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="60b26-107">The **CIM\_WiFiEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="60b26-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60b26-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60b26-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60b26-109">Properties</span></span>

<span data-ttu-id="60b26-110">La clase **CIM \_ WiFiEndpoint** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="60b26-110">The **CIM\_WiFiEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60b26-111">**AccessPointAddress**</span><span class="sxs-lookup"><span data-stu-id="60b26-111">**AccessPointAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b26-112">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60b26-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b26-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b26-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60b26-114">Dirección MAC del punto de acceso que está asociado al extremo de Wi-Fi; de lo contrario, **es null**.</span><span class="sxs-lookup"><span data-stu-id="60b26-114">The MAC address of the access point that is associated with the Wi-Fi endpoint; otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="60b26-115">**Asociado**</span><span class="sxs-lookup"><span data-stu-id="60b26-115">**Associated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b26-116">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="60b26-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60b26-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b26-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60b26-118">**true** si el punto de conexión Wi-Fi está asociado actualmente a un punto de acceso o a una estación de cliente; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="60b26-118">**true** if the WiFi endpoint is currently associated with an access point or client station; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="60b26-119">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="60b26-119">**AuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b26-120">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60b26-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60b26-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b26-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b26-122">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**EncryptionMethod**","**\_ WiFiEndpoint CIM**.**IEEE8021xAuthenticationProtocol**","**\_ WiFiEndpoint CIM**.**OtherAuthenticationMethod**")</span><span class="sxs-lookup"><span data-stu-id="60b26-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**EncryptionMethod**", "**CIM\_WiFiEndpoint**.**IEEE8021xAuthenticationProtocol**", "**CIM\_WiFiEndpoint**.**OtherAuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="60b26-123">El tipo de autenticación usado entre el extremo de Wi-Fi y la red.</span><span class="sxs-lookup"><span data-stu-id="60b26-123">The authentication type used between the Wi-Fi endpoint and the network.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="60b26-124">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="60b26-124">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="60b26-125">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="60b26-125">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>

<span data-ttu-id="60b26-126">**Abrir sistema** (2)</span><span class="sxs-lookup"><span data-stu-id="60b26-126">**Open System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>

<span data-ttu-id="60b26-127">**Clave compartida** (3)</span><span class="sxs-lookup"><span data-stu-id="60b26-127">**Shared Key** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA_PSK"></span><span id="wpa_psk"></span>

<span data-ttu-id="60b26-128">**WPA PSK** (4)</span><span class="sxs-lookup"><span data-stu-id="60b26-128">**WPA PSK** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>

<span data-ttu-id="60b26-129">**WPA IEEE 802.1 x** (5)</span><span class="sxs-lookup"><span data-stu-id="60b26-129">**WPA IEEE 802.1x** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA2_PSK"></span><span id="wpa2_psk"></span>

<span data-ttu-id="60b26-130">**PSK de WPA2** (6)</span><span class="sxs-lookup"><span data-stu-id="60b26-130">**WPA2 PSK** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>

<span data-ttu-id="60b26-131">**IEEE 802.1 de WPA2 x** (7)</span><span class="sxs-lookup"><span data-stu-id="60b26-131">**WPA2 IEEE 802.1x** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>

<span data-ttu-id="60b26-132">**CCKM IEEE 802.1 x** (8)</span><span class="sxs-lookup"><span data-stu-id="60b26-132">**CCKM IEEE 802.1x** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="60b26-133">**DMTF reservado** (9..)</span><span class="sxs-lookup"><span data-stu-id="60b26-133">**DMTF Reserved** (9..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60b26-134">**BSSType**</span><span class="sxs-lookup"><span data-stu-id="60b26-134">**BSSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b26-135">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60b26-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60b26-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b26-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b26-137">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 3,16")</span><span class="sxs-lookup"><span data-stu-id="60b26-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 3.16")</span></span>
</dt> </dl>

<span data-ttu-id="60b26-138">El tipo básico de Service Set (BSS) de la red que corresponde a la instancia.</span><span class="sxs-lookup"><span data-stu-id="60b26-138">The basic service set (BSS) type of the network that corresponds to the instance.</span></span> <span data-ttu-id="60b26-139">Un BSS es un conjunto de estaciones controlado por una única función de coordinación.</span><span class="sxs-lookup"><span data-stu-id="60b26-139">A BSS is a set of stations controlled by a single coordination function.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="60b26-140">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="60b26-140">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

<span data-ttu-id="60b26-141">**Independiente** (2)</span><span class="sxs-lookup"><span data-stu-id="60b26-141">**Independent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span>

<span data-ttu-id="60b26-142">**Infraestructura** (3)</span><span class="sxs-lookup"><span data-stu-id="60b26-142">**Infrastructure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="60b26-143">**DMTF reservado** (4..)</span><span class="sxs-lookup"><span data-stu-id="60b26-143">**DMTF Reserved** (4..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60b26-144">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="60b26-144">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b26-145">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60b26-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60b26-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b26-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b26-147">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**","**CIM \_ WiFiEndpoint**.**OtherEncryptionMethod**")</span><span class="sxs-lookup"><span data-stu-id="60b26-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**", "**CIM\_WiFiEndpoint**.**OtherEncryptionMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="60b26-148">El tipo de cifrado que se usa al enviar y recibir datos a través del punto de conexión de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="60b26-148">The encryption type used when sending and receiving data through the Wi-Fi endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="60b26-149">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="60b26-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="60b26-150">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="60b26-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WEP"></span><span id="wep"></span>

<span data-ttu-id="60b26-151">**WEP** (2)</span><span class="sxs-lookup"><span data-stu-id="60b26-151">**WEP** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TKIP"></span><span id="tkip"></span>

<span data-ttu-id="60b26-152">**TKIP** (3)</span><span class="sxs-lookup"><span data-stu-id="60b26-152">**TKIP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CCMP"></span><span id="ccmp"></span>

<span data-ttu-id="60b26-153">**CCMP** (4)</span><span class="sxs-lookup"><span data-stu-id="60b26-153">**CCMP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="60b26-154">**Ninguno** (5)</span><span class="sxs-lookup"><span data-stu-id="60b26-154">**None** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="60b26-155">**DMTF reservado** (6..)</span><span class="sxs-lookup"><span data-stu-id="60b26-155">**DMTF Reserved** (6..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60b26-156">**IEEE8021xAuthenticationProtocol**</span><span class="sxs-lookup"><span data-stu-id="60b26-156">**IEEE8021xAuthenticationProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b26-157">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60b26-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60b26-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b26-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b26-159">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RFC4017. IETF "," RFC2716. IETF "," draft-ietf-pppext-EAP-TTLS. IETF "," draft-Kamath-pppext-PEAPv0. IETF "," draft-Josefsson-pppext-EAP-TLS-EAP "," RFC4851. IETF "," RFC3748. IETF "," RFC4764. IETF "," RFC4186. IETF "," RFC4187. IETF "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**")</span><span class="sxs-lookup"><span data-stu-id="60b26-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RFC4017.IETF", "RFC2716.IETF", "draft-ietf-pppext-eap-ttls.IETF", "draft-kamath-pppext-peapv0.IETF", "draft-josefsson-pppext-eap-tls-eap", "RFC4851.IETF", "RFC3748.IETF", "RFC4764.IETF", "RFC4186.IETF", "RFC4187.IETF"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="60b26-160">El tipo de protocolo de autenticación extensible (EAP) para el punto de conexión de Wi-Fi cuando **AuthenticationMethod** contiene "7" (WPA IEEE 802.1 x) o "8" (CCKM IEEE 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="60b26-160">The EAP (Extensible Authentication Protocol) type for the Wi-Fi endpoint when **AuthenticationMethod** contains "7" (WPA IEEE 802.1x) or "8" (CCKM IEEE 802.1x).</span></span>

<dt>

<span id="EAP-TLS"></span><span id="eap-tls"></span>

<span data-ttu-id="60b26-161">**EAP-TLS** (0)</span><span class="sxs-lookup"><span data-stu-id="60b26-161">**EAP-TLS** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>

<span data-ttu-id="60b26-162">**EAP-TTLS/MSCHAPv2** (1)</span><span class="sxs-lookup"><span data-stu-id="60b26-162">**EAP-TTLS/MSCHAPv2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>

<span data-ttu-id="60b26-163">**PEAPv0/EAP-MSCHAPv2** (2)</span><span class="sxs-lookup"><span data-stu-id="60b26-163">**PEAPv0/EAP-MSCHAPv2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>

<span data-ttu-id="60b26-164">**PEAPv1/EAP-GTC** (3)</span><span class="sxs-lookup"><span data-stu-id="60b26-164">**PEAPv1/EAP-GTC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>

<span data-ttu-id="60b26-165">**EAP-FAST/MSCHAPv2** (4)</span><span class="sxs-lookup"><span data-stu-id="60b26-165">**EAP-FAST/MSCHAPv2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>

<span data-ttu-id="60b26-166">**EAP-FAST/GTC** (5)</span><span class="sxs-lookup"><span data-stu-id="60b26-166">**EAP-FAST/GTC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-MD5"></span><span id="eap-md5"></span>

<span data-ttu-id="60b26-167">**EAP-MD5** (6)</span><span class="sxs-lookup"><span data-stu-id="60b26-167">**EAP-MD5** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-PSK"></span><span id="eap-psk"></span>

<span data-ttu-id="60b26-168">**EAP-PSK** (7)</span><span class="sxs-lookup"><span data-stu-id="60b26-168">**EAP-PSK** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-SIM"></span><span id="eap-sim"></span>

<span data-ttu-id="60b26-169">**EAP-SIM** (8)</span><span class="sxs-lookup"><span data-stu-id="60b26-169">**EAP-SIM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-AKA"></span><span id="eap-aka"></span>

<span data-ttu-id="60b26-170">**EAP-AKA** (9)</span><span class="sxs-lookup"><span data-stu-id="60b26-170">**EAP-AKA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>

<span data-ttu-id="60b26-171">**EAP-FAST/TLS** (10)</span><span class="sxs-lookup"><span data-stu-id="60b26-171">**EAP-FAST/TLS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="60b26-172">**DMTF reservado** (11..)</span><span class="sxs-lookup"><span data-stu-id="60b26-172">**DMTF Reserved** (11..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60b26-173">**LANID**</span><span class="sxs-lookup"><span data-stu-id="60b26-173">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b26-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60b26-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b26-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b26-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b26-176">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LANID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 7.3.2.1")</span><span class="sxs-lookup"><span data-stu-id="60b26-176">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LANID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 7.3.2.1")</span></span>
</dt> </dl>

<span data-ttu-id="60b26-177">El identificador del conjunto de servicios (SSID) de la LAN inalámbrica que está asociado al extremo de Wi-Fi; de lo contrario, **es null**.</span><span class="sxs-lookup"><span data-stu-id="60b26-177">The service set identifier (SSID) of the wireless LAN that is associated with the Wi-Fi endpoint; otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="60b26-178">**OtherAuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="60b26-178">**OtherAuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b26-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60b26-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b26-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b26-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b26-181">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**")</span><span class="sxs-lookup"><span data-stu-id="60b26-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="60b26-182">El tipo de autenticación usado entre el punto de conexión de Wi-Fi y la red cuando **AuthenticationMethod** contiene "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="60b26-182">The authentication type used between the Wi-Fi endpoint and the network when **AuthenticationMethod** contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="60b26-183">**OtherEncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="60b26-183">**OtherEncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b26-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60b26-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b26-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b26-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b26-186">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**EncryptionMethod**")</span><span class="sxs-lookup"><span data-stu-id="60b26-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**EncryptionMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="60b26-187">Describe el tipo de cifrado para el punto de conexión de Wi-Fi cuando **EncryptionMethod** contiene "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="60b26-187">Describes the encryption type for the Wi-Fi endpoint when **EncryptionMethod** contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="60b26-188">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="60b26-188">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b26-189">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60b26-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60b26-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b26-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b26-191">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ProtocolIFType")</span><span class="sxs-lookup"><span data-stu-id="60b26-191">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ProtocolIFType")</span></span>
</dt> </dl>

<span data-ttu-id="60b26-192">Categoría o clasificación de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="60b26-192">The category or classification of this instance.</span></span> <span data-ttu-id="60b26-193">Los valores posibles se limitan a los valores Wi-Fi y Reserved de la MIB de DMTF e [IANA ifType](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="60b26-193">The possible values are limited to the Wi-Fi and reserved values from the DMTF and [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span>

<span data-ttu-id="60b26-194">Si **ProtocolIFType** se establece en "1" (otro), se debe proporcionar la información de tipo en la propiedad **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="60b26-194">If the **ProtocolIFType** is set to "1" (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="60b26-195">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="60b26-195">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>

<span data-ttu-id="60b26-196">**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="60b26-196">**IEEE 802.11** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>

<span data-ttu-id="60b26-197">**IANA reservado** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="60b26-197">**IANA Reserved** (225..4095)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="60b26-198">**DMTF reservado** (4301.. 32767)</span><span class="sxs-lookup"><span data-stu-id="60b26-198">**DMTF Reserved** (4301..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="60b26-199">**Proveedor reservado** (32768...)</span><span class="sxs-lookup"><span data-stu-id="60b26-199">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="60b26-200"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="60b26-200"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="60b26-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60b26-201">Requirements</span></span>



| <span data-ttu-id="60b26-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="60b26-202">Requirement</span></span> | <span data-ttu-id="60b26-203">Value</span><span class="sxs-lookup"><span data-stu-id="60b26-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b26-204">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60b26-204">Minimum supported client</span></span><br/> | <span data-ttu-id="60b26-205">Windows 8</span><span class="sxs-lookup"><span data-stu-id="60b26-205">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="60b26-206">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60b26-206">Minimum supported server</span></span><br/> | <span data-ttu-id="60b26-207">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60b26-207">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="60b26-208">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60b26-208">Namespace</span></span><br/>                | <span data-ttu-id="60b26-209">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="60b26-209">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="60b26-210">MOF</span><span class="sxs-lookup"><span data-stu-id="60b26-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60b26-211"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60b26-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="60b26-212">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60b26-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60b26-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60b26-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="60b26-214">Vea también</span><span class="sxs-lookup"><span data-stu-id="60b26-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b26-215">**\_LANENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="60b26-215">**CIM\_LANEndpoint**</span></span>](cim-lanendpoint.md)
</dt> </dl>

 

