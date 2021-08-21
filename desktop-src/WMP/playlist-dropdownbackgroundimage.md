---
title: PLAYLIST.dropDownBackgroundImage
description: El atributo dropDownBackgroundImage especifica o recupera el nombre de la imagen que se muestra en el fondo de la lista desplegable.
ms.assetid: 40253d82-7178-4f6c-805b-7c1e92ea0636
keywords:
- PLAYLIST.dropDownBackgroundImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.dropDownBackgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47f964e1aaa4b2d22a922d70ea41970b5c1ae667920dbebf49dd5e6cc1d4dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571465"
---
# <a name="playlistdropdownbackgroundimage"></a>PLAYLIST.dropDownBackgroundImage

El **atributo dropDownBackgroundImage** especifica o recupera el nombre de la imagen que se muestra en el fondo de la lista desplegable.

``` syntax
        elementID.dropDownBackgroundImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene el nombre de un archivo de imagen. No tiene valor predeterminado.

## <a name="remarks"></a>Comentarios

Este atributo admite archivos PNG, JPG, BMP y GIF. Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente mediante los **atributos hueShift** y **saturación.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.dropDownImage**](playlist-dropdownimage.md)
</dt> <dt>

[**PLAYLIST.hueShift**](playlist-hueshift.md)
</dt> <dt>

[**PLAYLIST.saturation**](playlist-saturation.md)
</dt> </dl>

 

 





