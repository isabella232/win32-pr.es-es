---
description: Proporciona acceso al análisis de diseño, la clasificación de escritura y de dibujo y el reconocimiento de escritura a mano.
ms.assetid: 3a19db78-df14-43c2-9e3e-8cf674aa7b9c
title: Interfaz IInkAnalyzer (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd1bca0a00cbe95c4d32b2dfad8afe6c5db8ad63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360922"
---
# <a name="iinkanalyzer-interface"></a>Interfaz IInkAnalyzer

Proporciona acceso al análisis de diseño, la clasificación de escritura y de dibujo y el reconocimiento de escritura a mano.

## <a name="members"></a>Miembros

La interfaz **IInkAnalyzer** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IInkAnalyzer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IInkAnalyzer** tiene estos métodos.



| Método                                                                                                  | Descripción                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aborta**](iinkanalyzer-abort.md)                                                                     | Cancela la operación de análisis actual.<br/>                                                                                                                                           |
| [**AddStroke**](iinkanalyzer-addstroke.md)                                                             | Agrega datos de trazo para un solo trazo al **IInkAnalyzer** y asigna el identificador de referencia cultural del subproceso de entrada activo al trazo.<br/>                                              |
| [**AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)                                       | Agrega datos de trazo para un solo trazo al **IInkAnalyzer** y asigna un identificador de referencia cultural específico al trazo.<br/>                                                             |
| [**AddStrokes**](iinkanalyzer-addstrokes.md)                                                           | Agrega datos de trazo para varios trazos al **IInkAnalyzer** y asigna el identificador de referencia cultural del subproceso de entrada activo a los trazos.<br/>                                            |
| [**AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)                                     | Agrega datos de trazo para varios trazos al **IInkAnalyzer** y asigna el identificador de referencia cultural especificado a los trazos.<br/>                                                        |
| [**AddStrokesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)                       | Agrega datos de trazo para varios trazos a un nodo de reconocedor personalizado.<br/>                                                                                                                |
| [**AddStrokeToCustomRecognizer**](iinkanalyzer-addstroketocustomrecognizer.md)                         | Agrega datos de trazo para un solo trazo a un nodo de reconocedor personalizado.<br/>                                                                                                                 |
| [**Examina**](iinkanalyzer-analyze.md)                                                                 | Realiza análisis sincrónicos de tinta.<br/>                                                                                                                                                |
| [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)                                             | Realiza el análisis de tinta asincrónica.<br/>                                                                                                                                               |
| [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md)                                                 | Borra los datos de los paquetes de trazos de **IInkAnalyzer**.<br/>                                                                                                                              |
| [**CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)                                           | Agrega un nuevo nodo de sugerencia de análisis con un área infinita a **IInkAnalyzer**.<br/>                                                                                                      |
| [**CreateContextNodes**](iinkanalyzer-createcontextnodes.md)                                           | Crea un objeto [**IContextNodes**](icontextnodes.md) .<br/>                                                                                                                         |
| [**CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)                                   | Crea un nuevo nodo de reconocedor personalizado para el **IInkAnalyzer**.<br/>                                                                                                                    |
| [**DeleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)                                           | Quita una sugerencia de análisis de **IInkAnalyzer**.<br/>                                                                                                                               |
| [**FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)                                               | Recupera todos los nodos de hoja de tinta.<br/>                                                                                                                                              |
| [**FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)                           | Recupera los nodos de hoja de tinta que contienen los trazos especificados.<br/>                                                                                                                  |
| [**FindLeafNodes**](iinkanalyzer-findleafnodes.md)                                                     | Recupera todos los nodos hoja.<br/>                                                                                                                                                  |
| [**FindNode**](iinkanalyzer-findnode.md)                                                               | Recupera el objeto [**IContextNode**](icontextnode.md) para un identificador único global (GUID) especificado.<br/>                                                                      |
| [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md)                                                 | Recupera todos los objetos [**IContextNode**](icontextnode.md) del tipo especificado.<br/>                                                                                          |
| [**FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)                             | Recupera todos los objetos [**IContextNode**](icontextnode.md) del tipo especificado que contienen los trazos especificados.<br/>                                                       |
| [**FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)                               | Recupera todos los objetos [**IContextNode**](icontextnode.md) del tipo especificado que son descendientes del objeto **IContextNode** especificado.<br/>                            |
| [**FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)                                     | Recupera todos los objetos [**IContextNode**](icontextnode.md) que coinciden con los criterios especificados.<br/>                                                                              |
| [**FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)                   | Recupera todos los objetos [**IContextNode**](icontextnode.md) que coinciden con los criterios especificados y son descendientes del objeto **IContextNode** especificado.<br/>                 |
| [**GetAlternates**](iinkanalyzer-getalternates.md)                                                     | Recupera 10 alternativas de análisis para todas las entradas de lápiz asociadas a **IInkAnalyzer**.<br/>                                                                                                |
| [**GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)                       | Recupera alternativas de análisis para los nodos de una colección [**IContextNodes**](icontextnodes.md) especificada.<br/>                                                                     |
| [**GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)                                 | Recupera alternativas de análisis para los trazos con los identificadores de trazo especificados.<br/>                                                                                              |
| [**GetAnalysisHints**](iinkanalyzer-getanalysishints.md)                                               | Recupera todos los objetos [**IContextNode**](icontextnode.md) de la sugerencia de análisis que están asociados a **IInkAnalyzer**.<br/>                                                        |
| [**GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)                                   | Recupera todos los objetos [**IContextNode**](icontextnode.md) de la sugerencia de análisis que están asociados a **IInkAnalyzer** y que tienen el nombre especificado.<br/>                       |
| [**GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)                                               | Recupera marcas que controlan cómo el **IInkAnalyzer** realiza el análisis de tinta.<br/>                                                                                                      |
| [**GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)                                                   | Recupera el área que ha cambiado desde la última operación de análisis.<br/>                                                                                                            |
| [**GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)         | Recupera una colección ordenada de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .<br/>                                                                              |
| [**GetNodesFromTextRange**](iinkanalyzer-getnodesfromtextrange.md)                                     | Recupera una colección de objetos [**IContextNode**](icontextnode.md) que son pertinentes para el intervalo de texto especificado para los nodos de contexto especificados.<br/>                             |
| [**GetRecognizedString**](iinkanalyzer-getrecognizedstring.md)                                         | Recupera la cadena de resultado mejor de la operación de reconocimiento para todo el árbol de nodos de contexto en el **IInkAnalyzer**.<br/>                                                           |
| [**GetRootNode**](iinkanalyzer-getrootnode.md)                                                         | Recupera el [**IContextNode**](icontextnode.md) raíz del árbol de contexto del objeto **IInkAnalyzer** .<br/>                                                                            |
| [**GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md)                                         | Recupera el identificador de configuración regional del trazo especificado.<br/>                                                                                                                          |
| [**GetStrokeType**](iinkanalyzer-getstroketype.md)                                                     | Recupera el tipo del trazo especificado.<br/>                                                                                                                                       |
| [**GetTextRangeFromNodes**](iinkanalyzer-gettextrangefromnodes.md)                                     | Busca el intervalo de texto en la cadena reconocida que corresponde a una colección de objetos [**IContextNode**](icontextnode.md) .<br/>                                                   |
| [**IsAnalyzing**](iinkanalyzer-isanalyzing.md)                                                         | Recupera un valor que indica si el **IInkAnalyzer** está realizando el análisis de tinta.<br/>                                                                                             |
| [**LoadResults**](iinkanalyzer-loadresults.md)                                                         | Carga los resultados del análisis guardado en el **IInkAnalyzer**.<br/>                                                                                                                           |
| [**ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)                                           | Cambia la alternativa superior actual a la alternativa especificada y borra el tipo de confirmación de todos los objetos [**IContextNode**](icontextnode.md) asociados con la alternativa.<br/> |
| [**ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)           | Cambia la alternativa superior actual al [**IAnalysisAlternate**](ianalysisalternate.md)especificado.<br/>                                                                              |
| [**Reconcile**](iinkanalyzer-reconcile.md)                                                             | Determina qué partes de los resultados del análisis han cambiado durante el análisis de la tinta de fondo.<br/>                                                                                    |
| [**RemoveStroke**](iinkanalyzer-removestroke.md)                                                       | Quita el trazo especificado de **IInkAnalyzer**.<br/>                                                                                                                           |
| [**RemoveStrokes**](iinkanalyzer-removestrokes.md)                                                     | Quita los trazos especificados de **IInkAnalyzer**.<br/>                                                                                                                          |
| [**SaveResults**](iinkanalyzer-saveresults.md)                                                         | Guarda todos los resultados de análisis de un **IInkAnalyzer**.<br/>                                                                                                                               |
| [**SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)                                         | Guarda los resultados del análisis de una colección de nodos de contexto específica asociada a un **IInkAnalyzer**.<br/>                                                                                |
| [**SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)                                     | Guarda los resultados del análisis para los trazos especificados asociados a un **IInkAnalyzer**.<br/>                                                                                             |
| [**Search**](iinkanalyzer-search.md)                                                                   | Proporciona una búsqueda aproximada de mayúsculas y minúsculas basada en frases para los trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.<br/>                                      |
| [**SearchWithLanguageId**](iinkanalyzer-searchwithlanguageid.md)                                       | Proporciona una búsqueda aproximada de mayúsculas y minúsculas basada en frases para los trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.<br/>                                      |
| [**SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)                                               | Modifica las marcas que controlan cómo el **IInkAnalyzer** realiza el análisis de tinta.<br/>                                                                                                       |
| [**SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)                                                   | Modifica el área que ha cambiado desde la última operación de análisis.<br/>                                                                                                             |
| [**SetHighestPriorityInkAnalysisRecognizer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) | Mueve el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) especificado a la primera posición de la lista de reconocedores de tinta del objeto **IInkAnalyzer** .<br/>                      |
| [**SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md)                                         | Cambia el identificador de configuración regional del trazo especificado.<br/>                                                                                                                           |
| [**SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md)                                       | Cambia el identificador de configuración regional para los trazos especificados.<br/>                                                                                                                          |
| [**SetStrokesType**](iinkanalyzer-setstrokestype.md)                                                   | Cambia el tipo de los trazos especificados.<br/>                                                                                                                                        |
| [**SetStrokeType**](iinkanalyzer-setstroketype.md)                                                     | Cambia el tipo del trazo especificado.<br/>                                                                                                                                         |
| [**UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)                                             | Actualiza los datos del paquete para los trazos especificados.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Observaciones

**IInkAnalyzer** usa datos de paquetes de trazo para analizar la entrada manuscrita y no interactúa directamente con los objetos de la [**clase InkDisp**](inkdisp-class.md) o [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

Para agregar o quitar trazos de **IInkAnalyzer** para su análisis, use uno de los métodos siguientes.

-   [**IInkAnalyzer:: AddStroke (método)**](iinkanalyzer-addstroke.md)
-   [**IInkAnalyzer:: AddStrokes (método)**](iinkanalyzer-addstrokes.md)
-   [**IInkAnalyzer:: RemoveStroke (método)**](iinkanalyzer-removestroke.md)
-   [**IInkAnalyzer:: RemoveStrokes (método)**](iinkanalyzer-removestrokes.md)

Estos métodos actualizan la región desfasada (vea [**IInkAnalyzer:: GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)), que es la región para la que se analizan los trazos en la siguiente operación de análisis.

Para analizar la entrada de lápiz, use el método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o el método [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) . Durante el análisis, el **IInkAnalyzer** realiza el análisis de diseño, la clasificación del trazo y el reconocimiento de escritura a mano.

Para cambiar el análisis del diseño y la configuración de la clasificación del trazo, use la propiedad del [**método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md) .

Durante el análisis, el **IInkAnalyzer** recibe un número de eventos, incluidos los eventos generados durante el análisis en segundo plano. [**\_ IAnalysisProxyEvents**](-ianalysisproxyevents.md) admite las características del proxy de datos de **IInkAnalyzer**. Para obtener más información, consulte [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md). Para detener el proceso de análisis desde un controlador de eventos, llame al [**método IInkAnalyzer:: ABORT**](iinkanalyzer-abort.md).

Para modificar el idioma que usa el analizador de tinta para reconocer la escritura a mano, use el método [**IInkAnalyzer:: SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md) o [**IInkAnalyzer:: SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md). Para modificar el modo en que el analizador de tintas clasifica los trazos específicos, use el método [**IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) o [**IInkAnalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md).

**IInkAnalyzer** carga información de todos los reconocedores de tinta instalados. El [**método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) devuelve una colección [**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md) que contiene cada [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)disponible. Si más de un reconocedor de tinta admite un idioma específico, use el [**método IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) para establecer qué reconocedor de tinta controla los trazos para ese idioma.

El uso de sugerencias de análisis puede mejorar la precisión del reconocimiento proporcionando contexto adicional al analizador de tinta. La información de contexto adicional puede ayudar a que el analizador de tintas limite el número de resultados de reconocimiento posibles. Por ejemplo, puede restringir el ámbito definiendo Factoids y las palabras esperadas o estructurando la entrada en una guía de reconocimiento. Para obtener más información acerca de cómo proporcionar contexto al analizador de tinta, vea:

-   [**IInkAnalyzer:: CreateAnalysisHint (método)**](iinkanalyzer-createanalysishint.md)
-   [**IInkAnalyzer::D método eleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)
-   [**IInkAnalyzer:: GetAnalysisHints (método)**](iinkanalyzer-getanalysishints.md)
-   [**IInkAnalyzer:: GetAnalysisHintsByName (método)**](iinkanalyzer-getanalysishintsbyname.md)

El analizador de tinta representa los resultados del análisis como una cadena o como un árbol de objetos [**IContextNode**](icontextnode.md) . Para acceder a la cadena reconocida, use el [**método IInkAnalyzer:: GetRecognizedString**](iinkanalyzer-getrecognizedstring.md). Para tener acceso a la raíz del árbol de nodos de contexto, use el [**método IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md). El analizador de tinta tiene los siguientes métodos para buscar determinados nodos de contexto o texto.

-   [**IInkAnalyzer:: FindInkLeafNodes (método)**](iinkanalyzer-findinkleafnodes.md)
-   [**IInkAnalyzer:: FindInkLeafNodesForStrokes (método)**](iinkanalyzer-findinkleafnodesforstrokes.md)
-   [**IInkAnalyzer:: FindLeafNodes (método)**](iinkanalyzer-findleafnodes.md)
-   [**IInkAnalyzer:: FindNode (método)**](iinkanalyzer-findnode.md)
-   [**IInkAnalyzer:: FindNodesOfType (método)**](iinkanalyzer-findnodesoftype.md)
-   [**IInkAnalyzer:: FindNodesOfTypeForStrokes (método)**](iinkanalyzer-findnodesoftypeforstrokes.md)
-   [**IInkAnalyzer:: FindNodesOfTypeInSubTree (método)**](iinkanalyzer-findnodesoftypeinsubtree.md)
-   [**IInkAnalyzer:: FindNodesWithCallBack (método)**](iinkanalyzer-findnodeswithcallback.md)
-   [**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**](iinkanalyzer-findnodeswithcallbackinsubtree.md)

Para trabajar con resultados de análisis alternativos, use uno de los métodos siguientes.

-   [**IInkAnalyzer:: GetAlternates (método)**](iinkanalyzer-getalternates.md)
-   [**IInkAnalyzer:: GetAlternatesForContextNodes (método)**](iinkanalyzer-getalternatesforcontextnodes.md)
-   [**IInkAnalyzer:: GetAlternatesForStrokes (método)**](iinkanalyzer-getalternatesforstrokes.md)
-   [**IInkAnalyzer:: ModifyTopAlternate (método)**](iinkanalyzer-modifytopalternate.md)
-   [**IInkAnalyzer:: ModifyTopAlternateWithConfirmation (método)**](iinkanalyzer-modifytopalternatewithconfirmation.md)

Para guardar los resultados del análisis, use uno de los métodos siguientes.

-   [**IInkAnalyzer:: SaveResults (método)**](iinkanalyzer-saveresults.md)
-   [**IInkAnalyzer:: SaveResultsForNodes (método)**](iinkanalyzer-saveresultsfornodes.md)
-   [**IInkAnalyzer:: SaveResultsForStrokes (método)**](iinkanalyzer-saveresultsforstrokes.md)

Para cargar los resultados guardados, use el [**método IInkAnalyzer:: LoadResults**](iinkanalyzer-loadresults.md).

Para obtener más información sobre el uso de **IInkAnalyzer** para analizar la entrada de lápiz, consulte [información general del análisis de tinta](ink-analysis-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

