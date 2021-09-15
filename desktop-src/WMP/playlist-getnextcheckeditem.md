---
title: PLAYLIST.getNextCheckedItem
description: El método getNextCheckedItem recupera el índice del siguiente elemento activado en la lista de reproducción después del índice especificado.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- LISTA DE REPRODUCCIÓN.getNextCheckedItem Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b4a85fdccc5de227ab8aea3d0ee4f93d46eed50
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359505"
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

**Number** (**long**) que indica el índice del elemento después del que se buscará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor Number** (**long**).

## <a name="remarks"></a>Observaciones

Cuando no hay más elementos comprobados, este método devuelve 1.

Este método se ha reemplazado por **getNextCheckedItem2,** que admite listas de reproducción anidadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextCheckedItem2**](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





