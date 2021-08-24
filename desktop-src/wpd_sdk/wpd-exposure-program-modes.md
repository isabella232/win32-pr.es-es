---
description: El tipo de enumeración WPD EXPOSURE PROGRAM MODES describe un modo de exposición que se usará al \_ capturar imágenes con un \_ \_ dispositivo.
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: WPD_EXPOSURE_PROGRAM_MODES enumeración (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_PROGRAM_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: dc64012c4f13f84abef55d2426c856b931eb447e61df4f04c69781c089857930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083279"
---
# <a name="wpd_exposure_program_modes-enumeration"></a>Enumeración WPD \_ EXPOSURE \_ PROGRAM \_ MODES

El **tipo de \_ enumeración WPD EXPOSURE \_ PROGRAM \_ MODES** describe un modo de exposición que se usará al capturar imágenes con un dispositivo.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_EXPOSURE_PROGRAM_MODES { 
  WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED          = 0,
  WPD_EXPOSURE_PROGRAM_MODE_MANUAL             = 1,
  WPD_EXPOSURE_PROGRAM_MODE_AUTO               = 2,
  WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY  = 3,
  WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY   = 4,
  WPD_EXPOSURE_PROGRAM_MODE_CREATIVE           = 5,
  WPD_EXPOSURE_PROGRAM_MODE_ACTION             = 6,
  WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT           = 7
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**MODO DE PROGRAMA DE EXPOSICIÓN DE WPD \_ \_ SIN \_ \_ DEFINIR**
</dt> <dd>

No se ha especificado el modo de exposición.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**MANUAL DEL \_ MODO DE PROGRAMA DE EXPOSICIÓN \_ \_ DE \_ WPD**
</dt> <dd>

La aplicación debe especificar toda la configuración de exposición.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**MODO AUTOMÁTICO \_ DEL PROGRAMA DE EXPOSICIÓN \_ \_ WPD \_**
</dt> <dd>

Use un modo de exposición automática definido por el dispositivo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**PRIORIDAD DE APERTURA \_ DEL MODO DE EXPOSICIÓN \_ \_ DE \_ \_ WPD**
</dt> <dd>

Modo de exposición automatizado que indica que el valor de la apertura de la lente debe permanecer fijo, pero el dispositivo debe determinar la velocidad de obturación.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**PRIORIDAD DE PRIORIDAD DE \_ PRIORIDAD DEL PROGRAMA DE \_ \_ \_ \_ EXPOSICIÓN DE WPD**
</dt> <dd>

Un modo de exposición automatizado que indica que la velocidad de obturación debe permanecer fija, pero el dispositivo debe determinar esa apertura de la lente.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**WPD \_ EXPOSURE \_ PROGRAM \_ MODE \_ CREATIVE**
</dt> <dd>

Modo de exposición automatizado que intenta maximizar la profundidad de campo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**ACCIÓN DEL \_ MODO DE PROGRAMA DE EXPOSICIÓN DE \_ \_ \_ WPD**
</dt> <dd>

Modo de exposición automatizado que intenta maximizar la velocidad de obturación.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**WPD \_ EXPOSURE \_ PROGRAM \_ MODE \_ PORTRAIT**
</dt> <dd>

Modo de exposición automatizado que especifica una profundidad de campo relativamente superficial.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Indica el modo de programa de exposición del dispositivo. Esta enumeración la usa la [propiedad \_ WPD STILL \_ IMAGE EXPOSURE \_ PROGRAM \_ \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




