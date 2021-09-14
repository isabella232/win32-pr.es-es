---
description: El tipo de enumeración WPD EXPOSURE METERING MODES describe el modo de medición que se usará al calcular la exposición para la captura de imágenes \_ \_ \_ fijas por un dispositivo.
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
ms.openlocfilehash: 76c2594339c6fa4997e4d646fc89e8c30dcdf8fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247089"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a>Enumeración \_ WPD EXPOSURE \_ METERING \_ MODES

El **tipo de \_ enumeración WPD EXPOSURE \_ METERING \_ MODES** describe el modo de medición que se usará al calcular la exposición para la captura de imágenes fijas por un dispositivo.

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

<span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**MODO DE MEDICIÓN DE EXPOSICIÓN DE WPD \_ \_ SIN \_ \_ DEFINIR**
</dt> <dd>

El modo de medición no está definido.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**MEDIA DEL MODO \_ DE \_ MEDICIÓN \_ DE EXPOSICIÓN DE \_ WPD**
</dt> <dd>

Use la exposición media en toda la imagen.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**MEDIA PONDERADA DEL CENTRO DE MODO DE MEDICIÓN DE EXPOSICIÓN \_ DE \_ \_ \_ \_ \_ WPD**
</dt> <dd>

Use una exposición promedio, con el centro de la imagen dado más peso.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**MODO DE \_ MEDICIÓN \_ DE EXPOSICIÓN \_ WPD MULTI \_ \_ SPOT**
</dt> <dd>

Use una técnica de promedio de varios puntos.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**PUNTO CENTRAL DEL MODO DE \_ \_ MEDICIÓN \_ DE EXPOSICIÓN \_ DE \_ WPD**
</dt> <dd>

Use una técnica de promedio de punto central.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Indica el modo de medición del dispositivo. Esta enumeración la usa la propiedad [ \_ WPD STILL \_ IMAGE EXPOSURE \_ \_ METERING \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




