---
title: AmbientAttributes.moveTo
description: El método moveTo mueve el control a una nueva ubicación a una velocidad lineal.
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- AmbientAttributes.moveTo Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af481526c0923c527bb14aa4700a6c6fe5ea3613
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889945"
---
# <a name="ambientattributesmoveto"></a>AmbientAttributes.moveTo

El **método moveTo** mueve el control a una nueva ubicación a una velocidad lineal.

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*
</dt> <dd>

**Number** (**long**) que especifica el nuevo valor para el **atributo** izquierdo del control.

</dd> <dt>

<span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*
</dt> <dd>

**Number** (**long**) que especifica el nuevo valor para el **atributo** superior del control.

</dd> <dt>

<span id="time"></span><span id="TIME"></span>*hora*
</dt> <dd>

**Number** (**long**) que especifica el tiempo, en milisegundos, que tarda el control en moverse a su nueva ubicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método es útil para elementos **ANIMADOS SUBVIEW** (por ejemplo, si el usuario hace clic en una bandeja y los controles se deslizan hacia abajo).

Este método crea un movimiento lineal al mover el control. Esto difiere de **slideTo**, que crea un movimiento no lineal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.slideTo**](ambientattributes-slideto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





