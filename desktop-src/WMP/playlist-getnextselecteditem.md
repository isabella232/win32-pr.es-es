---
title: PLAYLIST.getNextSelectedItem
description: El método getNextSelectedItem recupera el índice del siguiente elemento seleccionado en la lista de reproducción después del índice especificado.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- Lista de reproducción.getNextSelectedItem Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 872dd31694384dfa35d7ce98c2f26756ede14539f4e788cbb6f699d17ca78a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467755"
---
# <a name="playlistgetnextselecteditem"></a>PLAYLIST.getNextSelectedItem

El **método getNextSelectedItem** recupera el índice del siguiente elemento seleccionado en la lista de reproducción después del índice especificado.

``` syntax
        elementID.getNextSelectedItem(item)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Artículo*
</dt> <dd>

**Number** (**long**) que indica el índice del elemento del que se buscará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor Number** (**long**).

## <a name="remarks"></a>Observaciones

Cuando no hay más elementos seleccionados, este método devuelve 1.

Este método se ha reemplazado por **getNextSelectedItem2,** que admite listas de reproducción anidadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextSelectedItem2**](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





