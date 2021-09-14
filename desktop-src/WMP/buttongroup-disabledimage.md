---
title: BUTTONGROUP.disabledImage
description: El atributo disabledImage especifica o recupera el nombre de la imagen que representa el estado deshabilitado de los botones en BUTTONGROUP.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- BUTTONGROUP.disabledImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9659c4d726313c0fb202a840e12891f00ad3fcf0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068491"
---
# <a name="buttongroupdisabledimage"></a>BUTTONGROUP.disabledImage

El **atributo disabledImage** especifica o recupera el nombre de la imagen que representa el estado deshabilitado de los botones de **BUTTONGROUP.**

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura y **escritura.**

## <a name="remarks"></a>Observaciones

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF. Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente mediante los atributos **hueShift** y **saturación.**

Cuando el **atributo deshabilitado** de un **elemento BUTTONELEMENT** se establece en true, se muestra la región correspondiente de **disabledImage** para **BUTTONGROUP.** Si la imagen deshabilitada es mayor que la región definida, se recortará la imagen deshabilitada.

Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen red-x).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP.saturation**](buttongroup-saturation.md)
</dt> </dl>

 

 





