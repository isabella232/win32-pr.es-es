---
description: Carga los resultados de análisis guardados en IInkAnalyzer.
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: Método IInkAnalyzer::LoadResults (IACom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572397"
---
# <a name="iinkanalyzerloadresults-method"></a>IInkAnalyzer::LoadResults (método)

Carga los resultados de análisis guardados [**en IInkAnalyzer.**](iinkanalyzer.md)

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

*ulDataSize* \[ En\]
</dt> <dd>

Número de bytes de *pbSerializedResults.*

</dd> <dt>

*pbSerializedResults* \[ En\]
</dt> <dd>

Resultados del análisis serializado.

</dd> <dt>

*ulStrokeIdsCount* \[ En\]
</dt> <dd>

Número de identificadores de trazo.

</dd> <dt>

*plOriginalStrokeIds* \[ En\]
</dt> <dd>

Matriz de identificadores de trazo originales.

</dd> <dt>

*plNewStrokeIds* \[ En\]
</dt> <dd>

Matriz de nuevos identificadores de trazo.

</dd> <dt>

*pfSuccessful* \[ out, retval\]
</dt> <dd>

**VARIANT \_ TRUE** si la carga se ha realizado correctamente; en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

Cuando [**IInkAnalyzer**](iinkanalyzer.md) agrega un [**IContextNode**](icontextnode.md) a partir de los resultados guardados, asigna un nuevo identificador único global (GUID) a **IContextNode** (vea [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md) y Propiedades del nodo [de contexto).](context-node-properties.md)

Este método agrega los resultados del análisis guardados al árbol [**IContextNode**](icontextnode.md) existente. Para asegurarse de que los resultados combinados se ordenan correctamente, agregue el área que contiene los nodos de contexto cargados a la región desusada del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IInkAnalyzer::GetDirtyRegion Method)**](iinkanalyzer-getdirtyregion.md)y vuelva aanalizar la entrada de lápiz.

Los [**métodos IInkAnalyzer::SaveResults**](iinkanalyzer-saveresults.md), [**IInkAnalyzer::SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)y el método [**IInkAnalyzer::SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md) no guarda los datos del paquete junto con los resultados del análisis.

Cada identificador de *plOriginalStrokeIds* es el identificador de trazo del trazo en los resultados del análisis guardados. Cada identificador de *plNewStrokeIds* es el nuevo identificador por el que reemplazar el identificador original en los resultados del análisis cargado.

Si una sugerencia de análisis guardada entra en conflicto con una sugerencia de análisis existente, [**IInkAnalyzer**](iinkanalyzer.md) no carga la sugerencia guardada, pero carga el resto de los resultados guardados. Sin embargo, si **IInkAnalyzer** carga los resultados de un trazo que se encuentra dentro del área de una sugerencia de análisis guardada que **IInkAnalyzer** no carga, **el IInkAnalyzer** agrega el cuadro de límite del trazo a la región desusada del objeto **IInkAnalyzer.** Además, si **IInkAnalyzer** carga los resultados de un trazo que se encuentra dentro del área de una sugerencia de análisis existente, **el IInkAnalyzer** también agrega el rectángulo delimitador del trazo a la región desusada del objeto **IInkAnalyzer.** Para obtener más información sobre las sugerencias de análisis, vea [Propiedades de la sugerencia de análisis](analysis-hint-properties.md).

Este método puede generar los eventos [**\_ IAnalysisProxyEvents::ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_ IAnalysisProxyEvents::ContextNodeLinkAdding e**](-ianalysisproxyevents-contextnodelinkadding.md) [**\_ IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) a medida que carga los resultados guardados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer::GetDirtyRegion (Método)**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer::SetDirtyRegion (Método)**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer::SaveResults (Método)**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**IInkAnalyzer::SaveResultsForNodes (Método)**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IInkAnalyzer::SaveResultsForStrokes (Método)**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




