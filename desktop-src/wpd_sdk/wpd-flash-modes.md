---
description: El tipo de enumeración WPD FLASH MODES describe un modo flash que se usará \_ al capturar imágenes con un \_ dispositivo.
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: WPD_FLASH_MODES enumeración (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FLASH_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 72e9b6cb2b52f1d90c584b6f425711769b25ea0c5d44065b5aa377d2811592e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005925"
---
# <a name="wpd_flash_modes-enumeration"></a>Enumeración WPD \_ FLASH \_ MODES

El **tipo de enumeración \_ \_ WPD FLASH MODES** describe un modo flash que se usará al capturar imágenes con un dispositivo.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_FLASH_MODES { 
  WPD_FLASH_MODE_UNDEFINED      = 0,
  WPD_FLASH_MODE_AUTO           = 1,
  WPD_FLASH_MODE_OFF            = 2,
  WPD_FLASH_MODE_FILL           = 3,
  WPD_FLASH_MODE_RED_EYE_AUTO   = 4,
  WPD_FLASH_MODE_RED_EYE_FILL   = 5,
  WPD_FLASH_MODE_EXTERNAL_SYNC  = 6
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**MODO \_ FLASH WPD \_ \_ SIN DEFINIR**
</dt> <dd>

No se ha especificado ningún modo flash.

</dd> <dt>

<span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**MODO \_ FLASH WPD \_ \_ AUTO**
</dt> <dd>

Especifica que el flash debe usarse en el modo automático, tal y como especifica el dispositivo.

</dd> <dt>

<span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**MODO \_ FLASH WPD \_ \_ DESACTIVADO**
</dt> <dd>

Especifica que no se debe usar flash.

</dd> <dt>

<span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**RELLENO DEL \_ MODO FLASH \_ WPD \_**
</dt> <dd>

Especifica un flash de tipo de relleno.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**WPD \_ FLASH \_ MODE \_ RED \_ EYE \_ AUTO**
</dt> <dd>

Especifica que se debe usar el flash de reducción de ojos rojos.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**RELLENO DE LOS OJOS \_ ROJOS EN MODO FLASH \_ \_ \_ \_ WPD**
</dt> <dd>

Especifica que se debe usar el flash de relleno de los ojos rojos.

</dd> <dt>

<span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**SINCRONIZACIÓN EXTERNA DEL MODO FLASH WPD \_ \_ \_ \_**
</dt> <dd>

Especifica que el flash debe sincronizarse con otros dispositivos flash externos.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta enumeración la usa la propiedad [ \_ WPD STILL \_ IMAGE FLASH \_ \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




