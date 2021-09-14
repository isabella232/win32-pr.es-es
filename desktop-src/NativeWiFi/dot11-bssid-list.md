---
description: Contiene una lista de identificadores de conjunto de servicios básicos (BSS).
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: DOT11_BSSID_LIST estructura (Windot11.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSSID_LIST
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 345053a8d39ea37bea2fa2350dcc426420aed422
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071615"
---
# <a name="dot11_bssid_list-structure"></a>Dot11 \_ BSSID \_ LIST (estructura)

La **estructura DOT11 \_ BSSID \_ LIST** contiene una lista de identificadores de conjunto de servicios básicos (BSS).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DOT11_BSSID_LIST {
  NDIS_OBJECT_HEADER Header;
  ULONG              uNumOfEntries;
  ULONG              uTotalNumOfEntries;
  DOT11_MAC_ADDRESS  BSSIDs[1];
} DOT11_BSSID_LIST, *PDOT11_BSSID_LIST;
```



## <a name="members"></a>Members

<dl> <dt>

**Header**
</dt> <dd>

Estructura [**OBJECT \_ HEADER \_ de NDIS**](ndis-object-header.md) que contiene la información de tipo, versión y tamaño de una estructura NDIS. Para la mayoría de las estructuras  **DOT11 \_ BSSID \_ LIST,** establezca  el miembro Type en **NDIS \_ OBJECT \_ TYPE \_ DEFAULT,** establezca el miembro Revision en **DOT11 \_ BSSID LIST REVISION \_ \_ \_ 1** y establezca el miembro **Size** en **sizeof(DOT11 \_ BSSID \_ LIST).**

</dd> <dt>

**uNumOfEntries**
</dt> <dd>

Número de entradas de esta estructura.

</dd> <dt>

**uTotalNumOfEntries**
</dt> <dd>

Número total de entradas admitidas.

</dd> <dt>

**SSID**
</dt> <dd>

Lista de identificadores de BSS. Un identificador BSS se almacena como un tipo [**DE \_ DIRECCIÓN MAC \_ DOT11.**](dot11-mac-address-type.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio SP3 \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                       |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Windot11.h (incluir Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PARÁMETROS DE \_ CONEXIÓN WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




