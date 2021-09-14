---
description: La estructura KSMULTIPLE ITEM describe el tamaño y el recuento de propiedades de longitud variable en los \_ pines en modo kernel.
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: KSMULTIPLE_ITEM estructura (Ks.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSMULTIPLE_ITEM
api_type:
- HeaderDef
api_location:
- ks.h
ms.openlocfilehash: 62e26b1aa8804514588e66c1d02e1f0643e97bcb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061043"
---
# <a name="ksmultiple_item-structure"></a>KSMULTIPLE \_ ITEM (estructura)

La `KSMULTIPLE_ITEM` estructura describe el tamaño y el recuento de propiedades de longitud variable en los pines en modo kernel.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  ULONG Size;
  ULONG Count;
} KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM;
```



## <a name="members"></a>Members

<dl> <dt>

**Tamaño**
</dt> <dd>

Tamaño del bloque de memoria devuelto, en bytes. El tamaño incluye la **estructura KSMULTIPLE \_ ITEM** y los elementos que la siguen.

</dd> <dt>

**Recuento**
</dt> <dd>

Especifica el número total de elementos que siguen esta estructura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Ks.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DirectShow Estructuras](directshow-structures.md)
</dt> <dt>

[**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md)
</dt> <dt>

[**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




