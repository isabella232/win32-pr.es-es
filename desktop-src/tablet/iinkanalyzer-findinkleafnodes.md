---
description: Recupera todos los nodos de hoja de tinta.
ms.assetid: 988ae9f9-8fca-4757-8eb0-ae161e5690c9
title: 'IInkAnalyzer:: FindInkLeafNodes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d5ebcfe542ab03f2e3d3a24c29142e41433c9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908014"
---
# <a name="iinkanalyzerfindinkleafnodes-method"></a><span data-ttu-id="276a4-103">IInkAnalyzer:: FindInkLeafNodes (método)</span><span class="sxs-lookup"><span data-stu-id="276a4-103">IInkAnalyzer::FindInkLeafNodes method</span></span>

<span data-ttu-id="276a4-104">Recupera todos los nodos de hoja de tinta.</span><span class="sxs-lookup"><span data-stu-id="276a4-104">Retrieves all of the ink leaf nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="276a4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="276a4-105">Syntax</span></span>


```C++
HRESULT FindInkLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="276a4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="276a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="276a4-107">*ppContextNodesFound* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="276a4-107">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="276a4-108">Puntero a la colección [**IContextNodes**](icontextnodes.md) que contiene todos los nodos de hoja de tinta.</span><span class="sxs-lookup"><span data-stu-id="276a4-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all ink leaf nodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="276a4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="276a4-109">Return value</span></span>

<span data-ttu-id="276a4-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="276a4-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="276a4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="276a4-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="276a4-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodesFound* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="276a4-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="276a4-113">Los nodos hoja no contienen nodos secundarios.</span><span class="sxs-lookup"><span data-stu-id="276a4-113">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="276a4-114">Los nodos de tinta contienen datos de trazo.</span><span class="sxs-lookup"><span data-stu-id="276a4-114">Ink nodes contain stroke data.</span></span> <span data-ttu-id="276a4-115">Ejemplos de nodos de hoja de tinta son los objetos InkWord, InkDrawing y InkBullet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="276a4-115">Examples of ink leaf nodes are InkWord, InkDrawing, and InkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="276a4-116">Para obtener más información, vea [tipos de nodo de contexto](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="276a4-116">For more information, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="276a4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="276a4-117">Requirements</span></span>



| <span data-ttu-id="276a4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="276a4-118">Requirement</span></span> | <span data-ttu-id="276a4-119">Value</span><span class="sxs-lookup"><span data-stu-id="276a4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="276a4-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="276a4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="276a4-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="276a4-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="276a4-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="276a4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="276a4-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="276a4-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="276a4-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="276a4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="276a4-125"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="276a4-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="276a4-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="276a4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="276a4-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="276a4-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="276a4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="276a4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="276a4-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="276a4-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="276a4-130">**IInkAnalyzer:: FindInkLeafNodesForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="276a4-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="276a4-131">**IInkAnalyzer:: FindLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="276a4-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="276a4-132">**IInkAnalyzer:: FindNode (método)**</span><span class="sxs-lookup"><span data-stu-id="276a4-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="276a4-133">**IInkAnalyzer:: FindNodesOfType (método)**</span><span class="sxs-lookup"><span data-stu-id="276a4-133">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="276a4-134">**IInkAnalyzer:: FindNodesOfTypeForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="276a4-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="276a4-135">**IInkAnalyzer:: FindNodesOfTypeInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="276a4-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="276a4-136">**IInkAnalyzer:: FindNodesWithCallBack (método)**</span><span class="sxs-lookup"><span data-stu-id="276a4-136">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="276a4-137">**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="276a4-137">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="276a4-138">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="276a4-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

