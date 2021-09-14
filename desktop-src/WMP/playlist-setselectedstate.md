---
title: PLAYLIST.setSelectedState
description: El método setSelectedState especifica que el elemento indexado de la lista de reproducción está seleccionado.
ms.assetid: 61770053-733f-40b5-8b1f-92b6975d3ad3
keywords:
- PLAYLIST.setSelectedState Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359476"
---
# <a name="playlistsetselectedstate"></a>PLAYLIST.setSelectedState

El **método setSelectedState** especifica que el elemento indexado de la lista de reproducción está seleccionado.

``` syntax
        elementID.setSelectedState(item)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Artículo*
</dt> <dd>

**Number** (**long**) que indica el índice de un elemento en la lista de reproducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Puede establecer todos los elementos en el estado seleccionado especificando 1 en el parámetro *item.*

Este método se ha reemplazado por **setSelectedState2**, que admite listas de reproducción anidadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.setSelectedState2**](playlist-setselectedstate2.md)
</dt> </dl>

 

 





