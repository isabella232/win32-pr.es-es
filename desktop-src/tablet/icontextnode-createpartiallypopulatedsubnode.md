---
description: Crea un objeto IContextNode secundario que solo contiene información sobre el tipo, el identificador y la ubicación.
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: Método IContextNode::CreatePartiallyPopulatedSubNode (IACom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251979"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a>IContextNode::CreatePartiallyPopulatedSubNode (método)

Crea un objeto [**IContextNode secundario**](icontextnode.md) que solo contiene información sobre el tipo, el identificador y la ubicación.

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

*pNodeType* \[ En\]
</dt> <dd>

Tipo de nodo de contexto que se creará.

</dd> <dt>

*pNodeId* \[ En\]
</dt> <dd>

Identificador del nuevo nodo.

</dd> <dt>

*pNodeLocation* \[ En\]
</dt> <dd>

Ubicación del nuevo nodo.

</dd> <dt>

*pPartiallyPopulatedContextNodeCreated* \[ out\]
</dt> <dd>

Puntero al nuevo IContextNode parcialmente [**rellenado.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *pPartiallyPopulatedContextNodeCreated* cuando ya no necesite usar el nodo de contexto.

 

El nuevo [**IContextNode**](icontextnode.md) se agrega a la colección de nodos secundarios de este nodo de contexto (vea [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md) Cuando hay nodos secundarios existentes, el **IContextNode** recién creado se agrega como el último nodo secundario.

Para obtener más información sobre el tipo, el identificador y la ubicación, vea [**IContextNode::GetType**](icontextnode-gettype.md), [**IContextNode::GetId**](icontextnode-getid.md)e [**IContextNode::GetLocation**](icontextnode-getlocation.md).

Este método se usa para el proxy de datos como una manera de crear un objeto [**IContextNode**](icontextnode.md) en el árbol de nodos de contexto antes de que toda la información sobre él esté disponible. Para obtener más información, vea [Proxy de datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
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

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

