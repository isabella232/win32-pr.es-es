---
title: AmbientAttributes.clippingImage
description: El atributo clippingImage especifica o recupera la región a la que se recortará el control.
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- AmbientAttributes.clippingImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e05e05ca9c7c3efdf842ffd4297da6f9fee035d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890012"
---
# <a name="ambientattributesclippingimage"></a>AmbientAttributes.clippingImage

El **atributo clippingImage** especifica o recupera la región a la que se recortará el control.

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que indica el nombre del archivo de imagen. No tiene valor predeterminado.

## <a name="remarks"></a>Observaciones

El **atributo clippingImage** admite archivos PNG, JPG, BMP y GIF (sin incluir GIF animados). Dado que los JPG son perdidos y, por tanto, están sujetos a un cambio de color inesperado, no se recomiendan para recortar imágenes.

Este atributo es útil cuando se desea mostrar solo una parte de la imagen de control y no todo el área rectangular. El **atributo clippingColor** indica las regiones de la imagen de recorte que corresponden a partes transparentes del control en las que no se puede hacer clic. Por lo tanto, el control puede ser de cualquier forma. Para obtener mejores resultados, la imagen de recorte debe tener el mismo tamaño que la imagen de control.

Los elementos **PLAYLIST,** **VIEW** y **SUBVIEW** no admiten el atributo **clippingImage.** Una imagen de recorte no funcionará con el **elemento VIDEO** si *VIDEO*. **windowless** se establece en false, ni con el **elemento EFFECTS** si *EFFECTS*. **windowed** se establece en true.

Dado que el uso de imágenes de recorte impone una penalización de rendimiento, no se deben usar cuando la eficacia es un problema.

## <a name="examples"></a>Ejemplos

Vea el [atributo BUTTONELEMENT.mappingColor](buttonelement-mappingcolor.md) para obtener un ejemplo que ilustra el uso de este atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.clippingColor**](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





