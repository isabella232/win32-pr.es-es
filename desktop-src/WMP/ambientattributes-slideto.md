---
title: AmbientAttributes. slideto
description: El método Slider mueve el control a una nueva ubicación. El control se mueve de forma no lineal en el período de tiempo especificado.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- AmbientAttributes. slideto Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deb214046ace59094b6bd5c362dfa716b9fceb57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700198"
---
# <a name="ambientattributesslideto"></a>AmbientAttributes. slideto

El método **Slider** mueve el control a una nueva ubicación. El control se mueve de forma no lineal en el período de tiempo especificado.

``` syntax
        elementID.slideTo(newX, newY, moveTime)
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

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Número** (**largo**) que especifica el tiempo, en milisegundos, que tarda el control en moverse a su nueva ubicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método es diferente de **moveTo**, que crea un movimiento lineal al mover el control. El movimiento no lineal creado por este método es un movimiento deslizante que se acelera a partir de una velocidad de cero al principio del movimiento y se ralentiza a cero al final, lo que llega a una parada suave.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. Left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes. moveTo**](ambientattributes-moveto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





