---
description: Proporciona acceso al análisis de diseño, la clasificación de escritura y dibujo y el reconocimiento de escritura a mano.
ms.assetid: 3a19db78-df14-43c2-9e3e-8cf674aa7b9c
title: Interfaz IInkAnalyzer (IACom.h)
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
ms.openlocfilehash: b37e6d72b87ac31bda7e6c9b0d6f9bf3d35af524eea201e446b50905447404b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939864"
---
# <a name="iinkanalyzer-interface"></a>Interfaz IInkAnalyzer

Proporciona acceso al análisis de diseño, la clasificación de escritura y dibujo y el reconocimiento de escritura a mano.

## <a name="members"></a>Miembros

La **interfaz IInkAnalyzer** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IInkAnalyzer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IInkAnalyzer** tiene estos métodos.



| Método                                                                                                  | Descripción                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aborta**](iinkanalyzer-abort.md)                                                                     | Cancela la operación de análisis actual.<br/>                                                                                                                                           |
| [**AddStroke**](iinkanalyzer-addstroke.md)                                                             | Agrega datos de trazo para un único trazo al **IInkAnalyzer** y asigna el identificador de referencia cultural del subproceso de entrada activo al trazo.<br/>                                              |
| [**AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)                                       | Agrega datos de trazo para un único trazo al **IInkAnalyzer** y asigna un identificador de referencia cultural específico al trazo.<br/>                                                             |
| [**AddStrokes**](iinkanalyzer-addstrokes.md)                                                           | Agrega datos de trazo para varios trazos al **IInkAnalyzer** y asigna el identificador de referencia cultural del subproceso de entrada activo a los trazos.<br/>                                            |
| [**AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)                                     | Agrega datos de trazo para varios trazos al **IInkAnalyzer** y asigna el identificador de referencia cultural especificado a los trazos.<br/>                                                        |
| [**AddStrokesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)                       | Agrega datos de trazo para varios trazos a un nodo de reconocedor personalizado.<br/>                                                                                                                |
| [**AddStrokeToCustomRecognizer**](iinkanalyzer-addstroketocustomrecognizer.md)                         | Agrega datos de trazo para un único trazo a un nodo de reconocedor personalizado.<br/>                                                                                                                 |
| [**Analizar**](iinkanalyzer-analyze.md)                                                                 | Realiza un análisis de entrada de lápiz sincrónica.<br/>                                                                                                                                                |
| [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)                                             | Realiza análisis de entrada de lápiz asincrónicos.<br/>                                                                                                                                               |
| [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md)                                                 | Borra los datos del paquete de trazo de **IInkAnalyzer.**<br/>                                                                                                                              |
| [**CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)                                           | Agrega un nuevo nodo de sugerencia de análisis con un área infinita a **IInkAnalyzer**.<br/>                                                                                                      |
| [**CreateContextNodes**](iinkanalyzer-createcontextnodes.md)                                           | Crea un [**objeto IContextNodes.**](icontextnodes.md)<br/>                                                                                                                         |
| [**CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)                                   | Crea un nuevo nodo de reconocedor personalizado para **IInkAnalyzer.**<br/>                                                                                                                    |
| [**DeleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)                                           | Quita una sugerencia de análisis de **IInkAnalyzer.**<br/>                                                                                                                               |
| [**FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)                                               | Recupera todos los nodos hoja de entrada de lápiz.<br/>                                                                                                                                              |
| [**FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)                           | Recupera los nodos hoja de entrada de lápiz que contienen los trazos especificados.<br/>                                                                                                                  |
| [**FindLeafNodes**](iinkanalyzer-findleafnodes.md)                                                     | Recupera todos los nodos hoja.<br/>                                                                                                                                                  |
| [**FindNode**](iinkanalyzer-findnode.md)                                                               | Recupera el [**objeto IContextNode**](icontextnode.md) para un identificador único global (GUID) especificado.<br/>                                                                      |
| [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md)                                                 | Recupera todos los objetos [**IContextNode**](icontextnode.md) del tipo especificado.<br/>                                                                                          |
| [**FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)                             | Recupera todos los objetos [**IContextNode**](icontextnode.md) del tipo especificado que contienen los trazos especificados.<br/>                                                       |
| [**FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)                               | Recupera todos los objetos [**IContextNode**](icontextnode.md) del tipo especificado que son descendientes del objeto **IContextNode** especificado.<br/>                            |
| [**FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)                                     | Recupera todos los objetos [**IContextNode**](icontextnode.md) que coinciden con los criterios especificados.<br/>                                                                              |
| [**FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)                   | Recupera todos los objetos [**IContextNode**](icontextnode.md) que coinciden con los criterios especificados y son descendientes del objeto **IContextNode** especificado.<br/>                 |
| [**GetAlternates**](iinkanalyzer-getalternates.md)                                                     | Recupera 10 alternativas de análisis para toda la entrada de lápiz asociada a **IInkAnalyzer.**<br/>                                                                                                |
| [**GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)                       | Recupera alternativas de análisis para los nodos de una colección [**IContextNodes**](icontextnodes.md) especificada.<br/>                                                                     |
| [**GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)                                 | Recupera alternativas de análisis para los trazos con los identificadores de trazo especificados.<br/>                                                                                              |
| [**GetAnalysisHints**](iinkanalyzer-getanalysishints.md)                                               | Recupera todos los objetos [**IContextNode**](icontextnode.md) de la sugerencia de análisis que están asociados a **IInkAnalyzer.**<br/>                                                        |
| [**GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)                                   | Recupera todos los objetos [**IContextNode**](icontextnode.md) de la sugerencia de análisis que están asociados a **IInkAnalyzer** y que tienen el nombre especificado.<br/>                       |
| [**GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)                                               | Recupera marcas que controlan cómo **IInkAnalyzer** realiza el análisis de entrada de lápiz.<br/>                                                                                                      |
| [**GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)                                                   | Recupera el área que ha cambiado desde la última operación de análisis.<br/>                                                                                                            |
| [**GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)         | Recupera una colección ordenada de [**objetos IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)<br/>                                                                              |
| [**GetNodesFromTextRange**](iinkanalyzer-getnodesfromtextrange.md)                                     | Recupera una colección de [**objetos IContextNode**](icontextnode.md) que son relevantes para el intervalo de texto especificado para los nodos de contexto especificados.<br/>                             |
| [**GetRecognizedString**](iinkanalyzer-getrecognizedstring.md)                                         | Recupera la cadena de mejor resultado de la operación de reconocimiento para todo el árbol de nodos de contexto en **IInkAnalyzer**.<br/>                                                           |
| [**GetRootNode**](iinkanalyzer-getrootnode.md)                                                         | Recupera el [**IContextNode raíz**](icontextnode.md) del árbol de contexto del objeto **IInkAnalyzer.**<br/>                                                                            |
| [**GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md)                                         | Recupera el identificador de configuración regional del trazo especificado.<br/>                                                                                                                          |
| [**GetStrokeType**](iinkanalyzer-getstroketype.md)                                                     | Recupera el tipo del trazo especificado.<br/>                                                                                                                                       |
| [**GetTextRangeFromNodes**](iinkanalyzer-gettextrangefromnodes.md)                                     | Busca el intervalo de texto en la cadena reconocida que corresponde a una colección de [**objetos IContextNode.**](icontextnode.md)<br/>                                                   |
| [**IsAnalyzing**](iinkanalyzer-isanalyzing.md)                                                         | Recupera un valor que indica si **IInkAnalyzer** está realizando análisis de entrada de lápiz.<br/>                                                                                             |
| [**LoadResults**](iinkanalyzer-loadresults.md)                                                         | Carga los resultados de análisis guardados **en IInkAnalyzer.**<br/>                                                                                                                           |
| [**ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)                                           | Cambia la alternativa superior actual a la alternativa especificada y borra el tipo de confirmación para todos los [**objetos IContextNode**](icontextnode.md) asociados a la alternativa.<br/> |
| [**ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)           | Cambia la alternativa superior actual a la propiedad [**IAnalysisAlternate especificada.**](ianalysisalternate.md)<br/>                                                                              |
| [**Reconcile**](iinkanalyzer-reconcile.md)                                                             | Determina qué partes de los resultados del análisis han cambiado durante el análisis de entrada de lápiz en segundo plano.<br/>                                                                                    |
| [**RemoveStroke**](iinkanalyzer-removestroke.md)                                                       | Quita el trazo especificado de **IInkAnalyzer.**<br/>                                                                                                                           |
| [**RemoveStrokes**](iinkanalyzer-removestrokes.md)                                                     | Quita los trazos especificados de **IInkAnalyzer.**<br/>                                                                                                                          |
| [**SaveResults**](iinkanalyzer-saveresults.md)                                                         | Guarda todos los resultados de análisis de **un IInkAnalyzer.**<br/>                                                                                                                               |
| [**SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)                                         | Guarda los resultados del análisis de una colección de nodos de contexto específica asociada a **un IInkAnalyzer.**<br/>                                                                                |
| [**SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)                                     | Guarda los resultados del análisis de los trazos especificados asociados a **un IInkAnalyzer.**<br/>                                                                                             |
| [**Search**](iinkanalyzer-search.md)                                                                   | Proporciona una búsqueda aproximada basada en frases sin mayúsculas de minúsculas para trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.<br/>                                      |
| [**SearchWithLanguageId**](iinkanalyzer-searchwithlanguageid.md)                                       | Proporciona una búsqueda aproximada basada en frases sin mayúsculas de minúsculas para trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.<br/>                                      |
| [**SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)                                               | Modifica las marcas que controlan cómo **IInkAnalyzer** realiza el análisis de entrada de lápiz.<br/>                                                                                                       |
| [**SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)                                                   | Modifica el área que ha cambiado desde la última operación de análisis.<br/>                                                                                                             |
| [**SetHighestPriorityInkAnalysisRecognizer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) | Mueve el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) especificado a la primera posición de la lista de reconocedores de lápiz del objeto **IInkAnalyzer.**<br/>                      |
| [**SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md)                                         | Cambia el identificador de configuración regional del trazo especificado.<br/>                                                                                                                           |
| [**SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md)                                       | Cambia el identificador de configuración regional de los trazos especificados.<br/>                                                                                                                          |
| [**SetStrokesType**](iinkanalyzer-setstrokestype.md)                                                   | Cambia el tipo de los trazos especificados.<br/>                                                                                                                                        |
| [**SetStrokeType**](iinkanalyzer-setstroketype.md)                                                     | Cambia el tipo del trazo especificado.<br/>                                                                                                                                         |
| [**UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)                                             | Actualiza los datos del paquete para los trazos especificados.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Comentarios

**IInkAnalyzer** usa datos de paquetes de trazo para analizar la entrada de lápiz y no interactúa directamente con los objetos [**InkDisp Class**](inkdisp-class.md) o [InkStrokes Collection.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))

Para agregar o quitar trazos a **IInkAnalyzer** para su análisis, use uno de los métodos siguientes.

-   [**IInkAnalyzer::AddStroke (Método)**](iinkanalyzer-addstroke.md)
-   [**IInkAnalyzer::AddStrokes (Método)**](iinkanalyzer-addstrokes.md)
-   [**IInkAnalyzer::RemoveStroke (Método)**](iinkanalyzer-removestroke.md)
-   [**IInkAnalyzer::RemoveStrokes (Método)**](iinkanalyzer-removestrokes.md)

Estos métodos actualizan la región desusada (vea [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)), que es la región para la que se analizan los trazos en la siguiente operación de análisis.

Para analizar la entrada de lápiz, use el método [**IInkAnalyzer::Analyze o**](iinkanalyzer-analyze.md) el método [**IInkAnalyzer::BackgroundAnalyze.**](iinkanalyzer-backgroundanalyze.md) Durante el análisis, **IInkAnalyzer** realiza análisis de diseño, clasificación de trazos y reconocimiento de escritura a mano.

Para cambiar la configuración del análisis de diseño y la clasificación de trazos, use la propiedad [**IInkAnalyzer::SetAnalysisModes (Método).**](iinkanalyzer-setanalysismodes.md)

Durante el análisis, **IInkAnalyzer** recibe una serie de eventos, incluidos los eventos generados durante el análisis en segundo plano. [**\_ IAnalysisProxyEvents**](-ianalysisproxyevents.md) admite las características de proxy de datos de **IInkAnalyzer.** Para obtener más información, vea [Proxy de datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md) Para detener el proceso de análisis desde dentro de un controlador de eventos, llame al [**método IInkAnalyzer::Abort**](iinkanalyzer-abort.md).

Para modificar el lenguaje que usa el analizador de lápiz para reconocer la escritura a mano, use el método [**IInkAnalyzer::SetStrokeLanguageId o**](iinkanalyzer-setstrokelanguageid.md) el método [**IInkAnalyzer::SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md). Para modificar cómo el analizador de entrada de lápiz clasifica trazos específicos, use el método [**IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md) o el método [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md).

**IInkAnalyzer** carga información para todos los reconocedores de lápiz instalados. [**El método IInkAnalyzer::GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) devuelve una colección [**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md) que contiene cada [**IInkAnalysisRecognizer disponible.**](iinkanalysisrecognizer.md) Si más de un reconocedor de lápiz admite un lenguaje específico, use [**IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer (Método)**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) para establecer qué reconocedor de lápiz controla los trazos de ese lenguaje.

El uso de sugerencias de análisis puede mejorar la precisión del reconocimiento proporcionando contexto adicional al analizador de lápiz. La información de contexto adicional puede ayudar al analizador de lápiz a limitar el número de posibles resultados de reconocimiento. Por ejemplo, puede restringir el ámbito definiendo factoids y palabras esperadas o estructurando la entrada en una guía de reconocimiento. Para obtener más información sobre cómo proporcionar contexto al analizador de entrada de lápiz, consulte:

-   [**IInkAnalyzer::CreateAnalysisHint (Método)**](iinkanalyzer-createanalysishint.md)
-   [**IInkAnalyzer::D eleteAnalysisHint (Método)**](iinkanalyzer-deleteanalysishint.md)
-   [**IInkAnalyzer::GetAnalysisHints (Método)**](iinkanalyzer-getanalysishints.md)
-   [**IInkAnalyzer::GetAnalysisHintsByName (Método)**](iinkanalyzer-getanalysishintsbyname.md)

El analizador de lápiz representa los resultados del análisis como una cadena o como un árbol de [**objetos IContextNode.**](icontextnode.md) Para obtener acceso a la cadena reconocida, use [**el método IInkAnalyzer::GetRecognizedString**](iinkanalyzer-getrecognizedstring.md). Para acceder a la raíz del árbol de nodos de contexto, use el método [**IInkAnalyzer::GetRootNode**](iinkanalyzer-getrootnode.md). El analizador de lápiz tiene los métodos siguientes para buscar nodos de contexto o texto específicos.

-   [**IInkAnalyzer::FindInkLeafNodes (Método)**](iinkanalyzer-findinkleafnodes.md)
-   [**IInkAnalyzer::FindInkLeafNodesForStrokes (Método)**](iinkanalyzer-findinkleafnodesforstrokes.md)
-   [**IInkAnalyzer::FindLeafNodes (Método)**](iinkanalyzer-findleafnodes.md)
-   [**IInkAnalyzer::FindNode (Método)**](iinkanalyzer-findnode.md)
-   [**IInkAnalyzer::FindNodesOfType (Método)**](iinkanalyzer-findnodesoftype.md)
-   [**IInkAnalyzer::FindNodesOfTypeForStrokes (Método)**](iinkanalyzer-findnodesoftypeforstrokes.md)
-   [**IInkAnalyzer::FindNodesOfTypeInSubTree (Método)**](iinkanalyzer-findnodesoftypeinsubtree.md)
-   [**IInkAnalyzer::FindNodesWithCallBack (Método)**](iinkanalyzer-findnodeswithcallback.md)
-   [**IInkAnalyzer::FindNodesWithCallBackInSubTree (Método)**](iinkanalyzer-findnodeswithcallbackinsubtree.md)

Para trabajar con resultados de análisis alternativos, use uno de los métodos siguientes.

-   [**IInkAnalyzer::GetAlternates (Método)**](iinkanalyzer-getalternates.md)
-   [**IInkAnalyzer::GetAlternatesForContextNodes (Método)**](iinkanalyzer-getalternatesforcontextnodes.md)
-   [**IInkAnalyzer::GetAlternatesForStrokes (Método)**](iinkanalyzer-getalternatesforstrokes.md)
-   [**IInkAnalyzer::ModifyTopAlternate (Método)**](iinkanalyzer-modifytopalternate.md)
-   [**IInkAnalyzer::ModifyTopAlternateWithConfirmation (Método)**](iinkanalyzer-modifytopalternatewithconfirmation.md)

Para guardar los resultados del análisis, use uno de los métodos siguientes.

-   [**IInkAnalyzer::SaveResults (Método)**](iinkanalyzer-saveresults.md)
-   [**IInkAnalyzer::SaveResultsForNodes (Método)**](iinkanalyzer-saveresultsfornodes.md)
-   [**IInkAnalyzer::SaveResultsForStrokes (Método)**](iinkanalyzer-saveresultsforstrokes.md)

Para cargar los resultados guardados, use [**el método IInkAnalyzer::LoadResults**](iinkanalyzer-loadresults.md).

Para obtener más información sobre el uso de **IInkAnalyzer para** analizar la entrada de lápiz, vea [Ink Analysis Overview](ink-analysis-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
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

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

