---
description: La estructura KSMULTIPLE ITEM describe el tamaño y el recuento de las propiedades de longitud variable en los \_ pines en modo kernel.
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
ms.openlocfilehash: 2e1cdf3d8edcea88fbcfb260d87d3e79d62eb2aebc57144ae38defb018065f1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823315"
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



## <a name="members"></a>Miembros

<dl> <dt>

**Tamaño**
</dt> <dd>

Tamaño del bloque de memoria devuelto, en bytes. El tamaño incluye la **estructura ITEM de KSMULTIPLE \_** y los elementos que la siguen.

</dd> <dt>

**Recuento**
</dt> <dd>

Especifica el número total de elementos que siguen a esta estructura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Ks.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[DirectShow Estructuras](directshow-structures.md)
</dt> <dt>

[**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md)
</dt> <dt>

[**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




