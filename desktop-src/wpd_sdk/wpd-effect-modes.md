---
description: El \_ tipo de enumeración de modos de efecto de WPD \_ describe varios efectos visuales que se pueden aplicar a una imagen.
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: Enumeración WPD_EFFECT_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EFFECT_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7e29f89207a74d335fbe1c2561f8dcf9cec3e923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698525"
---
# <a name="wpd_effect_modes-enumeration"></a>\_Enumeración de modos de efecto de WPD \_

El tipo de enumeración de **\_ \_ modos de efecto de WPD** describe varios efectos visuales que se pueden aplicar a una imagen.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WPD_EFFECT_MODES { 
  WPD_EFFECT_MODE_UNDEFINED        = 0,
  WPD_EFFECT_MODE_COLOR            = 1,
  WPD_EFFECT_MODE_BLACK_AND_WHITE  = 2,
  WPD_EFFECT_MODE_SEPIA            = 3
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**modo de efecto de WPD \_ \_ \_ sin definir**
</dt> <dd>

No se ha especificado ningún efecto.

</dd> <dt>

<span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**\_color del \_ modo de efecto de WPD \_**
</dt> <dd>

La imagen debe ser de color.

</dd> <dt>

<span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**\_ \_ modo de efecto \_ \_ de WPD \_ en blanco y negro**
</dt> <dd>

La imagen debe estar en blanco y negro.

</dd> <dt>

<span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**modo de efecto de WPD \_ \_ \_ sepia**
</dt> <dd>

La imagen debe ser sepia.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración la usa la propiedad de [ \_ modo de \_ \_ efecto \_ de imagen de WPD](still-image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




