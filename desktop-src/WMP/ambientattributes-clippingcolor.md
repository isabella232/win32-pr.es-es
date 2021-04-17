---
title: AmbientAttributes.clippingColor
description: El atributo clippingColor especifica o recupera el color que se va a recortar del mapa de bits clippingImage.
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- AmbientAttributes. clippingColor Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad526eb0f705d1fce95f3813a666420b29db9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700067"
---
# <a name="ambientattributesclippingcolor"></a>AmbientAttributes.clippingColor

El atributo **clippingColor** especifica o recupera el color que se va a recortar del mapa de bits **clippingImage** .

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.



| Value                                       | Descripción                                       |
|---------------------------------------------|---------------------------------------------------|
| Automático                                        | Predeterminada. Se utiliza el color en la ubicación de píxel 0, 0. |
| cualquier valor de color de Microsoft Internet Explorer | Se utiliza el color especificado de Internet Explorer.    |



 

## <a name="remarks"></a>Observaciones

El color de recorte indica las regiones del **clippingImage** (o la **BackgroundImage** para la **vista** o la **subvista**) que corresponden a partes transparentes y no en las que se pueda hacer clic en el control. El color de recorte puede indicar varias regiones que se van a recortar. Se emite una advertencia si el **clippingImage** es un jpg para advertir de la pérdida de color en jpgs.

El elemento de **lista de reproducción** no admite el atributo **clippingColor** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> <dt>

[**Referencia de color**](color-reference.md)
</dt> </dl>

 

 





