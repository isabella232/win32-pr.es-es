---
description: Recupera todos los objetos IContextNode del tipo especificado.
ms.assetid: e6e68d78-9697-40e6-a4ae-a187ef01a769
title: 'IInkAnalyzer:: FindNodesOfType (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 51611fd4b3c77b43f2ea0d967f81dcc9547edb24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908011"
---
# <a name="iinkanalyzerfindnodesoftype-method"></a><span data-ttu-id="7ded2-103">IInkAnalyzer:: FindNodesOfType (método)</span><span class="sxs-lookup"><span data-stu-id="7ded2-103">IInkAnalyzer::FindNodesOfType method</span></span>

<span data-ttu-id="7ded2-104">Recupera todos los objetos [**IContextNode**](icontextnode.md) del tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="7ded2-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ded2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ded2-105">Syntax</span></span>


```C++
HRESULT FindNodesOfType(
  [in]  const GUID          *pNodeType,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="7ded2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ded2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ded2-107">*pNodeType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7ded2-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ded2-108">**GUID** que especifica el tipo de nodo.</span><span class="sxs-lookup"><span data-stu-id="7ded2-108">The **GUID** that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="7ded2-109">*ppContextNodesFound* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7ded2-109">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ded2-110">Un puntero a la [**IContextNodes**](icontextnodes.md) que contiene todos los nodos de tipo *pNodeType*.</span><span class="sxs-lookup"><span data-stu-id="7ded2-110">A pointer to the [**IContextNodes**](icontextnodes.md) containing all nodes of type *pNodeType*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ded2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ded2-111">Return value</span></span>

<span data-ttu-id="7ded2-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7ded2-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ded2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ded2-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="7ded2-114">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodesFound* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="7ded2-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="7ded2-115">La propiedad *pNodeType* debe contener un GUID de las constantes de [tipos de nodo de contexto](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="7ded2-115">The *pNodeType* property must contain a GUID from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="7ded2-116">Si [**IInkAnalyzer**](iinkanalyzer.md) no contiene este [**IContextNode**](icontextnode.md), se devuelve una colección [**IContextNodes**](icontextnodes.md) vacía.</span><span class="sxs-lookup"><span data-stu-id="7ded2-116">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ded2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ded2-117">Requirements</span></span>



| <span data-ttu-id="7ded2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ded2-118">Requirement</span></span> | <span data-ttu-id="7ded2-119">Value</span><span class="sxs-lookup"><span data-stu-id="7ded2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ded2-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ded2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7ded2-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7ded2-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7ded2-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ded2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7ded2-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7ded2-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7ded2-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ded2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ded2-125"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7ded2-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7ded2-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7ded2-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ded2-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ded2-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7ded2-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ded2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ded2-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="7ded2-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="7ded2-130">**IInkAnalyzer:: FindInkLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="7ded2-130">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="7ded2-131">**IInkAnalyzer:: FindInkLeafNodesForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="7ded2-131">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="7ded2-132">**IInkAnalyzer:: FindLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="7ded2-132">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="7ded2-133">**IInkAnalyzer:: FindNode (método)**</span><span class="sxs-lookup"><span data-stu-id="7ded2-133">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="7ded2-134">**IInkAnalyzer:: FindNodesOfTypeForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="7ded2-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="7ded2-135">**IInkAnalyzer:: FindNodesOfTypeInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="7ded2-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="7ded2-136">**IInkAnalyzer:: FindNodesWithCallBack (método)**</span><span class="sxs-lookup"><span data-stu-id="7ded2-136">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="7ded2-137">**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="7ded2-137">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="7ded2-138">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="7ded2-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

