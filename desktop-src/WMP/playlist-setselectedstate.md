---
title: Lista de reproducción. setSelectedState
description: El método setSelectedState especifica que el elemento indexado de la lista de reproducción está seleccionado.
ms.assetid: 61770053-733f-40b5-8b1f-92b6975d3ad3
keywords:
- Windows Media Player de lista de reproducción. setSelectedState
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a7bb545330710ae4fe2c39eae4556207061203
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709263"
---
# <a name="playlistsetselectedstate"></a>Lista de reproducción. setSelectedState

El método **setSelectedState** especifica que el elemento indexado de la lista de reproducción está seleccionado.

``` syntax
        elementID.setSelectedState(item)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*movs*
</dt> <dd>

**Número** (**largo**) que indica el índice de un elemento de la lista de reproducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Puede establecer todos los elementos en el estado seleccionado especificando 1 en el parámetro *Item* .

Este método se ha reemplazado por **setSelectedState2**, que admite listas de reproducción anidadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Lista de reproducción. setSelectedState2**](playlist-setselectedstate2.md)
</dt> </dl>

 

 





