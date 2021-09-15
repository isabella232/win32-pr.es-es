---
title: PLAYLIST.getNextCheckedItem2
description: El método getNextCheckedItem2 recupera el índice del siguiente elemento activado en la lista de reproducción después del índice especificado.
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- PLAYLIST.getNextCheckedItem2 Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50bb2fd6ed6e3328df29a59381571204ebd28369
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359503"
---
# <a name="playlistgetnextcheckeditem2"></a>PLAYLIST.getNextCheckedItem2

El **método getNextCheckedItem2** recupera el índice del siguiente elemento activado en la lista de reproducción después del índice especificado.

``` syntax
        elementID.getNextCheckedItem2(item)
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

Este método puede funcionar con listas de reproducción anidadas y reemplaza el **método getNextCheckedItem,** que no puede. Pase 1 en el *parámetro item* para buscar el primer elemento activado. Cuando no hay más elementos comprobados, este método devuelve 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextCheckedItem**](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





