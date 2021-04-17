---
description: Almacena información sobre las secciones de la memoria compartida.
ms.assetid: 73a650ee-110c-43f2-a5e2-783d52fd29ee
title: Estructura de SHAREDMEMORY_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHAREDMEMORY_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 695f3ef09cb5e7e67de757ee3926df6fde7ddff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678155"
---
# <a name="sharedmemory_header-structure"></a>\_Estructura del encabezado SHAREDMEMORY

Almacena información sobre las secciones de la memoria compartida.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SHAREDMEMORY_HEADER {
  DWORD             cbTotal;
  DWORD             cbOffsetSns;
  DWORD             idxEvent;
  DWORD             dwEvent;
  CURSOR_ID         cid;
  DWORD             sn;
  SYSTEM_EVENT      sysEvt;
  SYSTEM_EVENT_DATA sysEvtData;
  DWORD             cPackets;
  DWORD             cbPackets;
  BOOL              fSnsPresent;
} SHAREDMEMORY_HEADER, *PSHAREDMEMORY_HEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbTotal**
</dt> <dd>

Tamaño, en bytes, de los datos a los que hace referencia esta estructura de encabezado.

</dd> <dt>

**cbOffsetSns**
</dt> <dd>

Tamaño, en bytes, que los números de serie se desplazan de la estructura de encabezado.

</dd> <dt>

**idxEvent**
</dt> <dd>

Índice del evento. Este valor se incrementa con eventos sucesivos.

</dd> <dt>

**dwEvent**
</dt> <dd>

Evento asociado a este encabezado.

</dd> <dt>

**Cid**
</dt> <dd>

Identificador de cursor al que hace referencia el encabezado de memoria compartida.

</dd> <dt>

**sn**
</dt> <dd>

Número de serie del encabezado de memoria compartida.

</dd> <dt>

**sysEvt**
</dt> <dd>

El evento del sistema, prefijo SE \_ \* asocia a este encabezado. Vea la sección Comentarios para obtener más información.

</dd> <dt>

**sysEvtData**
</dt> <dd>

La estructura de [**\_ \_ datos de eventos del sistema**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) asociada al evento del sistema.

</dd> <dt>

**cPackets**
</dt> <dd>

Un recuento de los paquetes asociados a la sección memoria compartida actual.

</dd> <dt>

**cbPackets**
</dt> <dd>

Tamaño, en bytes, de los paquetes asociados a la sección memoria compartida actual.

</dd> <dt>

**fSnsPresent**
</dt> <dd>

Marca que indica si los números de serie están presentes en la sección memoria compartida actual.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los siguientes valores se definen para el miembro **sysEvt** .


```C++
#define SE_NONE                  0x00000000
#define SE_TAP                   0x00000010
#define SE_DBL_TAP               0x00000011
#define SE_RIGHT_TAP             0x00000012
#define SE_DRAG                  0x00000013
#define SE_RIGHT_DRAG            0x00000014
#define SE_HOLD_ENTER            0x00000015
#define SE_HOLD_LEAVE            0x00000016
#define SE_HOVER_ENTER           0x00000017
#define SE_HOVER_LEAVE           0x00000018
#define SE_FLICK                 0x0000001F
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_datos de eventos del sistema \_**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 



