---
title: CUSTOMSLIDER.downImage
description: El atributo downImage especifica o recupera la imagen de estado de bajada del control deslizante personalizado.
ms.assetid: e1efe703-df0a-4ef9-92a9-c9cfb991ee37
keywords:
- CUSTOMSLIDER.downImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3e151f825dab7170c3e3678f280303265af0df91561c7dc709323dd8043809e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750344"
---
# <a name="customsliderdownimage"></a>CUSTOMSLIDER.downImage

El **atributo downImage** especifica o recupera la imagen de estado de bajada del control deslizante personalizado.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Comentarios

Este atributo es opcional. Si no se especifica, se usará el archivo especificado en el atributo **image.**

DownImage **representa** el estado fuera de servicio del control **CUSTOMSLIDER.** Puede ser una sola imagen o una serie de imágenes que representan los distintos estados del control deslizante. Si se usan varias imágenes, se organizan de la misma manera que el **archivo de** imagen.

Los tipos de archivo de imagen admitidos son BMP, JPG, PNG y GIF (sin incluir GIF animados).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER.image**](customslider-image.md)
</dt> </dl>

 

 





