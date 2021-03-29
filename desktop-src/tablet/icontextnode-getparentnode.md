---
description: Recupera el nodo primario de este IContextNode en el árbol de nodos de contexto.
ms.assetid: 782fd973-f8f3-4902-b8e0-cc5e70a66d28
title: 'IContextNode:: GetParentNode (método) (IACom. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542062"
---
# <a name="icontextnodegetparentnode-method"></a><span data-ttu-id="c3987-103">IContextNode:: GetParentNode (método)</span><span class="sxs-lookup"><span data-stu-id="c3987-103">IContextNode::GetParentNode method</span></span>

<span data-ttu-id="c3987-104">Recupera el nodo primario de este [**IContextNode**](icontextnode.md) en el árbol de nodos de contexto.</span><span class="sxs-lookup"><span data-stu-id="c3987-104">Retrieves the parent node of this [**IContextNode**](icontextnode.md) in the context node tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3987-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3987-105">Syntax</span></span>


```C++
HRESULT GetParentNode(
  [out] IContextNode **ppParentContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="c3987-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3987-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3987-107">*ppParentContextNode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c3987-107">*ppParentContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3987-108">Puntero al nodo primario de este objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="c3987-108">A pointer to the parent node of this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3987-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3987-109">Return value</span></span>

<span data-ttu-id="c3987-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c3987-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c3987-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3987-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c3987-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppParentContextNode* cuando ya no necesite usar el nodo de contexto primario.</span><span class="sxs-lookup"><span data-stu-id="c3987-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppParentContextNode* when you no longer need to use the parent context node.</span></span>

 

<span data-ttu-id="c3987-113">Si este es el nodo raíz, el parámetro *ppParentContextNode* se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="c3987-113">If this is the root node, the *ppParentContextNode* parameter is set to **NULL**.</span></span>

## <a name="examples"></a><span data-ttu-id="c3987-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c3987-114">Examples</span></span>

<span data-ttu-id="c3987-115">En el ejemplo siguiente se muestra un método auxiliar que recupera información sobre un nodo especificado, su parámetro *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="c3987-115">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="c3987-116">Este método auxiliar devuelve información de los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="c3987-116">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="c3987-117">**IContextNode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="c3987-117">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   [<span data-ttu-id="c3987-118">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="c3987-118">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   [<span data-ttu-id="c3987-119">**IContextNode:: GetLocation**</span><span class="sxs-lookup"><span data-stu-id="c3987-119">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   <span data-ttu-id="c3987-120">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="c3987-120">**IContextNode::GetParentNode**</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c3987-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3987-121">Requirements</span></span>



| <span data-ttu-id="c3987-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3987-122">Requirement</span></span> | <span data-ttu-id="c3987-123">Value</span><span class="sxs-lookup"><span data-stu-id="c3987-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3987-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3987-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c3987-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c3987-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c3987-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3987-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c3987-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c3987-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c3987-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3987-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3987-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c3987-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c3987-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c3987-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3987-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3987-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c3987-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3987-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3987-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="c3987-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c3987-134">**IContextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="c3987-134">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="c3987-135">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="c3987-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

