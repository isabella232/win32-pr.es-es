---
description: Recupera marcas que controlan cómo el IInkAnalyzer realiza el análisis de tinta.
ms.assetid: 982cb9cd-2d73-4064-9a6e-fe123adf0fb6
title: 'IInkAnalyzer:: GetAnalysisModes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d03ec255b10dd607889768795b00f5b2aff4dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705697"
---
# <a name="iinkanalyzergetanalysismodes-method"></a>IInkAnalyzer:: GetAnalysisModes (método)

Recupera marcas que controlan cómo el [**IInkAnalyzer**](iinkanalyzer.md) realiza el análisis de tinta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAnalysisModes(
  [out] AnalysisModes *pAnalysisMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAnalysisMode* \[ enuncia\]
</dt> <dd>

Combinación bit a bit de los valores de la enumeración [**AnalysisModes**](analysismodes.md) .

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

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**IInkAnalyzer:: Analyze (método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer:: BackgroundAnalyze (método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer:: SetAnalysisModes (método)**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




