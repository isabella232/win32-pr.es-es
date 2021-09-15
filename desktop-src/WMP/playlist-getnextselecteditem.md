---
title: PLAYLIST.getNextSelectedItem
description: El método getNextSelectedItem recupera el índice del siguiente elemento seleccionado en la lista de reproducción después del índice especificado.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- PLAYLIST.getNextSelectedItem Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c5e37ad5109066a11cf28a593ed69f8c86b8b639
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466176"
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

**Number** (**long**) que indica el índice del elemento después del que se buscará.

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

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextSelectedItem2**](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





