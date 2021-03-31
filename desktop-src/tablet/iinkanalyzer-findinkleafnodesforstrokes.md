---
description: Recupera los nodos de hoja de tinta que contienen los trazos especificados.
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: 'IInkAnalyzer:: FindInkLeafNodesForStrokes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d19bed823f5385533dfc938eb9f6013b4a5640c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908012"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a><span data-ttu-id="01f0a-103">IInkAnalyzer:: FindInkLeafNodesForStrokes (método)</span><span class="sxs-lookup"><span data-stu-id="01f0a-103">IInkAnalyzer::FindInkLeafNodesForStrokes method</span></span>

<span data-ttu-id="01f0a-104">Recupera los nodos de hoja de tinta que contienen los trazos especificados.</span><span class="sxs-lookup"><span data-stu-id="01f0a-104">Retrieves the ink leaf nodes that contain the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="01f0a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01f0a-105">Syntax</span></span>


```C++
HRESULT FindInkLeafNodesForStrokes(
  [in]  ULONG         ulStrokeIdsCount,
  [in]  LONG          *plStrokeIds,
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="01f0a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01f0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01f0a-107">*ulStrokeIdsCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01f0a-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01f0a-108">Número de identificadores de trazo pasados.</span><span class="sxs-lookup"><span data-stu-id="01f0a-108">The number of stroke identifiers passed in.</span></span>

</dd> <dt>

<span data-ttu-id="01f0a-109">*plStrokeIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01f0a-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01f0a-110">Matriz de los identificadores de trazo.</span><span class="sxs-lookup"><span data-stu-id="01f0a-110">An array of the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="01f0a-111">*ppContextNodesFound* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="01f0a-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01f0a-112">Colección de objetos [**IContextNode**](icontextnode.md) que contienen todos los nodos de hoja de tinta que contienen los trazos con identificadores en la matriz *plStrokeIds* .</span><span class="sxs-lookup"><span data-stu-id="01f0a-112">The collection of [**IContextNode**](icontextnode.md) objects that contain all the ink leaf nodes that contain the strokes with identifiers in the *plStrokeIds* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01f0a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01f0a-113">Return value</span></span>

<span data-ttu-id="01f0a-114">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="01f0a-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="01f0a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01f0a-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="01f0a-116">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodesFound* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="01f0a-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="01f0a-117">Los nodos hoja no contienen nodos secundarios.</span><span class="sxs-lookup"><span data-stu-id="01f0a-117">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="01f0a-118">Los nodos de tinta contienen datos de trazo.</span><span class="sxs-lookup"><span data-stu-id="01f0a-118">Ink nodes contain stroke data.</span></span> <span data-ttu-id="01f0a-119">Ejemplos de nodos de hoja de tinta son los objetos InkWord, InkDrawing, andInkBullet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="01f0a-119">Examples of ink leaf nodes are InkWord, InkDrawing, andInkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="01f0a-120">Para obtener más información, vea [tipos de nodo de contexto](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="01f0a-120">For more information, see [Context Node Types](context-node-types.md).</span></span>

<span data-ttu-id="01f0a-121">Si ningún nodo contiene los trazos especificados, se devuelve una colección [**IContextNodes**](icontextnodes.md) vacía.</span><span class="sxs-lookup"><span data-stu-id="01f0a-121">If no nodes contain the specified strokes, an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span> <span data-ttu-id="01f0a-122">Del mismo modo, si *ulStrokeIdsCount* es cero, se devuelve una colección **IContextNodes** vacía.</span><span class="sxs-lookup"><span data-stu-id="01f0a-122">Similarly, if *ulStrokeIdsCount* is zero, an empty **IContextNodes** collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="01f0a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01f0a-123">Requirements</span></span>



| <span data-ttu-id="01f0a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="01f0a-124">Requirement</span></span> | <span data-ttu-id="01f0a-125">Value</span><span class="sxs-lookup"><span data-stu-id="01f0a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01f0a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01f0a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="01f0a-127">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="01f0a-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="01f0a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01f0a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="01f0a-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="01f0a-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="01f0a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01f0a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="01f0a-131"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="01f0a-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="01f0a-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="01f0a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01f0a-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01f0a-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="01f0a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="01f0a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f0a-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="01f0a-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="01f0a-136">**IInkAnalyzer:: FindInkLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="01f0a-136">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="01f0a-137">**IInkAnalyzer:: FindLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="01f0a-137">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="01f0a-138">**IInkAnalyzer:: FindNode (método)**</span><span class="sxs-lookup"><span data-stu-id="01f0a-138">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="01f0a-139">**IInkAnalyzer:: FindNodesOfType (método)**</span><span class="sxs-lookup"><span data-stu-id="01f0a-139">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="01f0a-140">**IInkAnalyzer:: FindNodesOfTypeForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="01f0a-140">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="01f0a-141">**IInkAnalyzer:: FindNodesOfTypeInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="01f0a-141">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="01f0a-142">**IInkAnalyzer:: FindNodesWithCallBack (método)**</span><span class="sxs-lookup"><span data-stu-id="01f0a-142">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="01f0a-143">**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="01f0a-143">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="01f0a-144">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="01f0a-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

