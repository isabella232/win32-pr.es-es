---
description: Devuelve los identificadores de trazo asociados a este IAnalysisAlternate.
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: Método IAnalysisAlternate::GetStrokeIds (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2682107a58f126011c4d80a02a119219ccea0976408937e19eb7b511eb82cff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967504"
---
# <a name="ianalysisalternategetstrokeids-method"></a>IAnalysisAlternate::GetStrokeIds (método)

Devuelve los identificadores de trazo asociados a [**este objeto IAnalysisAlternate.**](ianalysisalternate.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulStrokeIdsCount* \[ in, out\]
</dt> <dd>

Puntero a un **ULONG** que se establece en el número de identificadores de trazo asociados a [**este objeto IAnalysisAlternate.**](ianalysisalternate.md)

</dd> <dt>

*pplStrokeIds* \[ out\]
</dt> <dd>

\[out, size \_ is( \* *pulStrokeIdsCount* \* sizeof(LONG))\]

Matriz de **LONG de** longitud *pulStrokeIdsCount* que se establece en los identificadores de trazo asociados a [**esta clase IAnalysisAlternate.**](ianalysisalternate.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, use [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *pplStrokeIds* cuando ya no necesite la información.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

