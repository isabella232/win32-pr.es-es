---
description: Define un algoritmo de autenticación de LAN inalámbrica.
ms.assetid: ac4097df-46dc-4c64-b72a-7cb9dce8b418
title: Enumeración DOT11_AUTH_ALGORITHM (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 1b14886c62448194b79eab2e0302ce5608ad282d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678017"
---
# <a name="dot11_auth_algorithm-enumeration"></a><span data-ttu-id="ab190-103">\_Enumeración de algoritmos de autenticación de DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="ab190-103">DOT11\_AUTH\_ALGORITHM enumeration</span></span>

<span data-ttu-id="ab190-104">El tipo enumerado de **\_ \_ algoritmo** de autenticación de DOT11 define un algoritmo de autenticación de LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="ab190-104">The **DOT11\_AUTH\_ALGORITHM** enumerated type defines a wireless LAN authentication algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab190-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab190-105">Syntax</span></span>


```C++
typedef enum _DOT11_AUTH_ALGORITHM { 
  DOT11_AUTH_ALGO_80211_OPEN        = 1,
  DOT11_AUTH_ALGO_80211_SHARED_KEY  = 2,
  DOT11_AUTH_ALGO_WPA               = 3,
  DOT11_AUTH_ALGO_WPA_PSK           = 4,
  DOT11_AUTH_ALGO_WPA_NONE          = 5,
  DOT11_AUTH_ALGO_RSNA              = 6,
  DOT11_AUTH_ALGO_RSNA_PSK          = 7,
  DOT11_AUTH_ALGO_IHV_START         = 0x80000000,
  DOT11_AUTH_ALGO_IHV_END           = 0xffffffff
} DOT11_AUTH_ALGORITHM, *PDOT11_AUTH_ALGORITHM;
```



## <a name="constants"></a><span data-ttu-id="ab190-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ab190-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ab190-107"><span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**ALGO de autenticación de DOT11 \_ \_ \_ 80211 \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="ab190-107"><span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11\_AUTH\_ALGO\_80211\_OPEN**</span></span>
</dt> <dd>

<span data-ttu-id="ab190-108">Especifica un algoritmo de autenticación del sistema abierto IEEE 802,11.</span><span class="sxs-lookup"><span data-stu-id="ab190-108">Specifies an IEEE 802.11 Open System authentication algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="ab190-109"><span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**\_ \_ \_ Clave compartida algo 80211 \_ de autenticación de DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="ab190-109"><span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**DOT11\_AUTH\_ALGO\_80211\_SHARED\_KEY**</span></span>
</dt> <dd>

<span data-ttu-id="ab190-110">Especifica un algoritmo de autenticación de clave compartida 802,11 que requiere el uso de una clave de privacidad equivalente por cable (WEP) previamente compartida para la autenticación 802,11.</span><span class="sxs-lookup"><span data-stu-id="ab190-110">Specifies an 802.11 Shared Key authentication algorithm that requires the use of a pre-shared Wired Equivalent Privacy (WEP) key for the 802.11 authentication.</span></span>

</dd> <dt>

<span data-ttu-id="ab190-111"><span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**\_Autenticación de \_ algo \_ WPA de DOT11**</span><span class="sxs-lookup"><span data-stu-id="ab190-111"><span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11\_AUTH\_ALGO\_WPA**</span></span>
</dt> <dd>

<span data-ttu-id="ab190-112">Especifica un algoritmo de acceso protegido Wi-Fi (WPA).</span><span class="sxs-lookup"><span data-stu-id="ab190-112">Specifies a Wi-Fi Protected Access (WPA) algorithm.</span></span> <span data-ttu-id="ab190-113">El solicitante, el autenticador y el servidor de autenticación realizan la autenticación del puerto IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="ab190-113">IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.</span></span> <span data-ttu-id="ab190-114">Las claves de cifrado se derivan dinámicamente a través del proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="ab190-114">Cipher keys are dynamically derived through the authentication process.</span></span>

<span data-ttu-id="ab190-115">Este algoritmo solo es válido para los tipos de BSS de la \_ infraestructura de tipo BSS de dot11 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ab190-115">This algorithm is valid only for BSS types of dot11\_BSS\_type\_infrastructure.</span></span>

<span data-ttu-id="ab190-116">Cuando el algoritmo de WPA está habilitado, la estación 802,11 solo se asociará a un punto de acceso cuyas contestaciones de señal o sondeo contengan el conjunto de autenticación de tipo 1 (802.1 X) dentro del elemento de información de WPA (es decir,).</span><span class="sxs-lookup"><span data-stu-id="ab190-116">When the WPA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the WPA information element (IE).</span></span>

</dd> <dt>

<span data-ttu-id="ab190-117"><span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**\_ \_ Algo WPA de \_ autenticación de DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="ab190-117"><span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11\_AUTH\_ALGO\_WPA\_PSK**</span></span>
</dt> <dd>

<span data-ttu-id="ab190-118">Especifica un algoritmo de WPA que usa claves previamente compartidas (PSK).</span><span class="sxs-lookup"><span data-stu-id="ab190-118">Specifies a WPA algorithm that uses preshared keys (PSK).</span></span> <span data-ttu-id="ab190-119">El solicitante y el autenticador realizan la autenticación del puerto IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="ab190-119">IEEE 802.1X port authentication is performed by the supplicant and authenticator.</span></span> <span data-ttu-id="ab190-120">Las claves de cifrado se derivan dinámicamente a través de una clave previamente compartida que se utiliza en el solicitante y el autenticador.</span><span class="sxs-lookup"><span data-stu-id="ab190-120">Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.</span></span>

<span data-ttu-id="ab190-121">Este algoritmo solo es válido para los tipos de BSS de la **\_ \_ \_ infraestructura de tipo BSS de dot11**.</span><span class="sxs-lookup"><span data-stu-id="ab190-121">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="ab190-122">Cuando el algoritmo WPA PSK está habilitado, la estación 802,11 solo se asociará con un punto de acceso cuyas respuestas de señal o sondeo contengan el conjunto de autenticación de tipo 2 (clave previamente compartida) dentro de la IE de WPA.</span><span class="sxs-lookup"><span data-stu-id="ab190-122">When the WPA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2 (preshared key) within the WPA IE.</span></span>

</dd> <dt>

<span data-ttu-id="ab190-123"><span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**Autenticación de DOT11 \_ \_ algo \_ WPA \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="ab190-123"><span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11\_AUTH\_ALGO\_WPA\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="ab190-124">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="ab190-124">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ab190-125"><span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**ALGO de autenticación de DOT11 \_ \_ \_ RSNA**</span><span class="sxs-lookup"><span data-stu-id="ab190-125"><span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**DOT11\_AUTH\_ALGO\_RSNA**</span></span>
</dt> <dd>

<span data-ttu-id="ab190-126">Especifica un algoritmo de Asociación de red de seguridad (RSNA) 802.11 i robusto.</span><span class="sxs-lookup"><span data-stu-id="ab190-126">Specifies an 802.11i Robust Security Network Association (RSNA) algorithm.</span></span> <span data-ttu-id="ab190-127">WPA2 es un algoritmo de este tipo.</span><span class="sxs-lookup"><span data-stu-id="ab190-127">WPA2 is one such algorithm.</span></span> <span data-ttu-id="ab190-128">El solicitante, el autenticador y el servidor de autenticación realizan la autenticación del puerto IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="ab190-128">IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.</span></span> <span data-ttu-id="ab190-129">Las claves de cifrado se derivan dinámicamente a través del proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="ab190-129">Cipher keys are dynamically derived through the authentication process.</span></span>

<span data-ttu-id="ab190-130">Este algoritmo solo es válido para los tipos de BSS de la **\_ \_ \_ infraestructura de tipo BSS de dot11**.</span><span class="sxs-lookup"><span data-stu-id="ab190-130">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="ab190-131">Cuando el algoritmo RSNA está habilitado, la estación 802,11 solo se asociará a un punto de acceso cuyas respuestas de sondeo o sondeo contengan el conjunto de autenticación de tipo 1 (802.1 X) dentro del RSN de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ab190-131">When the RSNA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the RSN IE.</span></span>

</dd> <dt>

<span data-ttu-id="ab190-132"><span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**Autenticación de DOT11 \_ \_ algo \_ RSNA \_ PSK**</span><span class="sxs-lookup"><span data-stu-id="ab190-132"><span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11\_AUTH\_ALGO\_RSNA\_PSK**</span></span>
</dt> <dd>

<span data-ttu-id="ab190-133">Especifica un algoritmo 802.11 i RSNA que usa PSK.</span><span class="sxs-lookup"><span data-stu-id="ab190-133">Specifies an 802.11i RSNA algorithm that uses PSK.</span></span> <span data-ttu-id="ab190-134">El solicitante y el autenticador realizan la autenticación del puerto IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="ab190-134">IEEE 802.1X port authentication is performed by the supplicant and authenticator.</span></span> <span data-ttu-id="ab190-135">Las claves de cifrado se derivan dinámicamente a través de una clave previamente compartida que se utiliza en el solicitante y el autenticador.</span><span class="sxs-lookup"><span data-stu-id="ab190-135">Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.</span></span>

<span data-ttu-id="ab190-136">Este algoritmo solo es válido para los tipos de BSS de la **\_ \_ \_ infraestructura de tipo BSS de dot11**.</span><span class="sxs-lookup"><span data-stu-id="ab190-136">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="ab190-137">Cuando el algoritmo RSNA PSK está habilitado, la estación 802,11 solo se asociará con un punto de acceso cuyas contestaciones de señal o sondeo contengan el conjunto de autenticación de tipo 2 (clave previamente compartida) dentro de la IE de RSN.</span><span class="sxs-lookup"><span data-stu-id="ab190-137">When the RSNA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2(preshared key) within the RSN IE.</span></span>

</dd> <dt>

<span data-ttu-id="ab190-138"><span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**\_Inicio de \_ IHV de algo de autenticación de DOT11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ab190-138"><span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**DOT11\_AUTH\_ALGO\_IHV\_START**</span></span>
</dt> <dd>

<span data-ttu-id="ab190-139">Indica el inicio del intervalo que especifica los algoritmos de autenticación propietarios desarrollados por un IHV.</span><span class="sxs-lookup"><span data-stu-id="ab190-139">Indicates the start of the range that specifies proprietary authentication algorithms that are developed by an IHV.</span></span>

<span data-ttu-id="ab190-140">El enumerador de inicio de IHV de algo de autenticación de DOT11 solo es válido cuando el controlador de minipuerto está funcionando en modo de estación extensible (ExtSTA). **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ab190-140">The **DOT11\_AUTH\_ALGO\_IHV\_START** enumerator is valid only when the miniport driver is operating in Extensible Station (ExtSTA) mode.</span></span>

</dd> <dt>

<span data-ttu-id="ab190-141"><span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**\_Final de \_ IHV de algo de autenticación de DOT11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ab190-141"><span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11\_AUTH\_ALGO\_IHV\_END**</span></span>
</dt> <dd>

<span data-ttu-id="ab190-142">Indica el final del intervalo que especifica los algoritmos de autenticación propietarios desarrollados por un IHV.</span><span class="sxs-lookup"><span data-stu-id="ab190-142">Indicates the end of the range that specifies proprietary authentication algorithms that are developed by an IHV.</span></span>

<span data-ttu-id="ab190-143">El enumerador de **\_ \_ algo \_ IHV \_ de autenticación de DOT11** solo es válido cuando el controlador de minipuerto está funcionando en modo ExtSTA.</span><span class="sxs-lookup"><span data-stu-id="ab190-143">The **DOT11\_AUTH\_ALGO\_IHV\_END** enumerator is valid only when the miniport driver is operating in ExtSTA mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab190-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab190-144">Requirements</span></span>



| <span data-ttu-id="ab190-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab190-145">Requirement</span></span> | <span data-ttu-id="ab190-146">Value</span><span class="sxs-lookup"><span data-stu-id="ab190-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab190-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab190-147">Minimum supported client</span></span><br/> | <span data-ttu-id="ab190-148">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="ab190-148">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ab190-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab190-149">Minimum supported server</span></span><br/> | <span data-ttu-id="ab190-150">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab190-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="ab190-151">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ab190-151">Redistributable</span></span><br/>          | <span data-ttu-id="ab190-152">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="ab190-152">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="ab190-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab190-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab190-154"><dt>Wlantypes. h (incluye Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab190-154"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab190-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab190-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab190-156">**\_Par de \_ cifrado de autenticación de DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="ab190-156">**DOT11\_AUTH\_CIPHER\_PAIR**</span></span>](dot11-auth-cipher-pair.md)
</dt> <dt>

[<span data-ttu-id="ab190-157">**\_red disponible de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="ab190-157">**WLAN\_AVAILABLE\_NETWORK**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[<span data-ttu-id="ab190-158">**\_atributos de seguridad de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="ab190-158">**WLAN\_SECURITY\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




