---
description: El \_ tipo de enumeración de valores de equilibrio de blanco de WPD \_ \_ describe cómo un dispositivo de vídeo o imagen pondera los canales de color para lograr un equilibrio de blanco adecuado.
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: Enumeración WPD_WHITE_BALANCE_SETTINGS (PortableDevice. h)
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
ms.openlocfilehash: 06e607acc06ed00cc9fe91670650caee44c30430
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649731"
---
# <a name="wpd_white_balance_settings-enumeration"></a>\_ \_ Enumeración de valores de equilibrio de blanco de WPD \_

El tipo de enumeración de valores de equilibrio de blanco de WPD describe cómo un dispositivo de vídeo o imagen pondera los canales de color para lograr un equilibrio de blanco adecuado. **\_ \_ \_**

## <a name="syntax"></a>Sintaxis


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

<span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**\_balance blanco de WPD \_ \_ sin definir**
</dt> <dd>

Este valor no se ha definido.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**\_manual de \_ balance \_ blanco de WPD**
</dt> <dd>

El balance de blanco se establece explícitamente mediante la propiedad de [ \_ \_ ganancia de imagen \_ RGB \_ ](still-image-properties.md) de la imagen de carga continua de WPD y no cambiará.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**\_balance blanco de WPD \_ \_ automático**
</dt> <dd>

El dispositivo establecerá el balance de blanco.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**equilibrio de blanco de WPD \_ en \_ \_ una \_ instalación \_ automática**
</dt> <dd>

El dispositivo establecerá el balance de blanco, pero solo cuando el usuario inserte el botón de captura del dispositivo mientras dirige el dispositivo a un campo en blanco.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**\_verano de \_ balance \_ blanco de WPD**
</dt> <dd>

El dispositivo usará los números de balance de blanco adecuados para su uso en la mayoría de los valores de horario de verano.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**\_Tungsten de \_ equilibrio de blanco de WPD \_**
</dt> <dd>

El dispositivo usará los números de balance de blanco adecuados para su uso en la mayoría de los valores de iluminación de la luz de los interiores.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**BALANCE de blanco de WPD \_ en \_ \_ Flash**
</dt> <dd>

El dispositivo usará los números de balance de blanco adecuados para su uso con un flash.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración se usa en la propiedad de equilibrio de blancos de la imagen de la [ \_ \_ imagen \_ \_ ](still-image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




