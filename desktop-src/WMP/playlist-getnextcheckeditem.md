---
title: PLAYLIST.getNextCheckedItem
description: El método getNextCheckedItem recupera el índice del siguiente elemento activado en la lista de reproducción después del índice especificado.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- PLAYLIST.getNextCheckedItem Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54b6e598737d1aac09754b15c037c27a435deb5fff34c729aa48c51019e12982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571455"
---
# <a name="playlistgetnextcheckeditem"></a>PLAYLIST.getNextCheckedItem

El **método getNextCheckedItem** recupera el índice del siguiente elemento activado en la lista de reproducción después del índice especificado.

``` syntax
        elementID.getNextCheckedItem(item)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Artículo*
</dt> <dd>

**Number** (**long**) que indica el índice del elemento del que se buscará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor Number** (**long**).

## <a name="remarks"></a>Comentarios

Cuando no hay más elementos comprobados, este método devuelve 1.

Este método se ha reemplazado por **getNextCheckedItem2,** que admite listas de reproducción anidadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextCheckedItem2**](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





