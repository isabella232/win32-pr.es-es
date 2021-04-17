---
description: Obtiene el número de trazos asociados al objeto IContextNode.
ms.assetid: bb3c1cb3-dcf6-4465-b1bc-5c613e9747da
title: 'IContextNode:: GetStrokeCount (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2652168fa2846995aeb17ec23c194f908f22e5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497584"
---
# <a name="icontextnodegetstrokecount-method"></a><span data-ttu-id="68e78-103">IContextNode:: GetStrokeCount (método)</span><span class="sxs-lookup"><span data-stu-id="68e78-103">IContextNode::GetStrokeCount method</span></span>

<span data-ttu-id="68e78-104">Obtiene el número de trazos asociados al objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="68e78-104">Gets the number of strokes associated with the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="68e78-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68e78-105">Syntax</span></span>


```C++
HRESULT GetStrokeCount(
  [out] ULONG *pulStrokeCount
);
```



## <a name="parameters"></a><span data-ttu-id="68e78-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68e78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68e78-107">*pulStrokeCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="68e78-107">*pulStrokeCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68e78-108">Número de trazos asociados al objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="68e78-108">The number of strokes associated with the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68e78-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68e78-109">Return value</span></span>

<span data-ttu-id="68e78-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="68e78-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="68e78-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68e78-111">Remarks</span></span>

<span data-ttu-id="68e78-112">Solo los nodos de contexto de hoja de tinta tienen datos de trazo asociados (vea [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="68e78-112">Only ink leaf context nodes have associated stroke data (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

## <a name="examples"></a><span data-ttu-id="68e78-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="68e78-113">Examples</span></span>

<span data-ttu-id="68e78-114">En este ejemplo se muestra un método, `ExploreContextNode` , que examina un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="68e78-114">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="68e78-115">El método hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="68e78-115">The method does the following:</span></span>

-   <span data-ttu-id="68e78-116">Obtiene el tipo del nodo de contexto.</span><span class="sxs-lookup"><span data-stu-id="68e78-116">Gets the context node's type.</span></span>
-   <span data-ttu-id="68e78-117">Examina las propiedades específicas del tipo de nodo mediante una llamada a un método auxiliar, si el nodo de contexto es una tinta sin clasificar, una sugerencia de análisis o un nodo de reconocedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="68e78-117">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="68e78-118">Examina cada subnodo llamando a sí mismo, si el nodo tiene subnodos.</span><span class="sxs-lookup"><span data-stu-id="68e78-118">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="68e78-119">Examina los datos de trazo del nodo llamando a un método auxiliar, si el nodo es un nodo de hoja de tinta.</span><span class="sxs-lookup"><span data-stu-id="68e78-119">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="68e78-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68e78-120">Requirements</span></span>



| <span data-ttu-id="68e78-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="68e78-121">Requirement</span></span> | <span data-ttu-id="68e78-122">Value</span><span class="sxs-lookup"><span data-stu-id="68e78-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68e78-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68e78-123">Minimum supported client</span></span><br/> | <span data-ttu-id="68e78-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="68e78-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="68e78-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68e78-125">Minimum supported server</span></span><br/> | <span data-ttu-id="68e78-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="68e78-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="68e78-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68e78-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="68e78-128"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="68e78-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="68e78-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68e78-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68e78-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68e78-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="68e78-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="68e78-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e78-132">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="68e78-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="68e78-133">**IContextNode::GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="68e78-133">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="68e78-134">**IContextNode::GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="68e78-134">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="68e78-135">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="68e78-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




