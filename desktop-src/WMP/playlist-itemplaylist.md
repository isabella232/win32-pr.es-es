---
title: PLAYLIST.itemPlaylist
description: El atributo itemPlaylist recupera la lista de reproducción del elemento multimedia que se muestra en el índice especificado en el elemento PLAYLIST.
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- LISTA DE REPRODUCCIÓN.elementoPlaylist Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f2ed3173042d68ec048486189d909be60427df92e9936d4446f8d7a99ef592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571187"
---
# <a name="playlistitemplaylist"></a>PLAYLIST.itemPlaylist

El **atributo itemPlaylist** recupera la lista de reproducción del elemento multimedia que se muestra en el índice especificado en el elemento **PLAYLIST.**

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un objeto De lista de **reproducción de solo** lectura.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Índice*
</dt> <dd>

**Number**(**long**) que contiene el índice de un elemento de lista de reproducción.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **propiedad itemPlaylist** devolverá el objeto de lista de reproducción que se expande en el elemento **PLAYLIST.** Por ejemplo, si hay dos listas de reproducción anidadas que no se expanden en el elemento **PLAYLIST** y que contienen tres clips multimedia cada una, **itemPlaylist**(1) devolverá la lista de reproducción primaria que contiene las dos listas de reproducción anidadas. Si se expande la segunda lista de reproducción, **itemPlaylist**(1) devolverá la segunda lista de reproducción. Si ambas listas de reproducción se expanden, **itemPlaylist**(1) devolverá la primera lista de reproducción.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> </dl>

 

 





