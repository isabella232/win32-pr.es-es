---
description: Contiene el SSID de una interfaz.
ms.assetid: f2b15ef9-99ee-4505-8575-224112024d7a
title: DOT11_SSID estructura (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_SSID
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: e319d22db33a627be631f9b6b0ee36591bc7a5bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910650"
---
# <a name="dot11_ssid-structure"></a>Estructura de SSID de DOT11 \_

Una estructura de **\_ SSID de DOT11** contiene el SSID de una interfaz.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DOT11_SSID {
  ULONG uSSIDLength;
  UCHAR ucSSID[DOT11_SSID_MAX_LENGTH];
} DOT11_SSID, *PDOT11_SSID;
```



## <a name="members"></a>Miembros

<dl> <dt>

**uSSIDLength**
</dt> <dd>

La longitud, en bytes, de la matriz **ucSSID** .

</dd> <dt>

**ucSSID**
</dt> <dd>

SSID. \_ \_ \_ Longitud máxima de SSID de DOT11 establecida en 32.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El SSID especificado por el miembro **ucSSID** no es una cadena ASCII terminada en NULL. La longitud del SSID viene determinada por el miembro **uSSIDLength** .

Un SSID de carácter comodín es un SSID cuyo miembro **uSSIDLength** se establece en cero. Cuando el SSID deseado se establece en el SSID del carácter comodín, la estación 802,11 puede conectarse a cualquier red del conjunto de servicios básico (BSS).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                        |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>Wlantypes. h (incluye Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_parámetros de conexión de WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[**WlanGetNetworkBssList**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> <dt>

[**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
</dt> </dl>

 

 




