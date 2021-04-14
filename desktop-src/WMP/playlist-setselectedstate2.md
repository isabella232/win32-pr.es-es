---
title: Lista de reproducción. setSelectedState2
description: El método setSelectedState2 establece el estado seleccionado del elemento con el índice especificado en el elemento de lista de reproducción.
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- Windows Media Player de lista de reproducción. setSelectedState2
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1a4e317543765fb24755516a0637b16958ad679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661413"
---
# <a name="playlistsetselectedstate2"></a>Lista de reproducción. setSelectedState2

El método **setSelectedState2** establece el estado seleccionado del elemento con el índice especificado en el elemento de **lista de reproducción** .

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*movs*
</dt> <dd>

**Número** (**largo**) que indica el índice de un elemento de la lista de reproducción.

</dd> <dt>

<span id="selected"></span><span id="SELECTED"></span>*seleccionadas*
</dt> <dd>

**Valor booleano** que indica si el elemento especificado se va a seleccionar (true) o si no se ha seleccionado (false).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método puede trabajar con listas de reproducción anidadas y reemplaza el método **setSelectedState** que no puede. Puede establecer todos los elementos en el estado solicitado especificando 1 en el parámetro *Item* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Lista de reproducción. setSelectedState**](playlist-setselectedstate.md)
</dt> </dl>

 

 





