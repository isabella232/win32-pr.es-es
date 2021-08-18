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
ms.openlocfilehash: 0e0135a6210aebbca38bfdede00231315dd2680461f366930b24925eda830604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063725"
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



## <a name="members"></a>Miembros

<dl> <dt>

**MinValue**
</dt> <dd>

Valor más bajo posible en un intervalo.

</dd> <dt>

**MaxValue**
</dt> <dd>

Valor más alto posible en un intervalo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura RANGE** se usa para especificar un intervalo válido de números para una propiedad de protocolo. Si el **miembro DataQualifier** de la estructura **PROPERTYINFO** se establece en **PROP QUAL \_ \_ RANGE**, el miembro **lpRange** de la estructura [PROPERTYINFO](propertyinfo.md) debe proporcionar un puntero a una **estructura RANGE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propertyinfo](propertyinfo.md)
</dt> </dl>

 

 




