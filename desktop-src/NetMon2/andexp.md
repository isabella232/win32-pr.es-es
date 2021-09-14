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
ms.openlocfilehash: 1d27d5bdd51a45b31f518271053f44b45917cdeb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074167"
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



## <a name="members"></a>Members

<dl> <dt>

**nPatternMatches**
</dt> <dd>

Número de coincidencias de patrón.

</dd> <dt>

**PatternMatch**
</dt> <dd>

Matriz de elementos de coincidencia de patrón. Tenga en cuenta que **cada estructura ANDEXP** puede contener hasta cuatro elementos de coincidencia de patrón. Para obtener más información sobre este miembro, vea [Filtros de captura](capture-filters.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los patrones de la matriz **PatternMatch** MAX PATTERNS se unen como elementos del mismo nivel en \[ instrucciones OR \_ \] lógicas con el formato

(Patrón 1 \| \| Patrón 2 \| \| Patrón 3).

Para obtener más información sobre cómo implementar esta estructura, vea [Capturar filtros](capture-filters.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




