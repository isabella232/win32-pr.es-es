---
title: BUTTONGROUP. transparencyColor
description: El atributo transparencyColor especifica o recupera el color transparente de las imágenes BUTTONGROUP.
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- BUTTONGROUP. transparencyColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaf6fb70db7d2699a63eb7b4fd34009f7b8ba75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699516"
---
# <a name="buttongrouptransparencycolor"></a>BUTTONGROUP. transparencyColor

El atributo **transparencyColor** especifica o recupera el color transparente de las imágenes **BUTTONGROUP** .

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura y escritura sin valores predeterminados, que contiene uno de los valores siguientes.



| Value                                       | Descripción                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| Automático                                        | El píxel de la ubicación 0, 0 en la imagen se convierte en el color transparente.                              |
| cualquier valor de color de Microsoft Internet Explorer | Un valor de color de Internet Explorer se convierte en el color transparente (por ejemplo, "red" o " \# FF0000"). |
| None                                        | Predeterminada. Sin transparencia.                                                                          |



 

## <a name="remarks"></a>Observaciones

Un color transparente en una imagen permitirá todo lo que haya detrás de la imagen para que se muestre a través de las áreas de transparencia. La región transparente es seleccionable a menos que se recorte por la etiqueta **clippingImage** .

El color puede ser cualquier valor de color de Microsoft Internet Explorer. Si el valor es auto, se usa el color del píxel de la ubicación 0, 0 de la imagen.

Si el color especificado no es uno de los colores válidos de Internet Explorer, se devuelve una advertencia y se mantiene el valor anterior.

Dado que los JPGs se pierden y, por lo tanto, están sujetos a cambios de color inesperados, no se recomiendan cuando se usa **transparencyColor** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**Referencia de color**](color-reference.md)
</dt> </dl>

 

 





