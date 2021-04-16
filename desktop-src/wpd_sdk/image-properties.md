---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de imagen.
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: Propiedades de la imagen (PortableDevice. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671783"
---
# <a name="image-properties"></a>Propiedades de la imagen

Los dispositivos portátiles de Windows admiten las siguientes propiedades de imagen.



| Propiedad                                                                                                                                       | VarType     | Descripción                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_BITDEPTH de imagen de WPD \_**                                                                                                                       | **VT \_ UI4** | Profundidad de bits de la imagen.                                                                                                                                                                                                                                                                                                                     |
| <span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**\_ \_ \_ Estado corregido de color de imagen de WPD \_** | **VT \_ UI4** | Una enumeración de [**\_ \_ \_ \_ valores de estado corregidos en color de WPD**](wpd-color-corrected-status-values.md) que especifica si el archivo se ha corregido por color. Esto impide que varios dispositivos corrijan automáticamente la imagen durante el procesamiento posterior.<br/>                                                                       |
| **\_ \_ Estado recortado de imagen de WPD \_**                                                                                                                | **VT \_ UI4** | Una enumeración de [**\_ \_ \_ valores recortados de WPD**](wpd-cropped-status-values.md) que especifica si el archivo se ha recortado. Esto impide que varios dispositivos recorten automáticamente la imagen durante el procesamiento posterior.<br/>                                                                                                        |
| **\_Índice de \_ exposición de imagen de WPD \_**                                                                                                                | **VT \_ UI4** | Valor que identifica la configuración de velocidad de la película cuando se capturó esta imagen. La configuración corresponde a las designaciones ISO de ASA/DIN.<br/> Normalmente, un dispositivo admite valores enumerados discretos, pero es posible el control continuo sobre un intervalo.<br/> Un valor de 0xFFFFFFFF corresponde a la configuración automática de ISO.<br/> |
| **tiempo de exposición de la imagen de WPD \_ \_ \_**                                                                                                                 | **VT \_ UI4** | Identifica la velocidad del obturador del dispositivo cuando se capturó esta imagen. Las unidades están en segundos escaladas por 10000.<br/>                                                                                                                                                                                                                        |
| **\_FNUMBER de imagen de WPD \_**                                                                                                                        | **VT \_ UI4** | Identifica el valor de abertura de la lente cuando se capturó esta imagen. Las unidades son iguales al número f escalado por 100.<br/>                                                                                                                                                                                                              |
| **\_ \_ resolución horizontal de imagen de WPD \_**                                                                                                         | **VT \_ R8**  | Indica la resolución horizontal de una imagen, en puntos por pulgada (PPP).                                                                                                                                                                                                                                                                       |
| **\_ \_ resolución vertical de imagen de WPD \_**                                                                                                           | **VT \_ R8**  | Indica la resolución vertical de una imagen, en puntos por pulgada (PPP).                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




