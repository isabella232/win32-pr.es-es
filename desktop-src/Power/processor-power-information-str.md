---
description: Contiene información sobre un procesador.
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: Estructura de PROCESSOR_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROCESSOR_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 500a346080d7bf0c44d392a63a71310db74225a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360696"
---
# <a name="processor_power_information-structure"></a>Estructura de información de \_ energía del procesador \_

Contiene información sobre un procesador.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PROCESSOR_POWER_INFORMATION {
  ULONG Number;
  ULONG MaxMhz;
  ULONG CurrentMhz;
  ULONG MhzLimit;
  ULONG MaxIdleState;
  ULONG CurrentIdleState;
} PROCESSOR_POWER_INFORMATION, *PPROCESSOR_POWER_INFORMATION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Number**
</dt> <dd>

El número de procesador del sistema.

</dd> <dt>

**MaxMhz**
</dt> <dd>

La frecuencia de reloj máxima especificada del procesador del sistema, en megahercios.

</dd> <dt>

**CurrentMhz**
</dt> <dd>

Frecuencia del reloj del procesador, en megahercios. Este número es la frecuencia máxima del reloj del procesador multiplicada por la limitación actual del procesador.

</dd> <dt>

**MhzLimit**
</dt> <dd>

Límite de la frecuencia del reloj del procesador, en megahercios. Este número es la frecuencia de reloj de procesador máxima especificada multiplicada por el límite de aceleración térmica del procesador actual.

</dd> <dt>

**MaxIdleState**
</dt> <dd>

El estado de inactividad máximo de este procesador.

</dd> <dt>

**CurrentIdleState**
</dt> <dd>

Estado de inactividad actual de este procesador.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que esta definición de estructura se omitió accidentalmente en Winnt. h. Este error se corregirá en el futuro. Mientras tanto, para compilar la aplicación, incluya la definición de la estructura contenida en este tema en el código fuente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




