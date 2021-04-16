---
title: Lista de reproducción. setCheckedState
description: El método setCheckedState especifica que se comprueba el elemento indexado de la lista de reproducción.
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- Windows Media Player de lista de reproducción. setCheckedState
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708208"
---
# <a name="playlistsetcheckedstate"></a>Lista de reproducción. setCheckedState

El método **setCheckedState** especifica que se comprueba el elemento indexado de la lista de reproducción.

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*movs*
</dt> <dd>

**Número** (**largo**) que indica el índice del elemento de lista de reproducción que se va a comprobar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano**.

## <a name="remarks"></a>Observaciones

Puede establecer todos los elementos en el estado activado si especifica 1 en el parámetro *Item* .

Este método se ha reemplazado por **setCheckedState2**, que admite listas de reproducción anidadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Lista de reproducción. setCheckedState2**](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





