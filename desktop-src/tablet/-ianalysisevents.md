---
description: Especifica los eventos asociados a los pasos de análisis de un objeto IInkAnalyzer.
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: _IAnalysisEvents interfaz
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2f49455e3e6fb68b2884cda380c304d7655b70d49ff338bcfb7c36904b449019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452170"
---
# <a name="_ianalysisevents-interface"></a>\_IAnalysisEvents (interfaz)

Especifica los eventos asociados a los pasos de análisis de [**un objeto IInkAnalyzer.**](iinkanalyzer.md)

-   [Eventos](/windows)

### <a name="events"></a>Eventos

La **\_ interfaz IAnalysisEvents** tiene estos eventos.



| Evento                                                               | Descripción                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Actividad**](-ianalysisevents-activity.md)                       | Se produce durante las llamadas al método [**IInkAnalyzer::Analyze o**](iinkanalyzer-analyze.md) [**al método IInkAnalyzer::BackgroundAnalyze.**](iinkanalyzer-backgroundanalyze.md)<br/> |
| [**IntermediateResults**](-ianalysisevents-intermediateresults.md) | Se produce cuando finaliza la fase de análisis intermedia actual.<br/>                                                                                                                    |
| [**ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)       | Se produce cuando [**IInkAnalyzer**](iinkanalyzer.md) está listo para conciliar los resultados del análisis en segundo plano con su estado actual.<br/>                                                  |
| [**Results**](-ianalysisevents-results.md)                         | Se produce cuando finaliza la fase de análisis final.<br/>                                                                                                                                   |
| [**UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)   | Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) acceda a los datos del trazo.<br/>                                                                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

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

 

