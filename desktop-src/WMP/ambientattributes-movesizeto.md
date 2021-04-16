---
title: AmbientAttributes.moveSizeTo
description: El método moveSizeTo mueve el control y especifica un nuevo tamaño para el control en la nueva ubicación. El control se mueve y cambia de tamaño de manera animada en el período de tiempo especificado.
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- AmbientAttributes. moveSizeTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406d48772e85a55ab82241518d499182931cc2fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699434"
---
# <a name="ambientattributesmovesizeto"></a>AmbientAttributes.moveSizeTo

El método **moveSizeTo** mueve el control y especifica un nuevo tamaño para el control en la nueva ubicación. El control se mueve y cambia de tamaño de manera animada en el período de tiempo especificado.

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*
</dt> <dd>

**Número** (**largo**) que especifica el nuevo valor para el atributo **izquierdo** del control.

</dd> <dt>

<span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*
</dt> <dd>

**Número** (**largo**) que especifica el nuevo valor para el atributo **superior** del control.

</dd> <dt>

<span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*
</dt> <dd>

**Número** (**largo**) que especifica el nuevo valor para el atributo de **ancho** del control.

</dd> <dt>

<span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*
</dt> <dd>

**Número** (**largo**) que especifica el nuevo valor para el atributo de **alto** del control.

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Número** (**largo**) que especifica el tiempo, en milisegundos, que tarda el control en moverse a su nueva ubicación.

</dd> <dt>

<span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*
</dt> <dd>

**Valor booleano** que especifica el tipo de movimiento que se crea al mover el control.



| Value | Descripción                                                             |
|-------|-------------------------------------------------------------------------|
| true  | El movimiento no es lineal (movimiento deslizante que acelera y desacelera). |
| false | El movimiento es lineal.                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El movimiento del control puede ser lineal o no lineal. Movimiento lineal significa que el control se mueve a una velocidad constante a su nueva ubicación, desde el inicio y la detención brusca. Cuando se especifica un movimiento no lineal, se crea un movimiento deslizante que se acelera desde cero al principio del movimiento y se ralentiza hasta cero al final, lo que llega a una parada suave.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. Height**](ambientattributes-height.md)
</dt> <dt>

[**AmbientAttributes. Left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> <dt>

[**AmbientAttributes. width**](ambientattributes-width.md)
</dt> </dl>

 

 





