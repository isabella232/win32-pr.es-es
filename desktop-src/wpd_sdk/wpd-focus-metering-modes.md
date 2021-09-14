---
description: El tipo de enumeración WPD FOCUS METERING MODES describe cómo un dispositivo debe decidir qué parte de un fotograma usar \_ \_ para establecer el \_ foco.
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: WPD_FOCUS_METERING_MODES enumeración (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266791"
---
# <a name="wpd_focus_metering_modes-enumeration"></a>Enumeración \_ WPD FOCUS \_ METERING \_ MODES

El **tipo de \_ enumeración WPD FOCUS \_ METERING \_ MODES** describe cómo un dispositivo debe decidir qué parte de un fotograma usar para establecer el foco.

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

<span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**MODO DE \_ \_ MEDICIÓN DE \_ FOCO WPD \_ SIN DEFINIR**
</dt> <dd>

Indica que no se ha especificado ningún modo de enfoque.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**PUNTO CENTRAL DEL MODO DE \_ \_ \_ MEDICIÓN DE FOCO \_ WPD \_**
</dt> <dd>

Se centra en el centro del área enmarcada.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**MODO DE \_ \_ MEDICIÓN DE \_ FOCO WPD \_ MULTI \_ SPOT**
</dt> <dd>

Determine el foco mediante el análisis de varias partes del área enmarcada.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración se especifica mediante la propiedad [ \_ WPD STILL \_ IMAGE FOCUS \_ \_ METERING \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




