---
title: TEXT.foregroundColor
description: El atributo foregroundColor especifica o recupera el color del texto para el control Text.
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- TEXT.foregroundColor Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b134058fdc39b653982f752f2623c6cd69b192e24e417ac012a02813a38334a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467075"
---
# <a name="textforegroundcolor"></a>TEXT.foregroundColor

El **atributo foregroundColor** especifica o recupera el color del texto para el control Text.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene cualquier valor de color Internet Explorer Microsoft. El valor predeterminado es "black".

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

Cuando se usa **alphaBlend** o **alphaBlendTo** con un elemento **TEXT** que no tiene especificado **backgroundColor,** se usará un color de fondo negro. Si el color de primer plano también es negro (que es el valor predeterminado del atributo **foregroundColor),** es posible que el texto se vuelva ilegible. Para evitarlo, especifique siempre el atributo **backgroundColor** o establezca **foregroundColor** en un color distinto del negro.

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

[**TEXT.backgroundColor**](text-backgroundcolor.md)
</dt> </dl>

 

 





