---
description: Recupera un nombre de tipo legible de este IContextNode.
ms.assetid: 02031efd-1e9c-4e96-8dc1-280cc1a6e58f
title: 'IContextNode:: GetTypeName (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetTypeName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9d7bc4a24b7abc3ee507d7bda0c547f4c55a787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154433"
---
# <a name="icontextnodegettypename-method"></a>IContextNode:: GetTypeName (método)

Recupera un nombre de tipo legible de este [**IContextNode**](icontextnode.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTypeName(
  [out] BSTR *pbstrContextNodeType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbstrContextNodeType* \[ enuncia\]
</dt> <dd>

Un nombre de tipo legible de este [**IContextNode**](icontextnode.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) en \* *pbstrContextNodeType* cuando ya no necesite usar la cadena.

 

Por ejemplo, este método establece *pbstrContextNodeType* en "InkWordNode" para un nodo de palabra de tinta (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [tipos de nodo de contexto](context-node-types.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode:: GetType**](icontextnode-gettype.md)
</dt> <dt>

[Tipos de nodo de contexto](context-node-types.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

