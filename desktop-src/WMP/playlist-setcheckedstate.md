---
title: PLAYLIST.setCheckedState
description: El método setCheckedState especifica que el elemento indexado de la lista de reproducción está activado.
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- PLAYLIST.setCheckedState Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a8c86459dcf590b1ff1e884a8aa671dc1bba78a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359483"
---
# <a name="playlistsetcheckedstate"></a>PLAYLIST.setCheckedState

El **método setCheckedState** especifica que el elemento indexado de la lista de reproducción está activado.

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Artículo*
</dt> <dd>

**Number** ( long )**que** indica el índice del elemento de lista de reproducción que se va a comprobar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano**.

## <a name="remarks"></a>Observaciones

Puede establecer todos los elementos en el estado activado especificando 1 en el parámetro *item.*

Este método se ha reemplazado por **setCheckedState2,** que admite listas de reproducción anidadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.setCheckedState2**](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





