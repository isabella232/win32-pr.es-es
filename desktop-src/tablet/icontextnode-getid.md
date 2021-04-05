---
description: Recupera el identificador del objeto IContextNode.
ms.assetid: 7578bcc1-7c69-45fc-b3c2-7350ce4df99c
title: 'IContextNode:: GetId (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ef316111c7464bac0339a4888b887bc5cf20b93f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908025"
---
# <a name="icontextnodegetid-method"></a><span data-ttu-id="560c4-103">IContextNode:: GetId (método)</span><span class="sxs-lookup"><span data-stu-id="560c4-103">IContextNode::GetId method</span></span>

<span data-ttu-id="560c4-104">Recupera el identificador del objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="560c4-104">Retrieves the identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="560c4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="560c4-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] GUID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="560c4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="560c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="560c4-107">*pId* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="560c4-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="560c4-108">Identificador del objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="560c4-108">The identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="560c4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="560c4-109">Return value</span></span>

<span data-ttu-id="560c4-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="560c4-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="560c4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="560c4-111">Remarks</span></span>

<span data-ttu-id="560c4-112">El analizador de tinta asigna un identificador único a todos los nodos de contexto que crea.</span><span class="sxs-lookup"><span data-stu-id="560c4-112">The ink analyzer assigns a unique identifier to all context nodes it creates.</span></span> <span data-ttu-id="560c4-113">Durante el análisis de tinta, el analizador de tinta puede cambiar el identificador de un nodo de contexto.</span><span class="sxs-lookup"><span data-stu-id="560c4-113">During ink analysis, the ink analyzer may change the identifier for a context node.</span></span> <span data-ttu-id="560c4-114">Por ejemplo, el analizador de tinta puede volver a clasificar un nodo de Word como dos nodos de Word y, a continuación, asignar el identificador original a uno y un nuevo identificador al otro.</span><span class="sxs-lookup"><span data-stu-id="560c4-114">For example, the ink analyzer may reclassify one word node as two word nodes and then assign the original identifier to one and a new identifier to the other.</span></span> <span data-ttu-id="560c4-115">O bien, el analizador de tinta puede reclasificar dos nodos de Word como un nodo de Word y asignar uno de los identificadores originales al nuevo nodo de Word.</span><span class="sxs-lookup"><span data-stu-id="560c4-115">Or, the ink analyzer may reclassify two word nodes as one word node and assign one of the original identifiers to the new word node.</span></span>

## <a name="examples"></a><span data-ttu-id="560c4-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="560c4-116">Examples</span></span>

<span data-ttu-id="560c4-117">En el ejemplo siguiente se muestra un método auxiliar que recupera información sobre un nodo especificado, su parámetro *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="560c4-117">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="560c4-118">Este método auxiliar devuelve información de los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="560c4-118">This helper method returns information from the following methods.</span></span>

-   <span data-ttu-id="560c4-119">**IContextNode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="560c4-119">**IContextNode::GetId**</span></span>
-   [<span data-ttu-id="560c4-120">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="560c4-120">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   [<span data-ttu-id="560c4-121">**IContextNode:: GetLocation**</span><span class="sxs-lookup"><span data-stu-id="560c4-121">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   [<span data-ttu-id="560c4-122">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="560c4-122">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="560c4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="560c4-123">Requirements</span></span>



| <span data-ttu-id="560c4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="560c4-124">Requirement</span></span> | <span data-ttu-id="560c4-125">Value</span><span class="sxs-lookup"><span data-stu-id="560c4-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="560c4-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="560c4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="560c4-127">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="560c4-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="560c4-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="560c4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="560c4-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="560c4-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="560c4-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="560c4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="560c4-131"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="560c4-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="560c4-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="560c4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="560c4-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="560c4-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="560c4-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="560c4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="560c4-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="560c4-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="560c4-136">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="560c4-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




