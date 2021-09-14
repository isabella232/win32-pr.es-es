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
ms.openlocfilehash: 1c9d7f5807bcb5fd90dae211d80faf78006b6b35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070778"
---
# <a name="viewbackgroundimagesaturation"></a>VIEW.backgroundImageSaturation

El **atributo backgroundImageSaturation** especifica o recupera el valor de saturación de la imagen de fondo.

``` syntax
        elementID.backgroundImageSaturation
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** (**float**) con un valor que va de 0,0 a 2,0 con un valor predeterminado de 1,0.

## <a name="remarks"></a>Observaciones

Este atributo cambia el valor de saturación de las imágenes especificadas por el atributo **backgroundImage** si se ha especificado y hace referencia a una imagen BMP de 8 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





