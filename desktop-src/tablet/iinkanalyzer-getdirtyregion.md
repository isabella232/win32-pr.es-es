---
description: Recupera el área que ha cambiado desde la última operación de análisis.
ms.assetid: 0cd62775-59c6-41f5-957e-709a53a8c257
title: Método IInkAnalyzer::GetDirtyRegion (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d1d621991b4af3d22322529af7541395fddccc7a2c180a13419296eac61d7322
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773595"
---
# <a name="iinkanalyzergetdirtyregion-method"></a>IInkAnalyzer::GetDirtyRegion (método)

Recupera el área que ha cambiado desde la última operación de análisis.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDirtyRegion(
  [out] IAnalysisRegion **ppDirtyRegion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDirtyRegion* \[ out\]
</dt> <dd>

[**IAnalysisRegion que**](ianalysisregion.md) describe el área que ha cambiado desde la última operación de análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppDirtyRegion* cuando ya no necesite usar el objeto .

 

Este método identifica las áreas que se deben analizar o volver a analizar. Todos los métodos [**IInkAnalyzer**](iinkanalyzer.md) que agregan, actualizan o quitan datos de trazo actualizan la región desusada. Para marcar manualmente un área para el reanálisis:

1.  Obtenga la región desa prueba **mediante el método IInkAnalyzer::GetDirtyRegion**.
2.  Use [**el método IAnalysisRegion::UnionRegion o**](ianalysisregion-unionregion.md) el método [**IAnalysisRegion::UnionRectangle**](ianalysisregion-unionrectangle.md) para agregar el área a la región del paso 1.
3.  Use [**el método IInkAnalyzer::SetDirtyRegion para**](iinkanalyzer-setdirtyregion.md) actualizar la región desa prueba.

[**IInkAnalyzer**](iinkanalyzer.md) analiza la entrada de lápiz dentro de su región desusado durante una llamada al método [**IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md) o al método [**IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md). Sin embargo, **IInkAnalyzer** puede expandir la operación de análisis para incluir regiones vecinos.

Esta propiedad puede contener áreas nojacentes.

Use [**CoTaskMemFree para**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) liberar la memoria de la matriz *ppDirtyRegion* cuando haya terminado con ella.

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

 

