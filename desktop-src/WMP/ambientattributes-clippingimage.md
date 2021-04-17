---
title: AmbientAttributes.clippingImage
description: El atributo clippingImage especifica o recupera la región en la que se va a recortar el control.
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- AmbientAttributes. clippingImage Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e05e05ca9c7c3efdf842ffd4297da6f9fee035d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700066"
---
# <a name="ambientattributesclippingimage"></a>AmbientAttributes.clippingImage

El atributo **clippingImage** especifica o recupera la región en la que se va a recortar el control.

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que indica el nombre del archivo de imagen. No tiene valor predeterminado.

## <a name="remarks"></a>Observaciones

El atributo **clippingImage** admite archivos PNG, JPG, BMP y GIF (sin incluir los GIF animados). Dado que los JPGs se pierden y, por lo tanto, están sujetos a cambios de color inesperados, no se recomiendan para recortar imágenes.

Este atributo es útil si desea mostrar solo una parte de la imagen de control y no el área rectangular completa. El atributo **clippingColor** indica las regiones de la imagen de recorte que corresponden a partes transparentes y no en las que se pueda hacer clic del control. Por tanto, el control puede ser cualquier forma. Para obtener los mejores resultados, la imagen de recorte debe tener el mismo tamaño que la imagen de control.

El atributo **clippingImage** no es compatible con los elementos de **lista de reproducción**, **vista** y **subvista** . Una imagen de recorte no funcionará con el elemento de **vídeo** si se trata de un *vídeo*. **Windowless** está establecido en false, y en el elemento **Effects** si tiene *efectos*. **windowed** está establecido en true.

Dado que el uso de imágenes de recorte impone una reducción del rendimiento, no se deben usar cuando la eficacia es un problema.

## <a name="examples"></a>Ejemplos

Vea el atributo [BUTTONELEMENT. mappingColor](buttonelement-mappingcolor.md) para obtener un ejemplo que ilustra el uso de este atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.clippingColor**](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





