---
title: AmbientAttributes.moveSizeTo
description: El método moveSizeTo mueve el control y especifica un nuevo tamaño para el control en la nueva ubicación. El control se mueve y cambia de tamaño de forma animada durante el período de tiempo especificado.
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- AmbientAttributes.moveSizeTo Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936a6696dfcc99c5a181906eb970f84c7019af7905c466f09e820044f6220271
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469955"
---
# <a name="ambientattributesmovesizeto"></a>AmbientAttributes.moveSizeTo

El **método moveSizeTo** mueve el control y especifica un nuevo tamaño para el control en la nueva ubicación. El control se mueve y cambia de tamaño de forma animada durante el período de tiempo especificado.

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*
</dt> <dd>

**Number** (**long**) especificando el nuevo valor para el **atributo** izquierdo del control.

</dd> <dt>

<span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*
</dt> <dd>

**Number** (**long**) especificando el nuevo valor para el **atributo superior** del control.

</dd> <dt>

<span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*
</dt> <dd>

**Number** (**long**) que especifica el nuevo valor para el **atributo de** ancho del control.

</dd> <dt>

<span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*
</dt> <dd>

**Number** (**long**) que especifica el nuevo valor para el **atributo height** del control.

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Number** (**long**) que especifica el tiempo, en milisegundos, que tarda el control en moverse a su nueva ubicación.

</dd> <dt>

<span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*
</dt> <dd>

**Booleano** que especifica el tipo de movimiento creado al mover el control.



| Value | Descripción                                                             |
|-------|-------------------------------------------------------------------------|
| true  | El movimiento no es lineal (movimiento deslizante que acelera y disminuye la velocidad). |
| false | El movimiento es lineal.                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El movimiento del control puede ser lineal o no lineal. El movimiento lineal significa que el control se mueve a una velocidad constante a su nueva ubicación, iniciando y deteniéndose repentinamente. Cuando se especifica un movimiento no lineal, se crea un movimiento deslizante que se acelera desde cero al principio del movimiento y se reduce a cero al final, y se detiene sin problemas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.height**](ambientattributes-height.md)
</dt> <dt>

[**AmbientAttributes.left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> <dt>

[**AmbientAttributes.width**](ambientattributes-width.md)
</dt> </dl>

 

 





