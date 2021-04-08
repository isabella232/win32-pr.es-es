---
description: Se usan para definir una dirección IEEE Media Access Control (MAC).
ms.assetid: c1335127-a2d2-4f44-a895-1abbc5eaf98d
title: DOT11_MAC_ADDRESS (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77b43635462c4b48890599512cc1a413461de72e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910658"
---
# <a name="dot11_mac_address"></a>\_Dirección Mac de DOT11 \_

Los tipos de **\_ \_ dirección Mac de DOT11** se usan para definir una dirección de Media Access Control IEEE (Mac).


```C++
typedef UCHAR DOT11_MAC_ADDRESS[6];
typedef DOT11_MAC_ADDRESS* PDOT11_MAC_ADDRESS;
```



<dl> <dt>

**\_Dirección Mac de DOT11 \_ \[ 6\]**
</dt> <dd>

Una dirección MAC en formato de unidifusión, multidifusión o difusión.

</dd> <dt>

**\_Dirección Mac \_ PDOT11**
</dt> <dd>

Puntero a una dirección MAC en formato de unidifusión, multidifusión o difusión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                       |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Windot11. h (incluye Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Lista de BSSID de DOT11 \_**](dot11-bssid-list.md)
</dt> <dt>

[**atributos de la Asociación de WLAN \_ \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[**\_entrada de BSS de WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> </dl>

 

 




