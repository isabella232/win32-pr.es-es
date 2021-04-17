---
description: Contiene una lista de identificadores básicos del conjunto de servicios (BSS).
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: DOT11_BSSID_LIST estructura (Windot11. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687762"
---
# <a name="dot11_bssid_list-structure"></a>\_Estructura de lista BSSID de DOT11 \_

La estructura de **\_ \_ lista BSSID de DOT11** contiene una lista de identificadores básicos del conjunto de servicios (BSS).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DOT11_BSSID_LIST {
  NDIS_OBJECT_HEADER Header;
  ULONG              uNumOfEntries;
  ULONG              uTotalNumOfEntries;
  DOT11_MAC_ADDRESS  BSSIDs[1];
} DOT11_BSSID_LIST, *PDOT11_BSSID_LIST;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Header**
</dt> <dd>

Una estructura de [**\_ \_ encabezado de objeto NDIS**](ndis-object-header.md) que contiene la información de tipo, versión y tamaño de una estructura NDIS. En el caso de la mayoría de las estructuras de **\_ \_ listas BSSID de DOT11** , establezca el miembro de **tipo** en el **tipo de \_ objeto NDIS \_ \_ predeterminado**, establezca el miembro de **revisión** en la **revisión de \_ lista BSSID de DOT11 \_ \_ \_ 1** y establezca el miembro de **tamaño** en **sizeof (lista de BSSID de dot11 \_ \_ )**.

</dd> <dt>

**uNumOfEntries**
</dt> <dd>

Número de entradas en esta estructura.

</dd> <dt>

**uTotalNumOfEntries**
</dt> <dd>

Número total de entradas admitidas.

</dd> <dt>

**BSSIDs**
</dt> <dd>

Una lista de identificadores de BSS. Un identificador de BSS se almacena como un tipo de [**\_ \_ dirección Mac de DOT11**](dot11-mac-address-type.md) .

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

[**\_parámetros de conexión de WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




