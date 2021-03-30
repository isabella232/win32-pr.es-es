---
description: Se produce cuando IInkAnalyzer está listo para conciliar los resultados del análisis de fondo con su estado actual.
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: 'Evento _IAnalysisEvents:: ReadyToReconcile (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.ReadyToReconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f3144f34dc680f9bc31f51b9e6b4284a70fb9bc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279855"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a>\_Evento IAnalysisEvents:: ReadyToReconcile

Se produce cuando [**IInkAnalyzer**](iinkanalyzer.md) está listo para conciliar los resultados del análisis de fondo con su estado actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

[**IInkAnalyzer**](iinkanalyzer.md) realiza la conciliación automática cuando se establece la **marca \_ AutomaticReconciliation AnalysisModes** del analizador de tinta (vea el [**método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)). Cuando no se establece la marca **AnalysisModes \_ AutomaticReconciliation** , la aplicación debe conciliar los resultados del análisis de fondo manualmente.

Para realizar la reconciliación manual, siga estos pasos.

1.  Borre la marca **AnalysisModes \_ AutomaticReconciliation** del analizador de tinta.
2.  Controle el evento **\_ IAnalysisEvents:: ReadyToReconcile** .
3.  Para conciliar los resultados del análisis, llame al método [**IInkAnalyzer:: Reconciliate**](iinkanalyzer-reconcile.md) del controlador de eventos para el evento **\_ IAnalysisEvents:: ReadyToReconcile** . Para cancelar la operación de análisis en segundo plano actual, llame al método [**IInkAnalyzer:: ABORT**](iinkanalyzer-abort.md) del controlador de eventos para el evento **\_ IAnalysisEvents:: ReadyToReconcile** .

[**IInkAnalyzer**](iinkanalyzer.md) genera este evento antes de generar el evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).

[**IInkAnalyzer**](iinkanalyzer.md) genera este evento durante el análisis en segundo plano.

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

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer:: Analyze (método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer:: BackgroundAnalyze (método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer:: reconciliate (método)**](iinkanalyzer-reconcile.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




