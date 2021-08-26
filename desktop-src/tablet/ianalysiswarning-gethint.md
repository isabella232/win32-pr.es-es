---
description: Recupera la sugerencia de análisis que produjo esta advertencia.
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: Método IAnalysisWarning::GetHint (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 51eb76839b157c2ac9611ef9be978ea967c8e9b3506513a23b0ca70906dd32b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940515"
---
# <a name="ianalysiswarninggethint-method"></a>IAnalysisWarning::GetHint (método)

Recupera la sugerencia de análisis que produjo esta advertencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAnalysisHint* \[ out\]
</dt> <dd>

Nodo de contexto de sugerencia de análisis que produjo esta advertencia o **NULL** si una sugerencia de análisis no produjo esta advertencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *pAnalysisHint* cuando ya no necesite usar el nodo de contexto de sugerencia de análisis.

 

Un ejemplo de una sugerencia de análisis que genera [**un IAnalysisWarning**](ianalysiswarning.md) es una sugerencia de análisis que contiene un factoid mal escrito. En este caso, el análisis de entrada de lápiz devuelve un [**IAnalysisStatus**](ianalysisstatus.md) que contiene un **IAnalysisWarning** que hace referencia al nodo de contexto de sugerencia de análisis con el factoid mal escrito. Además, en este caso, el método [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md) de la advertencia de análisis devuelve un valor [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) **de AnalysisWarningCode \_ FactoidNotSupported**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IInkAnalyzer::Analyze (Método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze (Método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

