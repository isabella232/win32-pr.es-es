---
description: Recupera el nodo primario de este IContextNode en el árbol de nodos de contexto.
ms.assetid: 782fd973-f8f3-4902-b8e0-cc5e70a66d28
title: Método IContextNode::GetParentNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetParentNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 50bba716486910802e91cbe6d3f003d172f1cb29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247820"
---
# <a name="icontextnodegetparentnode-method"></a>IContextNode::GetParentNode (método)

Recupera el nodo primario de este [**IContextNode**](icontextnode.md) en el árbol de nodos de contexto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetParentNode(
  [out] IContextNode **ppParentContextNode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppParentContextNode* \[ out\]
</dt> <dd>

Puntero al nodo primario de este [**objeto IContextNode.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppParentContextNode* cuando ya no necesite usar el nodo de contexto primario.

 

Si este es el nodo raíz, el *parámetro ppParentContextNode* se establece en **NULL.**

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra un método auxiliar que recupera información sobre un nodo especificado, su *parámetro pContextNode.* Este método auxiliar devuelve información de los métodos siguientes.

-   [**IContextNode::GetId**](icontextnode-getid.md)
-   [**IContextNode::GetType**](icontextnode-gettype.md)
-   [**IContextNode::GetLocation**](icontextnode-getlocation.md)
-   **IContextNode::GetParentNode**


```C++
// Helper method for collecting information about a context node.
HRESULT CMyClass::GetNodeInformation(
    IContextNode *pContextNode,
    GUID *pNodeIdentifier,
    GUID *pContextNodeType,
    IAnalysisRegion **ppAnalysisRegion,
    IContextNode **ppParentNode,
    IContextNodes **ppSubNodes)
{
    // Get the identifier of the context node.
    HRESULT hr = pContextNode->GetId(pNodeIdentifier);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the type identifier for the context node.
    hr = pContextNode->GetType(pContextNodeType);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the location of the context node.
    hr = pContextNode->GetLocation(ppAnalysisRegion);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the parent node of the context node.
    hr = pContextNode->GetParentNode(ppParentNode);

    if (FAILED(hr))
    {
        if ((*ppAnalysisRegion) != NULL)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        return hr;
    }

    // Get the subnodes of the context node.
    hr = pContextNode->GetSubNodes(ppSubNodes);

    if (FAILED(hr))
    {
        if (*ppAnalysisRegion)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        if (*ppParentNode)
        {
            (*ppParentNode)->Release();
            (*ppParentNode) = NULL;
        }
        return hr;
    }

    return hr;
}
```



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

[**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

