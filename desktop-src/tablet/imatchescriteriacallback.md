---
description: Expone un método para evaluar si un objeto IContextNode cumple o no los criterios especificados.
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: Interfaz IMatchesCriteriaCallBack (IACom. h)
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
ms.openlocfilehash: 960bd221bdd1f621f6ec4deb5ea167f5bf9ee4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540451"
---
# <a name="imatchescriteriacallback-interface"></a>Interfaz IMatchesCriteriaCallBack

Expone un método para evaluar si un objeto [**IContextNode**](icontextnode.md) cumple o no los criterios especificados.

## <a name="members"></a>Miembros

La interfaz **IMatchesCriteriaCallBack** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMatchesCriteriaCallBack** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IMatchesCriteriaCallBack** tiene estos métodos.



| Método                                                                      | Descripción                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) | Cuando se reemplaza en una clase derivada, evalúa si un objeto [**IContextNode**](icontextnode.md) especificado cumple los criterios.<br/> |



 

## <a name="remarks"></a>Observaciones

Para usar el método [**IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) o [**IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), cree una clase que implemente **IMatchesCriteriaCallBack**. Implemente [**IMatchesCriteriaCallBack:: EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) para devolver **Variant \_ true** si el objeto [**IContextNode**](icontextnode.md) coincide con los criterios y **Variant \_ false** en caso contrario. En algunos criterios, puede que tenga que proporcionar un medio para inicializar o mantener el estado del objeto **IMatchesCriteriaCallBack** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer:: FindNodesWithCallBack (método)**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

