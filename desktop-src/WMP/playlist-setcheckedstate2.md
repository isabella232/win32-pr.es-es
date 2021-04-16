---
title: Lista de reproducción. setCheckedState2
description: El método setCheckedState2 establece el estado de activación del elemento con el índice especificado en el elemento de lista de reproducción.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- Windows Media Player de lista de reproducción. setCheckedState2
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708213"
---
# <a name="playlistsetcheckedstate2"></a>Lista de reproducción. setCheckedState2

El método **setCheckedState2** establece el estado de activación del elemento con el índice especificado en el elemento de **lista de reproducción** .

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*movs*
</dt> <dd>

**Número** (**largo**) que indica el índice del elemento de lista de reproducción que se va a activar o desactivar.

</dd> <dt>

<span id="checked"></span><span id="CHECKED"></span>*incorpora*
</dt> <dd>

**Valor booleano** que indica si el elemento especificado debe comprobarse (true) o desactivado (false).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano**.

## <a name="remarks"></a>Observaciones

Este método puede trabajar con listas de reproducción anidadas y reemplaza al método **setCheckedState** , que no puede. Puede establecer todos los elementos en el estado solicitado especificando 1 en el parámetro *Item* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Lista de reproducción. setCheckedState**](playlist-setcheckedstate.md)
</dt> </dl>

 

 





