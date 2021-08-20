---
title: VIEW.backgroundImageSaturation
description: El atributo backgroundImageSaturation especifica o recupera el valor de saturación de la imagen de fondo.
ms.assetid: 9e1f205b-6366-4816-9430-1153f57d686c
keywords:
- VIEW.backgroundImageSaturation Reproductor de Windows Media
topic_type:
- apiref
api_name:
- VIEW.backgroundImageSaturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934c10ee090f99d456c38a5eb56512d3adb9b748d45b166167b49f3249d819e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506865"
---
# <a name="viewbackgroundimagesaturation"></a>VIEW.backgroundImageSaturation

El **atributo backgroundImageSaturation** especifica o recupera el valor de saturación de la imagen de fondo.

``` syntax
        elementID.backgroundImageSaturation
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** (**float**) con un valor que va de 0,0 a 2,0 con un valor predeterminado de 1,0.

## <a name="remarks"></a>Comentarios

Este atributo cambia el valor de saturación de las imágenes especificadas por el atributo **backgroundImage** si se ha especificado y hace referencia a una imagen BMP de 8 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO VIEW**](view-element.md)
</dt> <dt>

[**VIEW.backgroundImage**](view-backgroundimage.md)
</dt> <dt>

[**VIEW.backgroundImageHueShift**](view-backgroundimagehueshift.md)
</dt> </dl>

 

 





