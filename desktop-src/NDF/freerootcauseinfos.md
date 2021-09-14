---
title: Función FreeRootCauseInfos (Ndattributils.h)
description: Desasigne la memoria asignada internamente a una matriz de estructuras RootCauseInfo.
ms.assetid: b45fa432-0db4-470b-80ce-ae25c33f88d6
keywords:
- Función FreeRootCauseInfos NDF
topic_type:
- apiref
api_name:
- FreeRootCauseInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d302a1c58f1a77aafa7611f437f3d445f29f9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161209"
---
# <a name="freerootcauseinfos-function"></a>Función FreeRootCauseInfos

La **función FreeRootCauseInfos** desasigna la memoria asignada internamente a una matriz de [**estructuras RootCauseInfo.**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) Esta función llama [**a CoTaskMemFree para**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) desasignar memoria.

## <a name="syntax"></a>Sintaxis


```C++
VOID FreeRootCauseInfos(
  _In_ RootCauseInfo *pInfo,
       ULONG         RootCauseCount,
       BOOL          bFreePointer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInfo* \[ En\]
</dt> <dd>

Tipo: **[ **RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\***

Matriz de estructuras. Se liberará la memoria asignada a la que apuntan estas estructuras.

</dd> <dt>

*RootCauseCount* 
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

[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

