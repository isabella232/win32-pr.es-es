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
ms.openlocfilehash: 7eca04f47f6e157d5ede529c47fb6ae65b4333cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359527"
---
# <a name="playlistbackgroundimage"></a>PLAYLIST.backgroundImage

El **atributo backgroundImage** especifica o recupera la imagen de fondo.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene el nombre de un archivo de imagen. No tiene valor predeterminado.

## <a name="remarks"></a>Observaciones

Si el alto y el ancho de la imagen son menores que el alto y ancho del elemento **PLAYLIST,** la imagen se muestra en mosaico. Los formatos admitidos son BMP, JPG, GIF y PNG.

La especificación de un valor de "degradado" para la imagen de fondo hace que el fondo de la lista de reproducción se muestre como un degradado de color. Esto significa que el color de fondo pasa gradualmente entre los valores [PLAYLIST.backgroundColor](playlist-backgroundcolor.md) (en la parte superior del fondo) y [PLAYLIST.statusColor.](playlist-statuscolor.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior, Reproductor de Windows Media 10 para la característica de degradado<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





