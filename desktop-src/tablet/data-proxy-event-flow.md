---
description: En este tema se de abordan los detalles de los eventos al usar las características de proxy de datos de análisis de entrada de lápiz.
ms.assetid: 837867a4-7cda-41b0-b20d-eec9a3a7fb86
title: Eventos de proxy de datos Flow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b88fbb43e54b19486a6413bc44319fa2dd737486
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247850"
---
# <a name="data-proxy-event-flow"></a>Eventos de proxy de datos Flow

En este tema se de abordan los detalles de los eventos al usar las características de proxy de datos de análisis de entrada de lápiz.

## <a name="data-proxy-event-flow-overview"></a>Información general sobre eventos de proxy Flow datos

En el uso del proxy de datos de [**InkAnalyzer**](inkanalyzer.md), se supone que la aplicación que integra InkAnalyzer ya tiene un modelo de documento existente en el que desea proxy los resultados del análisis. También se supone que la aplicación tendrá resultados de cualquier operación de análisis anterior en la que quiera basar almacenados en su modelo de documento. También puede haber contexto que no sea de entrada de lápiz que se puede agregar a **InkAnalyzer** en forma de **ImageNode** o **TextWordNode**[**ContextNode**](icontextnode.md) para anotarse potencialmente con lápiz.

La clave del sistema de proxy de datos es que la aplicación marca [**contextNode**](icontextnode.md) como "parcialmente rellenado" mediante [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md). Cuando esta marca es true, [**InkAnalyzer**](inkanalyzer.md) asume que hay tres cosas sobre **ese ContextNode**:

-   La ubicación de [**ContextNode**](icontextnode.md) es correcta.
-   El tipo de [**ContextNode**](icontextnode.md) es correcto.
-   Toda la información sobre ese [**ContextNode se**](icontextnode.md) almacena en otro lugar.

En función de estas tres reglas, si y cuando [**InkAnalyzer**](inkanalyzer.md) necesita información adicional sobre [**un ContextNode,**](icontextnode.md) se genera el evento [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) y se hace referencia a **ContextNode** en cuestión. Esto ofrece a la aplicación la oportunidad de establecer toda la información conocida sobre **ese ContextNode** antes de que **InkAnalyzer** la vea con más detalle. Después de controlar un evento **PopulateContextNode,** **contextNode** en cuestión debe tener una propiedad de ubicación válida, el número correcto de subnodos establecido si es un contenedor **ContextNode** o tiene establecidos los trazos correctos, mediante [**SetStrokes**](icontextnode-setstrokes.md), si es un **contextNode** de hoja de lápiz. Si no se establece correctamente esta ubicación y la información del subnodo o del trazo, se producirá una **excepción InvalidOperation.** Los subnodos de un **contenedor ContextNode** se pueden establecer como rellenados parcialmente, en cuyo caso se generarán más eventos **PopulateContextNode** si **InkAnalyzer** determina que serán necesarios para la operación de análisis actual.

En las tablas siguientes se describe cuándo se genera el evento [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) a lo largo del uso de [**InkAnalyzer.**](inkanalyzer.md)

Una vez [**que InkAnalyzer**](inkanalyzer.md) haya calculado algunas restuls, volverá a la aplicación para actualizar los resultados. El primer evento que se genera es [**el evento InkAnalyzerStateChanging.**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Este evento simplemente indica a la aplicación que el estado del árbol del objeto **InkAnalyzer** está a punto de cambiar. Esto proporciona a las aplicaciones la oportunidad de establecer [**la marca PartiallyPopulated**](icontextnode-setpartiallypopulated.md) en true en cualquier [**ContextNodes**](icontextnodes.md) que tenga el estado almacenado en otro lugar. A **continuación, InkAnalyzer** genera una serie de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) para determinar el estado actual de los datos. Una vez que se haya disuadido, se impulsa una operación de conciliación para determinar qué resultados en segundo plano todavía se pueden aplicar.

Para aplicar los resultados a [**InkAnalyzer,**](inkanalyzer.md) se genera una serie de eventos de modificación de árbol. Los eventos de modificación de árbol describen, paso a paso, todos los cambios necesarios para actualizar los resultados. Estos eventos están diseñados para controlarse en sucesión sin interuption ni canceling. Si la operación de análisis se cancela (a través del método [**Abort)**](iinkanalyzer-abort.md) durante el procesamiento de los eventos de modificación del árbol, el estado de **InkAnalyzer** no será válido y es posible que sea necesario volver a analizar todo el documento.

En las tablas siguientes se describe cuándo se genera el evento de modificación del árbol a lo largo del uso de InkAnalyzer. Las tablas hacen referencia a las marcas de tiempo que se muestran a continuación del diagrama de flujo de eventos.

![iimage que muestra el flujo entre la interfaz de usuario de la aplicación y el analizador de fondo](images/7a0a54af-889e-43ed-8689-7f2d685567bf.jpg)

### <a name="adding-a-stroke"></a>Agregar un trazo



| Marca de tiempo | Tipo de evento o propósito | Evento generado | Comentario                          |
|--------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T1, T5 y T9<br/> | \[Dentro de la llamada al evento de exploración de árbol AddStroke() \] \[\]<br/> | [**Evento PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) que se genera<br/> | Podría haber n número de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) que se generaran en función del número de [**ContextNodes**](icontextnodes.md) sin clasificar que exista con un valor [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) establecido en true.<br/> |
| T1, T5 y T9<br/> | \[Evento de modificación de árbol\]<br/>                                  | [**Evento ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) que se ha producido<br/>   | Solo habrá un evento [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) que se genera como resultado de llamar al [**método AddStroke.**](iinkanalyzer-addstroke.md) Todos los trazos se agregan al mismo [**ContextNode**](icontextnode.md)sin clasificar.<br/>                      |



 

### <a name="deleting-a-stroke"></a>Eliminación de un trazo



| Marca de tiempo | Tipo de evento o propósito | Evento generado | Comentario                          |
|---------------------------|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T2, T6 y T10<br/> | \[Dentro de la llamada a [**RemoveStroke**](iinkanalyzer-removestroke.md)() \] \[ Tree exploration Event\]<br/> | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Evento producido<br/> | Podría haber una serie de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) que se generaron en función de cuántos [**ContextNodes**](icontextnodes.md) relacionados con los trazos que se eliminan tienen un valor [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) de true.<br/> |
| T2, T6 y T10<br/> | \[Evento de modificación de árbol\]<br/>                                                                          | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Evento producido<br/> | Podría haber cualquier número de eventos [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) que se generaron, dependiendo del contenido de entrada de lápiz que se elimine y de la estructura analysis actual.<br/>                                                                                                       |



 

### <a name="calling-the-backgroundanalyze-method"></a>Llamada al método BackgroundAnalyze



| Marca de tiempo | Tipo de evento o propósito | Evento generado | Comentario                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T3<br/>         | \[Dentro de la llamada a [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)() \] \[ Tree exploration Event\]<br/> | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Evento producido<br/> | Podría haber n número de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) que se generaron, en función del número de [**ContextNodes**](icontextnodes.md) en todo el árbol que tengan un valor [**PartiallyPopulated**](icontextnode-createpartiallypopulatedsubnode.md) de true (un evento por [**ContextNode**](icontextnode.md) necesario en la operación analysis actual).<br/> |



 

### <a name="after-the-call-to-backgroundanalyze-returns"></a>Después de que la llamada a BackgroundAnalyze() vuelva



| Marca de tiempo | Tipo de evento o propósito | Evento generado | Comentario                          |
|-----------------------|---------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------|
| T3 a T7<br/>   | \[Eventos producidos desde el subproceso BG\]<br/> | Evento de actividad producido<br/> | Durante este período de análisis en segundo plano se generarán varios eventos de actividad.<br/> |



 

### <a name="when-intermediateresults-are-ready"></a>Cuando IntermediateResults está listo



| Marca de tiempo | Tipo de evento o propósito | Evento generado | Comentario                          |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T7 a T8<br/>   | \[Eventos que se han producido desde el subproceso BG, lo que significa el inicio de la primera operación de conciliación\]<br/> | [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Evento producido<br/>         | Solo se [**ha producido un evento InkAnalyzerStateChanging.**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Este evento se genera antes de inspeccionar el estado de [**InkAnalyzer,**](inkanalyzer.md)lo que da a la aplicación la oportunidad de establecer el valor [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) en cualquier nodo o realizar cualquier bloqueo de documento local necesario.<br/> |
| T7 a T8<br/>   | \[Evento de exploración de árbol\]<br/>                                                              | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Evento producido<br/>                   | Podría haber n número de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) que se generaron, dependiendo del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                                               |
| T7 a T8<br/>   | \[Evento de modificación de árbol\]<br/>                                                             | [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) Evento producido<br/>                     | Podría haber n número de eventos [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) que se generaran, en función del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                                                 |
| T7 a T8<br/>   | \[Evento de modificación de árbol\]<br/>                                                             | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Evento producido<br/>                   | Podría haber n número de eventos [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) que se generaron, en función del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                                               |
| T7 a T8<br/>   | \[Evento de modificación de árbol\]<br/>                                                             | [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | Podría haber n número de eventos [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) producidos, dependiendo del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                               |
| T7 a T8<br/>   | \[Evento de modificación de árbol\]<br/>                                                             | [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | Podría haber n eventos [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md) en función del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                                         |
| T7 a T8<br/>   | \[Evento de modificación de árbol\]<br/>                                                             | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | Podría haber n eventos [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md) producidos, dependiendo del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                                                     |
| T7 a T8<br/>   | \[Evento de modificación de árbol\]<br/>                                                             | [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | Podría haber n número de eventos [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) producidos, en función del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                                           |
| T7 a T8<br/>   | \[Evento de modificación de árbol\]<br/>                                                             | [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | Podría haber n número de eventos [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) producidos, en función del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                                       |
| T7 a T8<br/>   | \[Evento de modificación de árbol\]<br/>                                                             | [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) Evento producido<br/> | Podría haber n número de eventos [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) producidos, en función del contenido de entrada de lápiz. **ContextNodePropertiesUpdated** está programado para ser rasied después de que todos los demás eventos de modificación de [**ContextNode**](icontextnode.md) se han producido durante este [**período de conciliación.**](iinkanalyzer-reconcile.md)<br/>              |
| T7 a T8<br/>   | \[Evento que indica el final de la primera operación de conciliación\]<br/>                            | [**IntermediateResults**](-ianalysisevents-intermediateresults.md) Evento producido<br/>                        | Solo se genera un evento [**IntermediateResults**](-ianalysisevents-intermediateresults.md) por operación de análisis.<br/>                                                                                                                                                                                                                                                                  |



 

### <a name="after-intermediateresults-have-been-handled"></a>Una vez que se han manipulado los IntermediateResults



| Marca de tiempo | Tipo de evento o propósito | Evento generado | Comentario                          |
|-----------------------|---------------------------------------------|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| T8 a T11<br/>  | \[Eventos producidos desde el subproceso BG\]<br/> | [**Actividad**](-ianalysisevents-activity.md) Evento producido<br/> | Durante [**este período**](-ianalysisevents-activity.md) de análisis en segundo plano se generarán varios eventos de actividad.<br/> |



 

### <a name="when-final-results-are-ready"></a>Cuando los resultados finales estén listos



| Marca de tiempo | Tipo de evento o propósito | Evento generado | Comentario                          |
|-----------------------|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T11 a T12<br/> | \[Eventos producidos desde el subproceso BG, lo que significa el inicio de la segunda operación de conciliación\]<br/> | [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Evento producido<br/>         | Solo se [**ha producido un evento InkAnalyzerStateChanging.**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Este evento se genera antes de inspeccionar el estado de [**InkAnalyzer,**](inkanalyzer.md)lo que ofrece a la aplicación la oportunidad de establecer el valor [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) en cualquier nodo o realizar cualquier bloqueo de documento local necesario.<br/> |
| T11 a T12<br/> | \[Evento de exploración de árbol\]<br/>                                                               | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Evento producido<br/>                   | Podría haber cualquier número de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) producidos, en función del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                                             |
| T11 a T12<br/> | \[Evento de modificación de árbol\]<br/>                                                              | [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) Evento producido<br/>                     | Podría haber cualquier número de eventos [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) producidos, dependiendo del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                                               |
| T11 a T12<br/> | \[Evento de modificación de árbol\]<br/>                                                              | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Evento producido<br/>                   | Podría haber cualquier número de eventos [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) producidos, dependiendo del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                                             |
| T11 a T12<br/> | \[Evento de modificación de árbol\]<br/>                                                              | [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | Podría haber cualquier número de eventos [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) producidos, en función del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                             |
| T11 a T12<br/> | \[Evento de modificación de árbol\]<br/>                                                              | [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | Puede haber cualquier número de eventos [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md) producidos, en función del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                                       |
| T11 a T12<br/> | \[Evento de modificación de árbol\]<br/>                                                              | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | Puede haber cualquier número de eventos [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md) producidos, en función del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                                                   |
| T11 a T12<br/> | \[Evento de modificación de árbol\]<br/>                                                              | [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | Puede haber cualquier número de eventos [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) producidos, en función del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                                         |
| T11 a T12<br/> | \[Evento de modificación de árbol\]<br/>                                                              | [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | Podría haber cualquier número de eventos [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) producidos, en función del contenido de entrada de lápiz.<br/>                                                                                                                                                                                                                                     |
| T11 a T12<br/> | \[Evento de modificación de árbol\]<br/>                                                              | [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) Evento producido<br/> | Podría haber cualquier número de eventos [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) producidos, en función del contenido de entrada de lápiz. **ContextNodePropertiesUpdated** está programado para ser rasied después de que todos los demás eventos de modificación de [**ContextNode**](icontextnode.md) se han producido durante este [**período de conciliación.**](iinkanalyzer-reconcile.md)<br/>            |
| T11 a T12<br/> | \[Evento que indica el final de la segunda operación de conciliación\]<br/>                            | [**Resultados**](-ianalysisevents-results.md) Evento producido<br/>                                                | Solo se [**genera un**](-ianalysisevents-results.md) evento Results por operación de análisis.<br/>                                                                                                                                                                                                                                                                                          |



 

 

 




