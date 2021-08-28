---
title: CUSTOMSLIDER.hoverImage
description: El atributo hoverImage especifica o recupera la imagen que aparece cuando el mouse está sobre el control deslizante personalizado.
ms.assetid: b5d10289-280c-4578-83e8-6259249ff448
keywords:
- CUSTOMSLIDER.hoverImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d12f337c8d4889e0d2e94bac0c0a4dce74f3a80fda9261d245b91ce5612754d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651405"
---
# <a name="customsliderhoverimage"></a>CUSTOMSLIDER.hoverImage

El **atributo hoverImage** especifica o recupera la imagen que aparece cuando el mouse está sobre el control deslizante personalizado.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Comentarios

Este atributo es opcional. Si no se especifica, se usará el archivo especificado en el atributo **image.**

**HoverImage representa** el estado de desplazamiento del control CUSTOMSLIDER; es decir, el estado que se muestra cuando el cursor del mouse se desplaza sobre él. Puede ser una sola imagen o una serie de imágenes que representan los distintos estados del control deslizante. Si se usan varias imágenes, se organizan de la misma manera que el **archivo de** imagen.

Los tipos de archivo de imagen admitidos son BMP, JPG, PNG y GIF (sin incluir GIF animados).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER.image**](customslider-image.md)
</dt> </dl>

 

 





