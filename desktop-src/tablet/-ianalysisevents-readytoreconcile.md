---
description: Se produce cuando IInkAnalyzer está listo para conciliar sus resultados de análisis en segundo plano con su estado actual.
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: _IAnalysisEvents::ReadyToReconcile (evento) (IACom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256851"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a>\_Evento IAnalysisEvents::ReadyToReconcile

Se produce cuando [**IInkAnalyzer**](iinkanalyzer.md) está listo para conciliar sus resultados de análisis en segundo plano con su estado actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

[**IInkAnalyzer**](iinkanalyzer.md) realiza la conciliación automática cuando se establece la marca Detección automática de **AnalysisModes \_** del analizador de entrada manuscrita (vea [**IInkAnalyzer::SetAnalysisModes (Método).**](iinkanalyzer-setanalysismodes.md) Cuando no **se establece la marca AnalysisModes \_ AutomaticReconanalysisation,** la aplicación debe conciliar los resultados del análisis en segundo plano manualmente.

Para realizar la conciliación manual, siga estos pasos.

1.  Borre la marca Detección automática de AnalysisModes del analizador **\_ de entrada manuscrita.**
2.  Controle **\_ el evento IAnalysisEvents::ReadyToReconcile.**
3.  Para conciliar los resultados del análisis, llame al método [**IInkAnalyzer::Reconcile Desde**](iinkanalyzer-reconcile.md) el controlador de eventos para el evento **\_ IAnalysisEvents::ReadyToReconcile.** Para cancelar la operación de análisis en segundo plano actual, llame al método [**IInkAnalyzer::Abort Desde**](iinkanalyzer-abort.md) el controlador de eventos para el evento **\_ IAnalysisEvents::ReadyToReconcile.**

[**IInkAnalyzer**](iinkanalyzer.md) genera este evento antes de generar el evento [**\_ IAnalysisProxyEvents::InkAnalyzerStateChanging.**](-ianalysisproxyevents-inkanalyzerstatechanging.md)

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea Proxy de [datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

[**IInkAnalyzer**](iinkanalyzer.md) genera este evento durante el análisis en segundo plano.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::Analyze (Método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze (Método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer::Reconcile (Método)**](iinkanalyzer-reconcile.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




