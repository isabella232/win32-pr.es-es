---
description: Cancela la operación de análisis actual.
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: Método IInkAnalyzer::Abort (IACom.h)
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
ms.openlocfilehash: 4f52b2037210e39533d1247cb338bb22a7785f354dbca6b615c6ada67eff3bb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773605"
---
# <a name="iinkanalyzerabort-method"></a>IInkAnalyzer::Abort (método)

Cancela la operación de análisis actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppAbortedRegion* \[ out\]
</dt> <dd>

Puntero a una [**región IAnalysisRegion**](ianalysisregion.md) que representa la región desdumbre (vea [**IInkAnalyzer::GetDirtyRegion (método)**](iinkanalyzer-getdirtyregion.md)de la operación de análisis actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Llame [**a IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppAbortedRegion* cuando ya no necesite usar el objeto .

Este método cancela la operación de análisis actual.

Cuando *ppAbortedRegion* es **NULL,** este método realiza la anulación de la forma normal, ya que esto indica que el autor de la llamada no tiene interés en el valor devuelto.

**El método IInkAnalyzer::Abort** silencia los eventos [**\_ IAnalysisEvents::Results**](-ianalysisevents-results.md) e [**\_ IAnalysisEvents::Activity**](-ianalysisevents-activity.md) para la operación de análisis actual.

**El método IInkAnalyzer::Abort se** ejecuta de forma asincrónica hasta que se cancela la operación de análisis en segundo plano actual. Dado que el proceso de cancelación es asincrónico, la aplicación puede realizar otras tareas mientras se cancelan las operaciones de análisis actuales.

Si no hay ninguna operación de análisis en curso, este método devuelve una región de análisis vacía.

Si hay una operación de análisis en curso, este método cancela la operación.

Si hay operaciones de análisis sincrónicas y asincrónicas en curso, este método cancela la operación sincrónica.

Si se llama a este método más de una vez para la misma operación de análisis, la primera llamada devuelve la región desa prueba para la operación y las llamadas posteriores devuelven una región vacía.

Si la aplicación mantiene su propia estructura de datos que está sincronizada con la de [**IInkAnalyzer,**](iinkanalyzer.md)llamar al método **IInkAnalyzer::Abort** puede dejar el documento con resultados parciales. Para evitarlo, no llame al método **IInkAnalyzer::Abort** entre el momento en que **IInkAnalyzer** recibe el evento [**\_ IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) y el momento en que **IInkAnalyzer** recibe el evento [**\_ IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) o [**\_ IAnalysisEvents::Results.**](-ianalysisevents-results.md)

Para obtener más información sobre cómo sincronizar los datos de la aplicación con el analizador de entrada de lápiz, vea [Proxy de datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

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

[**IInkAnalyzer::GetDirtyRegion (Método)**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer::SetDirtyRegion (Método)**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

