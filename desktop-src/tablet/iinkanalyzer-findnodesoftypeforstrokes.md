---
description: Recupera todos los objetos IContextNode del tipo especificado que contienen los trazos especificados.
ms.assetid: c674a03b-841c-4a9c-8268-302bc4038934
title: 'IInkAnalyzer:: FindNodesOfTypeForStrokes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dd98c72007a69521506e2be21ad10edeb46df27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715208"
---
# <a name="iinkanalyzerfindnodesoftypeforstrokes-method"></a><span data-ttu-id="7eaef-103">IInkAnalyzer:: FindNodesOfTypeForStrokes (método)</span><span class="sxs-lookup"><span data-stu-id="7eaef-103">IInkAnalyzer::FindNodesOfTypeForStrokes method</span></span>

<span data-ttu-id="7eaef-104">Recupera todos los objetos [**IContextNode**](icontextnode.md) del tipo especificado que contienen los trazos especificados.</span><span class="sxs-lookup"><span data-stu-id="7eaef-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type that contain the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eaef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7eaef-105">Syntax</span></span>


```C++
HRESULT FindNodesOfTypeForStrokes(
  [in]  const GUID          *pNodeType,
  [in]        ULONG         ulStrokeIdsCount,
  [in]        LONG          *plStrokeIds,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="7eaef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7eaef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eaef-107">*pNodeType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7eaef-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eaef-108">Identificador único global (GUID) que especifica el tipo de nodo.</span><span class="sxs-lookup"><span data-stu-id="7eaef-108">The globally unique identifier (GUID) that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="7eaef-109">*ulStrokeIdsCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7eaef-109">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eaef-110">Número de identificadores de trazo pasados.</span><span class="sxs-lookup"><span data-stu-id="7eaef-110">The number of stroke identifiers passed in.</span></span>

</dd> <dt>

<span data-ttu-id="7eaef-111">*plStrokeIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7eaef-111">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eaef-112">Matriz de los identificadores de trazo.</span><span class="sxs-lookup"><span data-stu-id="7eaef-112">An array of the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="7eaef-113">*ppContextNodesFound* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7eaef-113">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7eaef-114">Colección de objetos [**IContextNode**](icontextnode.md) que contienen todos los nodos de tipo *pNodeType* que contienen los trazos con identificadores en la matriz *plStrokeIds* .</span><span class="sxs-lookup"><span data-stu-id="7eaef-114">The collection of [**IContextNode**](icontextnode.md) objects that contain all the nodes of type *pNodeType* that contain the strokes with identifiers in the *plStrokeIds* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eaef-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7eaef-115">Return value</span></span>

<span data-ttu-id="7eaef-116">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7eaef-116">For a description of return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7eaef-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7eaef-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="7eaef-118">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppContextNodesFound* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="7eaef-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="7eaef-119">La propiedad *pNodeType* debe contener un GUID de las constantes de [tipos de nodo de contexto](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="7eaef-119">The *pNodeType* property must contain a GUID from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="7eaef-120">Si el tipo de nodo especificado no es un nodo hoja, pero uno de los descendientes del nodo hace referencia a un trazo de la colección Strokes, ese nodo se agrega a la colección que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="7eaef-120">If the specified node type is not a leaf node, but one of the node's descendants references a stroke in the strokes collection, that node is added to the collection that is returned.</span></span>

<span data-ttu-id="7eaef-121">Si [**IInkAnalyzer**](iinkanalyzer.md) no contiene este [**IContextNode**](icontextnode.md), se devuelve una colección [**IContextNodes**](icontextnodes.md) vacía.</span><span class="sxs-lookup"><span data-stu-id="7eaef-121">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eaef-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eaef-122">Requirements</span></span>



| <span data-ttu-id="7eaef-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eaef-123">Requirement</span></span> | <span data-ttu-id="7eaef-124">Value</span><span class="sxs-lookup"><span data-stu-id="7eaef-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eaef-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7eaef-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7eaef-126">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7eaef-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7eaef-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7eaef-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7eaef-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7eaef-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7eaef-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7eaef-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7eaef-130"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7eaef-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7eaef-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7eaef-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eaef-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7eaef-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7eaef-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="7eaef-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eaef-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="7eaef-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="7eaef-135">**IInkAnalyzer:: FindInkLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="7eaef-135">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="7eaef-136">**IInkAnalyzer:: FindInkLeafNodesForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="7eaef-136">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="7eaef-137">**IInkAnalyzer:: FindLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="7eaef-137">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="7eaef-138">**IInkAnalyzer:: FindNode (método)**</span><span class="sxs-lookup"><span data-stu-id="7eaef-138">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="7eaef-139">**IInkAnalyzer:: FindNodesOfType (método)**</span><span class="sxs-lookup"><span data-stu-id="7eaef-139">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="7eaef-140">**IInkAnalyzer:: FindNodesOfTypeInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="7eaef-140">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="7eaef-141">**IInkAnalyzer:: FindNodesWithCallBack (método)**</span><span class="sxs-lookup"><span data-stu-id="7eaef-141">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="7eaef-142">**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="7eaef-142">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="7eaef-143">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="7eaef-143">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

