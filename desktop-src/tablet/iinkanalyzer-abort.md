---
description: Cancela la operación de análisis actual.
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: 'IInkAnalyzer:: ABORT (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Abort
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eac96809bfbe41e7d6a070782da3ffd0f6407c60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715219"
---
# <a name="iinkanalyzerabort-method"></a>IInkAnalyzer:: ABORT (método)

Cancela la operación de análisis actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppAbortedRegion* \[ enuncia\]
</dt> <dd>

Un puntero a un [**IAnalysisRegion**](ianalysisregion.md) que representa la región desfasada (vea [**IInkAnalyzer:: GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) de la operación de análisis actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppAbortedRegion* cuando ya no necesite usar el objeto.

Este método cancela la operación de análisis actual.

Cuando *ppAbortedRegion* es **null**, este método realiza la anulación como normal, porque esto indica que el autor de la llamada no tiene ningún interés en el valor devuelto.

**IInkAnalyzer:: ABORT (método** ) silencia los eventos [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) y [**\_ IAnalysisEvents:: Activity**](-ianalysisevents-activity.md) para la operación de análisis actual.

**IInkAnalyzer:: ABORT el método** se ejecuta de forma asincrónica hasta que se cancela la operación de análisis en segundo plano actual. Dado que el proceso de cancelación es asincrónico, la aplicación puede realizar otras tareas mientras se cancela el opertions de análisis actual.

Si no hay operaciones de análisis en curso, este método devuelve una región de análisis vacía.

Si una operación de análisis está en curso, este método cancela la operación.

Si hay operaciones de análisis sincrónicas y asincrónicas en curso, este método cancela la operación sincrónica.

Si se llama a este método más de una vez para la misma operación de análisis, la primera llamada devuelve la región desfasada de la operación y las llamadas subsiguientes devuelven una región vacía.

Si la aplicación mantiene su propia estructura de datos que está sincronizada con la del [**IInkAnalyzer**](iinkanalyzer.md), la llamada al **método IInkAnalyzer:: ABORT** puede dejar el documento con resultados parciales. Para evitar esto, no llame al **método IInkAnalyzer:: ABORT** entre el momento en que **IInkAnalyzer** recibe el evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) y la hora en que el **IInkAnalyzer** recibe el evento [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) o [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .

Para obtener más información acerca de cómo sincronizar los datos de aplicación con el analizador de tinta, consulte [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

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

[**IInkAnalyzer:: GetDirtyRegion (método)**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer:: SetDirtyRegion (método)**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

