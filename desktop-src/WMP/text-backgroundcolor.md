---
title: TEXT.backgroundColor
description: El atributo backgroundColor especifica o recupera el color de fondo para el control Text.
ms.assetid: 0c16318f-bf57-4c5f-85c1-46641124d431
keywords:
- TEXT.backgroundColor Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TEXT.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65361f581a265b2fa65c8f64e3a05f165691d2c03276bd3412ecd86588f8ff73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901055"
---
# <a name="textbackgroundcolor"></a>TEXT.backgroundColor

El **atributo backgroundColor** especifica o recupera el color de fondo para el control Text.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura y **escritura** que contiene cualquier valor de color Internet Explorer microsoft o el valor "none". Tiene un valor predeterminado de "none", lo que significa que el fondo es transparente.

## <a name="remarks"></a>Comentarios

El color de fondo se establece para el alto y el ancho del control. Si no se establecen el alto y el ancho, el color de fondo se establece en el alto y ancho del texto.

Cuando se usa **alphaBlend** o **alphaBlendTo** con un elemento **TEXT** que no tiene especificado **backgroundColor,** se usará un color de fondo negro. Si el color de primer plano también es negro (que es el valor predeterminado para el atributo **foregroundColor),** es posible que el texto sea ilegible. Para evitarlo, especifique siempre el atributo **backgroundColor** o establezca **foregroundColor** en un color distinto del negro.

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AmbientAttributes.alphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**AmbientAttributes.alphaBlendTo**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Referencia de color**](color-reference.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





