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
ms.openlocfilehash: 90e32669d8b542202f6166052c072f224bb2954a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256844"
---
# <a name="_ianalysisevents-interface"></a>\_Interfaz IAnalysisEvents

Especifica los eventos asociados a los pasos de análisis de un [**objeto IInkAnalyzer.**](iinkanalyzer.md)

-   [Eventos](/windows)

### <a name="events"></a>Eventos

La **\_ interfaz IAnalysisEvents** tiene estos eventos.



| Evento                                                               | Descripción                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Actividad**](-ianalysisevents-activity.md)                       | Se produce durante las llamadas al método [**IInkAnalyzer::Analyze o**](iinkanalyzer-analyze.md) al método [**IInkAnalyzer::BackgroundAnalyze.**](iinkanalyzer-backgroundanalyze.md)<br/> |
| [**IntermediateResults**](-ianalysisevents-intermediateresults.md) | Se produce cuando finaliza la fase de análisis intermedia actual.<br/>                                                                                                                    |
| [**ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)       | Se produce cuando [**IInkAnalyzer**](iinkanalyzer.md) está listo para conciliar sus resultados de análisis en segundo plano con su estado actual.<br/>                                                  |
| [**Results**](-ianalysisevents-results.md)                         | Se produce cuando finaliza la fase de análisis final.<br/>                                                                                                                                   |
| [**UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)   | Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) acceda a los datos del trazo.<br/>                                                                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



## <a name="see-also"></a>Consulte también

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

 

