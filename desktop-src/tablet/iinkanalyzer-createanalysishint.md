---
description: Agrega un nuevo nodo de sugerencia de análisis con un área infinita a IInkAnalyzer.
ms.assetid: 4cc592c4-456f-4aa5-9a87-d9427de487f3
title: 'IInkAnalyzer:: CreateAnalysisHint (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 041dc1a60c1eeb18d6896a6a23537ac9ebccd321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360340"
---
# <a name="iinkanalyzercreateanalysishint-method"></a>IInkAnalyzer:: CreateAnalysisHint (método)

Agrega un nuevo nodo de sugerencia de análisis con un área infinita a [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateAnalysisHint(
  [out] IContextNode **ppAnalysisHint
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppAnalysisHint* \[ enuncia\]
</dt> <dd>

Nuevo nodo de sugerencia de análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Vea [clases e interfaces: Análisis de tinta](classes-and-interfaces---ink-analysis.md) para obtener una descripción de los valores devueltos.

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppAnalysisHint* cuando ya no necesite usar el objeto.

 

Para proporcionar información de contexto adicional para el [**IInkAnalyzer**](iinkanalyzer.md), puede Agregar sugerencias de análisis al analizador de tinta. Las sugerencias de análisis pueden mejorar la precisión del reconocimiento. Por ejemplo, puede Agregar Factoid y la información de la guía para los campos de una aplicación de formulario.

Este método crea un nuevo [**IContextNode**](icontextnode.md) con un tipo de nodo de contexto de AnalysisHint (vea [**IContextNode:: GetType**](icontextnode-gettype.md)) y agrega la nueva sugerencia como un subnodo del nodo raíz del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) y [**IInkAnalyzer:: GetRootNode Method**](iinkanalyzer-getrootnode.md)).

Para agregar información de contexto a la sugerencia, use [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) con el parámetro *pPropertyDataId* establecido en una de las constantes de [las propiedades](analysis-hint-properties.md) de la sugerencia de análisis.

Si a una sugerencia se le asigna un área infinita, que se denomina una sugerencia global, el [**IInkAnalyzer**](iinkanalyzer.md) aplica el contexto de la sugerencia a todas las entradas de lápiz que no se encuentran dentro de otro área de la sugerencia. Se pueden adjuntar varias sugerencias a un único **IInkAnalyzer**. Sin embargo, solo se puede adjuntar una sugerencia global a un único analizador de tinta y no se pueden superponer las sugerencias no globales. Para obtener más información sobre los tipos de información de contexto que puede proporcionar una sugerencia, consulte propiedades de la [sugerencia de análisis](analysis-hint-properties.md).

La adición de una sugerencia de análisis no marca el área de la sugerencia para su análisis. Para marcar el área dentro de la sugerencia para su reanálisis, use el [**método IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) para establecer la región desfasada en la Unión de la región desfasada actual y el área de la sugerencia de análisis.

Al utilizar sugerencias para una aplicación de formulario, la aplicación debe evitar mezclar el contexto del texto con la entrada de lápiz en los formularios. Esto significa que, por ejemplo, los nombres de campo de texto no se deben crear en el árbol de análisis. Las sugerencias están diseñadas para asociar la tinta a áreas de las páginas; cualquier contexto de texto interfiere con esta asociación de entrada de lápiz a sugerencia. La operación de análisis puede mezclar la tinta y el contexto de texto en la misma región de escritura, lo que impediría que la tinta se asociara con el área de sugerencias.

Para obtener más información sobre el análisis de tinta, consulte [información general del análisis de tinta](ink-analysis-overview.md).

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

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IInkAnalyzer::D método eleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[**IInkAnalyzer:: GetAnalysisHints (método)**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**IInkAnalyzer:: GetAnalysisHintsByName (método)**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Propiedades de la sugerencia de análisis](analysis-hint-properties.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

