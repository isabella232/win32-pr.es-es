---
description: El \_ tipo de \_ enumeración modos de medición de exposición \_ de WPD describe el modo de medición que se va a usar al estimar la exposición de una captura de imagen continuada por un dispositivo.
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: Enumeración WPD_EXPOSURE_METERING_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 76c2594339c6fa4997e4d646fc89e8c30dcdf8fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680388"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a>\_ \_ Enumeración de modos de medición de exposición de WPD \_

El tipo de enumeración modos de medición de exposición de WPD describe el modo de medición que se va a usar al estimar la exposición de una captura de imagen continuada por un dispositivo. **\_ \_ \_**

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WPD_EXPOSURE_METERING_MODES { 
  WPD_EXPOSURE_METERING_MODE_UNDEFINED                = 0,
  WPD_EXPOSURE_METERING_MODE_AVERAGE                  = 1,
  WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE  = 2,
  WPD_EXPOSURE_METERING_MODE_MULTI_SPOT               = 3,
  WPD_EXPOSURE_METERING_MODE_CENTER_SPOT              = 4
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**modo de disponibilidad de exposición de WPD \_ \_ \_ \_ sin definir**
</dt> <dd>

El modo de disponibilidad no está definido.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**\_promedio del \_ modo de medición de exposición de WPD \_ \_**
</dt> <dd>

Usar la exposición mediada en toda la imagen.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**\_ \_ \_ \_ \_ media ponderada del centro del modo de medición de exposición \_ de WPD**
</dt> <dd>

Use una exposición media, con el centro de la imagen dado más peso.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**el modo de disponibilidad de exposición de WPD es \_ \_ multi- \_ \_ \_ Spot**
</dt> <dd>

Usar una técnica de promedio de varias zonas.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**\_zona del \_ centro del \_ modo \_ de \_ medición de exposición de WPD**
</dt> <dd>

Usar una técnica de promedio de punto central.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Indica el modo de medición del dispositivo. Esta enumeración se usa en la propiedad de [modo de medición de \_ \_ \_ exposición de \_ \_ imagen de WPD](still-image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




