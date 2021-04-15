---
title: Función FreeRepairInfoExs (Ndattributils. h)
description: Desasigna la memoria asignada internamente a una matriz de estructuras RepairInfoEx.
ms.assetid: b4e3e758-88cd-4ce2-b1a4-5b47889aae9b
keywords:
- FreeRepairInfoExs función NDF
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534312"
---
# <a name="freerepairinfoexs-function"></a>FreeRepairInfoExs función)

La función **FreeRepairInfoExs** desasigna la memoria asignada internamente a una matriz de estructuras [**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) . Esta función llama a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desasignar memoria.

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

*Pinfo* \[ de\]
</dt> <dd>

Tipo: **[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) \** _

Matriz de estructuras. La memoria asignada a la que apuntan estas estructuras se liberará.

</dd> <dt>

_RepairCount * 
</dt> <dd>

Tipo: **ULong**

El número de estructuras de la matriz a las que apunta *Pinfo*.

</dd> <dt>

*bFreePointer* 
</dt> <dd>

Tipo: **bool**

True si también se debe eliminar la matriz de estructuras; en caso contrario, false.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

