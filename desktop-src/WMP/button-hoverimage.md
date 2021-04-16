---
title: BUTTON. hoverImage
description: El atributo hoverImage especifica o recupera la imagen que se muestra cuando el botón está en el estado up y el usuario mantiene el puntero del mouse sobre ella.
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- BUTTON. hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80b17a461ffde4b9f6777f3ce360c6b3f1747235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699328"
---
# <a name="buttonhoverimage"></a>BUTTON. hoverImage

El atributo **hoverImage** especifica o recupera la imagen que se muestra cuando el **botón** está en el estado up y el usuario mantiene el puntero del mouse sobre ella.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene el nombre del archivo de imagen.

## <a name="remarks"></a>Observaciones

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF.

La imagen predeterminada es la especificada en el atributo de **imagen** o su valor predeterminado.

Si la imagen de mantener el mouse es mayor que la región definida en el atributo ambiente, se recortará la imagen de desplazamiento.

Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BOTÓN. imagen**](button-image.md)
</dt> </dl>

 

 





