---
title: BUTTONGROUP.transparencyColor
description: El atributo transparencyColor especifica o recupera el color transparente de las imágenes BUTTONGROUP.
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- BUTTONGROUP.transparencyColor Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf97a25081e3f5c5729721bd675d9c59be1a4d52adc86acf6b9b75a0ee86dbac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342668"
---
# <a name="buttongrouptransparencycolor"></a>BUTTONGROUP.transparencyColor

El **atributo transparencyColor** especifica o recupera el color transparente de las **imágenes BUTTONGROUP.**

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y** escritura sin ningún valor predeterminado, que contiene uno de los siguientes valores.



| Valor                                       | Descripción                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| Auto                                        | El píxel situado en la ubicación 0,0 de la imagen se convierte en el color transparente.                              |
| cualquier valor de color Internet Explorer microsoft | Un Internet Explorer de color se convierte en el color transparente (por ejemplo, "rojo" o \# "FF0000"). |
| Ninguno                                        | Predeterminada. Sin transparencia.                                                                          |



 

## <a name="remarks"></a>Comentarios

Un color transparente en una imagen permitirá que lo que hay detrás de la imagen se muestre a través de las áreas de transparencia. Se puede hacer clic en la región transparente a menos que se recorte mediante la **etiqueta clippingImage.**

El color puede ser cualquier valor de color Internet Explorer microsoft. Si el valor es Auto, se usa el color del píxel en la ubicación 0,0 de la imagen.

Si el color especificado no es uno de los colores Internet Explorer válidos, se devuelve una advertencia y se mantiene el valor anterior.

Dado que los JPG son de pérdida y, por tanto, están sujetos a un cambio de color inesperado, no se recomiendan cuando **se usa transparencyColor.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**Referencia de color**](color-reference.md)
</dt> </dl>

 

 





