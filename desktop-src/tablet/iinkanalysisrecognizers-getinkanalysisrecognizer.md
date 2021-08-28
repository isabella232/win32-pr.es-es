---
description: Recupera el IInkAnalysisRecognizer en el índice especificado.
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: Método IInkAnalysisRecognizers::GetInkAnalysisRecognizer (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6755b82beaea1bec9a38b9c15ea57a97c1d19fc4eecb5a2b55c80e2070562d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967344"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a>IInkAnalysisRecognizers::GetInkAnalysisRecognizer (método)

Recupera [**IInkAnalysisRecognizer en**](iinkanalysisrecognizer.md) el índice especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulIndex* \[ En\]
</dt> <dd>

Índice de base cero del objeto [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que se obtiene.

</dd> <dt>

*ppInkAnalysisRecognizer* \[ out\]
</dt> <dd>

Puntero a [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) en el índice especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppInkAnalysisRecognizer* cuando ya no necesite usar el reconocedor de análisis de entrada de lápiz.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

