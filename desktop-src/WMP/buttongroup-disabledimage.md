---
title: BUTTONGROUP.disabledImage
description: El atributo disabledImage especifica o recupera el nombre de la imagen que representa el Estado deshabilitado de los botones en el BUTTONGROUP.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- BUTTONGROUP. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9659c4d726313c0fb202a840e12891f00ad3fcf0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698683"
---
# <a name="buttongroupdisabledimage"></a>BUTTONGROUP.disabledImage

El atributo **disabledImage** especifica o recupera el nombre de la imagen que representa el Estado deshabilitado de los botones en el **BUTTONGROUP**.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF. Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente con los atributos **hueShift** y **saturación** .

Cuando el atributo **Disabled** de un elemento **BUTTONELEMENT** está establecido en true, se muestra la región correspondiente de **disabledImage** para **BUTTONGROUP** . Si la imagen deshabilitada es mayor que la región definida, se recortará la imagen deshabilitada.

Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).

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

[**BUTTONGROUP. saturación**](buttongroup-saturation.md)
</dt> </dl>

 

 





