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
ms.openlocfilehash: 400addd7d32914cb4e849e4e0bfae76ccc3ddf22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161211"
---
# <a name="freehelperattributes-function"></a>Función FreeHelperAttributes

La **función FreeHelperAttributes desasigna** la memoria asignada internamente a una matriz de estructuras [**HELPER \_ ATTRIBUTE.**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) Esta función llama [**a CoTaskMemFree para**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) desasignar memoria.

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
| Encabezado<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ATRIBUTO \_ DEL ASISTENTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

