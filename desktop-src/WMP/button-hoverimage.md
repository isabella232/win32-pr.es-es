---
title: BUTTON.hoverImage
description: El atributo hoverImage especifica o recupera la imagen que se muestra cuando button está en estado up y el usuario mantiene el puntero sobre él con el puntero del mouse.
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- BUTTON.hoverImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80b17a461ffde4b9f6777f3ce360c6b3f1747235
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889436"
---
# <a name="buttonhoverimage"></a>BUTTON.hoverImage

El **atributo hoverImage** especifica o recupera la imagen que se muestra cuando **button** está en estado up y el usuario mantiene el puntero sobre él con el puntero del mouse.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y** escritura que contiene el nombre del archivo de imagen.

## <a name="remarks"></a>Observaciones

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF.

La imagen predeterminada es la especificada en el atributo **image** o su valor predeterminado.

Si la imagen con el puntero es mayor que la región definida en el atributo ambient, se recortará la imagen con el puntero.

Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen red-x).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON.image**](button-image.md)
</dt> </dl>

 

 





