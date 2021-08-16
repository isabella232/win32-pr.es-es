---
title: PLAYLIST.setCheckedState2
description: El método setCheckedState2 establece el estado comprobado del elemento con el índice especificado en el elemento PLAYLIST.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- LISTA DE REPRODUCCIÓN.setCheckedState2 Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6b95cb332c5f5a9d86e6f49484b27c1ab5802f28b18195f610395a1c732e369
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336224"
---
# <a name="playlistsetcheckedstate2"></a>PLAYLIST.setCheckedState2

El **método setCheckedState2** establece el estado comprobado del elemento con el índice especificado en el elemento **PLAYLIST.**

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Artículo*
</dt> <dd>

**Number** ( long )**que** indica el índice del elemento de lista de reproducción que se va a comprobar o desactivar.

</dd> <dt>

<span id="checked"></span><span id="CHECKED"></span>*Comprobado*
</dt> <dd>

**Valor** booleano que indica si el elemento especificado se va a comprobar (true) o no (false).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano**.

## <a name="remarks"></a>Comentarios

Este método puede trabajar con listas de reproducción anidadas y reemplaza el **método setCheckedState,** que no puede. Puede establecer todos los elementos en el estado solicitado especificando 1 en el *parámetro item.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.setCheckedState**](playlist-setcheckedstate.md)
</dt> </dl>

 

 





