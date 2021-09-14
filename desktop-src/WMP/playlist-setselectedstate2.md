---
title: PLAYLIST.setSelectedState2
description: El método setSelectedState2 establece el estado seleccionado del elemento con el índice especificado en el elemento PLAYLIST.
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- PLAYLIST.setSelectedState2 Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243140"
---
# <a name="playlistsetselectedstate2"></a>PLAYLIST.setSelectedState2

El **método setSelectedState2** establece el estado seleccionado del elemento con el índice especificado en el elemento **PLAYLIST.**

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Artículo*
</dt> <dd>

**Number** (**long**) que indica el índice de un elemento en la lista de reproducción.

</dd> <dt>

<span id="selected"></span><span id="SELECTED"></span>*Seleccionado*
</dt> <dd>

**Valor** booleano que indica si el elemento especificado se va a seleccionar (true) o no seleccionar (false).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método puede funcionar con listas de reproducción anidadas y reemplaza el **método setSelectedState** que no puede. Puede establecer todos los elementos en el estado solicitado especificando 1 en el parámetro *item.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.setSelectedState**](playlist-setselectedstate.md)
</dt> </dl>

 

 





