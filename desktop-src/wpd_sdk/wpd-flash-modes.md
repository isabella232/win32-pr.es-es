---
description: El \_ tipo de \_ enumeración de modos Flash de WPD describe un modo flash que se usa al capturar imágenes con un dispositivo.
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: Enumeración WPD_FLASH_MODES (PortableDevice. h)
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
ms.openlocfilehash: 09a2a5b95e86d9d17267cafcfbf723e734ffc74f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671013"
---
# <a name="wpd_flash_modes-enumeration"></a>\_Enumeración de modos de Flash de WPD \_

El tipo de enumeración de **\_ \_ modos Flash de WPD** describe un modo flash que se usa al capturar imágenes con un dispositivo.

## <a name="syntax"></a>Sintaxis


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

<span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**\_modo Flash de WPD \_ \_ sin definir**
</dt> <dd>

No se ha especificado ningún modo flash.

</dd> <dt>

<span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**modo de Flash de WPD \_ \_ \_ auto**
</dt> <dd>

Especifica que el flash debe usarse en el modo automático, según lo especificado por el dispositivo.

</dd> <dt>

<span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**\_modo Flash de WPD \_ \_ desactivado**
</dt> <dd>

Especifica que no debe usarse Flash.

</dd> <dt>

<span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**\_relleno en \_ modo \_ Flash de WPD**
</dt> <dd>

Especifica un destello de tipo de relleno.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**\_modo Flash de la \_ \_ vista en color rojo \_ \_ de WPD**
</dt> <dd>

Especifica que debe usarse el Flash de reducción de ojos rojos.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**\_color de \_ \_ ojos rojos \_ del modo Flash de WPD \_**
</dt> <dd>

Especifica que debe usarse el parpadeo de relleno de ojos rojos.

</dd> <dt>

<span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**\_ \_ sincronización externa en modo flash \_ de \_ WPD**
</dt> <dd>

Especifica que el flash se debe sincronizar con otros dispositivos flash externos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración se usa en la propiedad de [ \_ \_ \_ \_ modo flash](still-image-properties.md) de la imagen de WPD.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




