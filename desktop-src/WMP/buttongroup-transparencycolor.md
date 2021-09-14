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
ms.openlocfilehash: fbaf6fb70db7d2699a63eb7b4fd34009f7b8ba75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889257"
---
# <a name="buttongrouptransparencycolor"></a>BUTTONGROUP.transparencyColor

El **atributo transparencyColor** especifica o recupera el color transparente de las **imágenes BUTTONGROUP.**

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura y **escritura** sin valor predeterminado, que contiene uno de los valores siguientes.



| Value                                       | Descripción                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| Auto                                        | El píxel en la ubicación 0,0 de la imagen se convierte en el color transparente.                              |
| cualquier valor de color Internet Explorer Microsoft | Un Internet Explorer de color se convierte en el color transparente (por ejemplo, "rojo" o \# "FF0000"). |
| None                                        | Predeterminada. Sin transparencia.                                                                          |



 

## <a name="remarks"></a>Observaciones

Un color transparente en una imagen permitirá que lo que esté detrás de la imagen se muestre a través de las áreas de transparencia. Se puede hacer clic en la región transparente a menos que la etiqueta **clippingImage** recorte.

El color puede ser cualquier valor de color Internet Explorer Microsoft. Si el valor es Auto, se usa el color del píxel en la ubicación 0,0 de la imagen.

Si el color especificado no es uno de los colores Internet Explorer válidos, se devuelve una advertencia y se mantiene el valor anterior.

Dado que los JPG son perdidos y, por tanto, están sujetos a un cambio de color inesperado, no se recomiendan cuando **se usa transparencyColor.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**Referencia de color**](color-reference.md)
</dt> </dl>

 

 





