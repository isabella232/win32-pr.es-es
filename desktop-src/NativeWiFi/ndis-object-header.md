---
description: Empaqueta la información de tipo de objeto, versión y tamaño necesaria en muchas estructuras de NDIS 6.0.
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: NDIS_OBJECT_HEADER estructura (Ntddndis.h)
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
ms.openlocfilehash: f9f4a4ef2a833081cde0c3c7ca4d395e59743944291a95d7680c241191988b35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065055"
---
# <a name="ndis_object_header-structure"></a>Estructura NDIS \_ OBJECT \_ HEADER

La **estructura \_ OBJECT HEADER \_ de NDIS** empaqueta la información de tipo de objeto, versión y tamaño necesaria en muchas estructuras de NDIS 6.0.

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

Especifica el tamaño total, en bytes, de la estructura NDIS que contiene **el NDIS \_ OBJECT \_ HEADER**. Este tamaño incluye el tamaño del miembro **\_ OBJECT HEADER \_ de NDIS** y de todos los demás miembros de la estructura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp3 \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                       |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                                        |
| Header<br/>                   | <dl> <dt>Ntddndis.h (incluye Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DOT11 \_ BSSID \_ LIST**](dot11-bssid-list.md)
</dt> </dl>

 

 




