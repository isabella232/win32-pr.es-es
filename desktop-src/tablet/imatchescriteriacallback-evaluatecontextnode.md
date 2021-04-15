---
description: Cuando se reemplaza en una clase derivada, evalúa si un objeto IContextNode especificado cumple los criterios.
ms.assetid: ade8e59c-6aeb-4a87-a95d-229f8f0b2223
title: 'IMatchesCriteriaCallBack:: EvaluateContextNode (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack.EvaluateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 554cf451396101de2238258de0a0706956f24a02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648181"
---
# <a name="imatchescriteriacallbackevaluatecontextnode-method"></a>IMatchesCriteriaCallBack:: EvaluateContextNode (método)

Cuando se reemplaza en una clase derivada, evalúa si un objeto [**IContextNode**](icontextnode.md) especificado cumple los criterios.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EvaluateContextNode(
  [in]  IContextNode *pContextNodeToEvaluate,
  [out] VARIANT_BOOL *pbResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContextNodeToEvaluate* \[ de\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) que se va a evaluar.

</dd> <dt>

*pbResult* \[ enuncia\]
</dt> <dd>

**Variante \_ TRUE** si *pContextNodeToEvaluate* coincide con los criterios; de lo contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Para usar el método [**IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) o [**IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), cree una clase que implemente [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md). Implemente **IMatchesCriteriaCallBack:: EvaluateContextNode** para devolver **Variant \_ true** si el objeto [**IContextNode**](icontextnode.md) coincide con los criterios y **Variant \_ false** en caso contrario. En algunos criterios, puede que tenga que proporcionar un medio para inicializar o mantener el estado del objeto **IMatchesCriteriaCallBack** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMatchesCriteriaCallBack**](imatchescriteriacallback.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesWithCallBack (método)**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




