---
title: PLAYLIST.itemPlaylist
description: El atributo itemPlaylist recupera la lista de reproducción del elemento multimedia que se muestra en el índice especificado en el elemento PLAYLIST.
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- LISTA DE REPRODUCCIÓN.elementoLista de reproducción Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d414692050e16dfd0aebe05901bcee0bc26580
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466164"
---
# <a name="playlistitemplaylist"></a>PLAYLIST.itemPlaylist

El **atributo itemPlaylist** recupera la lista de reproducción del elemento multimedia que se muestra en el índice especificado en el elemento **PLAYLIST.**

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un objeto De lista de reproducción **de** solo lectura.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Índice*
</dt> <dd>

**Number**(**long**) que contiene el índice de un elemento de lista de reproducción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **propiedad itemPlaylist** devolverá el objeto de lista de reproducción que se expande en el elemento **PLAYLIST.** Por ejemplo, si hay dos listas de reproducción anidadas que no se expanden en el elemento **PLAYLIST** y que contienen tres clips multimedia cada una, **itemPlaylist**(1) devolverá la lista de reproducción primaria que contiene las dos listas de reproducción anidadas. Si se expande la segunda lista de reproducción, **itemPlaylist**(1) devolverá la segunda lista de reproducción. Si ambas listas de reproducción se expanden, **itemPlaylist**(1) devolverá la primera lista de reproducción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> </dl>

 

 





