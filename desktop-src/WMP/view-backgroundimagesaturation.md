---
title: VER. backgroundImageSaturation
description: El atributo backgroundImageSaturation especifica o recupera el valor de saturación de la imagen de fondo.
ms.assetid: 9e1f205b-6366-4816-9430-1153f57d686c
keywords:
- VIEW. backgroundImageSaturation Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.backgroundImageSaturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c9d7f5807bcb5fd90dae211d80faf78006b6b35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649901"
---
# <a name="viewbackgroundimagesaturation"></a>VER. backgroundImageSaturation

El atributo **backgroundImageSaturation** especifica o recupera el valor de saturación de la imagen de fondo.

``` syntax
        elementID.backgroundImageSaturation
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura/escritura (**float**) con un valor comprendido entre 0,0 y 2,0 con un valor predeterminado de 1,0.

## <a name="remarks"></a>Observaciones

Este atributo cambia el valor de saturación de las imágenes especificadas por el atributo **BackgroundImage** si se ha especificado y hace referencia a una imagen BMP de 8 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de vista**](view-element.md)
</dt> <dt>

[**VIEW. backgroundImage**](view-backgroundimage.md)
</dt> <dt>

[**VER. backgroundImageHueShift**](view-backgroundimagehueshift.md)
</dt> </dl>

 

 





