---
description: El tipo de enumeración WPD WHITE BALANCE SETTINGS describe cómo un dispositivo de vídeo o imagen pondera los canales de \_ color para lograr un equilibrio de blanco \_ \_ adecuado.
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: WPD_WHITE_BALANCE_SETTINGS enumeración (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_WHITE_BALANCE_SETTINGS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1b596dd6d8fbcc2b2a875b70d80e8eb4040c966590642a004c551ec159c9f5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842052"
---
# <a name="wpd_white_balance_settings-enumeration"></a>Enumeración \_ WPD WHITE \_ BALANCE \_ SETTINGS

El **tipo de \_ enumeración WPD WHITE \_ BALANCE \_ SETTINGS** describe cómo un dispositivo de vídeo o imagen pondera los canales de color para lograr un equilibrio de blanco adecuado.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_WHITE_BALANCE_SETTINGS { 
  WPD_WHITE_BALANCE_UNDEFINED           = 0,
  WPD_WHITE_BALANCE_MANUAL              = 1,
  WPD_WHITE_BALANCE_AUTOMATIC           = 2,
  WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC  = 3,
  WPD_WHITE_BALANCE_DAYLIGHT            = 4,
  WPD_WHITE_BALANCE_TUNGSTEN            = 5,
  WPD_WHITE_BALANCE_FLASH               = 6
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**WPD \_ WHITE \_ BALANCE \_ UNDEFINED**
</dt> <dd>

Este valor no se ha definido.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**MANUAL DE \_ EQUILIBRIO DE BLANCO DE \_ \_ WPD**
</dt> <dd>

El equilibrio de blanco se establece explícitamente mediante la propiedad [ \_ WPD STILL \_ IMAGE RGB \_ \_ GAIN](still-image-properties.md) y no cambiará por sí mismo.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**WPD \_ WHITE \_ BALANCE \_ AUTOMATIC**
</dt> <dd>

El dispositivo establecerá el saldo blanco.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**WPD \_ WHITE \_ BALANCE \_ ONE \_ PUSH \_ AUTOMATIC**
</dt> <dd>

El dispositivo establecerá el equilibrio de blanco, pero solo cuando el usuario presione el botón de captura del dispositivo mientras apunta el dispositivo a un campo blanco.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD \_ WHITE \_ BALANCE \_ DAYLIGHT**
</dt> <dd>

El dispositivo usará números de saldo blanco adecuados para su uso en la mayoría de las configuraciones de verano.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD \_ WHITE \_ BALANCE \_ TUNGSTEN**
</dt> <dd>

El dispositivo usará números de saldo blanco adecuados para su uso en la mayoría de las configuraciones de iluminación incandescentes interiores.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**WPD \_ WHITE \_ BALANCE \_ FLASH**
</dt> <dd>

El dispositivo usará números de saldo blanco adecuados para su uso con un flash.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta enumeración la usa la [propiedad \_ WPD STILL \_ IMAGE WHITE \_ \_ BALANCE.](still-image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




