---
title: BUTTONGROUP. Image
description: El atributo Image especifica o recupera el nombre de la imagen que representa los botones de un BUTTONGROUP.
ms.assetid: dad50a1e-d147-4e0f-b5d6-8cbfeef32438
keywords:
- Media Player BUTTONGROUP. Image de Windows
topic_type:
- apiref
api_name:
- BUTTONGROUP.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa395edc149671ad05a38a5ff7c77053b6e3d82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700191"
---
# <a name="buttongroupimage"></a>BUTTONGROUP. Image

El atributo **Image** especifica o recupera el nombre de la imagen que representa los botones de un **BUTTONGROUP**.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF. Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente con los atributos **hueShift** y **saturación** .

Si la imagen del control es mayor que la región definida, se recortará la imagen.

Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP. saturación**](buttongroup-saturation.md)
</dt> </dl>

 

 





