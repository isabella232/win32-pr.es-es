---
title: PLAYLIST.hueShift
description: El atributo hueShift especifica o recupera la cantidad por la que se desplaza el matiz de las imágenes desplegables.
ms.assetid: 9d4d8b73-527e-43f3-a921-0576b8897918
keywords:
- LISTA DE REPRODUCCIÓN.hueShift Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.hueShift
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e9dbe89989ddd8f02d67ac8f14532b9b1fbf15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466172"
---
# <a name="playlisthueshift"></a>PLAYLIST.hueShift

El **atributo hueShift** especifica o recupera la cantidad por la que se desplaza el matiz de las imágenes desplegables.

``` syntax
        elementID.hueShift
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** (**float**) con un valor que va de 0,0 a 360,0 con un valor predeterminado de 0,0.

## <a name="remarks"></a>Observaciones

Este atributo cambia el valor de matiz de las imágenes especificadas por los atributos **dropDownBackgroundImage** y **dropDownImage** si se han especificado y hacen referencia a imágenes BMP de 8 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.dropDownBackgroundImage**](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[**PLAYLIST.dropDownImage**](playlist-dropdownimage.md)
</dt> <dt>

[**PLAYLIST.saturation**](playlist-saturation.md)
</dt> </dl>

 

 





