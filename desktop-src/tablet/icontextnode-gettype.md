---
description: Recupera el tipo del objeto IContextNode.
ms.assetid: 285384ce-5cdc-47f5-a1c4-6c6d7f18e215
title: 'IContextNode:: GetType (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 68b657d9acd6f25f7c067e339ec42c6994a34c48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154434"
---
# <a name="icontextnodegettype-method"></a><span data-ttu-id="f9fe4-103">IContextNode:: GetType (método)</span><span class="sxs-lookup"><span data-stu-id="f9fe4-103">IContextNode::GetType method</span></span>

<span data-ttu-id="f9fe4-104">Recupera el tipo del objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="f9fe4-104">Retrieves the type of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9fe4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9fe4-105">Syntax</span></span>


```C++
HRESULT GetType(
  [out] GUID *pContextNodeType
);
```



## <a name="parameters"></a><span data-ttu-id="f9fe4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9fe4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9fe4-107">*pContextNodeType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9fe4-107">*pContextNodeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9fe4-108">Tipo del objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="f9fe4-108">The type of the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9fe4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9fe4-109">Return value</span></span>

<span data-ttu-id="f9fe4-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f9fe4-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f9fe4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9fe4-111">Remarks</span></span>

<span data-ttu-id="f9fe4-112">Los tipos de nodos se describen en las constantes de [tipos de nodo de contexto](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="f9fe4-112">Types of nodes are described in the [Context Node Types](context-node-types.md) constants.</span></span>

## <a name="examples"></a><span data-ttu-id="f9fe4-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f9fe4-113">Examples</span></span>

<span data-ttu-id="f9fe4-114">En el ejemplo siguiente se muestra un método auxiliar que recupera información sobre un nodo especificado, su parámetro *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="f9fe4-114">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="f9fe4-115">Este método auxiliar devuelve información de los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="f9fe4-115">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="f9fe4-116">**IContextNode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="f9fe4-116">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   <span data-ttu-id="f9fe4-117">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="f9fe4-117">**IContextNode::GetType**</span></span>
-   [<span data-ttu-id="f9fe4-118">**IContextNode:: GetLocation**</span><span class="sxs-lookup"><span data-stu-id="f9fe4-118">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   [<span data-ttu-id="f9fe4-119">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="f9fe4-119">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="f9fe4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9fe4-120">Requirements</span></span>



| <span data-ttu-id="f9fe4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9fe4-121">Requirement</span></span> | <span data-ttu-id="f9fe4-122">Value</span><span class="sxs-lookup"><span data-stu-id="f9fe4-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9fe4-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9fe4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f9fe4-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f9fe4-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f9fe4-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9fe4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f9fe4-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f9fe4-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f9fe4-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9fe4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9fe4-128"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f9fe4-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f9fe4-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9fe4-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9fe4-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9fe4-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f9fe4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9fe4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9fe4-132">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="f9fe4-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f9fe4-133">Tipos de nodo de contexto</span><span class="sxs-lookup"><span data-stu-id="f9fe4-133">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="f9fe4-134">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="f9fe4-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




