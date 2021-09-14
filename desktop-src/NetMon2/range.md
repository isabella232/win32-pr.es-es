---
description: La estructura RANGE define un intervalo de valores de propiedad válidos.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: Estructura RANGE (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362120"
---
# <a name="range-structure"></a>Estructura RANGE

La **estructura RANGE** define un intervalo de valores de propiedad válidos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a>Members

<dl> <dt>

**MinValue**
</dt> <dd>

Valor más bajo posible en un intervalo.

</dd> <dt>

**MaxValue**
</dt> <dd>

Valor más alto posible en un intervalo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **estructura RANGE** se usa para especificar un intervalo válido de números para una propiedad de protocolo. Si el **miembro DataQualifier** de la estructura **PROPERTYINFO** se establece en **PROP QUAL \_ \_ RANGE**, el miembro **lpRange** de la estructura [PROPERTYINFO](propertyinfo.md) debe proporcionar un puntero a una **estructura RANGE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 




