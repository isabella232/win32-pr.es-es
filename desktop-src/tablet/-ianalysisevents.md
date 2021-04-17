---
description: Especifica eventos asociados a los pasos de análisis de un objeto IInkAnalyzer.
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: Interfaz _IAnalysisEvents
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697379"
---
# <a name="_ianalysisevents-interface"></a>\_Interfaz IAnalysisEvents

Especifica eventos asociados a los pasos de análisis de un objeto [**IInkAnalyzer**](iinkanalyzer.md) .

-   [Eventos](/windows)

### <a name="events"></a>Events

La interfaz **\_ IAnalysisEvents** tiene estos eventos.



| Evento                                                               | Descripción                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Actividad**](-ianalysisevents-activity.md)                       | Tiene lugar durante las llamadas al método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o al método [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) .<br/> |
| [**IntermediateResults**](-ianalysisevents-intermediateresults.md) | Se produce cuando finaliza la fase de análisis intermedio actual.<br/>                                                                                                                    |
| [**ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)       | Se produce cuando [**IInkAnalyzer**](iinkanalyzer.md) está listo para conciliar los resultados del análisis de fondo con su estado actual.<br/>                                                  |
| [**Results**](-ianalysisevents-results.md)                         | Se produce cuando finaliza la fase de análisis final.<br/>                                                                                                                                   |
| [**UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)   | Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) tenga acceso a los datos del trazo.<br/>                                                                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

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

 

