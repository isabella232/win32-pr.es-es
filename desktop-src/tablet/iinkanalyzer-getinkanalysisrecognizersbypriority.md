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
ms.openlocfilehash: d596a8138f8ab16852ce99116eef66372ff2b074
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360003"
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

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppInkAnalysisRecognizers* cuando ya no necesite usar el objeto .

 

El orden de los reconocedores de esta colección indica el orden en que [**IInkAnalyzer**](iinkanalyzer.md) evalúa los reconocedores disponibles. **IInkAnalyzer usa** el lenguaje de los trazos como criterio principal para aplicar un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md). Como criterio secundario, **IInkAnalyzer** compara la información de sugerencias de análisis con las funcionalidades admitidas de un objeto **IInkAnalysisRecognizer** (vea [**IInkAnalysisRecognizer::GetCapabilities).**](iinkanalysisrecognizer-getcapabilities.md) Para obtener más información sobre las sugerencias de análisis, vea [**IInkAnalyzer::CreateAnalysisHint (Método).**](iinkanalyzer-createanalysishint.md)

Si más de un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) admite un identificador de idioma, [**IInkAnalyzer**](iinkanalyzer.md) usa un algoritmo de "primer ajuste" para seleccionar el primer **IInkAnalysisRecognizer** para analizar los trazos de ese lenguaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
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

 

