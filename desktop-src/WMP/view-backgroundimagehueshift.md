---
title: VIEW.backgroundImageHueShift
description: El atributo backgroundImageHueShift especifica o recupera la cantidad por la que se desplaza el matiz de la imagen de fondo.
ms.assetid: 13cedc87-f43a-4d33-9339-f317ea7b8d3b
keywords:
- VIEW.backgroundImageHueShift Reproductor de Windows Media
topic_type:
- apiref
api_name:
- VIEW.backgroundImageHueShift
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72dcbf1dcb06939ab74398c39bb89bc512dbb47b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070779"
---
# <a name="viewbackgroundimagehueshift"></a>VIEW.backgroundImageHueShift

El **atributo backgroundImageHueShift** especifica o recupera la cantidad por la que se desplaza el matiz de la imagen de fondo.

``` syntax
        elementID.backgroundImageHueShift
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** (**float**) con un valor que va de 0,0 a 360,0 con un valor predeterminado de 0,0.

## <a name="remarks"></a>Observaciones

Este atributo cambia el valor de matiz de las imágenes especificadas por el atributo **backgroundImage** si se ha especificado y hace referencia a una imagen BMP de 8 bits.

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

[**VIEW.backgroundImageSaturation**](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





