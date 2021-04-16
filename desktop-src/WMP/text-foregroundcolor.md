---
title: TEXT. foregroundColor
description: El atributo foregroundColor especifica o recupera el color del texto del control de texto.
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- Media Player de Windows TEXT. foregroundColor
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e452a18a085337e8cbf0ec88567d6a57a0a498a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699360"
---
# <a name="textforegroundcolor"></a>TEXT. foregroundColor

El atributo **foregroundColor** especifica o recupera el color del texto del control de texto.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene cualquier valor de color de Microsoft Internet Explorer. El valor predeterminado es "Black".

Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .

Cuando se usa **alphaBlend** o **alphaBlendTo** con un elemento de **texto** que no tiene el parámetro **BackgroundColor** especificado, se usará un color de fondo negro. Si el color de primer plano también es negro (que es el valor predeterminado para el atributo **foregroundColor** ), es posible que el texto sea ilegible. Para evitarlo, especifique siempre el atributo **BackgroundColor** o establezca **foregroundColor** en un color distinto de Black.

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

[**TEXT. backgroundColor**](text-backgroundcolor.md)
</dt> </dl>

 

 





