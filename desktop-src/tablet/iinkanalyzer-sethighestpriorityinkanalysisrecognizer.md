---
description: Mueve el IInkAnalysisRecognizer especificado a la primera posición de la lista de reconocedores de lápiz del objeto IInkAnalyzer.
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: Método IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetHighestPriorityInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8404a2e1e89980ce5e8cadac1a468b3383d37d4952349f3702539975a304ac92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935215"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a>Método IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer

Mueve el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) especificado a la primera posición de la lista de reconocedores de lápiz del objeto [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalysisRecognizer* \[ En\]
</dt> <dd>

[**IInkAnalysisRecognizer para**](iinkanalysisrecognizer.md) colocarlo en la primera posición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Para obtener la lista de reconocedores de lápiz en orden de prioridad, llame al método [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).

Este método no afecta al orden del resto de los objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) en la lista de reconocedores de lápiz del objeto [**IInkAnalyzer.**](iinkanalyzer.md)

El orden de los reconocedores de lápiz devueltos por [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority (Método)**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indica el orden en que [**IInkAnalyzer**](iinkanalyzer.md) evalúa los objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) disponibles.

El uso de los reconocedores de lápiz se evalúa en función de su orden en la lista.

Durante el análisis de lápiz, [**IInkAnalyzer**](iinkanalyzer.md) recorre en iteración los reconocedores de lápiz de su lista hasta que encuentra un reconocedor que admita el idioma y otras propiedades de los trazos. Este reconocedor se usa para el reconocimiento de lápiz para esos trazos.

Si [**IInkAnalyzer**](iinkanalyzer.md) no encuentra un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que admita un conjunto de trazos durante el análisis, **IInkAnalyzer** genera un [**IAnalysisWarning**](ianalysiswarning.md) con un código de advertencia de **AnalysisWarningCode \_ InkAnalysisRecognizerNotInstalled** (vea [**IAnalysisWarning::GetWarningCode).**](ianalysiswarning-getwarningcode.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::GetInkAnalysisRecognizersByPriority (Método)**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




