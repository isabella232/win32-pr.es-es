---
title: SLIDEr. disabledImage
description: El atributo disabledImage especifica o recupera la imagen del control deslizante que se utiliza cuando se deshabilita el control deslizante.
ms.assetid: b6c4237d-8eb0-44ce-a23f-9bdc5c21aca8
keywords:
- CONTROL SLIDEr. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1b90dcbd551ca0f8bb332f858eac0b69c46733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660390"
---
# <a name="sliderdisabledimage"></a>SLIDEr. disabledImage

El atributo **disabledImage** especifica o recupera la imagen del control deslizante que se utiliza cuando se deshabilita el control deslizante.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Observaciones

**DisabledImage** es opcional. Si no se proporciona, el **BackgroundImage** se utiliza para todos los Estados deshabilitados. Cuando un control deslizante está deshabilitado, no hay ninguna imagen en primer plano visible.

Los formatos admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDEr**](slider-element.md)
</dt> <dt>

[**Control deslizante. backgroundImage**](slider-backgroundimage.md)
</dt> </dl>

 

 





