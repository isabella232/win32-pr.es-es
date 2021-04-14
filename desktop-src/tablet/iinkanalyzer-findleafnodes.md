---
description: Recupera todos los nodos hoja.
ms.assetid: 5534053c-c5b9-4576-857f-c8af39e821a7
title: 'IInkAnalyzer:: FindLeafNodes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f923afe94c25e45dbcbfe79d554282b69ebec3a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542022"
---
# <a name="iinkanalyzerfindleafnodes-method"></a><span data-ttu-id="fb711-103">IInkAnalyzer:: FindLeafNodes (método)</span><span class="sxs-lookup"><span data-stu-id="fb711-103">IInkAnalyzer::FindLeafNodes method</span></span>

<span data-ttu-id="fb711-104">Recupera todos los nodos hoja.</span><span class="sxs-lookup"><span data-stu-id="fb711-104">Retrieves all of the leaf nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb711-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb711-105">Syntax</span></span>


```C++
HRESULT FindLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="fb711-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb711-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb711-107">*ppContextNodesFound* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fb711-107">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb711-108">Un puntero a la colección [**IContextNodes**](icontextnodes.md) que contiene todos los nodos hoja.</span><span class="sxs-lookup"><span data-stu-id="fb711-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all leaf nodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb711-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb711-109">Return value</span></span>

<span data-ttu-id="fb711-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fb711-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb711-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb711-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="fb711-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodesFound* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="fb711-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="fb711-113">Los nodos hoja no contienen nodos secundarios.</span><span class="sxs-lookup"><span data-stu-id="fb711-113">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="fb711-114">Ejemplos de nodos de hoja de tinta son los objetos InkWord, TextWord, Image, InkDrawing y InkBullet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="fb711-114">Examples of ink leaf nodes are InkWord, TextWord, Image, InkDrawing, and InkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="fb711-115">Para obtener más información, vea [tipos de nodo de contexto](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="fb711-115">For more information, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb711-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb711-116">Requirements</span></span>



| <span data-ttu-id="fb711-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb711-117">Requirement</span></span> | <span data-ttu-id="fb711-118">Value</span><span class="sxs-lookup"><span data-stu-id="fb711-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb711-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb711-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fb711-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fb711-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fb711-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb711-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fb711-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fb711-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fb711-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb711-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb711-124"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fb711-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fb711-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb711-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb711-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb711-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fb711-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb711-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb711-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="fb711-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="fb711-129">**IInkAnalyzer:: FindInkLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="fb711-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="fb711-130">**IInkAnalyzer:: FindInkLeafNodesForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="fb711-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="fb711-131">**IInkAnalyzer:: FindNode (método)**</span><span class="sxs-lookup"><span data-stu-id="fb711-131">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="fb711-132">**IInkAnalyzer:: FindNodesOfType (método)**</span><span class="sxs-lookup"><span data-stu-id="fb711-132">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="fb711-133">**IInkAnalyzer:: FindNodesOfTypeForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="fb711-133">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="fb711-134">**IInkAnalyzer:: FindNodesOfTypeInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="fb711-134">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="fb711-135">**IInkAnalyzer:: FindNodesWithCallBack (método)**</span><span class="sxs-lookup"><span data-stu-id="fb711-135">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="fb711-136">**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="fb711-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="fb711-137">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="fb711-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

