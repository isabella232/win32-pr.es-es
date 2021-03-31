---
description: Recupera todos los objetos IContextNode que coinciden con los criterios especificados y son descendientes del objeto IContextNode especificado.
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: 'IInkAnalyzer:: FindNodesWithCallBackInSubTree (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBackInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6b4ba64cd9271158d49ddd72270d4e6f25538672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810021"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a><span data-ttu-id="79fb5-103">IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)</span><span class="sxs-lookup"><span data-stu-id="79fb5-103">IInkAnalyzer::FindNodesWithCallBackInSubTree method</span></span>

<span data-ttu-id="79fb5-104">Recupera todos los objetos [**IContextNode**](icontextnode.md) que coinciden con los criterios especificados y son descendientes del objeto **IContextNode** especificado.</span><span class="sxs-lookup"><span data-stu-id="79fb5-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects that match the specified criteria and are descendants of the specified **IContextNode** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="79fb5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79fb5-105">Syntax</span></span>


```C++
HRESULT FindNodesWithCallBackInSubTree(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [in]  IContextNode             *pContextNodeToSearchFrom,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="79fb5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79fb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79fb5-107">*pCriteria* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79fb5-107">*pCriteria* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fb5-108">Un objeto [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) que se usa para evaluar si un objeto [**IContextNode**](icontextnode.md) cumple o no los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="79fb5-108">An [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) object that is used to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails its specified criteria.</span></span>

</dd> <dt>

<span data-ttu-id="79fb5-109">*pContextNodeToSearchFrom* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79fb5-109">*pContextNodeToSearchFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fb5-110">Objeto [**IContextNode**](icontextnode.md) cuyos descendientes se buscan.</span><span class="sxs-lookup"><span data-stu-id="79fb5-110">The [**IContextNode**](icontextnode.md) object whose descendants are searched.</span></span>

</dd> <dt>

<span data-ttu-id="79fb5-111">*ppContextNodesFound* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79fb5-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79fb5-112">Puntero al [**IContextNodes**](icontextnodes.md) que contiene todos los nodos que cumplen los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="79fb5-112">A pointer to the [**IContextNodes**](icontextnodes.md) containing all nodes that meet the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79fb5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79fb5-113">Return value</span></span>

<span data-ttu-id="79fb5-114">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="79fb5-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="79fb5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79fb5-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="79fb5-116">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodesFound* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="79fb5-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="79fb5-117">Si [**IInkAnalyzer**](iinkanalyzer.md) no contiene el nodo *pContextNodeToSearchFrom* , este método devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="79fb5-117">If the [**IInkAnalyzer**](iinkanalyzer.md) does not contain the *pContextNodeToSearchFrom* node, this method returns an error code.</span></span>

<span data-ttu-id="79fb5-118">Si [**IInkAnalyzer**](iinkanalyzer.md) no contiene este [**IContextNode**](icontextnode.md), se devuelve una colección [**IContextNodes**](icontextnodes.md) vacía.</span><span class="sxs-lookup"><span data-stu-id="79fb5-118">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="79fb5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79fb5-119">Requirements</span></span>



| <span data-ttu-id="79fb5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="79fb5-120">Requirement</span></span> | <span data-ttu-id="79fb5-121">Value</span><span class="sxs-lookup"><span data-stu-id="79fb5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79fb5-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79fb5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="79fb5-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="79fb5-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="79fb5-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79fb5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="79fb5-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="79fb5-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="79fb5-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79fb5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="79fb5-127"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="79fb5-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="79fb5-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79fb5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79fb5-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79fb5-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="79fb5-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="79fb5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79fb5-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="79fb5-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="79fb5-132">**IInkAnalyzer:: FindInkLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="79fb5-132">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="79fb5-133">**IInkAnalyzer:: FindInkLeafNodesForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="79fb5-133">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="79fb5-134">**IInkAnalyzer:: FindLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="79fb5-134">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="79fb5-135">**IInkAnalyzer:: FindNode (método)**</span><span class="sxs-lookup"><span data-stu-id="79fb5-135">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="79fb5-136">**IInkAnalyzer:: FindNodesOfType (método)**</span><span class="sxs-lookup"><span data-stu-id="79fb5-136">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="79fb5-137">**IInkAnalyzer:: FindNodesOfTypeForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="79fb5-137">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="79fb5-138">**IInkAnalyzer:: FindNodesOfTypeInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="79fb5-138">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="79fb5-139">**IInkAnalyzer:: FindNodesWithCallBack (método)**</span><span class="sxs-lookup"><span data-stu-id="79fb5-139">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="79fb5-140">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="79fb5-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

