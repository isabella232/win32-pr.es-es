---
title: PLAYLIST. itemCount
description: El atributo itemCount recupera el número de elementos que se muestran actualmente en el elemento de lista de reproducción.
ms.assetid: d090d95c-e3c3-41bc-951e-ffeb0a314a0c
keywords:
- Lista de reproducción. itemCount de Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbde81ee6c2849a19c6400fee4ef7fa6514eaefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661227"
---
# <a name="playlistitemcount"></a>PLAYLIST. itemCount

El atributo **itemCount** recupera el número de elementos que se muestran actualmente en el elemento de **lista de reproducción** .

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de solo lectura (**Long**).

## <a name="remarks"></a>Observaciones

La propiedad **itemCount** contará el número total de elementos expandidos. Por ejemplo, si hay dos listas de reproducción que contienen tres elementos multimedia cada uno, **itemCount** devolverá 2 si las listas de reproducción no se expanden. Si solo se expande la primera lista de reproducción, **itemCount** devolverá 4. Si se expanden ambas listas de reproducción, **itemCount** devolverá 6.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





