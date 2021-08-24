---
title: BUTTON.disabledImage
description: El atributo disabledImage especifica o recupera la imagen que se muestra cuando el botón está deshabilitado.
ms.assetid: b5654323-589a-45da-9534-6fa67c3a4c4b
keywords:
- BUTTON.disabledImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTON.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c3768afd8b1356a1c0ca67a43f951e19143258dfc4f27a3a5e9d861fe9e930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864485"
---
# <a name="buttondisabledimage"></a>BUTTON.disabledImage

El **atributo disabledImage** especifica o recupera la imagen que se muestra cuando **el botón** está deshabilitado.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y** escritura que contiene el nombre del archivo de imagen.

## <a name="remarks"></a>Comentarios

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF.

Esta imagen se mostrará siempre que el **atributo deshabilitado** del control se establezca en true. Si la imagen deshabilitada es mayor que la región definida, se recortará la imagen deshabilitada.

Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen red-x).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> </dl>

 

 





