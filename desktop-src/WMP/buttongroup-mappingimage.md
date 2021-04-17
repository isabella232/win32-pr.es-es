---
title: BUTTONGROUP.mappingImage
description: El atributo mappingImage especifica o recupera el nombre de la imagen que representa el mapa de botones de BUTTONGROUP.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- BUTTONGROUP. mappingImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4afc44a00d5ce9b15ee01d4a0dc1aff52c555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699947"
---
# <a name="buttongroupmappingimage"></a>BUTTONGROUP.mappingImage

El atributo **mappingImage** especifica o recupera el nombre de la imagen que representa el mapa de botones de **BUTTONGROUP**.

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Se trata de un atributo obligatorio que debe especificarse.

La imagen de asignación debe ser las mismas dimensiones que la **imagen** principal. Se trata de un mapa de las áreas en las que se hace clic de la imagen principal. Construya el mapa rellenando cada área seleccionable con un color diferente.

Al definir cada **BUTTONELEMENT**, designe su color a partir del mapa mediante el atributo **mappingColor** . Por ejemplo, si tiene un gráfico de botón de signo de cierre en la imagen principal, puede crear un mapa con el área del signo de color rojo. El atributo **BUTTONELEMENT** debe especificarse en rojo para que se pueda hacer clic en la imagen de detención de firma.

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados). Debido a que las JPGs son perdidas y, por tanto, están sujetas a cambios de color inesperados, no se recomiendan para asignar imágenes.

## <a name="examples"></a>Ejemplos

La siguiente ilustración es un ejemplo de **mappingImage** y la imagen visible a la que corresponde. Estas imágenes forman parte de la máscara en la pequeña carpeta incluida con el SDK.

![imagen de asignación de ejemplo](images/absam01m.png)![imagen de fondo de ejemplo](images/absam01f.png)

Vea *BUTTONELEMENT*. atributo [mappingColor](buttonelement-mappingcolor.md) para un ejemplo de código que ilustra el uso de este atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BUTTONELEMENT. mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP. Image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP. transparencyColor**](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





