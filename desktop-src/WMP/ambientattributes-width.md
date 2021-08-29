---
title: AmbientAttributes.width
description: El atributo width especifica o recupera el ancho del control.
ms.assetid: f246958a-563c-40c0-8a74-4511103b95b2
keywords:
- AmbientAttributes.width Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.width
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc78b23dbedf75b7a58a16fc4aaa43413272c22e6513acbd13b5a6cd890e3c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004105"
---
# <a name="ambientattributeswidth"></a>AmbientAttributes.width

El **atributo width** especifica o recupera el ancho del control.

``` syntax
        elementID.width
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un entero de 16 bits de lectura y escritura **(de** 0 a 32 767) que representa el ancho del control en píxeles. El valor predeterminado es cero o el ancho de la imagen especificada en el atributo **image del** control.

## <a name="remarks"></a>Comentarios

Si el ancho especificado es más estrecho que el ancho de la imagen proporcionada, la imagen se recortará. Si el ancho es más ancho que el ancho de la imagen, la región de clic superará el límite de la imagen. Independientemente del valor que se le asigna a este atributo, la imagen no puede crecer más allá de su **elemento primario VIEW** o **SUBVIEW.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> </dl>

 

 





