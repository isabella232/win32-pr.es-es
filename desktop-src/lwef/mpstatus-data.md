---
title: MPSTATUS_DATA estructura (MpClient. h)
description: Contiene datos sobre el estado actual de un componente del producto.
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- MPSTATUS_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPSTATUS_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPSTATUS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5da4ea9c8c51d8ee74d3242e5020df23f758228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802876"
---
# <a name="mpstatus_data-structure"></a>\_Estructura de datos MPSTATUS

Contiene datos sobre el estado actual de un componente del producto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPSTATUS_DATA {
  MPCOMPONENT_ID ComponentID;
  BOOL           fEnable;
  union {
    PMPSTATUS_DATAEX_UNUSED p1;
    PMPSTATUS_DATAEX_UNUSED p2;
    PMPSTATUS_DATAEX_UNUSED p3;
    PMPSTATUS_DATAEX_UNUSED p4;
    PMPSTATUS_DATAEX_UNUSED p5;
    PMPSTATUS_DATAEX_UNUSED p6;
    PMPSTATUS_DATAEX_UNUSED p7;
    PMPSTATUS_DATAEX_UNUSED p8;
    PMPSTATUS_DATAEX_UNUSED p9;
    PMPSTATUS_DATAEX_UNUSED pa;
    PMPSTATUS_DATAEX_UNUSED pb;
  } ComponentStatus;
} MPSTATUS_DATA, *PMPSTATUS_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ComponentID**
</dt> <dd>

Tipo: **[ **\_ ID. de MPCOMPONENT**](mpcomponent-id.md)**

</dd> <dd>

IDENTIFICADOR de componente específico para el que se ha comunicado el estado.

</dd> <dt>

**fEnable**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

Estado solicitado para el componente. **hResult** en los datos de devolución de llamada indica si la solicitud se ha realizado correctamente o no.

</dd> <dt>

**ComponentStatus**
</dt> <dd>

Datos de estado adicionales en función del valor de **ComponentID**.

> [!Note]  
> En la actualidad, da como resultado un puntero a una estructura ficticia para todos los valores posibles de **ComponentID**.

 

<dl> <dt>

**P1**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ no usado**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ como \_ Signature**. Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).

</dd> <dt>

**P2**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ no usado**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ AV \_ Signature**. Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).

</dd> <dt>

**P3**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ no usado**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ \_ monitor en tiempo real**. Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).

</dd> <dt>

**P4**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ no usado**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT la \_ \_ protección de acceso**. Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).

</dd> <dt>

**P5**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ no usado**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ IOAV \_ PROTECTION**. Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).

</dd> <dt>

**microarquitectura**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ no usado**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ Behavior \_ monitor**. Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).

</dd> <dt>

**P7**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ no usado**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ se \_ examina automáticamente**. Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).

</dd> <dt>

**P8**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ no usado**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ \_ SIGUPDATE**. Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).

</dd> <dt>

**P9**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ no usado**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ IPC**. Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).

</dd> <dt>

**Pennsylvania**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ no usado**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ NIS**. Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).

</dd> <dt>

**PB**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ no usado**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ Elam**. Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**identificador de MPCOMPONENT \_**](mpcomponent-id.md)
</dt> <dt>

[**MPSTATUS \_ DATAEX \_ no usado**](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





