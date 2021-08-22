---
description: Expone un método para evaluar si un objeto IContextNode cumple o no un criterio especificado.
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: Interfaz IMatchesCriteriaCallBack (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc661f47c77d615df95f63e58beccbbf125b93078392a63f86ed50f52cc5636d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718974"
---
# <a name="imatchescriteriacallback-interface"></a>Interfaz IMatchesCriteriaCallBack

Expone un método para evaluar si un [**objeto IContextNode**](icontextnode.md) cumple o no un criterio especificado.

## <a name="members"></a>Miembros

La **interfaz IMatchesCriteriaCallBack** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMatchesCriteriaCallBack** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMatchesCriteriaCallBack** tiene estos métodos.



| Método                                                                      | Descripción                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) | Cuando se invalida en una clase derivada, evalúa si un objeto [**IContextNode**](icontextnode.md) especificado cumple los criterios.<br/> |



 

## <a name="remarks"></a>Comentarios

Para usar el método [**IInkAnalyzer::FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) o [**IInkAnalyzer::FindNodesWithCallBackInSubTree ,**](iinkanalyzer-findnodeswithcallbackinsubtree.md)cree una clase que implemente **IMatchesCriteriaCallBack**. Implemente [**IMatchesCriteriaCallBack::EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) para devolver **VARIANT \_ TRUE** si el objeto [**IContextNode**](icontextnode.md) coincide con los criterios y **VARIANT \_ FALSE** en caso contrario. Para algunos criterios, es posible que deba proporcionar un medio para inicializar o mantener el estado del objeto **IMatchesCriteriaCallBack.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalyzer::FindNodesWithCallBack (Método)**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBackInSubTree (Método)**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

