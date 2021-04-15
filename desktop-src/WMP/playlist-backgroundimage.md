---
title: Lista de reproducción. backgroundImage
description: El atributo backgroundImage especifica o recupera la imagen de fondo.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- Lista de reproducción. backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eca04f47f6e157d5ede529c47fb6ae65b4333cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708979"
---
# <a name="playlistbackgroundimage"></a>Lista de reproducción. backgroundImage

El atributo **BackgroundImage** especifica o recupera la imagen de fondo.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen. No tiene valor predeterminado.

## <a name="remarks"></a>Observaciones

Si el alto y el ancho de la imagen son más pequeños que el alto y el ancho del elemento de **lista de reproducción** , la imagen se coloca en mosaico. Los formatos admitidos son BMP, JPG, GIF y PNG.

Si se especifica un valor de "degradado" para la imagen de fondo, el fondo de la lista de reproducción se mostrará como degradado de color. Esto significa que el color de fondo pasa gradualmente entre la [lista de reproducción. BackgroundColor](playlist-backgroundcolor.md) (en la parte superior de los fondos) y los valores de [lista de reproducción. statusColor](playlist-statuscolor.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior, Windows Media Player 10 para la característica de degradado<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





