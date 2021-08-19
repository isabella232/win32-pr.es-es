---
description: La estructura ANDEXP contiene una matriz de coincidencias de patrón utilizadas para evaluar los datos de fotogramas.
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: Estructura ANDEXP (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ANDEXP
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7ee2ac65e10e0dc9be46ab103fe21abcc78dc403302b298f3eb2fc83000802cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982957"
---
# <a name="andexp-structure"></a>Estructura ANDEXP

La **estructura ANDEXP** contiene una matriz de coincidencias de patrón utilizadas para evaluar los datos de fotogramas.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _ANDEXP {
  DWORD        nPatternMatches;
  PATTERNMATCH PatternMatch[MAX_PATTERNS];
} ANDEXP, *LPANDEXP;
```



## <a name="members"></a>Miembros

<dl> <dt>

**nPatternMatches**
</dt> <dd>

Número de coincidencias de patrón.

</dd> <dt>

**PatternMatch**
</dt> <dd>

Matriz de elementos de coincidencia de patrón. Tenga en cuenta que **cada estructura ANDEXP** puede contener hasta cuatro elementos de coincidencia de patrón. Para obtener más información sobre este miembro, vea [Filtros de captura](capture-filters.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los patrones de la matriz **PatternMatch** MAX PATTERNS se unen como elementos del mismo nivel en \[ instrucciones OR \_ \] lógicas con el formato

(Patrón 1 \| \| Patrón 2 \| \| Patrón 3).

Para obtener más información sobre cómo implementar esta estructura, vea [Capturar filtros](capture-filters.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




