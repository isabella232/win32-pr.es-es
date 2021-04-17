---
description: Define un algoritmo de cifrado para el cifrado y descifrado de datos.
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
title: Enumeración DOT11_CIPHER_ALGORITHM (Wlantypes. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678015"
---
# <a name="dot11_cipher_algorithm-enumeration"></a>\_Enumeración de algoritmos de cifrado de DOT11 \_

El tipo enumerado del **\_ \_ algoritmo de cifrado de DOT11** define un algoritmo de cifrado para el cifrado y descifrado de datos.

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

<span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**\_Cifrado de DOT11 \_ algo \_ ninguno**
</dt> <dd>

Especifica que no se habilita ni se admite ningún algoritmo de cifrado.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**\_Cifrado de \_ algo \_ WEP40 de DOT11**
</dt> <dd>

Especifica un algoritmo de privacidad equivalente por cable (WEP), que es el algoritmo basado en RC4 que se especifica en el estándar 802.11-1999. Este enumerador especifica el algoritmo de cifrado de WEP con una clave de cifrado de 40 bits.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**\_Cifrado de \_ algo \_ TKIP de DOT11**
</dt> <dd>

Especifica un algoritmo del Protocolo de integridad de clave temporal (TKIP), que es el conjunto de cifrado basado en RC4 que se basa en los algoritmos definidos en la especificación de WPA y el estándar IEEE 802.11 i-2004. Este cifrado también usa el algoritmo de código de integridad del mensaje (MIC) de Michael para la protección de falsificación.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**\_Cifrado de DOT11 \_ algo \_ CCMP**
</dt> <dd>

Especifica un algoritmo AES-CCMP, tal y como se especifica en el estándar IEEE 802.11 i-2004 y RFC 3610. Estándar de cifrado avanzado (AES) es el algoritmo de cifrado definido en FIPS PUB 197.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**\_Cifrado de \_ algo \_ WEP104 de DOT11**
</dt> <dd>

Especifica un algoritmo de cifrado de WEP con una clave de cifrado de 104 bits.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**\_Cifrado de DOT11 \_ algo \_ grupo de uso de WPA \_ \_**
</dt> <dd>

Especifica un conjunto de cifrado de claves de grupo de uso de Wi-Fi protegido (WPA). Para obtener más información sobre el conjunto de cifrado de claves de grupo, consulte la cláusula 7.3.2.25.1 del estándar IEEE 802.11 i-2004.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**\_Cifrado de DOT11 \_ algo de uso de \_ RSN \_ \_**
</dt> <dd>

Especifica un conjunto de cifrado de claves de grupo de uso de redes de seguridad sólidas (RSN). Para obtener más información sobre el conjunto de cifrado de claves de grupo, consulte la cláusula 7.3.2.25.1 del estándar IEEE 802.11 i-2004.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**\_Cifrado de algo de DOT11 \_ \_ WEP**
</dt> <dd>

Especifica un algoritmo de cifrado WEP con una clave de cifrado de cualquier longitud.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**\_Inicio de \_ \_ IHV algo de CIFRAdo de DOT11 \_**
</dt> <dd>

Especifica el inicio del intervalo que se usa para definir los algoritmos de cifrado de propiedad desarrollados por un fabricante de hardware independiente (IHV).

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**\_Fin de \_ algo \_ IHV de CIFRAdo de DOT11 \_**
</dt> <dd>

Especifica el final del intervalo que se utiliza para definir los algoritmos de cifrado de propiedad desarrollados por un IHV.

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

 

 




