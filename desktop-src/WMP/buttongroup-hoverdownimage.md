---
title: BUTTONGROUP.hoverDownImage
description: El atributo hoverDownImage especifica o recupera el nombre de la imagen que representa el estado de desactivación de un botón en el BUTTONGROUP. El estado de desactivación se produce cuando el botón está en estado inactivo y el usuario mantiene el mouse sobre él.
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- BUTTONGROUP. hoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a40788fafffd6eb4626bc834a941f7330c988fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698501"
---
# <a name="buttongrouphoverdownimage"></a>BUTTONGROUP.hoverDownImage

El atributo **hoverDownImage** especifica o recupera el nombre de la imagen que representa el estado de desactivación de un botón en el **BUTTONGROUP**. El estado de desactivación se produce cuando el botón está en estado inactivo y el usuario mantiene el mouse sobre él.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF. Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente con los atributos **hueShift** y **saturación** .

La imagen predeterminada es la especificada en el atributo **downImage** o su valor predeterminado.

Si la imagen desplegable es más grande que la región definida, se recortará la imagen de la que se mantiene el puntero.

Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.downImage**](buttongroup-downimage.md)
</dt> <dt>

[**BUTTONGROUP.hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP. saturación**](buttongroup-saturation.md)
</dt> </dl>

 

 





