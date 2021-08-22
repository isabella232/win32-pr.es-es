---
title: PLAYLIST.backgroundImage
description: El atributo backgroundImage especifica o recupera la imagen de fondo.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- PLAYLIST.backgroundImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ddcb42f118a5a672b6678079825b6cb3d6aba5fbdc54953fb566e4222f583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054253"
---
# <a name="playlistbackgroundimage"></a>PLAYLIST.backgroundImage

El **atributo backgroundImage** especifica o recupera la imagen de fondo.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene el nombre de un archivo de imagen. No tiene valor predeterminado.

## <a name="remarks"></a>Comentarios

Si el alto y el ancho de la imagen son menores que el alto y ancho del elemento **PLAYLIST,** la imagen se muestra en mosaico. Los formatos admitidos son BMP, JPG, GIF y PNG.

La especificación de un valor de "degradado" para la imagen de fondo hace que el fondo de la lista de reproducción se muestre como un degradado de color. Esto significa que el color de fondo pasa gradualmente entre los valores [PLAYLIST.backgroundColor](playlist-backgroundcolor.md) (en la parte superior del fondo) y [PLAYLIST.statusColor.](playlist-statuscolor.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior, Reproductor de Windows Media 10 para la característica de degradado<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





