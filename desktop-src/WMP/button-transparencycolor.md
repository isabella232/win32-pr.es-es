---
title: BUTTON.transparencyColor
description: El atributo transparencyColor especifica o recupera el color que será transparente en las imágenes BUTTON.
ms.assetid: c22f9965-3118-4c96-8ff5-7fbaa28cbb57
keywords:
- BUTTON.transparencyColor Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTON.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d51e42b1636958edd772d27c4e5a29720fa0dd87a74784f28f3ffeb7891873c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118840468"
---
# <a name="buttontransparencycolor"></a>BUTTON.transparencyColor

El **atributo transparencyColor** especifica o recupera el color que será transparente en las **imágenes BUTTON.**

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y** escritura sin ningún valor predeterminado que contenga uno de los valores siguientes.



| Valor                                    | Descripción                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Auto                                     | El color del píxel en la ubicación 0,0 de la imagen se convierte en el color transparente.                        |
| Cualquier Internet Explorer de formato de color | Un Internet Explorer de formato de color se convierte en el color transparente (por ejemplo, "rojo" o \# "FF0000"). |
| Ninguno                                     | Sin transparencia.                                                                                          |



 

## <a name="remarks"></a>Comentarios

Un color transparente en una imagen permite que lo que hay detrás de la imagen se muestre a través de las áreas transparentes. El **BOTÓN** seguirá recibiendo clics en la región transparente.

El color transparente puede ser cualquier valor Internet Explorer de color. Si el valor del atributo **transparencyColor** se establece en "Auto", se usa el color del píxel en la ubicación 0,0 de la imagen.

Si el color especificado no es uno de los colores de IE válidos, se mantiene el valor anterior.

Dado que los JPG son de pérdida y, por tanto, están sujetos a un cambio de color inesperado, no se recomiendan cuando **se usa transparencyColor.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON.image**](button-image.md)
</dt> <dt>

[**Referencia de color**](color-reference.md)
</dt> </dl>

 

 





