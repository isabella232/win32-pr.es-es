---
description: Realiza análisis sincrónicos de tinta.
ms.assetid: 957845f3-96b4-4184-aaec-e266cbe47e46
title: 'Método IInkAnalyzer:: Analyze (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Analyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2867064067b902105508a7742c6fec88fdcd58be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715212"
---
# <a name="iinkanalyzeranalyze-method"></a>IInkAnalyzer:: Analyze (método)

Realiza análisis sincrónicos de tinta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Analyze(
  [out] IAnalysisStatus **ppStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppStatus* \[ enuncia\]
</dt> <dd>

Un puntero a un [**IAnalysisStatus**](ianalysisstatus.md) que describe el estado de la operación de análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppStatus* cuando ya no necesite usar el estado del análisis.

 

Este método inicia una operación sincrónica de análisis de tinta. El análisis de tinta incluye el análisis de diseño, la clasificación de escritura y dibujo y el reconocimiento de escritura a mano. Este método devuelve una vez completada la operación de análisis.

Este método devuelve **el \_ puntero E** si *ppStatus* es **null**.

Durante una llamada a un método **IInkAnalyzer:: Analyze** o [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), el [**IInkAnalyzer**](iinkanalyzer.md) analiza la tinta dentro de su región desfasada (vea [**IInkAnalyzer:: GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)). Sin embargo, el **IInkAnalyzer** puede expandir la operación de análisis para incluir las regiones vecinas.

Este método establece la región desfasada del objeto [**IInkAnalyzer**](iinkanalyzer.md) en una región vacía. Si otro subproceso ha agregado datos de trazo que no se han analizado, el **IInkAnalyzer** agrega el rectángulo de selección de los trazos sin analizar a su región desfasada durante la fase de conciliación del análisis.

Este método devuelve un error si la aplicación no controla el evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .

[**IInkAnalyzer**](iinkanalyzer.md) no genera los eventos [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) y [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) en respuesta a este método.

Para modificar la forma en que se realiza el análisis de tinta, use el [**método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md).

Para obtener más información sobre el análisis de tinta, consulte [información general del análisis de tinta](ink-analysis-overview.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se realiza el análisis de tinta de primer plano.


```C++
// Perform synchronous ink analysis.
IAnalysisStatus *pAnalysisStatus = NULL;
hr = this->m_spIInkAnalyzer->Analyze(&pAnalysisStatus);

if (SUCCEEDED(hr))
{
    // Insert code that processes the analysis results.
}

// Release this reference to the analysis status.
if (pAnalysisStatus != NULL)
{
    pAnalysisStatus->Release();
    pAnalysisStatus = NULL;
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

[**IInkAnalyzer:: GetDirtyRegion (método)**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer:: SetDirtyRegion (método)**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer:: GetRootNode (método)**](iinkanalyzer-getrootnode.md)
</dt> <dt>

[**IInkAnalyzer:: BackgroundAnalyze (método)**](iinkanalyzer-backgroundanalyze.md)
</dt> </dl>

 

