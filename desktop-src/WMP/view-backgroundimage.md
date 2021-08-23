---
title: VIEW.backgroundImage
description: El atributo backgroundImage especifica o recupera la imagen de fondo de VIEW o SUBVIEW.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- VIEW.backgroundImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1de8bcbd0eb47f03aaff46b4292a8afe226ca8a221ec570537351af8e509801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761745"
---
# <a name="viewbackgroundimage"></a>VIEW.backgroundImage

El **atributo backgroundImage** especifica o recupera la imagen de fondo de **VIEW** o **SUBVIEW.**

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura y **escritura.**

## <a name="remarks"></a>Comentarios

Los formatos admitidos son BMP, JPG, GIF y PNG. Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente mediante los atributos **backgroundImageHueShift** y **backgroundImageSaturation.**

En un Windows de descarga multimedia, si especifica el atributo **backgroundImage** para un elemento **VIEW,** también debe especificar el atributo **backgroundColor** para ese elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO VIEW**](view-element.md)
</dt> <dt>

[**VIEW.backgroundImageHueShift**](view-backgroundimagehueshift.md)
</dt> <dt>

[**VIEW.backgroundImageSaturation**](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





