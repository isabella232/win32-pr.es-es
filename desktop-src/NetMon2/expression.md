---
description: Contiene un grupo de matrices ANDEXP evaluadas como pares.
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: Estructura de expresión (Netmon. h)
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
ms.openlocfilehash: b6565c294c0d8e0a7a277769404cb8b1b206380e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666293"
---
# <a name="expression-structure"></a>Estructura de expresión

La estructura **Expression** contiene un grupo de matrices **ANDEXP** evaluadas como elementos del mismo nivel en expresiones y lógicas, que tienen el formato

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

Número de patrones de **ANDEXP** .

</dd> <dt>

**AndExp**
</dt> <dd>

Matriz de patrones de **ANDEXP** . El filtro de captura organiza todas las filas de esta matriz como instrucciones y lógicas. Tenga en cuenta que cada estructura de expresión puede contener un máximo de cuatro patrones **ANDEXP** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para obtener más información sobre la implementación de esta estructura como parte de un filtro de captura, vea [capturar filtros](capture-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




