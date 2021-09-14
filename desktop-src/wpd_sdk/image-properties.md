---
description: Windows Dispositivos portátiles admite las siguientes propiedades de imagen.
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: Propiedades de la imagen (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 959a008d9c30991058226e52db6e45ed417ee6e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262103"
---
# <a name="image-properties"></a>Propiedades de la imagen

Windows Dispositivos portátiles admite las siguientes propiedades de imagen.



| Propiedad.                                                                                                                                       | VarType     | Descripción                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IMAGEN DE \_ \_ WPD BITDEPTH**                                                                                                                       | **VT \_ UI4** | Profundidad de bits de la imagen.                                                                                                                                                                                                                                                                                                                     |
| <span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**ESTADO CORREGIDO \_ DEL COLOR DE LA IMAGEN \_ \_ WPD \_** | **VT \_ UI4** | Enumeración [**WPD \_ COLOR \_ CORRECTED \_ STATUS \_ VALUES**](wpd-color-corrected-status-values.md) que especifica si se ha corregido el color del archivo. Esto evita que varios dispositivos corrijan automáticamente el color de la imagen durante el procesamiento posterior.<br/>                                                                       |
| **ESTADO \_ RECORTADO DE \_ IMAGEN WPD \_**                                                                                                                | **VT \_ UI4** | Enumeración [**WPD \_ CROPPED \_ STATUS \_ VALUES**](wpd-cropped-status-values.md) que especifica si se ha recortado el archivo. Esto evita que varios dispositivos recorten automáticamente la imagen durante el procesamiento posterior.<br/>                                                                                                        |
| **ÍNDICE DE EXPOSICIÓN \_ DE \_ IMÁGENES WPD \_**                                                                                                                | **VT \_ UI4** | Valor que identifica la configuración de velocidad de película cuando se capturó esta imagen. La configuración corresponde a las designaciones ISO de ASA/ISO.<br/> Normalmente, un dispositivo admite valores enumerados discretos, pero es posible un control continuo sobre un intervalo.<br/> Un valor de 0xFFFFFFFF corresponde a la configuración ISO automática.<br/> |
| **TIEMPO DE EXPOSICIÓN \_ DE \_ IMÁGENES WPD \_**                                                                                                                 | **VT \_ UI4** | Identifica la velocidad de obturación del dispositivo cuando se capturó esta imagen. Las unidades se escalan en segundos en 10 000.<br/>                                                                                                                                                                                                                        |
| **WPD \_ IMAGE \_ FNUMBER**                                                                                                                        | **VT \_ UI4** | Identifica la configuración de apertura de la lente cuando se capturó esta imagen. Las unidades son iguales al número f escalado en 100.<br/>                                                                                                                                                                                                              |
| **RESOLUCIÓN HORIZONTAL DE \_ LA \_ IMAGEN \_ WPD**                                                                                                         | **VT \_ R8**  | Indica la resolución horizontal de una imagen, en puntos por pulgada (PPP).                                                                                                                                                                                                                                                                       |
| **RESOLUCIÓN VERTICAL DE \_ IMÁGENES \_ WPD \_**                                                                                                           | **VT \_ R8**  | Indica la resolución vertical de una imagen, en puntos por pulgada (PPP).                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




