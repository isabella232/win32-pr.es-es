---
title: AmbientAttributes.alphaBlend
description: El atributo alphaBlend especifica o recupera un valor para la combinación alfa de cualquier vista, subvista o widget de interfaz de usuario.
ms.assetid: a6c47d32-a497-4bfa-8fa3-ef94e267d94b
keywords:
- AmbientAttributes. alphaBlend Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlend
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8c0f0cb9d885f643b39acfbc5148403a5c8b788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700070"
---
# <a name="ambientattributesalphablend"></a>AmbientAttributes.alphaBlend

El atributo **alphaBlend** especifica o recupera un valor para la combinación alfa de cualquier **vista**, **subvista** o widget de interfaz de usuario.

``` syntax
        elementID.alphaBlend
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura y escritura (**Long**) con un valor comprendido entre 0 (sin opacidad) y 255 (opacidad completa) y un valor predeterminado de 255.

## <a name="remarks"></a>Observaciones

Este atributo permite que un elemento parezca semitransparente, dependiendo de la cantidad del conjunto de opacidad. Cuanto menor sea la opacidad, más transparente aparecerá el elemento. Cada elemento de la máscara puede tener un valor de opacidad independiente, excepto para los elementos de botón en un control **BUTTONGROUP** . Cuando **alphaBlend** se establece en la **vista**, se establecerá la opacidad de toda la máscara. Alpha Blend no funcionará con los controles con ventanas, como **listas de reproducción**, **efectos**, cuadros de **lista**, **ventanas emergentes, cuadro** de **edición** y **vídeo** (si **Windowless** está establecido en false). Cuando **alphaBlend** se establece en la **vista**, toda la máscara se vuelve transparente. Los atributos **transparencyColor** utilizados por varios elementos no se admiten con **alphaBlend**.

Cuando se usa **alphaBlend** con un elemento de **texto** que no tiene el parámetro **BackgroundColor** especificado, se usará un color de fondo negro. Si el color de primer plano también es negro (que es el valor predeterminado del *texto*).**foregroundColor**), es posible que el texto sea ilegible. Para evitarlo, especifique siempre el atributo **BackgroundColor** o establezca **foregroundColor** en un color distinto de Black.

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

[**AmbientAttributes.alphaBlendTo**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT. backgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**TEXT. foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





