---
title: AmbientAttributes.alphaBlend
description: El atributo alphaBlend especifica o recupera un valor para la combinación alfa de cualquier widget VIEW, SUBVIEW o UI.
ms.assetid: a6c47d32-a497-4bfa-8fa3-ef94e267d94b
keywords:
- AmbientAttributes.alphaBlend Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlend
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8c0f0cb9d885f643b39acfbc5148403a5c8b788
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890049"
---
# <a name="ambientattributesalphablend"></a>AmbientAttributes.alphaBlend

El **atributo alphaBlend** especifica o recupera un valor para la combinación alfa de cualquier **widget VIEW,** **SUBVIEW** o UI.

``` syntax
        elementID.alphaBlend
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** **(long)** con un valor que va de 0 (sin opacidad) a 255 (opacidad completa) y un valor predeterminado de 255.

## <a name="remarks"></a>Observaciones

Este atributo permite que un elemento aparezca semitransparente, en función de la cantidad de opacidad establecida. A menos opacidad, más transparente aparecerá el elemento. Cada elemento de la máscara puede tener un valor de opacidad independiente, excepto para los elementos button de un control **BUTTONGROUP.** Cuando **alphaBlend** se establece en **VIEW**, se establecerá la opacidad de toda la máscara. La combinación alfa no funcionará para los controles de ventana, **incluidos PLAYLIST**, **EFFECTS**, **LISTBOX,** **POPUP,** EDITBOX y **VIDEO** (si **windowless** está establecido en false).  Cuando **alphaBlend se** establece en **VIEW,** toda la máscara se vuelve transparente. Los **atributos transparencyColor** utilizados por varios elementos no se admiten **con alphaBlend.**

Cuando se usa **alphaBlend** con un **elemento TEXT** que no tiene especificado **backgroundColor,** se usará un color de fondo negro. Si el color de primer plano también es negro (que es el valor predeterminado para *TEXT.***foregroundColor**), es posible que el texto se vuelva ilegible. Para evitarlo, especifique siempre el atributo **backgroundColor** o establezca **foregroundColor** en un color distinto del negro.

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

[**AmbientAttributes.alphaBlendTo**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.backgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**TEXT.foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





