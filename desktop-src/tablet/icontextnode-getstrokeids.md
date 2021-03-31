---
description: Recupera una matriz de identificadores para los trazos dentro del objeto IContextNode.
ms.assetid: 2420afec-6859-449b-92d8-0f4327281852
title: 'IContextNode:: GetStrokeIds (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 25592cd245eba135fa7e459ff3c5c5207fc6ff0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154437"
---
# <a name="icontextnodegetstrokeids-method"></a>IContextNode:: GetStrokeIds (método)

Recupera una matriz de identificadores para los trazos dentro del objeto [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulStrokeIdsCount* \[ in, out\]
</dt> <dd>

Número de trazos. No se utiliza el valor que se pasa.

</dd> <dt>

*pplStrokes* \[ enuncia\]
</dt> <dd>

Puntero a la matriz de identificadores de trazo para este objeto [**IContextNode**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *pplStrokes* cuando ya no necesite la información.

 

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

[**IContextNode::GetStrokeId**](icontextnode-getstrokeid.md)
</dt> <dt>

[**IContextNode::GetStrokeCount**](icontextnode-getstrokecount.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

