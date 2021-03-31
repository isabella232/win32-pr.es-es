---
description: Recupera una colección ordenada de objetos IInkAnalysisRecognizer.
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: 'IInkAnalyzer:: GetInkAnalysisRecognizersByPriority (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetInkAnalysisRecognizersByPriority
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d596a8138f8ab16852ce99116eef66372ff2b074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908009"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a>IInkAnalyzer:: GetInkAnalysisRecognizersByPriority (método)

Recupera una colección ordenada de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppInkAnalysisRecognizers* \[ enuncia\]
</dt> <dd>

Colección ordenada de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppInkAnalysisRecognizers* cuando ya no necesite usar el objeto.

 

El orden de los reconocedores de esta colección indica el orden en que el [**IInkAnalyzer**](iinkanalyzer.md) evalúa los reconocedores disponibles. **IInkAnalyzer** usa el lenguaje de los trazos como criterio principal para aplicar un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md). Como criterio secundario, **IInkAnalyzer** compara la información de sugerencia de análisis con las capacidades admitidas de un objeto **IInkAnalysisRecognizer** (consulte [**IInkAnalysisRecognizer:: GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)). Para obtener más información sobre las sugerencias de análisis, vea [**IInkAnalyzer:: CreateAnalysisHint Method**](iinkanalyzer-createanalysishint.md).

Si más de un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) admite un identificador de idioma, el [**IInkAnalyzer**](iinkanalyzer.md) usa un algoritmo de "primer ajuste" para seleccionar el primer **IInkAnalysisRecognizer** para analizar los trazos de ese idioma.

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

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer (método)**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

