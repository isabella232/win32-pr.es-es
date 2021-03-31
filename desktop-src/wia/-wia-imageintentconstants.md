---
description: Las constantes de intención de imagen especifican qué tipo de datos pretende representar la imagen.
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: Constantes de intención de imagen (Wiadef. h)
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
ms.openlocfilehash: f35c1f7436c8cc5110215a6ccf0383960ec3fb87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001305"
---
# <a name="image-intent-constants"></a>Constantes de intención de imagen

Las constantes de intención de imagen especifican qué tipo de datos pretende representar la imagen. La propiedad del escáner de [**\_ \_ \_ intento de IPS de WIA IP**](-wia-wiaitempropscanneritem.md) utiliza estas marcas. Para proporcionar una intención, combine una marca de tipo de imagen deseada con una marca de tamaño/calidad deseada mediante el operador o. La \_ intención \_ de WIA ninguno no debe combinarse con otras marcas. Tenga en cuenta que una imagen no puede ser de escala de grises y de color.

Las siguientes son constantes de intención de imagen válidas:



| Marcas de tipo de imagen previsto           | Descripción                                  |
|-------------------------------------|----------------------------------------------|
| intento de WIA \_ \_ ninguno                   | Valor predeterminado. No configure ninguna propiedad. |
| \_color del \_ tipo de imagen de intención de WIA \_ \_     | Propiedades preestablecidas para el contenido de color.         |
| tipo de imagen de intención de WIA en \_ \_ escala de \_ \_ grises | Propiedades preestablecidas para el contenido de escala de grises.     |
| \_texto de \_ tipo de imagen de intención de WIA \_ \_      | Propiedades preestablecidas para el contenido de texto.          |
| \_máscara de \_ tipo de imagen de intención de WIA \_ \_      | Máscara para todas las marcas de tipo de imagen.        |



 



| Marcas de calidad y tamaño de imagen previsto | Descripción                                  |
|-----------------------------------|----------------------------------------------|
| tamaño de la intención de WIA \_ \_ minimizar \_       | Propiedades preestablecidas para minimizar el tamaño de la imagen.    |
| calidad de la \_ maximización del intento de WIA \_ \_    | Propiedades preestablecidas para maximizar la calidad de la imagen. |
| \_máscara de \_ tamaño de intención de WIA \_           | Máscara para todas las marcas de tamaño/calidad.      |
| \_ \_ mejor \_ vista previa de la intención de WIA        | Especifica la mejor vista previa de calidad.          |



 

La lista siguiente muestra el nombre de la constante de C/C++ seguido del nombre correspondiente entre paréntesis que se usa en el scripting. Los nombres de script son del tipo enumerado WiaIntent. Tenga en cuenta que no todas las constantes están disponibles a través del script.



| Constante o valor                                                                                                                                                                                                                                                                         | Descripción                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <dt>**WIA \_ \_Color del \_ tipo \_ de imagen de intención**</dt> <dt>0x00000001</dt> </dl>             | Propiedades preestablecidas para el contenido de color.<br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <dt>**WIA \_ Tipo de imagen de intención de \_ \_ escala de \_ grises**</dt> <dt>0x00000002</dt> </dl> | Propiedades preestablecidas para el contenido de escala de grises.<br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <dt>**WIA \_ Tipo de imagen de intención \_ \_ \_ texto**</dt> <dt>0x00000004</dt> </dl>                | Propiedades preestablecidas para el contenido de texto.<br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <dt>**WIA \_ INTENCIÓN de \_ minimizar \_ el tamaño**</dt> <dt>0x00010000</dt> </dl>                       | Propiedades preestablecidas para minimizar el tamaño de la imagen.<br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <dt>**WIA \_ INTENCIÓN de \_ maximizar la \_ calidad**</dt> <dt>0x00020000</dt> </dl>              | Propiedades preestablecidas para maximizar la calidad de la imagen.<br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <dt>**WIA \_ INTENCIÓN \_ Best \_ Preview**</dt> <dt>0x00040000</dt> </dl>                          | Especifica la mejor vista previa de calidad.<br/>          |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




