---
description: Las constantes de intención de imagen especifican el tipo de datos que la imagen está pensada para representar.
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: Constantes de intención de imagen (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_INTENT_IMAGE_TYPE_COLOR
- WIA_INTENT_IMAGE_TYPE_GRAYSCALE
- WIA_INTENT_IMAGE_TYPE_TEXT
- WIA_INTENT_MINIMIZE_SIZE
- WIA_INTENT_MAXIMIZE_QUALITY
- WIA_INTENT_BEST_PREVIEW
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 78130128a26057ed521512dd21acc5a1bd7e98c47ed689eaabc250a972c2a003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814125"
---
# <a name="image-intent-constants"></a>Constantes de intención de imagen

Las constantes de intención de imagen especifican el tipo de datos que la imagen está pensada para representar. La [**propiedad del analizador CUR INTENT \_ \_ \_ de WIA IPS**](-wia-wiaitempropscanneritem.md) usa estas marcas. Para proporcionar una intención, combine una marca de tipo de imagen prevista con una marca de tamaño o calidad prevista mediante el operador OR. WIA \_ INTENT NONE no debe \_ combinarse con ninguna otra marca. Tenga en cuenta que una imagen no puede ser de escala de grises ni de color.

Las siguientes son constantes de intención de imagen válidas:



| Marcas de tipo de imagen previstas           | Descripción                                  |
|-------------------------------------|----------------------------------------------|
| WIA \_ INTENT \_ NONE                   | Valor predeterminado. No preestablecte ninguna propiedad. |
| COLOR DEL \_ TIPO DE IMAGEN DE INTENCIÓN \_ \_ WIA \_     | Propiedades preestablecidas para el contenido de color.         |
| ESCALA DE \_ GRISES \_ DEL TIPO DE IMAGEN DE INTENCIÓN \_ \_ WIA | Propiedades preestablecidas para el contenido de escala de grises.     |
| TEXTO DE TIPO \_ DE IMAGEN DE INTENCIÓN \_ \_ WIA \_      | Propiedades preestablecidas para el contenido de texto.          |
| MÁSCARA DE TIPO \_ DE IMAGEN DE INTENCIÓN \_ \_ WIA \_      | Máscara para todas las marcas de tipo de imagen.        |



 



| Marcas de calidad y tamaño de imagen previstos | Descripción                                  |
|-----------------------------------|----------------------------------------------|
| INTENCIÓN DE WIA \_ \_ MINIMIZAR EL \_ TAMAÑO       | Propiedades preestablecidas para minimizar el tamaño de la imagen.    |
| INTENCIÓN DE WIA \_ \_ MAXIMIZAR LA \_ CALIDAD    | Propiedades preestablecidas para maximizar la calidad de la imagen. |
| MÁSCARA DE TAMAÑO \_ DE \_ INTENCIÓN DE \_ WIA           | Máscara para todas las marcas de tamaño y calidad.      |
| WIA \_ INTENT \_ BEST \_ PREVIEW        | Especifica la versión preliminar de mejor calidad.          |



 

En la lista siguiente se muestra el nombre de constante de C/C++ seguido del nombre correspondiente entre paréntesis que se usa en el scripting. Los nombres de script son del tipo enumerado WiaIntent. Tenga en cuenta que no todas las constantes están disponibles a través del script.



| Constante o valor                                                                                                                                                                                                                                                                         | Descripción                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <dt>**WIA \_ COLOR \_ DEL TIPO DE IMAGEN \_ \_ DE**</dt> <dt>INTENCIÓN 0x00000001</dt> </dl>             | Propiedades preestablecidas para el contenido de color.<br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <dt>**WIA \_ ESCALA \_ DE \_ GRISES DEL TIPO \_ DE**</dt> <dt>IMAGEN DE INTENCIÓN 0x00000002</dt> </dl> | Propiedades preestablecidas para el contenido de escala de grises.<br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <dt>**WIA \_ TIPO \_ DE IMAGEN DE INTENCIÓN \_ \_ TEXT**</dt> <dt>0x00000004</dt> </dl>                | Propiedades preestablecidas para el contenido de texto.<br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <dt>**WIA \_ INTENCIÓN \_ MINIMIZAR \_ TAMAÑO 0x00010000**</dt> <dt></dt> </dl>                       | Propiedades preestablecidas para minimizar el tamaño de la imagen.<br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <dt>**WIA \_ INTENCIÓN \_ MAXIMIZAR LA CALIDAD \_ 0x00020000**</dt> <dt></dt> </dl>              | Propiedades preestablecidas para maximizar la calidad de la imagen.<br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <dt>**WIA \_ INTENT \_ BEST \_ PREVIEW**</dt> <dt>0x00040000</dt> </dl>                          | Especifica la versión preliminar de mejor calidad.<br/>          |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




