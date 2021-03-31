---
description: Mueve el IInkAnalysisRecognizer especificado a la primera posición de la lista de reconocedores de tinta del objeto IInkAnalyzer.
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: 'IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer (método) (IACom. h)'
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
ms.openlocfilehash: 534b94e4f2964aa81f04e0adac6f45f346c530c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908007"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a>IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer (método)

Mueve el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) especificado a la primera posición de la lista de reconocedores de tinta del objeto [**IInkAnalyzer**](iinkanalyzer.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalysisRecognizer* \[ de\]
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que se va a colocar en la primera posición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Para obtener la lista de reconocedores de tinta en orden de prioridad, llame al [**método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).

Este método no afecta al orden del resto de los objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) de la lista de reconocedores de tinta del objeto [**IInkAnalyzer**](iinkanalyzer.md) .

El orden de los reconocedores de tinta devueltos por el [**método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indica el orden en el que [**IInkAnalyzer**](iinkanalyzer.md) evalúa los objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) disponibles.

El uso de los reconocedores de tinta se evalúa en función de su orden en la lista.

Durante el análisis de tinta, el [**IInkAnalyzer**](iinkanalyzer.md) recorre en iteración los reconocedores de tinta de su lista hasta que encuentra un reconocedor que admita el idioma y otras propiedades de los trazos. Este reconocedor se usa para el reconocimiento de tinta para esos trazos.

Si [**IInkAnalyzer**](iinkanalyzer.md) no encuentra un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que admita un conjunto de trazos durante el análisis, el **IInkAnalyzer** genera un [**IAnalysisWarning**](ianalysiswarning.md) con un código de advertencia de **AnalysisWarningCode \_ InkAnalysisRecognizerNotInstalled** (vea [**IAnalysisWarning:: GetWarningCode**](ianalysiswarning-getwarningcode.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer:: GetInkAnalysisRecognizersByPriority (método)**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




