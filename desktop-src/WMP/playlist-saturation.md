---
title: Lista de reproducción. saturación
description: El atributo saturación especifica o recupera el valor de saturación de las imágenes desplegables.
ms.assetid: 4c5dd3d9-828a-45c9-896a-9a702d354544
keywords:
- Lista de reproducción. saturación de Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eb53afeafb0754f0e754f68fd5ff785eaade8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708674"
---
# <a name="playlistsaturation"></a>Lista de reproducción. saturación

El atributo **saturación** especifica o recupera el valor de saturación de las imágenes desplegables.

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura/escritura (**float**) con un valor comprendido entre 0,0 y 2,0 con un valor predeterminado de 1,0.

## <a name="remarks"></a>Observaciones

Este atributo cambia el valor de saturación de las imágenes especificadas por los atributos **dropDownBackgroundImage** y **dropDownImage** si se han especificado y hacen referencia a imágenes BMP de 8 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Lista de reproducción. dropDownBackgroundImage**](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[**Lista de reproducción. dropDownImage**](playlist-dropdownimage.md)
</dt> <dt>

[**Lista de reproducción. hueShift**](playlist-hueshift.md)
</dt> </dl>

 

 





