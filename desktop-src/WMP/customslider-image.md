---
title: CUSTOMSLIDER. Image
description: El atributo Image especifica o recupera el nombre del archivo que contiene las imágenes correspondientes a los distintos Estados del control deslizante personalizado.
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- Media Player CUSTOMSLIDER. Image de Windows
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f425ce138b2a11d2be834f39603ecc295c52c706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698472"
---
# <a name="customsliderimage"></a>CUSTOMSLIDER. Image

El atributo **Image** especifica o recupera el nombre del archivo que contiene las imágenes correspondientes a los distintos Estados del control deslizante personalizado.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Observaciones

El atributo **Image** es obligatorio. Especifica un archivo de imagen que consta de una o más subimágenes, organizadas horizontal o verticalmente, que representan los distintos Estados del control deslizante personalizado. Cada subimagen debe tener las mismas dimensiones que **positionImage** o el control deslizante personalizado no funcionará correctamente. El alto o ancho de la imagen global debe ser, por tanto, un múltiplo par del alto o del ancho de **positionImage**.

Los tipos de archivo de imagen admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados).

## <a name="examples"></a>Ejemplos

El siguiente es un ejemplo de una imagen de control deslizante personalizado. El **positionImage** correspondiente se muestra en la sección ejemplo de la propiedad **positionImage** .

![imagen de customslider de ejemplo](images/dial.png)

El atributo **positionImage** también contiene un ejemplo de código que ilustra cómo se usan los atributos del elemento **CUSTOMSLIDER** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER.positionImage**](customslider-positionimage.md)
</dt> </dl>

 

 





