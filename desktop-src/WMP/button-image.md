---
title: BUTTON.image
description: El atributo image especifica o recupera la imagen predeterminada de BUTTON.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- Button.image Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d27363383d72110ebe7b3e94187013ab701a6a3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889425"
---
# <a name="buttonimage"></a>BUTTON.image

El **atributo** image especifica o recupera la imagen predeterminada de **BUTTON.**

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y** escritura que contiene el nombre del archivo de imagen.

## <a name="remarks"></a>Observaciones

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF (incluidos los GIF animados).

Si la **imagen BUTTON** es mayor que la  región definida por los atributos **de** ancho y alto, la imagen se recortará.

Si no se especifica la imagen  pero el **alto** y el ancho son, se muestra la imagen directamente detrás de este control. Esto puede facilitar el dibujo de la imagen en **la propia vista,** lo que reduce el número de archivos de imagen independientes necesarios.

Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen red-x).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> </dl>

 

 





