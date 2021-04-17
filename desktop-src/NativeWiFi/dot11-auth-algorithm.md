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
# <a name="dot11_auth_algorithm-enumeration"></a>\_Enumeración de algoritmos de autenticación de DOT11 \_

El tipo enumerado de **\_ \_ algoritmo** de autenticación de DOT11 define un algoritmo de autenticación de LAN inalámbrica.

## <a name="syntax"></a>Sintaxis


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

<span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**ALGO de autenticación de DOT11 \_ \_ \_ 80211 \_ abierto**
</dt> <dd>

Especifica un algoritmo de autenticación del sistema abierto IEEE 802,11.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**\_ \_ \_ Clave compartida algo 80211 \_ de autenticación de DOT11 \_**
</dt> <dd>

Especifica un algoritmo de autenticación de clave compartida 802,11 que requiere el uso de una clave de privacidad equivalente por cable (WEP) previamente compartida para la autenticación 802,11.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**\_Autenticación de \_ algo \_ WPA de DOT11**
</dt> <dd>

Especifica un algoritmo de acceso protegido Wi-Fi (WPA). El solicitante, el autenticador y el servidor de autenticación realizan la autenticación del puerto IEEE 802.1 X. Las claves de cifrado se derivan dinámicamente a través del proceso de autenticación.

Este algoritmo solo es válido para los tipos de BSS de la \_ infraestructura de tipo BSS de dot11 \_ \_ .

Cuando el algoritmo de WPA está habilitado, la estación 802,11 solo se asociará a un punto de acceso cuyas contestaciones de señal o sondeo contengan el conjunto de autenticación de tipo 1 (802.1 X) dentro del elemento de información de WPA (es decir,).

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**\_ \_ Algo WPA de \_ autenticación de DOT11 \_**
</dt> <dd>

Especifica un algoritmo de WPA que usa claves previamente compartidas (PSK). El solicitante y el autenticador realizan la autenticación del puerto IEEE 802.1 X. Las claves de cifrado se derivan dinámicamente a través de una clave previamente compartida que se utiliza en el solicitante y el autenticador.

Este algoritmo solo es válido para los tipos de BSS de la **\_ \_ \_ infraestructura de tipo BSS de dot11**.

Cuando el algoritmo WPA PSK está habilitado, la estación 802,11 solo se asociará con un punto de acceso cuyas respuestas de señal o sondeo contengan el conjunto de autenticación de tipo 2 (clave previamente compartida) dentro de la IE de WPA.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**Autenticación de DOT11 \_ \_ algo \_ WPA \_ ninguno**
</dt> <dd>

Este valor no se admite.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**ALGO de autenticación de DOT11 \_ \_ \_ RSNA**
</dt> <dd>

Especifica un algoritmo de Asociación de red de seguridad (RSNA) 802.11 i robusto. WPA2 es un algoritmo de este tipo. El solicitante, el autenticador y el servidor de autenticación realizan la autenticación del puerto IEEE 802.1 X. Las claves de cifrado se derivan dinámicamente a través del proceso de autenticación.

Este algoritmo solo es válido para los tipos de BSS de la **\_ \_ \_ infraestructura de tipo BSS de dot11**.

Cuando el algoritmo RSNA está habilitado, la estación 802,11 solo se asociará a un punto de acceso cuyas respuestas de sondeo o sondeo contengan el conjunto de autenticación de tipo 1 (802.1 X) dentro del RSN de Internet Explorer.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**Autenticación de DOT11 \_ \_ algo \_ RSNA \_ PSK**
</dt> <dd>

Especifica un algoritmo 802.11 i RSNA que usa PSK. El solicitante y el autenticador realizan la autenticación del puerto IEEE 802.1 X. Las claves de cifrado se derivan dinámicamente a través de una clave previamente compartida que se utiliza en el solicitante y el autenticador.

Este algoritmo solo es válido para los tipos de BSS de la **\_ \_ \_ infraestructura de tipo BSS de dot11**.

Cuando el algoritmo RSNA PSK está habilitado, la estación 802,11 solo se asociará con un punto de acceso cuyas contestaciones de señal o sondeo contengan el conjunto de autenticación de tipo 2 (clave previamente compartida) dentro de la IE de RSN.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**\_Inicio de \_ IHV de algo de autenticación de DOT11 \_ \_**
</dt> <dd>

Indica el inicio del intervalo que especifica los algoritmos de autenticación propietarios desarrollados por un IHV.

El enumerador de inicio de IHV de algo de autenticación de DOT11 solo es válido cuando el controlador de minipuerto está funcionando en modo de estación extensible (ExtSTA). **\_ \_ \_ \_**

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**\_Final de \_ IHV de algo de autenticación de DOT11 \_ \_**
</dt> <dd>

Indica el final del intervalo que especifica los algoritmos de autenticación propietarios desarrollados por un IHV.

El enumerador de **\_ \_ algo \_ IHV \_ de autenticación de DOT11** solo es válido cuando el controlador de minipuerto está funcionando en modo ExtSTA.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                        |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>Wlantypes. h (incluye Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Par de \_ cifrado de autenticación de DOT11 \_**](dot11-auth-cipher-pair.md)
</dt> <dt>

[**\_red disponible de WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[**\_atributos de seguridad de WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




