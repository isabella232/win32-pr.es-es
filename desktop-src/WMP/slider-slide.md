---
title: Control deslizante. Slide
description: El atributo de diapositiva especifica o recupera un valor que indica si la imagen de primer plano se desplaza sobre la imagen de fondo o se revela gradualmente en una posición estática sobre la imagen de fondo.
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- Control deslizante. Slide Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9f79b5016b323380c5a4d06c8af7ab5fb0b8a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660999"
---
# <a name="sliderslide"></a>Control deslizante. Slide

El atributo de **diapositiva** especifica o recupera un valor que indica si la imagen de primer plano se desplaza sobre la imagen de fondo o se revela gradualmente en una posición estática sobre la imagen de fondo.

``` syntax
        elementID.slide
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                                                          |
|-------|----------------------------------------------------------------------|
| true  | Predeterminada. La imagen de primer plano se desliza sobre la imagen de fondo.      |
| false | La imagen de primer plano se revela en el lugar de la imagen de fondo. |



 

## <a name="remarks"></a>Observaciones

Cuando el control deslizante **thumbImage** se mueve con el mouse, si la **diapositiva** está establecida en true, la imagen de primer plano se desliza como si lo extrajo el control deslizante para abarcar la imagen de fondo. Si **Slide** está establecido en false, la imagen de primer plano no se mueve, sino que se revela, como si el control deslizante fuera la imagen de fondo de la imagen de primer plano.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDEr**](slider-element.md)
</dt> <dt>

[**Control deslizante. backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDEr. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





