---
description: Contiene un grupo de matrices ANDEXP evaluadas como elementos del mismo nivel.
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: Estructura EXPRESSION (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPRESSION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4efa1f79477e3dcc13bedfddb2cdca7fd660f5430b7d7f2b87dbd9d4b4425098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366843"
---
# <a name="expression-structure"></a>Estructura EXPRESSION

La **estructura EXPRESSION** contiene un grupo de matrices **ANDEXP** evaluadas como elementos del mismo nivel en expresiones AND lógicas, que tienen el formato

(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _EXPRESSION {
  DWORD  nAndExps;
  ANDEXP AndExp[MAX_PATTERNS];
} EXPRESSION, *LPEXPRESSION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**nAndExps**
</dt> <dd>

Número de **patrones ANDEXP.**

</dd> <dt>

**AndExp**
</dt> <dd>

Matriz de **patrones ANDEXP.** El filtro de captura organiza todas las filas de esta matriz como instrucciones AND lógicas. Tenga en cuenta que cada estructura EXPRESSION puede contener un máximo de cuatro **patrones ANDEXP.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para obtener más información sobre cómo implementar esta estructura como parte de un filtro de captura, vea [Filtros de captura](capture-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




