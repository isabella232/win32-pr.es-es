---
description: Contiene información sobre un procesador.
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: PROCESSOR_POWER_INFORMATION estructura
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
ms.openlocfilehash: 3bdb6a3bb8ae5b768c42609817c76934c203989ba6dea665fc6cc0a6896659de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143338"
---
# <a name="processor_power_information-structure"></a>ESTRUCTURA \_ DE INFORMACIÓN DE POTENCIA DEL \_ PROCESADOR

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

Número de procesador del sistema.

</dd> <dt>

**MaxMhz**
</dt> <dd>

Frecuencia de reloj máxima especificada del procesador del sistema, en megahercios.

</dd> <dt>

**CurrentMhz**
</dt> <dd>

Frecuencia del reloj del procesador, en megahercios. Este número es la frecuencia máxima de reloj del procesador especificada multiplicada por la limitación del procesador actual.

</dd> <dt>

**MhzLimit**
</dt> <dd>

Límite de la frecuencia del reloj del procesador, en megahercios. Este número es la frecuencia máxima especificada del reloj del procesador multiplicada por el límite térmico del procesador actual.

</dd> <dt>

**MaxIdleState**
</dt> <dd>

Estado de inactividad máximo de este procesador.

</dd> <dt>

**CurrentIdleState**
</dt> <dd>

Estado de inactividad actual de este procesador.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Tenga en cuenta que esta definición de estructura se omitió accidentalmente de WinNT.h. Este error se corregirá en el futuro. Mientras tanto, para compilar la aplicación, incluya la definición de estructura contenida en este tema en el código fuente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




