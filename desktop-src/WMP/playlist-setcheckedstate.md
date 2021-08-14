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
ms.openlocfilehash: 93e143f738197524e1555f18aedf84aa606626de645a98149c65507b71291cde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336252"
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

## <a name="remarks"></a>Comentarios

Puede establecer todos los elementos en el estado activado especificando 1 en el parámetro *item.*

Este método se ha reemplazado por **setCheckedState2,** que admite listas de reproducción anidadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.setCheckedState2**](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





