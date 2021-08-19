---
title: BUTTON.downImage
description: El atributo downImage especifica o recupera la imagen que representa el estado de apagado de BUTTON.
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- BUTTON.downImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff24c568ae607b5b67d766f28eb7c221844f1434a959952628cc2ad5a5d6d5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123745"
---
# <a name="buttondownimage"></a>BUTTON.downImage

El **atributo downImage** especifica o recupera la imagen que representa el estado de apagado de **BUTTON.**

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y** escritura que contiene el nombre del archivo de imagen.

## <a name="remarks"></a>Comentarios

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF.

La imagen predeterminada es la especificada en el atributo **image** o su valor predeterminado.

Si la imagen inferior es mayor que la región definida en el atributo ambient, se recortará la imagen hacia abajo.

Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen red-x).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON.down**](button-down.md)
</dt> <dt>

[**BUTTON.image**](button-image.md)
</dt> </dl>

 

 





