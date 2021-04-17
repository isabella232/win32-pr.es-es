---
title: BUTTONGROUP.hoverImage
description: El atributo hoverImage especifica o recupera el nombre de la imagen que representa el estado de desplazamiento de un botón en el BUTTONGROUP. El estado de desplazamiento se produce cuando el botón está en el estado up y el usuario mantiene el mouse sobre él.
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- BUTTONGROUP. hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702a7aa73f5800628fdf14deb0dbfe142cd80dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698500"
---
# <a name="buttongrouphoverimage"></a>BUTTONGROUP.hoverImage

El atributo **hoverImage** especifica o recupera el nombre de la imagen que representa el estado de desplazamiento de un botón en el **BUTTONGROUP**. El estado de desplazamiento se produce cuando el botón está en el estado up y el usuario mantiene el mouse sobre él.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF. Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente con los atributos **hueShift** y **saturación** .

La imagen predeterminada es la especificada en el atributo de **imagen** o su valor predeterminado.

Si la imagen de mantener el mouse es mayor que la región definida, se recortará la imagen de desplazamiento.

Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).

## <a name="examples"></a>Ejemplos

Vea *BUTTONELEMENT*. atributo [mappingColor](buttonelement-mappingcolor.md) para un ejemplo que ilustra el uso de este atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP. Image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP. saturación**](buttongroup-saturation.md)
</dt> </dl>

 

 





