---
description: Recupera marcas que controlan cómo IInkAnalyzer realiza el análisis de entrada de lápiz.
ms.assetid: 982cb9cd-2d73-4064-9a6e-fe123adf0fb6
title: Método IInkAnalyzer::GetAnalysisModes (IACom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360642"
---
# <a name="iinkanalyzergetanalysismodes-method"></a>Método IInkAnalyzer::GetAnalysisModes

Recupera marcas que controlan cómo [**IInkAnalyzer**](iinkanalyzer.md) realiza el análisis de entrada de lápiz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAnalysisModes(
  [out] AnalysisModes *pAnalysisMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAnalysisMode* \[ out\]
</dt> <dd>

Combinación bit a bit de los valores [**de enumeración AnalysisModes.**](analysismodes.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**IInkAnalyzer::Analyze (Método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze (Método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer::SetAnalysisModes (Método)**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




