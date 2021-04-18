---
title: BUTTON. transparencyColor
description: El atributo transparencyColor especifica o recupera el color que será transparente en las imágenes del botón.
ms.assetid: c22f9965-3118-4c96-8ff5-7fbaa28cbb57
keywords:
- BUTTON. transparencyColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771249ddb070c596dc126b9b0c8c7d04a4b4268f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700262"
---
# <a name="buttontransparencycolor"></a>BUTTON. transparencyColor

El atributo **transparencyColor** especifica o recupera el color que será transparente en las imágenes del **botón** .

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura sin valor predeterminado que contiene uno de los valores siguientes.



| Value                                    | Descripción                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Automático                                     | El color del píxel en la ubicación 0, 0 en la imagen se convierte en el color transparente.                        |
| Cualquier valor de formato de color de Internet Explorer | Un valor de formato de color de Internet Explorer se convierte en el color transparente (por ejemplo, "red" o " \# FF0000"). |
| None                                     | Sin transparencia.                                                                                          |



 

## <a name="remarks"></a>Observaciones

Un color transparente en una imagen permite que el que está detrás de la imagen se muestre a través de las áreas transparentes. El **botón** seguirá recibiendo clics en la región transparente.

El color transparente puede ser cualquier valor de color de Internet Explorer. Si el valor del atributo **transparencyColor** se establece en "auto", se usa el color del píxel en la ubicación 0, 0 en la imagen.

Si el color especificado no es ninguno de los colores de IE válidos, se mantiene el valor anterior.

Dado que los JPGs se pierden y, por lo tanto, están sujetos a cambios de color inesperados, no se recomiendan cuando se usa **transparencyColor** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BOTÓN. imagen**](button-image.md)
</dt> <dt>

[**Referencia de color**](color-reference.md)
</dt> </dl>

 

 





