---
description: Realiza el análisis de tinta asincrónica.
ms.assetid: 36427b80-5e3b-4c9a-bb49-e6b7f9301cbd
title: 'IInkAnalyzer:: BackgroundAnalyze (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.BackgroundAnalyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 606e1444f66884564a6b9f2007adfc26b2eb2ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542030"
---
# <a name="iinkanalyzerbackgroundanalyze-method"></a>IInkAnalyzer:: BackgroundAnalyze (método)

Realiza el análisis de tinta asincrónica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BackgroundAnalyze();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Cuando se llama a este método, el [**IInkAnalyzer**](iinkanalyzer.md) realiza el análisis de tinta en un subproceso en segundo plano.

Este método devuelve **S \_ false** y no inicia una nueva operación de análisis en segundo plano en las siguientes circunstancias.

-   El [**IInkAnalyzer**](iinkanalyzer.md) está realizando el análisis en segundo plano.
-   la región desfasada (vea [**IInkAnalyzer:: GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) representa un área vacía.

El [**IInkAnalyzer**](iinkanalyzer.md) analiza la tinta dentro de su región desfasada durante una llamada al método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o **IInkAnalyzer:: BackgroundAnalyze**. Sin embargo, el **IInkAnalyzer** puede expandir la operación de análisis para incluir las regiones vecinas.

Este método establece la región desfasada en una región vacía.

Si los datos de trazo se agregaron al [**IInkAnalyzer**](iinkanalyzer.md) después de la llamada al **método IInkAnalyzer:: BackgroundAnalyze**, el **IInkAnalyzer** puede actualizar la región desfasada durante la fase de conciliación del análisis de tinta.

La configuración de modos de análisis (vea [**IInkAnalyzer:: GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)) especifica cómo realiza el [**IInkAnalyzer**](iinkanalyzer.md) el análisis en segundo plano. Para obtener más información sobre el análisis de tinta, consulte [información general del análisis de tinta](ink-analysis-overview.md).

Este método devuelve un código de error en las siguientes circunstancias.

-   La aplicación tiene establecido el valor [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ IntermediateResults** en [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IInkAnalyzer:: SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) y no controla el evento [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) .
-   La aplicación ha borrado el valor de [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ AutomaticReconciliation** en [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IInkAnalyzer:: SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) y no controla el evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .
-   La aplicación no controla el evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .
-   La aplicación no controla el evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se comprueba la región desfasada del analizador de tinta y, a continuación, se inicia el análisis de tinta de fondo si la región desfasada no está vacía.


```C++
// Check that the ink analyzer's dirty region is not empty.
IAnalysisRegion *pDirtyRegion;
hr = this->m_spIInkAnalyzer->GetDirtyRegion(&pDirtyRegion);

if (SUCCEEDED(hr))
{
    VARIANT_BOOL bIsEmpty;
    hr = pDirtyRegion->IsEmpty(&bIsEmpty);

    if (SUCCEEDED(hr))
    {
        if (!bIsEmpty)
        {
            // Insert code that prepares the application for background
            // ink analysis here.

            // Start background ink analysis. The _IAnalysisEvents::Results
            // event signals when background ink analysis is complete.
            hr = this->m_spIInkAnalyzer->BackgroundAnalyze();
        }
    }
}

// Free the memory for the dirty region.
if (pDirtyRegion != NULL)
{
    pDirtyRegion->Release();
}
```



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

[**IInkAnalyzer:: GetAnalysisModes (método)**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[**IInkAnalyzer:: SetAnalysisModes (método)**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[**IInkAnalyzer:: GetDirtyRegion (método)**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer:: SetDirtyRegion (método)**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer:: GetRootNode (método)**](iinkanalyzer-getrootnode.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




