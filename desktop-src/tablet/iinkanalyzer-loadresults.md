---
description: Carga los resultados del análisis guardado en el IInkAnalyzer.
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: 'IInkAnalyzer:: LoadResults (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.LoadResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 76c7fed63b38f1b4fc058fbe7676a727c2d47f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497560"
---
# <a name="iinkanalyzerloadresults-method"></a>IInkAnalyzer:: LoadResults (método)

Carga los resultados del análisis guardado en el [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LoadResults(
  [in]          ULONG        ulDataSize,
  [in]          BYTE         *pbSerializedResults,
  [in]          ULONG        ulStrokeIdsCount,
  [in]          LONG         *plOriginalStrokeIds,
  [in]          LONG         *plNewStrokeIds,
  [out, retval] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulDataSize* \[ de\]
</dt> <dd>

Número de bytes de *pbSerializedResults*.

</dd> <dt>

*pbSerializedResults* \[ de\]
</dt> <dd>

Los resultados del análisis serializado.

</dd> <dt>

*ulStrokeIdsCount* \[ de\]
</dt> <dd>

Número de identificadores de trazo.

</dd> <dt>

*plOriginalStrokeIds* \[ de\]
</dt> <dd>

Matriz de identificadores de trazo originales.

</dd> <dt>

*plNewStrokeIds* \[ de\]
</dt> <dd>

Matriz de nuevos identificadores de trazo.

</dd> <dt>

*pfSuccessful* \[ out, retval\]
</dt> <dd>

**Variante \_ TRUE** si la carga se realizó correctamente; de lo contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Cuando el [**IInkAnalyzer**](iinkanalyzer.md) agrega un [**IContextNode**](icontextnode.md) de los resultados guardados, asigna un nuevo identificador único global (GUID) a **IContextNode** (vea [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md) y [propiedades del nodo de contexto](context-node-properties.md)).

Este método agrega los resultados del análisis guardado al árbol [**IContextNode**](icontextnode.md) existente. Para asegurarse de que los resultados combinados se ordenen correctamente, agregue el área que contiene los nodos de contexto cargados a la región desfasada del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea el [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) y vuelva a analizar la tinta.

Los métodos de método [**IInkAnalyzer:: SaveResults**](iinkanalyzer-saveresults.md), [**IInkAnalyzer:: SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)y [**IInkAnalyzer:: SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md) no guardan los datos del paquete junto con los resultados del análisis.

Cada identificador de *plOriginalStrokeIds* es el identificador del trazo del trazo en los resultados del análisis guardado. Cada identificador de *plNewStrokeIds* es el nuevo identificador con el que se va a reemplazar el identificador original en los resultados del análisis cargado.

Si una sugerencia de análisis guardado entra en conflicto con una sugerencia de análisis existente, el [**IInkAnalyzer**](iinkanalyzer.md) no carga la sugerencia guardada, sino que carga el resto de los resultados guardados. Sin embargo, si **IInkAnalyzer** carga los resultados de un trazo que se encuentra dentro del área de una sugerencia de análisis guardado que el **IInkAnalyzer** no carga, **IInkAnalyzer** agrega el rectángulo de selección del trazo a la región desfasada del objeto **IInkAnalyzer** . Además, si **IInkAnalyzer** carga los resultados de un trazo que se encuentra dentro de un área de la sugerencia de análisis existente, el **IInkAnalyzer** también agrega el rectángulo de selección del trazo a la región desfasada del objeto **IInkAnalyzer** . Para obtener más información acerca de las sugerencias de análisis, consulte propiedades de la [sugerencia de análisis](analysis-hint-properties.md).

Este método puede generar los eventos [**\_ IAnalysisProxyEvents:: ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_ IAnalysisProxyEvents:: ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)y [**\_ IAnalysisProxyEvents:: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) cuando carga los resultados guardados.

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

[**IInkAnalyzer:: GetDirtyRegion (método)**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer:: SetDirtyRegion (método)**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer:: SaveResults (método)**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**IInkAnalyzer:: SaveResultsForNodes (método)**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IInkAnalyzer:: SaveResultsForStrokes (método)**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




