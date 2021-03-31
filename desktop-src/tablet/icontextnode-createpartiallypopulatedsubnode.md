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
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a><span data-ttu-id="c3978-103">IContextNode:: CreatePartiallyPopulatedSubNode (método)</span><span class="sxs-lookup"><span data-stu-id="c3978-103">IContextNode::CreatePartiallyPopulatedSubNode method</span></span>

<span data-ttu-id="c3978-104">Crea un objeto [**IContextNode**](icontextnode.md) secundario que solo contiene información sobre el tipo, el identificador y la ubicación.</span><span class="sxs-lookup"><span data-stu-id="c3978-104">Creates a child [**IContextNode**](icontextnode.md) object that contains only information about type, identifier, and location.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3978-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3978-105">Syntax</span></span>


```C++
HRESULT CreatePartiallyPopulatedSubNode(
  [in]  const GUID            *pNodeType,
  [in]  const GUID            *pNodeId,
  [in]        IAnalysisRegion *pNodeLocation,
  [out]       IContextNode    **pPartiallyPopulatedContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="c3978-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3978-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3978-107">*pNodeType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c3978-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3978-108">El tipo de nodo de contexto que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="c3978-108">The type of context node to create.</span></span>

</dd> <dt>

<span data-ttu-id="c3978-109">*pNodeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c3978-109">*pNodeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3978-110">Identificador del nuevo nodo.</span><span class="sxs-lookup"><span data-stu-id="c3978-110">The identifier for the new node.</span></span>

</dd> <dt>

<span data-ttu-id="c3978-111">*pNodeLocation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c3978-111">*pNodeLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3978-112">Ubicación del nuevo nodo.</span><span class="sxs-lookup"><span data-stu-id="c3978-112">The location of the new node.</span></span>

</dd> <dt>

<span data-ttu-id="c3978-113">*pPartiallyPopulatedContextNodeCreated* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c3978-113">*pPartiallyPopulatedContextNodeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3978-114">Puntero al nuevo [**IContextNode**](icontextnode.md)que se rellena parcialmente.</span><span class="sxs-lookup"><span data-stu-id="c3978-114">A pointer to the new, partially populated [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3978-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3978-115">Return value</span></span>

<span data-ttu-id="c3978-116">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c3978-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c3978-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3978-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c3978-118">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *pPartiallyPopulatedContextNodeCreated* cuando ya no necesite usar el nodo de contexto.</span><span class="sxs-lookup"><span data-stu-id="c3978-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pPartiallyPopulatedContextNodeCreated* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="c3978-119">El nuevo [**IContextNode**](icontextnode.md) se agrega a la colección de nodos secundarios del nodo de contexto (vea [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="c3978-119">The new [**IContextNode**](icontextnode.md) is added to this context node's collection of child nodes (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="c3978-120">Cuando hay nodos secundarios existentes, el **IContextNode** recién creado se agrega como el último nodo secundario.</span><span class="sxs-lookup"><span data-stu-id="c3978-120">When there are existing child nodes, the newly created **IContextNode** is added as the last child node.</span></span>

<span data-ttu-id="c3978-121">Para obtener más información sobre el tipo, el identificador y la ubicación, vea [**IContextNode:: GetType**](icontextnode-gettype.md), [**IContextNode:: getId**](icontextnode-getid.md)y [**IContextNode:: GetLocation**](icontextnode-getlocation.md).</span><span class="sxs-lookup"><span data-stu-id="c3978-121">For more information about type, identifier, and location, see [**IContextNode::GetType**](icontextnode-gettype.md), [**IContextNode::GetId**](icontextnode-getid.md), and [**IContextNode::GetLocation**](icontextnode-getlocation.md).</span></span>

<span data-ttu-id="c3978-122">Este método se usa para el proxy de datos como una manera de crear un objeto [**IContextNode**](icontextnode.md) en el árbol de nodos de contexto antes de que toda la información sobre él esté disponible.</span><span class="sxs-lookup"><span data-stu-id="c3978-122">This method is used for data proxy as a way to create an [**IContextNode**](icontextnode.md) object in the context node tree before all the information about it is available.</span></span> <span data-ttu-id="c3978-123">Para obtener más información, consulte [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c3978-123">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3978-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3978-124">Requirements</span></span>



| <span data-ttu-id="c3978-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3978-125">Requirement</span></span> | <span data-ttu-id="c3978-126">Value</span><span class="sxs-lookup"><span data-stu-id="c3978-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3978-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3978-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c3978-128">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c3978-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c3978-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3978-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c3978-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c3978-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c3978-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3978-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3978-132"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c3978-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c3978-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c3978-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3978-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3978-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c3978-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3978-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3978-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="c3978-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c3978-137">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="c3978-137">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="c3978-138">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="c3978-138">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="c3978-139">Tipos de nodo de contexto</span><span class="sxs-lookup"><span data-stu-id="c3978-139">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="c3978-140">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="c3978-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

