---
title: BUTTONGROUP.hueShift
description: El atributo hueShift especifica o recupera la cantidad por la que se desplaza el matiz de las imágenes BUTTONGROUP.
ms.assetid: 156256ef-ec24-40c4-ad23-064e38c79e69
keywords:
- ButtonGROUP.hueShift Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.hueShift
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf77faea27ecc5adee6525c4ee8d8ff1541aac4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126885348"
---
# <a name="buttongrouphueshift"></a>BUTTONGROUP.hueShift

El **atributo hueShift** especifica o recupera la cantidad por la que se desplaza el matiz de las imágenes **BUTTONGROUP.**

``` syntax
        elementID.hueShift
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** (**float**) con un valor que va de 0,0 a 360,0 con un valor predeterminado de 0,0.

## <a name="remarks"></a>Observaciones

Este atributo cambia el valor de matiz de las imágenes especificadas por los atributos **disabledImage**, **downImage**, **hoverDownImage**, **hoverImage** e **image** si se han especificado y hacen referencia a imágenes BMP de 8 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Version<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



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

[**BUTTONGROUP.image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP.saturation**](buttongroup-saturation.md)
</dt> </dl>

 

 





