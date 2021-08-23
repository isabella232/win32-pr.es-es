---
title: SLIDER.tiled
description: El atributo en mosaico especifica o recupera un valor que indica si la imagen del control deslizante se va a mosaico.
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- Slider.tiled Reproductor de Windows Media
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a97be7ee857574b24585ffd7ffd9b63acdfad0a37762445699daa3a06f94e97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832541"
---
# <a name="slidertiled"></a>SLIDER.tiled

El **atributo en** mosaico especifica o recupera un valor que indica si la imagen del control deslizante se va a mosaico.

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Valor | Descripción                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| true  | Predeterminada. El mapa de bits de la imagen se repetirá hasta que rellene toda la región del control. |
| false | La imagen no se pondrá en mosaico.                                                                |



 

## <a name="remarks"></a>Comentarios

Este atributo solo se aplica si usa imágenes de primer plano y de fondo para definir un control deslizante. Si las imágenes son más pequeñas que el área definida del control deslizante y el atributo **en** mosaico se establece en true, las imágenes se repetirán hasta que rellenen toda la longitud del control.

Es posible que desee usar este atributo junto con el **atributo borderSize.** El **atributo borderSize** permite definir un borde que no se repite durante el tiling.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDER.borderSize**](slider-bordersize.md)
</dt> <dt>

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





