---
title: BUTTONGROUP.hoverImage
description: El atributo hoverImage especifica o recupera el nombre de la imagen que representa el estado de mantener el puntero de un botón en BUTTONGROUP. El estado de mantener el puntero se produce cuando el botón está en estado hacia arriba y el usuario mantiene el mouse sobre él con el mouse.
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- BUTTONGROUP.hoverImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ee872c06d405d0f9cf5c09f59a86ba1962d0a5b349460c978e37fb5022f1d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135908"
---
# <a name="buttongrouphoverimage"></a>BUTTONGROUP.hoverImage

El **atributo hoverImage** especifica o recupera el nombre de la imagen que representa el estado del mouse de un botón en **BUTTONGROUP.** El estado de mantener el puntero se produce cuando el botón está en estado hacia arriba y el usuario mantiene el mouse sobre él con el mouse.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y escritura.**

## <a name="remarks"></a>Comentarios

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF. Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente mediante los **atributos hueShift** y **saturación.**

La imagen predeterminada es la especificada en el atributo **image** o su valor predeterminado.

Si la imagen con el puntero es mayor que la región definida, se recortará la imagen con el mouse.

Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen de color rojo-x).

## <a name="examples"></a>Ejemplos

Vea *BUTTONELEMENT*. [atributo mappingColor](buttonelement-mappingcolor.md) para un ejemplo que ilustra el uso de este atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP.image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP.saturation**](buttongroup-saturation.md)
</dt> </dl>

 

 





