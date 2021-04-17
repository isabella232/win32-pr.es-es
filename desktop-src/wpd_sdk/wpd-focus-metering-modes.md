---
description: El \_ tipo de enumeración de modos de medición de foco de WPD describe el modo en que \_ \_ un dispositivo debe decidir qué parte de un marco se va a usar para establecer el foco.
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: Enumeración WPD_FOCUS_METERING_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f59d6a2f1cabbbe7b072a87caa3e5d74d012fc49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671012"
---
# <a name="wpd_focus_metering_modes-enumeration"></a>\_ \_ Enumeración de modos de medición de foco de WPD \_

El tipo de enumeración de modos de medición de foco de WPD describe el modo en que un dispositivo debe decidir qué parte de un marco se va a usar para establecer el foco. **\_ \_ \_**

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WPD_FOCUS_METERING_MODES { 
  WPD_FOCUS_METERING_MODE_UNDEFINED    = 0,
  WPD_FOCUS_METERING_MODE_CENTER_SPOT  = 1,
  WPD_FOCUS_METERING_MODE_MULTI_SPOT   = 2
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**modo de medición de foco de WPD \_ \_ \_ \_ sin definir**
</dt> <dd>

Indica que no se ha especificado ningún modo de enfoque.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**\_zona del \_ centro del \_ modo \_ de \_ medición de foco de WPD**
</dt> <dd>

Se centra en el centro del área de fotogramas.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**modo de medición de foco de WPD \_ \_ \_ \_ \_ multispot**
</dt> <dd>

Determine el foco analizando varias partes del área de marco.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración se especifica mediante la propiedad del [modo de medición de \_ \_ \_ foco de \_ \_ imagen de WPD](still-image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




