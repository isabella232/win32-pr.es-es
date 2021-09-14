---
description: El tipo de \_ enumeración WPD EFFECT \_ MODES describe varios efectos visuales que se pueden aplicar a una imagen.
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: WPD_EFFECT_MODES enumeración (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262052"
---
# <a name="wpd_effect_modes-enumeration"></a>Enumeración \_ WPD EFFECT \_ MODES

El **tipo de \_ enumeración \_ WPD EFFECT MODES** describe varios efectos visuales que se pueden aplicar a una imagen.

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

<span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**MODO DE \_ EFECTO \_ WPD \_ SIN DEFINIR**
</dt> <dd>

No se ha especificado ningún efecto.

</dd> <dt>

<span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**COLOR DEL MODO \_ \_ DE EFECTO \_ WPD**
</dt> <dd>

La imagen debe ser de color.

</dd> <dt>

<span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**MODO DE \_ EFECTO \_ WPD \_ EN BLANCO \_ Y \_ NEGRO**
</dt> <dd>

La imagen debe ser en blanco y negro.

</dd> <dt>

<span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**SEPIA DEL \_ MODO \_ DE EFECTO \_ WPD**
</dt> <dd>

La imagen debe ser sepia.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración la usa la propiedad [ \_ WPD STILL \_ IMAGE EFFECT \_ \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




