---
title: PLAYLIST.dropDownImage
description: El atributo dropDownImage especifica o recupera el nombre de la imagen usada para el botón de lista desplegable que se muestra en el borde derecho de la lista desplegable.
ms.assetid: 92454a8a-1688-4b5d-887d-6847f4232d87
keywords:
- PLAYLIST.dropDownImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.dropDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3173462cc7b055639a685917b87f1560adf5eabc8d0d7678788fa6a6c72129d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054213"
---
# <a name="playlistdropdownimage"></a>PLAYLIST.dropDownImage

El **atributo dropDownImage** especifica o recupera el nombre de la imagen usada para el botón de lista desplegable que se muestra en el borde derecho de la lista desplegable.

``` syntax
        elementID.dropDownImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene el nombre de un archivo de imagen. No tiene valor predeterminado.

## <a name="remarks"></a>Comentarios

Este atributo admite archivos PNG, JPG, BMP y GIF. Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente mediante los **atributos hueShift** y **saturación.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.dropDownBackgroundImage**](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[**PLAYLIST.hueShift**](playlist-hueshift.md)
</dt> <dt>

[**PLAYLIST.saturation**](playlist-saturation.md)
</dt> </dl>

 

 





