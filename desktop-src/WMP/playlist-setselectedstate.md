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
ms.openlocfilehash: 1ba35f2030f4b2fb6e9acfde1a8310e6c9f1dac98b8ba8aa65d56cce206c8e00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862245"
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

## <a name="remarks"></a>Comentarios

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

 

 





