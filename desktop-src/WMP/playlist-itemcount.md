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
ms.openlocfilehash: 9b2c831535a0d7ed5643558ddb5305419bab0f0a85b6359f1234f68e78a659ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003005"
---
# <a name="playlistitemcount"></a>PLAYLIST.itemCount

El **atributo itemCount** recupera el número de elementos que se muestran actualmente en el elemento **PLAYLIST.**

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Comentarios

La **propiedad itemCount** contará el número total de elementos expandido. Por ejemplo, si hay dos listas de reproducción que contienen tres elementos multimedia cada una, **itemCount** devolverá 2 si las listas de reproducción no se expanden. Si solo se expande la primera lista de reproducción, **itemCount** devolverá 4. Si ambas listas de reproducción se expanden, **itemCount** devolverá 6.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





