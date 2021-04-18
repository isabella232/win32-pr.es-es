---
title: TEXT. backgroundColor
description: El atributo backgroundColor especifica o recupera el color de fondo del control de texto.
ms.assetid: 0c16318f-bf57-4c5f-85c1-46641124d431
keywords:
- TEXT. backgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff833fad0b5ad60b49479c57dc51cbe82f48dbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718676"
---
# <a name="textbackgroundcolor"></a>TEXT. backgroundColor

El atributo **BackgroundColor** especifica o recupera el color de fondo del control de texto.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene cualquier valor de color de Microsoft Internet Explorer o el valor "none". Tiene un valor predeterminado de "none", lo que significa que el fondo es transparente.

## <a name="remarks"></a>Observaciones

El color de fondo se establece para el alto y ancho del control. Si no se establece el alto y el ancho, el color de fondo se establece en el alto y ancho del texto.

Cuando se usa **alphaBlend** o **alphaBlendTo** con un elemento de **texto** que no tiene el parámetro **BackgroundColor** especificado, se usará un color de fondo negro. Si el color de primer plano también es negro (que es el valor predeterminado para el atributo **foregroundColor** ), es posible que el texto sea ilegible. Para evitarlo, especifique siempre el atributo **BackgroundColor** o establezca **foregroundColor** en un color distinto de Black.

Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



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

[**TEXT. foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





