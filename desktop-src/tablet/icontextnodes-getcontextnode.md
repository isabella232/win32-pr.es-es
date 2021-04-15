---
description: Recupera el objeto IContextNode en el índice especificado de esta colección.
ms.assetid: 4b266512-9e58-43d2-8430-68310230fc27
title: 'IContextNodes:: GetContextNode (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.GetContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ec907fdcac5a1ed18cca54c79a876959868f2ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497578"
---
# <a name="icontextnodesgetcontextnode-method"></a><span data-ttu-id="e729d-103">IContextNodes:: GetContextNode (método)</span><span class="sxs-lookup"><span data-stu-id="e729d-103">IContextNodes::GetContextNode method</span></span>

<span data-ttu-id="e729d-104">Recupera el objeto [**IContextNode**](icontextnode.md) en el índice especificado de esta colección.</span><span class="sxs-lookup"><span data-stu-id="e729d-104">Retrieves the [**IContextNode**](icontextnode.md) object at the specified index within this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e729d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e729d-105">Syntax</span></span>


```C++
HRESULT GetContextNode(
  [in]  ULONG        ulIndex,
  [out] IContextNode **ppContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="e729d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e729d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e729d-107">*ulIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e729d-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e729d-108">Índice de base cero del objeto [**IContextNode**](icontextnode.md) que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="e729d-108">The zero-based index of the [**IContextNode**](icontextnode.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="e729d-109">*ppContextNode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e729d-109">*ppContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e729d-110">Puntero a la [**IContextNode**](icontextnode.md) a la que se hace referencia en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="e729d-110">Pointer to the [**IContextNode**](icontextnode.md) referenced at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e729d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e729d-111">Return value</span></span>

<span data-ttu-id="e729d-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e729d-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e729d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e729d-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="e729d-114">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppContextNode* cuando ya no necesite usar el nodo de contexto.</span><span class="sxs-lookup"><span data-stu-id="e729d-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNode* when you no longer need to use the context node.</span></span>

 

## <a name="examples"></a><span data-ttu-id="e729d-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e729d-115">Examples</span></span>

<span data-ttu-id="e729d-116">En este ejemplo se muestra un método, `ExploreContextNode` , que examina un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="e729d-116">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="e729d-117">El método hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e729d-117">The method does the following:</span></span>

-   <span data-ttu-id="e729d-118">Obtiene el tipo del nodo de contexto.</span><span class="sxs-lookup"><span data-stu-id="e729d-118">Gets the context node's type.</span></span>
-   <span data-ttu-id="e729d-119">Examina las propiedades específicas del tipo de nodo mediante una llamada a un método auxiliar, si el nodo de contexto es una tinta sin clasificar, una sugerencia de análisis o un nodo de reconocedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="e729d-119">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="e729d-120">Examina cada subnodo llamando a sí mismo, si el nodo tiene subnodos.</span><span class="sxs-lookup"><span data-stu-id="e729d-120">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="e729d-121">Examina los datos de trazo del nodo llamando a un método auxiliar, si el nodo es un nodo de hoja de tinta.</span><span class="sxs-lookup"><span data-stu-id="e729d-121">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="e729d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e729d-122">Requirements</span></span>



| <span data-ttu-id="e729d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e729d-123">Requirement</span></span> | <span data-ttu-id="e729d-124">Value</span><span class="sxs-lookup"><span data-stu-id="e729d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e729d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e729d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e729d-126">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e729d-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e729d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e729d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e729d-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e729d-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e729d-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e729d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e729d-130"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e729d-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e729d-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e729d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e729d-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e729d-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e729d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e729d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e729d-134">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="e729d-134">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="e729d-135">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="e729d-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

