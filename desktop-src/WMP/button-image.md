---
title: BOTÓN. imagen
description: El atributo Image especifica o recupera la imagen predeterminada del botón.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- BOTÓN. Image Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d27363383d72110ebe7b3e94187013ab701a6a3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700134"
---
# <a name="buttonimage"></a>BOTÓN. imagen

El atributo **Image** especifica o recupera la imagen predeterminada del **botón**.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene el nombre del archivo de imagen.

## <a name="remarks"></a>Observaciones

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF (incluidos los GIF animados).

Si la imagen del **botón** es mayor que la región definida por los atributos de **ancho** y **alto** , se recortará la imagen.

Si no se especifica la imagen pero el **alto** y el **ancho** son, se muestra la imagen que se encuentra directamente detrás de este control. Esto puede facilitar el dibujo de la imagen en la propia **vista** , lo que reduce el número de archivos de imagen independientes necesarios.

Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> </dl>

 

 





