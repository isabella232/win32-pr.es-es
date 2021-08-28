---
description: Cuando se invalida en una clase derivada, evalúa si un objeto IContextNode especificado cumple los criterios.
ms.assetid: ade8e59c-6aeb-4a87-a95d-229f8f0b2223
title: Método IMatchesCriteriaCallBack::EvaluateContextNode (IACom.h)
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
ms.openlocfilehash: d5855928e0827632240c8230bdcc57dff836c5287eec61f2911cc62367a8915f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719055"
---
# <a name="imatchescriteriacallbackevaluatecontextnode-method"></a>IMatchesCriteriaCallBack::EvaluateContextNode (método)

Cuando se invalida en una clase derivada, evalúa si un objeto [**IContextNode**](icontextnode.md) especificado cumple los criterios.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EvaluateContextNode(
  [in]  IContextNode *pContextNodeToEvaluate,
  [out] VARIANT_BOOL *pbResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContextNodeToEvaluate* \[ En\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) que se evaluará.

</dd> <dt>

*pbResult* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE** si *pContextNodeToEvaluate* coincide con los criterios; en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Para usar el método [**IInkAnalyzer::FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) o el método [**IInkAnalyzer::FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), cree una clase que implemente [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md). Implemente **IMatchesCriteriaCallBack::EvaluateContextNode** para devolver **VARIANT \_ TRUE** si el objeto [**IContextNode**](icontextnode.md) coincide con sus criterios y **VARIANT \_ FALSE** en caso contrario. Para algunos criterios, es posible que tenga que proporcionar un medio para inicializar o mantener el estado del objeto **IMatchesCriteriaCallBack.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMatchesCriteriaCallBack**](imatchescriteriacallback.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBack (Método)**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBackInSubTree (Método)**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




