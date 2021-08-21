---
title: Función FreeHelperAttributes (Ndattributils.h)
description: Desasigna la memoria asignada internamente a una matriz de estructuras HELPER \_ ATTRIBUTE.
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- Función FreeHelperAttributes NDF
topic_type:
- apiref
api_name:
- FreeHelperAttributes
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb16ad2d7f505a90d806e3f6a155f2c20affce2c71267316c2278e2320c371b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802435"
---
# <a name="freehelperattributes-function"></a>Función FreeHelperAttributes

La **función FreeHelperAttributes desasigna** la memoria asignada internamente a una matriz de [**estructuras HELPER \_ ATTRIBUTE.**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) Esta función llama [**a CoTaskMemFree para**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) desasignar memoria.

## <a name="syntax"></a>Sintaxis


```C++
VOID FreeHelperAttributes(
  _In_ HELPER_ATTRIBUTE *pInfo,
       ULONG            HelperAttributeCount,
       BOOL             bFreePointer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInfo* \[ En\]
</dt> <dd>

Tipo: **[ **ATRIBUTO \_ DEL ASISTENTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\***

Matriz de estructuras. Se liberará la memoria asignada a la que apuntan estas estructuras.

</dd> <dt>

*HelperAttributeCount* 
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
| Header<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ATRIBUTO \_ DEL ASISTENTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

