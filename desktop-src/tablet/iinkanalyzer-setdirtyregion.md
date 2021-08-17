---
description: Modifica el área que ha cambiado desde la última operación de análisis.
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: Método IInkAnalyzer::SetDirtyRegion (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a39fc420b368911788efcb9462c9c4be5b4828c82906ef2c94bb5be99ca17568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091475"
---
# <a name="iinkanalyzersetdirtyregion-method"></a>IInkAnalyzer::SetDirtyRegion (método)

Modifica el área que ha cambiado desde la última operación de análisis.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDirtyRegion* \[ En\]
</dt> <dd>

[**IAnalysisRegion que**](ianalysisregion.md) describe el área que ha cambiado desde la última operación de análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Este método identifica las áreas que se deben analizar o volver a analizar. Todos los métodos [**IInkAnalyzer**](iinkanalyzer.md) que agregan, actualizan o quitan datos de trazo actualizan la región desusada. Para marcar manualmente un área para el reanálisis:

1.  Obtenga la región desa prueba [**mediante el método IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md).
2.  Use [**el método IAnalysisRegion::UnionRegion o**](ianalysisregion-unionregion.md) el método [**IAnalysisRegion::UnionRectangle para**](ianalysisregion-unionrectangle.md) agregar el área a la región del paso 1.
3.  Use **el método IInkAnalyzer::SetDirtyRegion para** actualizar la región desdumbre.

[**IInkAnalyzer**](iinkanalyzer.md) analiza la entrada de lápiz dentro de su región desusado durante una llamada al método [**IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md) o al método [**IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md). Sin embargo, **IInkAnalyzer** puede expandir la operación de análisis para incluir regiones vecinos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::Analyze (Método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze (Método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer::AddStroke (Método)**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokeForLanguage (Método)**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokes (Método)**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokesForLanguage (Método)**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStroke (Método)**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStrokes (Método)**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**IInkAnalyzer::UpdateStrokesData (Método)**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




