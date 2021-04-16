---
title: AmbientAttributes.alphaBlendTo
description: El método alphaBlendTo ajusta la propiedad alphaBlend durante un período de tiempo.
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- AmbientAttributes. alphaBlendTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16b21e78de3510e2e4a58c7214995f7888f778c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699541"
---
# <a name="ambientattributesalphablendto"></a>AmbientAttributes.alphaBlendTo

El método **alphaBlendTo** ajusta la propiedad **alphaBlend** durante un período de tiempo.

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*
</dt> <dd>

**Número** (largo) que especifica el nuevo valor de opacidad. Oscila entre 0 (sin opacidad) y 255 (opacidad completa).

</dd> <dt>

<span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*
</dt> <dd>

**Número** (**largo**) que especifica el tiempo, en milisegundos, que toma el elemento para cambiar la opacidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método es útil para que los elementos aparezcan o desaparezcan gradualmente.

Cuando se usa **alphaBlendTo** con un elemento de **texto** que no tiene el parámetro **BackgroundColor** especificado, se usará un color de fondo negro. Si el color de primer plano también es negro (que es el valor predeterminado del *texto*).**foregroundColor**), es posible que el texto sea ilegible. Para evitarlo, especifique siempre el atributo **BackgroundColor** o establezca **foregroundColor** en un color distinto de Black.

> [!Note]  
> Este atributo no se admite en Windows 98.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.alphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT. backgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**TEXT. foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





