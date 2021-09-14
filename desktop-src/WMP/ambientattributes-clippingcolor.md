---
title: AmbientAttributes.clippingColor
description: El atributo clippingColor especifica o recupera el color que se recortará del mapa de bits clippingImage.
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- AmbientAttributes.clippingColor Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad526eb0f705d1fce95f3813a666420b29db9de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889993"
---
# <a name="ambientattributesclippingcolor"></a>AmbientAttributes.clippingColor

El **atributo clippingColor** especifica o recupera el color que se recortará del mapa de **bits clippingImage.**

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura y **escritura.**



| Value                                       | Descripción                                       |
|---------------------------------------------|---------------------------------------------------|
| Auto                                        | Predeterminada. Se usa el color en la ubicación de píxeles 0,0. |
| cualquier valor de color Internet Explorer microsoft | Se usa el Internet Explorer especificado.    |



 

## <a name="remarks"></a>Observaciones

El color de recorte indica las regiones de **clippingImage** (o **backgroundImage** para **VIEW** o **SUBVIEW)** que corresponden a partes transparentes y no en las que se puede hacer clic del control. El color de recorte puede indicar varias regiones que se recortarán. Se emite una advertencia si **clippingImage** es un JPG para advertir de la pérdida de color en los JPG.

El elemento PLAYLIST no admite  el atributo **clippingColor.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> <dt>

[**Referencia de color**](color-reference.md)
</dt> </dl>

 

 





