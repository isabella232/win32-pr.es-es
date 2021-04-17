---
description: Define un tipo de red de Basic Service Set (BSS).
ms.assetid: 13d57339-655e-4978-974e-e7b12a83d18a
title: Enumeración DOT11_BSS_TYPE (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSS_TYPE
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 7815e75f3ef7ef8d908b7d2b26f2e5f9d3630009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678016"
---
# <a name="dot11_bss_type-enumeration"></a>\_Enumeración de tipo BSS de DOT11 \_

El tipo enumerado de BSS de DOT11 define un tipo de red de conjunto de servicio básico (BSS). **\_ \_**

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _DOT11_BSS_TYPE { 
  dot11_BSS_type_infrastructure  = 1,
  dot11_BSS_type_independent     = 2,
  dot11_BSS_type_any             = 3
} DOT11_BSS_TYPE, *PDOT11_BSS_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**\_infraestructura de \_ tipo \_ BSS de dot11**
</dt> <dd>

Especifica una red BSS de infraestructura.

</dd> <dt>

<span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**\_independiente del \_ tipo \_ BSS de dot11**
</dt> <dd>

Especifica una red BSS independiente (IBSS).

</dd> <dt>

<span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**\_tipo BSS de dot11 \_ \_ any**
</dt> <dd>

Especifica una red de infraestructura o IBSS.

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

[**\_entrada de BSS de WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> <dt>

[**\_parámetros de conexión de WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[**WlanGetNetworkBssList**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> </dl>

 

 




