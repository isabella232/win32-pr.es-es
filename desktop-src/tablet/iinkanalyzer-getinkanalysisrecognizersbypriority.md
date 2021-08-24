---
description: Recupera una colección ordenada de objetos IInkAnalysisRecognizer.
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: Método IInkAnalyzer::GetInkAnalysisRecognizersByPriority (IACom.h)
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
ms.openlocfilehash: fc663385006eedaca163f529af1f9f8a2da2eb5d3d41db823ffb53ee91775b93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713417"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a>IInkAnalyzer::GetInkAnalysisRecognizersByPriority (método)

Recupera una colección ordenada de [**objetos IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppInkAnalysisRecognizers* \[ out\]
</dt> <dd>

Colección ordenada de [**objetos IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppInkAnalysisRecognizers* cuando ya no necesite usar el objeto .

 

El orden de los reconocedores de esta colección indica el orden en que [**IInkAnalyzer**](iinkanalyzer.md) evalúa los reconocedores disponibles. **IInkAnalyzer usa** el lenguaje de los trazos como criterio principal para aplicar un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md). Como criterio secundario, **IInkAnalyzer** compara la información de sugerencias de análisis con las funcionalidades admitidas de un objeto **IInkAnalysisRecognizer** (vea [**IInkAnalysisRecognizer::GetCapabilities).**](iinkanalysisrecognizer-getcapabilities.md) Para obtener más información sobre las sugerencias de análisis, vea [**IInkAnalyzer::CreateAnalysisHint (Método).**](iinkanalyzer-createanalysishint.md)

Si más de un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) admite un identificador de idioma, [**IInkAnalyzer**](iinkanalyzer.md) usa un algoritmo de "primer ajuste" para seleccionar el primer **IInkAnalysisRecognizer** para analizar los trazos de ese lenguaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer (Método)**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

