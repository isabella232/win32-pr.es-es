---
description: Define un algoritmo de cifrado para el cifrado y descifrado de datos.
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
title: DOT11_CIPHER_ALGORITHM enumeración (Wlantypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_CIPHER_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fcbd61476458b5ed906ee57af6ab22b35f0378d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071611"
---
# <a name="dot11_cipher_algorithm-enumeration"></a>Enumeración \_ DOT11 CIPHER \_ ALGORITHM

El **tipo enumerado DOT11 \_ CIPHER \_ ALGORITHM** define un algoritmo de cifrado para el cifrado y descifrado de datos.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _DOT11_CIPHER_ALGORITHM { 
  DOT11_CIPHER_ALGO_NONE           = 0x00,
  DOT11_CIPHER_ALGO_WEP40          = 0x01,
  DOT11_CIPHER_ALGO_TKIP           = 0x02,
  DOT11_CIPHER_ALGO_CCMP           = 0x04,
  DOT11_CIPHER_ALGO_WEP104         = 0x05,
  DOT11_CIPHER_ALGO_WPA_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_RSN_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_WEP            = 0x101,
  DOT11_CIPHER_ALGO_IHV_START      = 0x80000000,
  DOT11_CIPHER_ALGO_IHV_END        = 0xffffffff
} DOT11_CIPHER_ALGORITHM, *PDOT11_CIPHER_ALGORITHM;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11 \_ CIPHER \_ ALGO \_ NONE**
</dt> <dd>

Especifica que no se habilita ni se admite ningún algoritmo de cifrado.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11 \_ CIPHER \_ ALGO \_ WEP40**
</dt> <dd>

Especifica un algoritmo de privacidad equivalente cableada (WEP), que es el algoritmo basado en RC4 que se especifica en el estándar 802.11-1999. Este enumerador especifica el algoritmo de cifrado WEP con una clave de cifrado de 40 bits.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**DOT11 \_ CIPHER \_ ALGO \_ TKIP**
</dt> <dd>

Especifica un algoritmo del Protocolo de integridad de claves temporales (TKIP), que es el conjunto de cifrado basado en RC4 que se basa en los algoritmos definidos en la especificación WPA y el estándar IEEE 802.11i-2004. Este cifrado también usa el algoritmo de código de integridad de mensajes (MIC) de Michael para la protección de falsificación.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**CCMP DE ALGO CIFRADO DOT11 \_ \_ \_**
</dt> <dd>

Especifica un algoritmo AES-CCMP, como se especifica en el estándar IEEE 802.11i-2004 y RFC 3610. Estándar de cifrado avanzado (AES) es el algoritmo de cifrado definido en FIPS PUB 197.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**ALGO DE \_ CIFRADO \_ DOT11 \_ WEP104**
</dt> <dd>

Especifica un algoritmo de cifrado WEP con una clave de cifrado de 104 bits.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**GRUPO DE USO \_ DE WPA DE ALGORITMO DE CIFRADO \_ \_ DOT11 \_ \_**
</dt> <dd>

Especifica un Wi-Fi de cifrado de clave de grupo de uso de acceso protegido (WPA). Para obtener más información sobre el conjunto de cifrado Usar clave de grupo, consulte la cláusula 7.3.2.25.1 del estándar IEEE 802.11i-2004.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11 \_ CIPHER \_ ALGO \_ RSN \_ USE \_ GROUP**
</dt> <dd>

Especifica una red de seguridad sólida (RSN) Que use el conjunto de cifrado de clave de grupo. Para obtener más información sobre el conjunto de cifrado Usar clave de grupo, consulte la cláusula 7.3.2.25.1 del estándar IEEE 802.11i-2004.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**ALGO \_ WEP DE CIFRADO \_ DOT11 \_**
</dt> <dd>

Especifica un algoritmo de cifrado WEP con una clave de cifrado de cualquier longitud.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**INICIO DE \_ \_ \_ IHV DEL ALGORITMO DE CIFRADO DOT11 \_**
</dt> <dd>

Especifica el inicio del intervalo que se usa para definir algoritmos de cifrado propietarios desarrollados por un proveedor de hardware independiente (IHV).

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11 \_ CIPHER \_ ALGO \_ IHV \_ END**
</dt> <dd>

Especifica el final del intervalo que se usa para definir algoritmos de cifrado propietarios desarrollados por un IHV.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp3 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                        |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>Wlantypes.h (incluye Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PAR DE CIFRADO DE \_ AUTENTICACIÓN \_ DE DOT11 \_**](dot11-auth-cipher-pair.md)
</dt> <dt>

[**RED DISPONIBLE DE WLAN \_ \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[**ATRIBUTOS DE SEGURIDAD DE WLAN \_ \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




