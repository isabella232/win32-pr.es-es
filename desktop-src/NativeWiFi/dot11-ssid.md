---
description: Contiene el SSID de una interfaz.
ms.assetid: f2b15ef9-99ee-4505-8575-224112024d7a
title: DOT11_SSID estructura (Wlantypes.h)
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
ms.openlocfilehash: d39def878077aca20e17b35f88ba210de032ea272940ba59e785ef0766a38f58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984995"
---
# <a name="dot11_ssid-structure"></a>Estructura \_ SSID de DOT11

Una **estructura \_ SSID DE DOT11** contiene el SSID de una interfaz.

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

Longitud, en bytes, de la **matriz ucSSID.**

</dd> <dt>

**ucSSID**
</dt> <dd>

The SSID. DOT11 \_ SSID \_ MAX LENGTH se establece \_ en 32.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El SSID especificado por el miembro **ucSSID** no es una cadena ASCII terminada en NULL. El miembro **uSSIDLength** determina la longitud del SSID.

Un SSID comodín es un SSID cuyo **miembro uSSIDLength** está establecido en cero. Cuando el SSID deseado se establece en el SSID comodín, la estación 802.11 puede conectarse a cualquier red de conjunto de servicios básico (BSS).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio SP3 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                        |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                                         |
| Header<br/>                   | <dl> <dt>Wlantypes.h (incluya Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PARÁMETROS DE \_ CONEXIÓN WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[**WlanGetNetworkBssList**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> <dt>

[**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
</dt> </dl>

 

 




