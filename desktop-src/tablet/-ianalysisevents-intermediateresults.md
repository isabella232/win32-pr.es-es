---
description: Se produce cuando finaliza la fase de análisis intermedio actual.
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: 'Evento _IAnalysisEvents:: IntermediateResults (IACom. h)'
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
ms.openlocfilehash: 33430225746ddd1a4099f89112f14f99f2b6da84
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105697994"
---
# <a name="_ianalysiseventsintermediateresults-event"></a>\_Evento IAnalysisEvents:: IntermediateResults

Se produce cuando finaliza la fase de análisis intermedio actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IntermediateResults(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalyzer* \[ de\]
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) que realiza el análisis.

</dd> <dt>

*pAnalysisStatus* \[ de\]
</dt> <dd>

Objeto [**IAnalysisStatus**](ianalysisstatus.md) que representa el estado de los resultados intermedios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

[**IInkAnalyzer**](iinkanalyzer.md) genera este evento después de haber reconciliado los resultados intermedios de la fase de análisis actual.

Si la aplicación mantiene su propia estructura de datos, que está sincronizada con la del [**IInkAnalyzer**](iinkanalyzer.md), este evento indica que el **IInkAnalyzer** ha terminado de realizar cambios en sus datos internos para esta fase de análisis.

Bloquee la estructura de datos cuando el [**IInkAnalyzer**](iinkanalyzer.md) provoque el evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) . Los cambios en la estructura de datos durante esta fase de análisis pueden provocar errores en el análisis y la sincronización de las entradas manuscritas. Puede desbloquear la estructura de datos cuando el **IInkAnalyzer** genera el evento **\_ IAnalysisEvents:: IntermediateResults** o [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).

[**IInkAnalyzer**](iinkanalyzer.md) genera resultados intermedios solo cuando sus modos de análisis tienen establecida la marca **\_ IntermediateResults de AnalysisModes** (vea el [**método IInkAnalyzer:: GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**\_IAnalysisEvents:: results**](-ianalysisevents-results.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer:: Analyze (método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer:: BackgroundAnalyze (método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>
