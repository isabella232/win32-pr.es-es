---
title: PLAYLIST.getNextSelectedItem2
description: El método getNextSelectedItem2 recupera el índice del siguiente elemento seleccionado en la lista de reproducción después del índice especificado.
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- PLAYLIST.getNextSelectedItem2 Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27d166887bb2fa98e184e1f64f4aaceb89930d00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466173"
---
# <a name="playlistgetnextselecteditem2"></a>PLAYLIST.getNextSelectedItem2

El **método getNextSelectedItem2** recupera el índice del siguiente elemento seleccionado en la lista de reproducción después del índice especificado.

``` syntax
        elementID.getNextSelectedItem2(item)
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

Este método puede trabajar con listas de reproducción anidadas y reemplaza el **método getNextSelectedItem,** que no puede. Pase 1 en el *parámetro item* para buscar el primer elemento seleccionado. Cuando no hay más elementos seleccionados, se devuelve -1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextSelectedItem**](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





