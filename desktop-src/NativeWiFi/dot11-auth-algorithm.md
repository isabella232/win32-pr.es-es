---
description: Define un algoritmo de autenticación de LAN inalámbrica.
ms.assetid: ac4097df-46dc-4c64-b72a-7cb9dce8b418
title: DOT11_AUTH_ALGORITHM enumeración (Wlantypes.h)
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
ms.openlocfilehash: 774b2218a451f4cbaa85e6b77559c0d5761b0b132ebdf9d3f11c15ea6658e7bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798475"
---
# <a name="dot11_auth_algorithm-enumeration"></a>Enumeración DOT11 \_ AUTH \_ ALGORITHM

El **tipo enumerado DOT11 \_ AUTH \_ ALGORITHM** define un algoritmo de autenticación LAN inalámbrica.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11 \_ AUTH \_ ALGO \_ 80211 \_ OPEN**
</dt> <dd>

Especifica un algoritmo de autenticación de sistema abierto IEEE 802.11.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**CLAVE COMPARTIDA \_ DE \_ ALGO \_ 80211 DE AUTENTICACIÓN DE DOT11 \_ \_**
</dt> <dd>

Especifica un algoritmo de autenticación de clave compartida 802.11 que requiere el uso de una clave de privacidad equivalente cableada (WEP) previamente compartida para la autenticación 802.11.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA**
</dt> <dd>

Especifica un algoritmo Wi-Fi acceso protegido (WPA). El servidor de suplicación, autenticador y autenticación realiza la autenticación de puerto IEEE 802.1X. Las claves de cifrado se derivan dinámicamente a través del proceso de autenticación.

Este algoritmo solo es válido para los tipos BSS de infraestructura de tipo \_ BSS dot11. \_ \_

Cuando se habilita el algoritmo WPA, la estación 802.11 solo se asociará a un punto de acceso cuyas respuestas de sondeo o señalización contengan el conjunto de autenticación de tipo 1 (802.1X) dentro del elemento de información wpa (IE).

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA \_ PSK**
</dt> <dd>

Especifica un algoritmo WPA que usa claves previamente compartidas (PSK). La autenticación de puerto IEEE 802.1X se realiza mediante el suplicante y el autenticador. Las claves de cifrado se derivan dinámicamente a través de una clave previamente compartida que se usa tanto en el suplicante como en el autenticador.

Este algoritmo solo es válido para los tipos BSS de la infraestructura **de tipo \_ BSS \_ \_ dot11.**

Cuando se habilita el algoritmo PSK de WPA, la estación 802.11 solo se asociará a un punto de acceso cuyas respuestas de sondeo o de señalización contengan el conjunto de autenticación de tipo 2 (clave previamente compartida) dentro de WPA IE.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA \_ NONE**
</dt> <dd>

Este valor no se admite.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**DOT11 \_ AUTH \_ ALGO \_ RSNA**
</dt> <dd>

Especifica un algoritmo 802.11i Robust Security Network Association (RSNA). WPA2 es uno de estos algoritmos. El servidor de suplicación, autenticador y autenticación realiza la autenticación de puerto IEEE 802.1X. Las claves de cifrado se derivan dinámicamente a través del proceso de autenticación.

Este algoritmo solo es válido para los tipos BSS de la infraestructura **de tipo \_ BSS \_ \_ dot11.**

Cuando se habilita el algoritmo RSNA, la estación 802.11 solo se asociará a un punto de acceso cuyas respuestas de sondeo o de señalización contengan el conjunto de autenticación de tipo 1 (802.1X) dentro del RSN IE.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11 \_ AUTH \_ ALGO \_ RSNA \_ PSK**
</dt> <dd>

Especifica un algoritmo RSNA 802.11i que usa PSK. La autenticación de puerto IEEE 802.1X se realiza mediante el suplicante y el autenticador. Las claves de cifrado se derivan dinámicamente a través de una clave previamente compartida que se usa tanto en el suplicante como en el autenticador.

Este algoritmo solo es válido para los tipos BSS de la infraestructura **de tipo \_ BSS \_ \_ dot11.**

Cuando se habilita el algoritmo PSK de RSNA, la estación 802.11 solo se asociará a un punto de acceso cuyas respuestas de sondeo o señalización contengan el conjunto de autenticación de tipo 2 (clave previamente compartida) dentro del RSN IE.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**PUNTO11 \_ AUTH \_ ALGO \_ IHV \_ START**
</dt> <dd>

Indica el inicio del intervalo que especifica algoritmos de autenticación propietarios desarrollados por un IHV.

El **enumerador DOT11 \_ AUTH \_ ALGO \_ IHV \_ START** solo es válido cuando el controlador de minipuerto funciona en modo Extensible Station (ExtSTA).

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11 \_ AUTH \_ ALGO \_ IHV \_ END**
</dt> <dd>

Indica el final del intervalo que especifica algoritmos de autenticación propietarios desarrollados por un IHV.

El **enumerador DOT11 \_ AUTH \_ ALGO \_ IHV \_ END** solo es válido cuando el controlador de minipuerto funciona en modo ExtSTA.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp3 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                        |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                                         |
| Header<br/>                   | <dl> <dt>Wlantypes.h (incluye Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PAR DE CIFRADO DE \_ AUTENTICACIÓN \_ DE DOT11 \_**](dot11-auth-cipher-pair.md)
</dt> <dt>

[**RED DISPONIBLE DE WLAN \_ \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[**ATRIBUTOS DE SEGURIDAD DE WLAN \_ \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




