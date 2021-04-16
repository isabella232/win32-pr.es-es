---
description: Especifica los eventos asociados con los pasos del proxy de datos de un objeto IInkAnalyzer.
ms.assetid: 57fee525-02e2-4721-b6e5-28112d53db2a
title: _IAnalysisProxyEvents interfaz (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b83019cafb6053b9f803c815289d9f9f64d32a5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105678661"
---
# <a name="_ianalysisproxyevents-interface"></a>\_Interfaz IAnalysisProxyEvents

Especifica los eventos asociados con los pasos del proxy de datos de un objeto [**IInkAnalyzer**](iinkanalyzer.md) .

-   [Eventos](/windows)

### <a name="events"></a>Events

La interfaz **\_ IAnalysisProxyEvents** tiene estos eventos.



| Evento                                                                                      | Descripción                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md)                     | Se produce después de que [**IInkAnalyzer**](iinkanalyzer.md) cree un objeto [**IContextNode**](icontextnode.md) .<br/>                                                                  |
| [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md)                   | Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) elimine un objeto [**IContextNode**](icontextnode.md) .<br/>                                                                 |
| [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)               | Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) agregue un objeto [**IContextLink**](icontextlink.md) entre dos objetos [**IContextNode**](icontextnode.md) .<br/>           |
| [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)           | Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) elimine un objeto [**IContextLink**](icontextlink.md) entre dos objetos [**IContextNode**](icontextnode.md) .<br/>         |
| [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)   | Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) mueva un objeto [**IContextNode**](icontextnode.md) a una nueva posición dentro de la colección de subnodos de su nodo primario.<br/> |
| [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) | Se produce después de que [**IInkAnalyzer**](iinkanalyzer.md) actualice una o varias propiedades de un objeto [**IContextNode**](icontextnode.md) .<br/>                                        |
| [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)             | Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) mueva un objeto [**IContextNode**](icontextnode.md) cambiando su nodo primario.<br/>                                       |
| [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md)         | Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) reconcilia los resultados del análisis para que una aplicación pueda sincronizar los datos con **IInkAnalyzer**.<br/>                      |
| [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md)                   | Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) realice el análisis dentro de la región de un objeto [**IContextNode**](icontextnode.md) parcialmente rellenado.<br/>               |
| [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)                         | Se produce cuando el [**IInkAnalyzer**](iinkanalyzer.md) mueve un trazo de un objeto [**IContextNode**](icontextnode.md) a otro.<br/>                                           |



 

## <a name="remarks"></a>Observaciones

Utilice estos eventos cuando la aplicación mantiene su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md). Para obtener más información sobre cómo sincronizar los datos de la aplicación con **IInkAnalyzer**, vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer:: Analyze (método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer:: BackgroundAnalyze (método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[\_IAnalysisEvents](-ianalysisevents.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

