---
title: BUTTONGROUP.mappingImage
description: El atributo mappingImage especifica o recupera el nombre de la imagen que representa el mapa de botones de BUTTONGROUP.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- BUTTONGROUP.mappingImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4afc44a00d5ce9b15ee01d4a0dc1aff52c555
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126885340"
---
# <a name="buttongroupmappingimage"></a>BUTTONGROUP.mappingImage

El **atributo mappingImage** especifica o recupera el nombre de la imagen que representa el mapa de botones de **BUTTONGROUP.**

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura y **escritura.**

## <a name="remarks"></a>Observaciones

Se trata de un atributo obligatorio que se debe especificar.

La imagen de asignación debe tener las mismas dimensiones que la imagen **principal.** Es un mapa de las áreas en las que se puede hacer clic de la imagen principal. Construya el mapa rellenando cada área en la que se puede hacer clic con un color diferente.

Al definir cada **BUTTONELEMENT**, designe su color del mapa mediante el **atributo mappingColor.** Por ejemplo, si tiene un gráfico de botón con forma de signo de detenerse en la imagen principal, puede crear un mapa con el área del signo coloreado en rojo. A **continuación, el** atributo BUTTONELEMENT debe especificarse como rojo para que se pueda hacer clic en la imagen de signo de detenerse.

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF (sin incluir GIF animados). Dado que los JPG son una pérdida y, por tanto, están sujetos a un cambio de color inesperado, no se recomiendan para asignar imágenes.

## <a name="examples"></a>Ejemplos

La siguiente ilustración es un ejemplo de **mappingImage** y la imagen visible a la que corresponde. Estas imágenes forman parte de la máscara de la carpeta Tiny incluida con el SDK.

![imagen de asignación de ejemplo](images/absam01m.png)![imagen de fondo de ejemplo](images/absam01f.png)

Vea *BUTTONELEMENT*. [atributo mappingColor](buttonelement-mappingcolor.md) para un ejemplo de código que ilustra el uso de este atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**BUTTONELEMENT.mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP.transparencyColor**](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





