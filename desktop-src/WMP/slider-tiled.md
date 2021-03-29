---
title: Control deslizante. en mosaico
description: El atributo en mosaico especifica o recupera un valor que indica si se va a colocar en mosaico la imagen del control deslizante.
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- Control deslizante. ventanas en mosaico Media Player
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1448f496ee45d6c8b01356499b9628c745d69f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660615"
---
# <a name="slidertiled"></a>Control deslizante. en mosaico

El atributo en **mosaico** especifica o recupera un valor que indica si se va a colocar en mosaico la imagen del control deslizante.

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| true  | Predeterminada. El mapa de bits de la imagen se repetirá hasta que rellene toda la región del control. |
| false | La imagen no se mostrará en mosaico.                                                                |



 

## <a name="remarks"></a>Observaciones

Este atributo solo se aplica si usa imágenes de primer plano y de fondo para definir un control deslizante. Si las imágenes son más pequeñas que el área definida del control deslizante y el atributo en **mosaico** está establecido en true, las imágenes se repetirán hasta que rellenen toda la longitud del control.

Puede que desee utilizar este atributo junto con el atributo de **borde** . El atributo **borde** le permite definir un borde que no se repite durante el mosaico.

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

[**SLIDEr. Border**](slider-bordersize.md)
</dt> <dt>

[**SLIDEr. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





