---
title: Lista de reproducción. itemPlaylist
description: El atributo itemPlaylist recupera la lista de reproducción del elemento multimedia que se muestra en el índice especificado del elemento de lista de reproducción.
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- Windows Media Player de lista de reproducción. itemPlaylist
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d414692050e16dfd0aebe05901bcee0bc26580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709210"
---
# <a name="playlistitemplaylist"></a>Lista de reproducción. itemPlaylist

El atributo **itemPlaylist** recupera la lista de reproducción del elemento multimedia que se muestra en el índice especificado del elemento de **lista de reproducción** .

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un objeto de **lista de reproducción** de solo lectura.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*ajustar*
</dt> <dd>

**Número**(**largo**) que contiene el índice de un elemento de lista de reproducción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La propiedad **itemPlaylist** devolverá el objeto de lista de reproducción que se expande en el elemento de **lista de reproducción** . Por ejemplo, si hay dos listas de reproducción anidadas que no se expanden en el elemento de **lista de reproducción** y que contienen tres clips multimedia cada una, **itemPlaylist**(1) devolverá la lista de reproducción primaria que contiene las dos listas de reproducción anidadas. Si se expande la segunda lista de reproducción, **itemPlaylist**(1) devolverá la segunda lista de reproducción. Si se expanden ambas listas de reproducción, **itemPlaylist**(1) devolverá la primera lista de reproducción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> </dl>

 

 





