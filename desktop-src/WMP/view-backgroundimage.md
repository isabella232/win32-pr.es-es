---
title: VIEW. backgroundImage
description: El atributo backgroundImage especifica o recupera la imagen de fondo de la vista o la subvista.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- VIEW. backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96f4a93882e02589d7f15b74ba5cb225f506d69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649620"
---
# <a name="viewbackgroundimage"></a>VIEW. backgroundImage

El atributo **BackgroundImage** especifica o recupera la imagen de fondo de la **vista** o la **subvista**.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Los formatos admitidos son BMP, JPG, GIF y PNG. Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente con los atributos **backgroundImageHueShift** y **backgroundImageSaturation** .

En un paquete de descarga de Windows Media, si especifica el atributo **BackgroundImage** para un elemento de **vista** , también debe especificar el atributo **BackgroundColor** para ese elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de vista**](view-element.md)
</dt> <dt>

[**VER. backgroundImageHueShift**](view-backgroundimagehueshift.md)
</dt> <dt>

[**VER. backgroundImageSaturation**](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





