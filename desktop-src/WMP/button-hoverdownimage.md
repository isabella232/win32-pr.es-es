---
title: BUTTON.hoverDownImage
description: El atributo hoverDownImage especifica o recupera la imagen que se muestra cuando button está en estado de bajada y el usuario mantiene el mouse sobre ella con el puntero del mouse.
ms.assetid: 06645307-50f1-400d-aa73-c48d0fba3ee1
keywords:
- BUTTON.hoverDownImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTON.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcdb23f9806e36cebd2f5da6a46a8307c268861d73f68361e07f56e9ce09dcc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902405"
---
# <a name="buttonhoverdownimage"></a>BUTTON.hoverDownImage

El **atributo hoverDownImage** especifica o recupera la imagen que se muestra cuando **button** está en estado de bajada y el usuario mantiene el mouse sobre ella con el puntero del mouse.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene el nombre del archivo de imagen.

## <a name="remarks"></a>Comentarios

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF.

La imagen predeterminada es la especificada en el atributo **downImage** o su valor predeterminado.

Si la imagen con el mouse hacia abajo es mayor que la región definida en el atributo ambient, se recortará la imagen con el mouse hacia abajo.

Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen red-x).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON.downImage**](button-downimage.md)
</dt> </dl>

 

 





