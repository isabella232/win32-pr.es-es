---
title: MPSTATUS_DATA estructura (MpClient.h)
description: Contiene datos sobre el estado actual de un componente del producto.
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- MPSTATUS_DATA estructura heredada de Windows environment
- PMPSTATUS_DATA puntero de estructura heredado Windows características del entorno de ejecución
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
ms.openlocfilehash: 78989b055e6de79c3da733ff8bc498a3fb6717c5dec226db73b80c4e5c9d899c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887915"
---
# <a name="mpstatus_data-structure"></a>Estructura DE DATOS DE MPSTATUS \_

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

Tipo: **[ **MPCOMPONENT \_ ID**](mpcomponent-id.md)**

</dd> <dd>

Identificador de componente específico para el que se notifica el estado.

</dd> <dt>

**fEnable**
</dt> <dd>

Tipo: **BOOL**

</dd> <dd>

Estado solicitado para el componente. **hResult en** los datos de devolución de llamada significa que la solicitud se ha completado correctamente o no.

</dd> <dt>

**ComponentStatus**
</dt> <dd>

Datos de estado adicionales según el valor de **ComponentID.**

> [!Note]  
> Actualmente, da como resultado un puntero a una estructura ficticia para todos los valores posibles de **ComponentID**.

 

<dl> <dt>

**p1**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ AS \_ SIGNATURE**. Vea [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p2**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ AV \_ SIGNATURE**. Vea [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p3**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ REALTIME \_ MONITOR**. Vea [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p4**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ ONACCESS \_ PROTECTION**. Vea [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p5**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ \_ IOAV PROTECTION**. Vea [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p6**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ BEHAVIOR \_ MONITOR**. Vea [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p7**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ AUTO \_ SCAN**. Vea [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p8**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ AUTO \_ SIGUPDATE**. Vea [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**p9**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ IPC**. Vea [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**Pa**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ NIS**. Vea [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> <dt>

**pb**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX \_ UNUSED**

</dd> <dd>

Cuando **ComponentID**  ==  **MPCOMPONENT \_ ELAM**. Vea [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Id. de \_ MPCOMPONENT**](mpcomponent-id.md)
</dt> <dt>

[**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





