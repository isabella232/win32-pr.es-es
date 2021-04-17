---
description: La \_ estructura de elementos KSMULTIPLE describe el tamaño y el recuento de las propiedades de longitud variable en los pin de modo kernel.
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: KSMULTIPLE_ITEM estructura (KS. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680614"
---
# <a name="ksmultiple_item-structure"></a>\_Estructura del elemento KSMULTIPLE

La `KSMULTIPLE_ITEM` estructura describe el tamaño y el recuento de las propiedades de longitud variable en los pin de modo kernel.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  ULONG Size;
  ULONG Count;
} KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tamaño**
</dt> <dd>

Tamaño del bloque de memoria devuelto, en bytes. El tamaño incluye la estructura del **\_ elemento KSMULTIPLE** y los elementos que lo siguen.

</dd> <dt>

**Recuento**
</dt> <dd>

Especifica el número total de elementos que siguen a esta estructura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>KS. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de DirectShow](directshow-structures.md)
</dt> <dt>

[**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md)
</dt> <dt>

[**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




