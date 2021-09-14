---
title: BUTTONGROUP.hoverDownImage
description: El atributo hoverDownImage especifica o recupera el nombre de la imagen que representa el estado de mantener el mouse sobre un botón en BUTTONGROUP. El estado de mantener el mouse hacia abajo se produce cuando el botón está en estado de bajada y el usuario mantiene el mouse sobre él con el mouse.
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- BUTTONGROUP.hoverDownImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a40788fafffd6eb4626bc834a941f7330c988fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068487"
---
# <a name="buttongrouphoverdownimage"></a>BUTTONGROUP.hoverDownImage

El **atributo hoverDownImage** especifica o recupera el nombre de la imagen que representa el estado de mantener el mouse sobre un botón en **BUTTONGROUP.** El estado de mantener el mouse hacia abajo se produce cuando el botón está en estado de bajada y el usuario mantiene el mouse sobre él con el mouse.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y escritura.**

## <a name="remarks"></a>Observaciones

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF. Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente mediante los **atributos hueShift** y **saturación.**

La imagen predeterminada es la especificada en el atributo **downImage** o su valor predeterminado.

Si la imagen con el mouse hacia abajo es mayor que la región definida, se recortará la imagen con el mouse hacia abajo.

Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen red-x).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.downImage**](buttongroup-downimage.md)
</dt> <dt>

[**BUTTONGROUP.hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP.saturation**](buttongroup-saturation.md)
</dt> </dl>

 

 





