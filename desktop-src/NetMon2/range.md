---
description: La estructura RANGE define un intervalo de valores de propiedad válidos.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: Estructura de intervalo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RANGE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: bf465636f315e60e43350bb370e2002b8a96e635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666989"
---
# <a name="range-structure"></a>Estructura de rango

La estructura **Range** define un intervalo de valores de propiedad válidos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**MinValue**
</dt> <dd>

Menor valor posible de un intervalo.

</dd> <dt>

**MaxValue**
</dt> <dd>

Mayor valor posible de un intervalo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura de **intervalo** se usa para especificar un intervalo válido de números para una propiedad de protocolo. Si el miembro de **Qualifier** de la estructura **PropertyInfo** está establecido en **props \_ \_ Range**, el miembro **lpRange** de la estructura [PropertyInfo](propertyinfo.md) debe proporcionar un puntero a una estructura de **intervalo** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 




