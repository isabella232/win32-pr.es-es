---
title: BUTTONGROUP.saturation
description: El atributo de saturación especifica o recupera el valor de saturación de las imágenes BUTTONGROUP.
ms.assetid: bfd957f0-8201-4a4f-9162-a397ed97c747
keywords:
- ButtonGROUP.saturation Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d3579ac8109cb56e56c78a07a8f53e4cd7c017a695b6018f6a2ad41f703035
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581307"
---
# <a name="buttongroupsaturation"></a>BUTTONGROUP.saturation

El **atributo de** saturación especifica o recupera el valor de saturación de las imágenes **BUTTONGROUP.**

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** (**float**) con un valor que va de 0,0 a 2,0 con un valor predeterminado de 1,0.

## <a name="remarks"></a>Comentarios

Este atributo cambia el valor de saturación de las imágenes especificadas por los atributos **disabledImage**, **downImage**, **hoverDownImage**, **hoverImage** e **image** si se han especificado y hacen referencia a imágenes BMP de 8 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.disabledImage**](buttongroup-disabledimage.md)
</dt> <dt>

[**BUTTONGROUP.downImage**](buttongroup-downimage.md)
</dt> <dt>

[**BUTTONGROUP.hoverDownImage**](buttongroup-hoverdownimage.md)
</dt> <dt>

[**BUTTONGROUP.hoverImage**](buttongroup-hoverimage.md)
</dt> <dt>

[**BUTTONGROUP.hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP.image**](buttongroup-image.md)
</dt> </dl>

 

 





