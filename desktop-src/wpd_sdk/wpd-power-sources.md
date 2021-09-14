---
description: El tipo de \_ enumeración WPD POWER \_ SOURCES describe la fuente de alimentación que usa un dispositivo.
ms.assetid: feebf213-052d-4315-84db-2109cab5f179
title: WPD_POWER_SOURCES enumeración (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262044"
---
# <a name="wpd_power_sources-enumeration"></a>Enumeración \_ DE WPD POWER \_ SOURCES

El **tipo de \_ enumeración WPD POWER \_ SOURCES** describe la fuente de alimentación que usa un dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**BATERÍA DE FUENTE \_ DE \_ ALIMENTACIÓN \_ WPD**
</dt> <dd>

La fuente de alimentación del dispositivo es una batería.

</dd> <dt>

<span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**WPD \_ POWER \_ SOURCE \_ EXTERNAL**
</dt> <dd>

El dispositivo usa una fuente de alimentación externa.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración la usa la [propiedad \_ WPD DEVICE \_ POWER \_ SOURCE.](device-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




