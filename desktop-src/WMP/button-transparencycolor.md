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
ms.openlocfilehash: 771249ddb070c596dc126b9b0c8c7d04a4b4268f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889385"
---
# <a name="buttontransparencycolor"></a>BUTTON.transparencyColor

El **atributo transparencyColor** especifica o recupera el color que será transparente en las **imágenes BUTTON.**

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura sin ningún valor predeterminado que contenga uno de los valores siguientes.



| Value                                    | Descripción                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Auto                                     | El color del píxel en la ubicación 0,0 de la imagen se convierte en el color transparente.                        |
| Cualquier valor Internet Explorer formato de color | Un Internet Explorer de formato de color se convierte en el color transparente (por ejemplo, "rojo" o \# "FF0000"). |
| None                                     | Sin transparencia.                                                                                          |



 

## <a name="remarks"></a>Observaciones

Un color transparente en una imagen permite que todo lo que está detrás de la imagen se muestre a través de las áreas transparentes. El **botón** seguirá recibiendo clics en la región transparente.

El color transparente puede ser cualquier valor Internet Explorer de color. Si el valor del atributo **transparencyColor** se establece en "Auto", se usa el color del píxel en la ubicación 0,0 de la imagen.

Si el color especificado no es uno de los colores de IE válidos, se mantiene el valor anterior.

Dado que los JPG son perdidos y, por tanto, están sujetos a un cambio de color inesperado, no se recomiendan cuando **se usa transparencyColor.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON.image**](button-image.md)
</dt> <dt>

[**Referencia de color**](color-reference.md)
</dt> </dl>

 

 





