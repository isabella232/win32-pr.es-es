---
description: Obtiene los nodos secundarios directos del objeto IContextNode.
ms.assetid: 50ce2fa4-031e-42e9-8e47-c0d3c2d2b4df
title: 'IContextNode:: GetSubNodes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetSubNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5c0526ca4a5b4db355c1f895a44ebbf634cb8bc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696536"
---
# <a name="icontextnodegetsubnodes-method"></a><span data-ttu-id="e433d-103">IContextNode:: GetSubNodes (método)</span><span class="sxs-lookup"><span data-stu-id="e433d-103">IContextNode::GetSubNodes method</span></span>

<span data-ttu-id="e433d-104">Obtiene los nodos secundarios directos del objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="e433d-104">Gets the direct child nodes of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e433d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e433d-105">Syntax</span></span>


```C++
HRESULT GetSubNodes(
  [out] IContextNodes **ppSubContextNodes
);
```



## <a name="parameters"></a><span data-ttu-id="e433d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e433d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e433d-107">*ppSubContextNodes* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e433d-107">*ppSubContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e433d-108">Colección de los objetos [**IContextNode**](icontextnode.md) que son nodos secundarios directos de este **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="e433d-108">A collection of the [**IContextNode**](icontextnode.md) objects that are direct child nodes of this **IContextNode**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e433d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e433d-109">Return value</span></span>

<span data-ttu-id="e433d-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e433d-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e433d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e433d-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="e433d-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppSubContextNodes* cuando ya no necesite usar la colección de subnodos.</span><span class="sxs-lookup"><span data-stu-id="e433d-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppSubContextNodes* when you no longer need to use the collection of subnodes.</span></span>

 

<span data-ttu-id="e433d-113">Esto devuelve solo los nodos secundarios directos, no todos los nodos descendientes.</span><span class="sxs-lookup"><span data-stu-id="e433d-113">This returns only the direct child nodes, not all of the descendant nodes.</span></span>

## <a name="examples"></a><span data-ttu-id="e433d-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e433d-114">Examples</span></span>

<span data-ttu-id="e433d-115">En este ejemplo se muestra un método, `ExploreContextNode` , que examina un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="e433d-115">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="e433d-116">El método hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e433d-116">The method does the following:</span></span>

-   <span data-ttu-id="e433d-117">Obtiene el tipo del nodo de contexto.</span><span class="sxs-lookup"><span data-stu-id="e433d-117">Gets the context node's type.</span></span>
-   <span data-ttu-id="e433d-118">Examina las propiedades específicas del tipo de nodo mediante una llamada a un método auxiliar, si el nodo de contexto es una tinta sin clasificar, una sugerencia de análisis o un nodo de reconocedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="e433d-118">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="e433d-119">Examina cada subnodo llamando a sí mismo, si el nodo tiene subnodos.</span><span class="sxs-lookup"><span data-stu-id="e433d-119">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="e433d-120">Examina los datos de trazo del nodo llamando a un método auxiliar, si el nodo es un nodo de hoja de tinta.</span><span class="sxs-lookup"><span data-stu-id="e433d-120">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="e433d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e433d-121">Requirements</span></span>



| <span data-ttu-id="e433d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e433d-122">Requirement</span></span> | <span data-ttu-id="e433d-123">Value</span><span class="sxs-lookup"><span data-stu-id="e433d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e433d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e433d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e433d-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e433d-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e433d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e433d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e433d-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e433d-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e433d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e433d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e433d-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e433d-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e433d-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e433d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e433d-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e433d-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e433d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e433d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e433d-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="e433d-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e433d-134">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="e433d-134">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="e433d-135">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="e433d-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

