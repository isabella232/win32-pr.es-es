---
title: Función FreeRepairInfoExs (Ndattributils.h)
description: Desasigna la memoria asignada internamente a una matriz de estructuras RepairInfoEx.
ms.assetid: b4e3e758-88cd-4ce2-b1a4-5b47889aae9b
keywords:
- Función FreeRepairInfoExs NDF
topic_type:
- apiref
api_name:
- FreeRepairInfoExs
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 094c745486526caa870a500019de3aa819b6fe5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161213"
---
# <a name="freerepairinfoexs-function"></a>Función FreeRepairInfoExs

La **función FreeRepairInfoExs** desasigna la memoria asignada internamente a una matriz de [**estructuras RepairInfoEx.**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) Esta función llama [**a CoTaskMemFree para**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) desasignar memoria.

## <a name="syntax"></a>Sintaxis


```C++
VOID FreeRepairInfoExs(
  _In_ RepairInfoEx *pInfo,
       ULONG        RepairCount,
       BOOL         bFreePointer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInfo* \[ En\]
</dt> <dd>

Tipo: **[ **RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)\***

Matriz de estructuras. Se liberará la memoria asignada a la que apuntan estas estructuras.

</dd> <dt>

*RepairCount* 
</dt> <dd>

Tipo: **ULONG**

Número de estructuras de la matriz a las que apunta *pInfo*.

</dd> <dt>

*bFreePointer* 
</dt> <dd>

Tipo: **BOOL**

True si también se debe eliminar la matriz de estructuras; de lo contrario, false.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

