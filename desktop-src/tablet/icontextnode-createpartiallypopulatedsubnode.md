---
description: Crea un objeto IContextNode secundario que solo contiene información sobre el tipo, el identificador y la ubicación.
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: 'IContextNode:: CreatePartiallyPopulatedSubNode (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreatePartiallyPopulatedSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7947ba4665bdb101e955246fcc99352a24a4397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908027"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a>IContextNode:: CreatePartiallyPopulatedSubNode (método)

Crea un objeto [**IContextNode**](icontextnode.md) secundario que solo contiene información sobre el tipo, el identificador y la ubicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreatePartiallyPopulatedSubNode(
  [in]  const GUID            *pNodeType,
  [in]  const GUID            *pNodeId,
  [in]        IAnalysisRegion *pNodeLocation,
  [out]       IContextNode    **pPartiallyPopulatedContextNodeCreated
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNodeType* \[ de\]
</dt> <dd>

El tipo de nodo de contexto que se va a crear.

</dd> <dt>

*pNodeId* \[ de\]
</dt> <dd>

Identificador del nuevo nodo.

</dd> <dt>

*pNodeLocation* \[ de\]
</dt> <dd>

Ubicación del nuevo nodo.

</dd> <dt>

*pPartiallyPopulatedContextNodeCreated* \[ enuncia\]
</dt> <dd>

Puntero al nuevo [**IContextNode**](icontextnode.md)que se rellena parcialmente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *pPartiallyPopulatedContextNodeCreated* cuando ya no necesite usar el nodo de contexto.

 

El nuevo [**IContextNode**](icontextnode.md) se agrega a la colección de nodos secundarios del nodo de contexto (vea [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)). Cuando hay nodos secundarios existentes, el **IContextNode** recién creado se agrega como el último nodo secundario.

Para obtener más información sobre el tipo, el identificador y la ubicación, vea [**IContextNode:: GetType**](icontextnode-gettype.md), [**IContextNode:: getId**](icontextnode-getid.md)y [**IContextNode:: GetLocation**](icontextnode-getlocation.md).

Este método se usa para el proxy de datos como una manera de crear un objeto [**IContextNode**](icontextnode.md) en el árbol de nodos de contexto antes de que toda la información sobre él esté disponible. Para obtener más información, consulte [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Tipos de nodo de contexto](context-node-types.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

