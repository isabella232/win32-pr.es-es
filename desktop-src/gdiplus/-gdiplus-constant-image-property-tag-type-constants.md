---
description: Puede almacenar y recuperar metadatos de imagen con la ayuda de un objeto PropertyItem. El miembro de datos type de un objeto PropertyItem especifica el tipo de datos de los valores almacenados en el miembro de datos value de ese mismo objeto PropertyItem.
ms.assetid: d05cdf42-4b30-45ce-85a1-025d4f4e9d13
title: Constantes de tipo de etiqueta de propiedad de imagen (Gdiplusimaging.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb565972b2dc8b8962e367c7d2f3c09b4f857382156538a83f7d6ee338c66ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977605"
---
# <a name="image-property-tag-type-constants"></a>Constantes de tipo de etiqueta de propiedad image

Puede almacenar y recuperar metadatos de imagen con la ayuda de un [**objeto PropertyItem.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) El **miembro** de datos type de un **objeto PropertyItem** especifica el tipo de datos de los valores almacenados en el miembro de datos value de ese **mismo objeto PropertyItem.**

Las siguientes constantes, definidas en Gdiplusimaging.h,  se pueden asignar al miembro de datos de tipo de un [**objeto PropertyItem.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem)



| Constante                                                                                                                                                                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PixelFormat4bppIndexed"></span><span id="pixelformat4bppindexed"></span><span id="PIXELFORMAT4BPPINDEXED"></span><dl> <dt>**PixelFormat4bppIndexed**</dt> </dl>         | Especifica que el formato es de 4 bits por píxel, indizado.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="PropertyTagTypeASCII"></span><span id="propertytagtypeascii"></span><span id="PROPERTYTAGTYPEASCII"></span><dl> <dt>**PropertyTagTypeASCII**</dt> </dl>                 | Especifica que el miembro **de datos de** valor es una cadena ASCII terminada en NULL. Si establece  el miembro de datos de tipo de un objeto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) en PropertyTagTypeASCII, debe establecer el miembro de datos **length** en la longitud de la cadena, incluido el terminador NULL. Por ejemplo, la cadena `HELLO` tendría una longitud de 6.<br/> |
| <span id="PropertyTagTypeByte"></span><span id="propertytagtypebyte"></span><span id="PROPERTYTAGTYPEBYTE"></span><dl> <dt>**PropertyTagTypeByte**</dt> </dl>                     | Especifica que el miembro **de datos de** valor es una matriz de bytes.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PropertyTagTypeLong"></span><span id="propertytagtypelong"></span><span id="PROPERTYTAGTYPELONG"></span><dl> <dt>**PropertyTagTypeLong**</dt> </dl>                     | Especifica que el miembro **de datos** de valor es una matriz de enteros largos sin signo (32 bits).<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PropertyTagTypeRational"></span><span id="propertytagtyperational"></span><span id="PROPERTYTAGTYPERATIONAL"></span><dl> <dt>**PropertyTagTypeRational**</dt> </dl>     | Especifica que el miembro **de datos de** valor es una matriz de pares de enteros largos sin signo. Cada par representa una fracción; el primer entero es el numerador y el segundo entero es el denominador.<br/>                                                                                                                                                                       |
| <span id="PropertyTagTypeShort"></span><span id="propertytagtypeshort"></span><span id="PROPERTYTAGTYPESHORT"></span><dl> <dt>**PropertyTagTypeShort**</dt> </dl>                 | Especifica que el miembro **de datos** value es una matriz de enteros cortos sin signo (16 bits).<br/>                                                                                                                                                                                                                                                                                     |
| <span id="PropertyTagTypeSLONG"></span><span id="propertytagtypeslong"></span><span id="PROPERTYTAGTYPESLONG"></span><dl> <dt>**PropertyTagTypeSLONG**</dt> </dl>                 | Especifica que el miembro **de datos value** es una matriz de enteros largos con signo (32 bits).<br/>                                                                                                                                                                                                                                                                                        |
| <span id="PropertyTagTypeSRational"></span><span id="propertytagtypesrational"></span><span id="PROPERTYTAGTYPESRATIONAL"></span><dl> <dt>**PropertyTagTypeSRational**</dt> </dl> | Especifica que el miembro **de datos de** valor es una matriz de pares de enteros largos con signo. Cada par representa una fracción; el primer entero es el numerador y el segundo entero es el denominador.<br/>                                                                                                                                                                         |
| <span id="PropertyTagTypeUndefined"></span><span id="propertytagtypeundefined"></span><span id="PROPERTYTAGTYPEUNDEFINED"></span><dl> <dt>**PropertyTagTypeUndefined**</dt> </dl> | Especifica que el miembro **de datos value** es una matriz de bytes que puede contener valores de cualquier tipo de datos. <br/>                                                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Gdiplusimaging.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de etiquetas de propiedades de imagen](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[Especificaciones de formato de archivo de imagen](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[Leer y escribir metadatos](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 
