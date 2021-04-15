---
description: El \_ tipo de \_ enumeración fuentes de alimentación de WPD describe la fuente de alimentación que usa un dispositivo.
ms.assetid: feebf213-052d-4315-84db-2109cab5f179
title: Enumeración WPD_POWER_SOURCES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_POWER_SOURCES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bf9a153d4d41a64b639f796ea2ba0eeb9e567a32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649602"
---
# <a name="wpd_power_sources-enumeration"></a>\_Enumeración de fuentes de alimentación de WPD \_

El tipo de enumeración **\_ \_ fuentes de alimentación de WPD** describe la fuente de alimentación que usa un dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**\_batería de \_ fuente de alimentación de WPD \_**
</dt> <dd>

La fuente de alimentación del dispositivo es una batería.

</dd> <dt>

<span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**fuente de alimentación de WPD \_ \_ \_ externa**
</dt> <dd>

El dispositivo usa una fuente de alimentación externa.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración la usa la [propiedad \_ \_ \_ origen de energía del dispositivo WPD](device-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




