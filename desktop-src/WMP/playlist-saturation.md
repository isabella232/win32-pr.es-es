---
title: PLAYLIST.saturation
description: El atributo de saturación especifica o recupera el valor de saturación de las imágenes desplegables.
ms.assetid: 4c5dd3d9-828a-45c9-896a-9a702d354544
keywords:
- LISTA DE REPRODUCCIÓN.saturación Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f5ce3c576fd923dae5c7a6cb4b7227b67dbebd87c6a497fc6c48e6e453b53f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336541"
---
# <a name="playlistsaturation"></a>PLAYLIST.saturation

El **atributo de** saturación especifica o recupera el valor de saturación de las imágenes desplegables.

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** (**float**) con un valor que va de 0,0 a 2,0 con un valor predeterminado de 1,0.

## <a name="remarks"></a>Comentarios

Este atributo cambia el valor de saturación de las imágenes especificadas por los atributos **dropDownBackgroundImage** y **dropDownImage** si se han especificado y hacen referencia a imágenes BMP de 8 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.dropDownBackgroundImage**](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[**PLAYLIST.dropDownImage**](playlist-dropdownimage.md)
</dt> <dt>

[**PLAYLIST.hueShift**](playlist-hueshift.md)
</dt> </dl>

 

 





