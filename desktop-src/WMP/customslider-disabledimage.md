---
title: CUSTOMSLIDER.disabledImage
description: El atributo disabledImage especifica o recupera la imagen del control deslizante utilizado cuando el control deslizante está deshabilitado.
ms.assetid: 91b1c2e3-6c92-4baa-b1f3-e44707157f4b
keywords:
- CUSTOMSLIDER.disabledImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9b5d75e26204fc362dfa714bc8720d6db87e511bbfda03096d60f58f91c3335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651565"
---
# <a name="customsliderdisabledimage"></a>CUSTOMSLIDER.disabledImage

El **atributo disabledImage** especifica o recupera la imagen del control deslizante utilizado cuando el control deslizante está deshabilitado.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Comentarios

Este atributo es opcional. Si no se especifica, se usará el archivo especificado en el atributo **image.**

**disabledImage representa** el estado deshabilitado del control **CUSTOMSLIDER.** Puede ser una sola imagen o una serie de imágenes que representan los distintos estados del control deslizante. Si se usan varias imágenes, se organizan de la misma manera que el **archivo de** imagen.

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

 

 





