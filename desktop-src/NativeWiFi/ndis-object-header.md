---
description: Empaqueta la información sobre el tipo de objeto, la versión y el tamaño necesaria en muchas estructuras NDIS 6,0.
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: NDIS_OBJECT_HEADER estructura (Ntddndis. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDIS_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- ntddndis.h
ms.openlocfilehash: fe28a87eeb1457bace0b72a386bcb07667b24a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687434"
---
# <a name="ndis_object_header-structure"></a>Estructura de encabezado de \_ objeto NDIS \_

La estructura de **\_ \_ encabezado de objeto NDIS** empaqueta la información sobre el tipo de objeto, la versión y el tamaño necesaria en muchas estructuras NDIS 6,0.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _NDIS_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Size;
} NDIS_OBJECT_HEADER, *PNDIS_OBJECT_HEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tipo**
</dt> <dd>

Especifica el tipo de objeto NDIS que describe una estructura.

</dd> <dt>

**Revisión**
</dt> <dd>

Especifica el número de revisión de esta estructura.

</dd> <dt>

**Tamaño**
</dt> <dd>

Especifica el tamaño total, en bytes, de la estructura NDIS que contiene el **\_ \_ encabezado de objeto NDIS**. Este tamaño incluye el tamaño del miembro **de \_ \_ encabezado de objeto NDIS** y de todos los demás miembros de la estructura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                       |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Ntddndis. h (incluye Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Lista de BSSID de DOT11 \_**](dot11-bssid-list.md)
</dt> </dl>

 

 




