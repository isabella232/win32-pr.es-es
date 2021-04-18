---
description: Recupera todos los objetos IContextNode del tipo especificado que contienen los trazos especificados.
ms.assetid: c674a03b-841c-4a9c-8268-302bc4038934
title: 'IInkAnalyzer:: FindNodesOfTypeForStrokes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dd98c72007a69521506e2be21ad10edeb46df27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715208"
---
# <a name="iinkanalyzerfindnodesoftypeforstrokes-method"></a>IInkAnalyzer:: FindNodesOfTypeForStrokes (método)

Recupera todos los objetos [**IContextNode**](icontextnode.md) del tipo especificado que contienen los trazos especificados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindNodesOfTypeForStrokes(
  [in]  const GUID          *pNodeType,
  [in]        ULONG         ulStrokeIdsCount,
  [in]        LONG          *plStrokeIds,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNodeType* \[ de\]
</dt> <dd>

Identificador único global (GUID) que especifica el tipo de nodo.

</dd> <dt>

*ulStrokeIdsCount* \[ de\]
</dt> <dd>

Número de identificadores de trazo pasados.

</dd> <dt>

*plStrokeIds* \[ de\]
</dt> <dd>

Matriz de los identificadores de trazo.

</dd> <dt>

*ppContextNodesFound* \[ enuncia\]
</dt> <dd>

Colección de objetos [**IContextNode**](icontextnode.md) que contienen todos los nodos de tipo *pNodeType* que contienen los trazos con identificadores en la matriz *plStrokeIds* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppContextNodesFound* cuando ya no necesite usar el objeto.

 

La propiedad *pNodeType* debe contener un GUID de las constantes de [tipos de nodo de contexto](context-node-types.md) .

Si el tipo de nodo especificado no es un nodo hoja, pero uno de los descendientes del nodo hace referencia a un trazo de la colección Strokes, ese nodo se agrega a la colección que se devuelve.

Si [**IInkAnalyzer**](iinkanalyzer.md) no contiene este [**IContextNode**](icontextnode.md), se devuelve una colección [**IContextNodes**](icontextnodes.md) vacía.

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

[**IInkAnalyzer:: FindInkLeafNodes (método)**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**IInkAnalyzer:: FindInkLeafNodesForStrokes (método)**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer:: FindLeafNodes (método)**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**IInkAnalyzer:: FindNode (método)**](iinkanalyzer-findnode.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesOfType (método)**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesOfTypeInSubTree (método)**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesWithCallBack (método)**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

