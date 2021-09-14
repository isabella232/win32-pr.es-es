---
title: PLAYLIST.itemCount
description: El atributo itemCount recupera el número de elementos que se muestran actualmente en el elemento PLAYLIST.
ms.assetid: d090d95c-e3c3-41bc-951e-ffeb0a314a0c
keywords:
- LISTA DE REPRODUCCIÓN.itemCount Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.itemCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbde81ee6c2849a19c6400fee4ef7fa6514eaefe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243171"
---
# <a name="playlistitemcount"></a>PLAYLIST.itemCount

El **atributo itemCount** recupera el número de elementos que se muestran actualmente en el elemento **PLAYLIST.**

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Observaciones

La **propiedad itemCount** cuenta el número total de elementos expandido. Por ejemplo, si hay dos listas de reproducción que contienen tres elementos multimedia cada una, **itemCount** devolverá 2 si las listas de reproducción no se expanden. Si solo se expande la primera lista de reproducción, **itemCount** devolverá 4. Si ambas listas de reproducción se expanden, **itemCount** devolverá 6.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





