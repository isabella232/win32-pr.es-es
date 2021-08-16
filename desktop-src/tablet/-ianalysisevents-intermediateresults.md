---
description: Se produce cuando finaliza la fase de análisis intermedia actual.
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: _IAnalysisEvents::IntermediateResults (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.IntermediateResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9efead00094fdcd773c3ac90b0d626e2036030171bcf3be011323b6da70fb665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857201"
---
# <a name="_ianalysiseventsintermediateresults-event"></a>\_Evento IAnalysisEvents::IntermediateResults

Se produce cuando finaliza la fase de análisis intermedia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IntermediateResults(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalyzer* \[ En\]
</dt> <dd>

[**IInkAnalyzer que**](iinkanalyzer.md) realiza el análisis.

</dd> <dt>

*pAnalysisStatus* \[ En\]
</dt> <dd>

Objeto [**IAnalysisStatus**](ianalysisstatus.md) que representa el estado de los resultados intermedios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

[**IInkAnalyzer**](iinkanalyzer.md) genera este evento después de haber conciliado los resultados intermedios de la fase de análisis actual.

Si la aplicación mantiene su propia estructura de datos, que se sincroniza con la de [**IInkAnalyzer,**](iinkanalyzer.md)este evento indica que **IInkAnalyzer** ha terminado de realizar cambios en sus datos internos para esta fase de análisis.

Bloquee la estructura de datos cuando [**IInkAnalyzer**](iinkanalyzer.md) genera el evento [**\_ IAnalysisProxyEvents::InkAnalyzerStateChanging.**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Los cambios en la estructura de datos durante esta fase de análisis pueden provocar errores en el análisis de entrada de lápiz y la sincronización. Puede desbloquear la estructura de datos cuando **IInkAnalyzer** genera el evento **\_ IAnalysisEvents::IntermediateResults** o [**\_ IAnalysisEvents::Results.**](-ianalysisevents-results.md)

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [Proxy de datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

[**IInkAnalyzer**](iinkanalyzer.md) genera resultados intermedios solo cuando sus modos de análisis tienen establecida la marca **AnalysisModes \_ IntermediateResults** (vea El método [**IInkAnalyzer::GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**\_IAnalysisEvents::Results**](-ianalysisevents-results.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::Analyze (Método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze (Método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>
