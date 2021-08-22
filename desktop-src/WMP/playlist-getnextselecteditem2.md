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
ms.openlocfilehash: e6d1f98a418da1d8b21345598999f847cbf2142e9ca575bcfdc7047e2f9fd524
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415285"
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

**Number** (**long**) que indica el índice del elemento del que se buscará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor Number** (**long**).

## <a name="remarks"></a>Comentarios

Este método puede funcionar con listas de reproducción anidadas y reemplaza el **método getNextSelectedItem,** que no puede. Pase 1 en el *parámetro item* para buscar el primer elemento seleccionado. Cuando no hay más elementos seleccionados, se devuelve -1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextSelectedItem**](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





