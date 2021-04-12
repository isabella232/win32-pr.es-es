---
title: Función FreeHelperAttributes (Ndattributils. h)
description: Desasigna la memoria asignada internamente a una matriz de estructuras de atributo de aplicación auxiliar \_ .
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- FreeHelperAttributes función NDF
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489880"
---
# <a name="freehelperattributes-function"></a>FreeHelperAttributes función)

La función **FreeHelperAttributes** desasigna la memoria asignada internamente a una matriz de estructuras de [**\_ atributo de aplicación auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) . Esta función llama a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desasignar memoria.

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

*Pinfo* \[ de\]
</dt> <dd>

Tipo: **\* [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)* _

Matriz de estructuras. La memoria asignada a la que apuntan estas estructuras se liberará.

</dd> <dt>

_HelperAttributeCount * 
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

[**atributo auxiliar \_**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

