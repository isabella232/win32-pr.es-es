---
title: PLAYLIST.setCheckedState2
description: El método setCheckedState2 establece el estado comprobado del elemento con el índice especificado en el elemento PLAYLIST.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- PLAYLIST.setCheckedState2 Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37cc9c821ae783e79d327e93b0c2f297fb75eab1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359482"
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

**Valor** booleano que indica si el elemento especificado se debe comprobar (true) o desactivar (false).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano**.

## <a name="remarks"></a>Observaciones

Este método puede trabajar con listas de reproducción anidadas y reemplaza el **método setCheckedState,** que no puede. Puede establecer todos los elementos en el estado solicitado especificando 1 en el *parámetro item.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.setCheckedState**](playlist-setcheckedstate.md)
</dt> </dl>

 

 





