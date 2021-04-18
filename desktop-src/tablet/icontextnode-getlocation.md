---
description: Recupera la posición y el tamaño del objeto IContextNode.
ms.assetid: 40787a9b-1017-4209-aec8-09b7332bfa8a
title: 'IContextNode:: GetLocation (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13366442399961eaba7a411b1b3c87171f0879b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715229"
---
# <a name="icontextnodegetlocation-method"></a><span data-ttu-id="99418-103">IContextNode:: GetLocation (método)</span><span class="sxs-lookup"><span data-stu-id="99418-103">IContextNode::GetLocation method</span></span>

<span data-ttu-id="99418-104">Recupera la posición y el tamaño del objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="99418-104">Retrieves the position and size of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="99418-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99418-105">Syntax</span></span>


```C++
HRESULT GetLocation(
  [out] IAnalysisRegion **ppIAnalysisRegion
);
```



## <a name="parameters"></a><span data-ttu-id="99418-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99418-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99418-107">*ppIAnalysisRegion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="99418-107">*ppIAnalysisRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99418-108">Puntero a la posición y tamaño del objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="99418-108">A pointer to the position and size of the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99418-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99418-109">Return value</span></span>

<span data-ttu-id="99418-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="99418-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="99418-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99418-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="99418-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppIAnalysisRegion* cuando ya no necesite usar la región de análisis.</span><span class="sxs-lookup"><span data-stu-id="99418-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppIAnalysisRegion* when you no longer need to use the analysis region.</span></span>

 

<span data-ttu-id="99418-113">La ubicación de un nodo contenedor se determina mediante la búsqueda de la Unión de todas las ubicaciones de la hoja.</span><span class="sxs-lookup"><span data-stu-id="99418-113">The location for a container node is determined by finding the union of all the leaf's locations.</span></span> <span data-ttu-id="99418-114">La ubicación de un nodo de hoja de tinta se determina mediante la búsqueda de la Unión del rectángulo de selección de los trazos asociados.</span><span class="sxs-lookup"><span data-stu-id="99418-114">The location for an ink leaf node is determined by finding the union of the bounding box of the associated strokes.</span></span> <span data-ttu-id="99418-115">La ubicación de un nodo de hoja que no es de tinta se establece cuando se crea el nodo y se puede actualizar mediante [**IContextNode:: SetLocation**](icontextnode-setlocation.md).</span><span class="sxs-lookup"><span data-stu-id="99418-115">The location for a non-ink leaf node is set when the node is created and can be updated using [**IContextNode::SetLocation**](icontextnode-setlocation.md).</span></span>

## <a name="examples"></a><span data-ttu-id="99418-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="99418-116">Examples</span></span>

<span data-ttu-id="99418-117">En el ejemplo siguiente se muestra un método auxiliar que recupera información sobre un nodo especificado, su parámetro *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="99418-117">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="99418-118">Este método auxiliar devuelve información de los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="99418-118">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="99418-119">**IContextNode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="99418-119">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   [<span data-ttu-id="99418-120">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="99418-120">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   <span data-ttu-id="99418-121">**IContextNode:: GetLocation**</span><span class="sxs-lookup"><span data-stu-id="99418-121">**IContextNode::GetLocation**</span></span>
-   [<span data-ttu-id="99418-122">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="99418-122">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="99418-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99418-123">Requirements</span></span>



| <span data-ttu-id="99418-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="99418-124">Requirement</span></span> | <span data-ttu-id="99418-125">Value</span><span class="sxs-lookup"><span data-stu-id="99418-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99418-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99418-126">Minimum supported client</span></span><br/> | <span data-ttu-id="99418-127">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="99418-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="99418-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99418-128">Minimum supported server</span></span><br/> | <span data-ttu-id="99418-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="99418-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="99418-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99418-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="99418-131"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="99418-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="99418-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="99418-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99418-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99418-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="99418-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="99418-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99418-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="99418-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="99418-136">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="99418-136">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="99418-137">**IContextNode:: SetLocation**</span><span class="sxs-lookup"><span data-stu-id="99418-137">**IContextNode::SetLocation**</span></span>](icontextnode-setlocation.md)
</dt> <dt>

[<span data-ttu-id="99418-138">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="99418-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

