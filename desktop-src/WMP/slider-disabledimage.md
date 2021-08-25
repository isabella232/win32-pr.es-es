---
title: SLIDER.disabledImage
description: El atributo disabledImage especifica o recupera la imagen del control deslizante que se usa cuando el control deslizante está deshabilitado.
ms.assetid: b6c4237d-8eb0-44ce-a23f-9bdc5c21aca8
keywords:
- SLIDER.disabledImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- SLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 596afbed41fa1a864d8ed4e5fd217cb4856a716623ad2a60db080b3e965ab48d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123075"
---
# <a name="sliderdisabledimage"></a>SLIDER.disabledImage

El **atributo disabledImage** especifica o recupera la imagen del control deslizante que se usa cuando el control deslizante está deshabilitado.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Comentarios

DisabledImage **es** opcional. Si no se proporciona, **backgroundImage** se usa para todos los estados deshabilitados. Cuando un control deslizante está deshabilitado, no se ve ninguna imagen en primer plano.

Los formatos admitidos son BMP, JPG, PNG y GIF (sin incluir GIF animados).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundImage**](slider-backgroundimage.md)
</dt> </dl>

 

 





