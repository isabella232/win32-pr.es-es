---
description: El tipo de enumeración WPD EXPOSURE METERING MODES describe el modo de medición que se usará al calcular la exposición para la captura de imágenes \_ \_ \_ fijas por parte de un dispositivo.
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: WPD_EXPOSURE_METERING_MODES enumeración (PortableDevice.h)
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
ms.openlocfilehash: 2a165493142fc25ea64adc2678e8bc4ccbeace32e245422f0fcea419063a26ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842285"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a>Enumeración DE MODOS DE \_ \_ MEDICIÓN \_ DE EXPOSICIÓN DE WPD

El **tipo de enumeración \_ WPD EXPOSURE \_ METERING \_ MODES** describe el modo de medición que se usará al calcular la exposición para la captura de imágenes fijas por parte de un dispositivo.

## <a name="syntax"></a>Syntax


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

<span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**MODO DE MEDICIÓN DE EXPOSICIÓN DE WPD \_ \_ SIN \_ \_ DEFINIR**
</dt> <dd>

El modo de medición no está definido.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**MEDIA DEL MODO \_ DE \_ MEDICIÓN \_ DE EXPOSICIÓN DE \_ WPD**
</dt> <dd>

Use la exposición media en toda la imagen.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**MEDIA \_ PONDERADA DEL \_ CENTRO \_ DE MEDICIÓN DE EXPOSICIÓN \_ \_ DE \_ WPD**
</dt> <dd>

Use una exposición promedio, con el centro de la imagen dado más peso.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**MODO DE \_ \_ MEDICIÓN DE \_ EXPOSICIÓN WPD \_ MULTI \_ SPOT**
</dt> <dd>

Use una técnica de promedio multi spot.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**PUNTO CENTRAL DEL \_ MODO \_ DE MEDICIÓN DE EXPOSICIÓN \_ \_ DE \_ WPD**
</dt> <dd>

Use una técnica de promedio de punto central.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Indica el modo de medición del dispositivo. Esta enumeración la usa la [propiedad \_ WPD STILL \_ IMAGE EXPOSURE \_ \_ METERING \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




