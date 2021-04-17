---
description: El \_ tipo de \_ enumeración modos del programa de exposición de WPD \_ describe un modo de exposición que se usa al capturar imágenes con un dispositivo.
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: Enumeración WPD_EXPOSURE_PROGRAM_MODES (PortableDevice. h)
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
ms.openlocfilehash: a88ce90bb9e776cd45245b32a363635c2ccf0560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680386"
---
# <a name="wpd_exposure_program_modes-enumeration"></a>\_ \_ Enumeración de modos de programa de exposición de WPD \_

El tipo de enumeración modos del programa de exposición de WPD describe un modo de exposición que se usa al capturar imágenes con un dispositivo. **\_ \_ \_**

## <a name="syntax"></a>Sintaxis


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

<span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**modo de programa de exposición de WPD \_ \_ \_ \_ sin definir**
</dt> <dd>

No se ha especificado el modo de exposición.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**\_manual del \_ modo de programa de exposición de WPD \_ \_**
</dt> <dd>

La aplicación debe especificar toda la configuración de exposición.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**modo de programa de exposición de WPD \_ \_ \_ \_ auto**
</dt> <dd>

Use un modo de exposición automática definido por el dispositivo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**\_prioridad de \_ abertura del modo de programa de exposición de \_ \_ WPD \_**
</dt> <dd>

Un modo de exposición automatizada que indica que el valor de apertura de la lente debe permanecer fijo, pero el dispositivo debe determinar la velocidad del obturador.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**\_prioridad de \_ \_ \_ obturador del \_ modo de exposición de WPD**
</dt> <dd>

Un modo de exposición automatizada que indica que la velocidad del obturador debe permanecer fija, pero el dispositivo debe determinar la abertura del objetivo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**\_creatividad del \_ modo de programa de exposición de WPD \_ \_**
</dt> <dd>

Modo de exposición automatizada que intenta maximizar la profundidad del campo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**\_acción del \_ modo de programa de exposición de WPD \_ \_**
</dt> <dd>

Modo de exposición automatizada que intenta maximizar la velocidad del obturador.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**modo de programa de exposición de WPD \_ \_ \_ \_ vertical**
</dt> <dd>

Modo de exposición automatizada que especifica una profundidad relativamente superficial de campo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Indica el modo del programa de exposición del dispositivo. Esta enumeración se usa en la propiedad del [modo de programa de \_ \_ exposición de imagen \_ \_ \_ estática de WPD](still-image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




