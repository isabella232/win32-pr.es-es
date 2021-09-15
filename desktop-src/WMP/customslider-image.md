---
title: CUSTOMSLIDER.image
description: El atributo image especifica o recupera el nombre del archivo que contiene las imágenes correspondientes a los distintos estados del control deslizante personalizado.
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- CustomSLIDER.image Reproductor de Windows Media
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f425ce138b2a11d2be834f39603ecc295c52c706
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258860"
---
# <a name="customsliderimage"></a>CUSTOMSLIDER.image

El **atributo** image especifica o recupera el nombre del archivo que contiene las imágenes correspondientes a los distintos estados del control deslizante personalizado.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Observaciones

El **atributo image** es obligatorio. Especifica un archivo de imagen que consta de una o varias submágenes, organizadas horizontal o verticalmente, que representan los distintos estados del control deslizante personalizado. Cada subimagen debe tener las mismas dimensiones que **positionImage** o el control deslizante personalizado no funcionará correctamente. Por lo tanto, el alto o ancho de la imagen general debe ser un múltiplo par del alto o ancho de **positionImage**.

Los tipos de archivo de imagen admitidos son BMP, JPG, PNG y GIF (sin incluir GIF animados).

## <a name="examples"></a>Ejemplos

A continuación se muestra un ejemplo de una imagen de control deslizante personalizado. La propiedad **positionImage** correspondiente se muestra en la sección de ejemplo de la **propiedad positionImage.**

![imagen de customslider de ejemplo](images/dial.png)

El **atributo positionImage** también contiene un ejemplo de código que ilustra cómo se usan los atributos del **elemento CUSTOMSLIDER.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER.positionImage**](customslider-positionimage.md)
</dt> </dl>

 

 





