---
title: CUSTOMSLIDER.disabledImage
description: El atributo disabledImage especifica o recupera la imagen del control deslizante que se usa cuando se deshabilita el control deslizante.
ms.assetid: 91b1c2e3-6c92-4baa-b1f3-e44707157f4b
keywords:
- CUSTOMSLIDER. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169057d952170fb92c4e3a98617c7db22f5456b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700127"
---
# <a name="customsliderdisabledimage"></a>CUSTOMSLIDER.disabledImage

El atributo **disabledImage** especifica o recupera la imagen del control deslizante que se usa cuando se deshabilita el control deslizante.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Observaciones

Este atributo es opcional. Si no se especifica, se utilizará el archivo especificado en el atributo de **imagen** .

**DisabledImage** representa el Estado deshabilitado del control **CUSTOMSLIDER** . Puede ser una sola imagen o una serie de imágenes que representan los distintos Estados del control deslizante. Si se usan varias imágenes, se organizan de la misma manera que el archivo de **imagen** .

Los tipos de archivo de imagen admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER. Image**](customslider-image.md)
</dt> </dl>

 

 





