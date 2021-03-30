---
description: Obtiene un valor que indica el nivel de confianza que IInkAnalyzer tiene en la precisión de IAnalysisAlternate.
ms.assetid: ac1c68df-2e0c-4633-b7ee-519482a4d67a
title: 'IAnalysisAlternate:: GetRecognitionConfidence (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognitionConfidence
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eacaf7e5a8feaddcd437e68cf7acfa4fc5a7fc80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810063"
---
# <a name="ianalysisalternategetrecognitionconfidence-method"></a>IAnalysisAlternate:: GetRecognitionConfidence (método)

Obtiene un valor que indica el nivel de confianza que [**IInkAnalyzer**](iinkanalyzer.md) tiene en la precisión de [**IAnalysisAlternate**](ianalysisalternate.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRecognitionConfidence(
  [out] RecognitionConfidence *pConfidence
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pConfidence* \[ enuncia\]
</dt> <dd>

Un puntero a una [**enumeración InkRecognitionConfidence**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) que indica el nivel de confianza que el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) tiene en la precisión de la alternativa de reconocimiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**RecognitionConfidence**](recognitionconfidence.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




