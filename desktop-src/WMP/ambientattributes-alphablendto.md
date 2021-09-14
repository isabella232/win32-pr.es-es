---
title: AmbientAttributes.alphaBlendTo
description: El método alphaBlendTo ajusta la propiedad alphaBlend durante un período de tiempo.
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- AmbientAttributes.alphaBlendTo Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890041"
---
# <a name="ambientattributesalphablendto"></a>AmbientAttributes.alphaBlendTo

El **método alphaBlendTo** ajusta la **propiedad alphaBlend** durante un período de tiempo.

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*
</dt> <dd>

**Número** (long) que especifica el nuevo valor de opacidad. Oscila entre 0 (sin opacidad) y 255 (opacidad completa).

</dd> <dt>

<span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*
</dt> <dd>

**Number** (**long**) que especifica el tiempo, en milisegundos, que tarda el elemento en cambiar la opacidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método es útil para hacer que los elementos aparezcan o desaparezcan gradualmente.

Cuando se usa **alphaBlendTo con** un elemento **TEXT** que no tiene especificado **backgroundColor,** se usará un color de fondo negro. Si el color de primer plano también es negro (que es el valor predeterminado para *TEXT.***foregroundColor**), es posible que el texto se vuelva ilegible. Para evitarlo, especifique siempre el atributo **backgroundColor** o establezca **foregroundColor** en un color distinto del negro.

> [!Note]  
> Este atributo no se admite en Windows 98.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.alphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.backgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**TEXT.foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





