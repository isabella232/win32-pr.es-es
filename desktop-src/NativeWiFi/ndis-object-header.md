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
ms.openlocfilehash: fe28a87eeb1457bace0b72a386bcb07667b24a64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069456"
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



## <a name="members"></a>Members

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

Especifica el tamaño total, en bytes, de la estructura NDIS que contiene **el encabezado de objeto \_ de \_ NDIS.** Este tamaño incluye el tamaño del miembro **\_ OBJECT HEADER \_ de NDIS** y todos los demás miembros de la estructura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio SP3 \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                       |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Ntddndis.h (incluya Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DOT11 \_ BSSID \_ LIST**](dot11-bssid-list.md)
</dt> </dl>

 

 




