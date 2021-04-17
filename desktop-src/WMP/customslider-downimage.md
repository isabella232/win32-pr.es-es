---
title: CUSTOMSLIDER.downImage
description: El atributo downImage especifica o recupera la imagen de estado hacia abajo del control deslizante personalizado.
ms.assetid: e1efe703-df0a-4ef9-92a9-c9cfb991ee37
keywords:
- CUSTOMSLIDER. downImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8365043654bc3cca9fbf79162302cf804155956d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700124"
---
# <a name="customsliderdownimage"></a>CUSTOMSLIDER.downImage

El atributo **downImage** especifica o recupera la imagen de estado hacia abajo del control deslizante personalizado.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Observaciones

Este atributo es opcional. Si no se especifica, se utilizará el archivo especificado en el atributo de **imagen** .

**DownImage** representa el estado inactivo del control **CUSTOMSLIDER** . Puede ser una sola imagen o una serie de imágenes que representan los distintos Estados del control deslizante. Si se usan varias imágenes, se organizan de la misma manera que el archivo de **imagen** .

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

 

 





