---
description: Recupera el área que ha cambiado desde la última operación de análisis.
ms.assetid: 0cd62775-59c6-41f5-957e-709a53a8c257
title: 'IInkAnalyzer:: GetDirtyRegion (método) (IACom. h)'
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
ms.openlocfilehash: 56f980189e22f50bb832be904933ef0b26d9b54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275467"
---
# <a name="iinkanalyzergetdirtyregion-method"></a>IInkAnalyzer:: GetDirtyRegion (método)

Recupera el área que ha cambiado desde la última operación de análisis.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDirtyRegion(
  [out] IAnalysisRegion **ppDirtyRegion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDirtyRegion* \[ enuncia\]
</dt> <dd>

[**IAnalysisRegion**](ianalysisregion.md) que describe el área que ha cambiado desde la última operación de análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppDirtyRegion* cuando ya no necesite usar el objeto.

 

Este método identifica las áreas que se deben analizar o volver a analizar. Todos los métodos de [**IInkAnalyzer**](iinkanalyzer.md) que agregan, actualizan o quitan datos de trazo actualizan la región desfasada. Para marcar manualmente un área para el análisis:

1.  Obtiene la región desfasada mediante el **método IInkAnalyzer:: GetDirtyRegion**.
2.  Use el método [**IAnalysisRegion:: UnionRegion**](ianalysisregion-unionregion.md) o [**IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md) para agregar el área a la región del paso 1.
3.  Use el [**método IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) para actualizar la región desfasada.

El [**IInkAnalyzer**](iinkanalyzer.md) analiza la tinta dentro de su región desfasada durante una llamada al método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md). Sin embargo, el **IInkAnalyzer** puede expandir la operación de análisis para incluir las regiones vecinas.

Esta propiedad puede contener áreas no adyacentes.

Use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar memoria de la matriz de *ppDirtyRegion* cuando termine de usarla.

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

[**IInkAnalyzer:: Analyze (método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer:: BackgroundAnalyze (método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer:: AddStroke (método)**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer:: AddStrokeForLanguage (método)**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer:: AddStrokes (método)**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer:: AddStrokesForLanguage (método)**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer:: RemoveStroke (método)**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer:: RemoveStrokes (método)**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**IInkAnalyzer:: UpdateStrokesData (método)**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

