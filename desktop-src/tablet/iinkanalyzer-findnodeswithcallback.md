---
description: Recupera todos los objetos IContextNode que coinciden con los criterios especificados.
ms.assetid: c0ba46f4-a286-454a-8de2-6663fd2dfed6
title: 'IInkAnalyzer:: FindNodesWithCallBack (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b34501e33d637ca65f13e6e2e5ea0a9001b06198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810022"
---
# <a name="iinkanalyzerfindnodeswithcallback-method"></a><span data-ttu-id="cea8d-103">IInkAnalyzer:: FindNodesWithCallBack (método)</span><span class="sxs-lookup"><span data-stu-id="cea8d-103">IInkAnalyzer::FindNodesWithCallBack method</span></span>

<span data-ttu-id="cea8d-104">Recupera todos los objetos [**IContextNode**](icontextnode.md) que coinciden con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="cea8d-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects that match the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="cea8d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cea8d-105">Syntax</span></span>


```C++
HRESULT FindNodesWithCallBack(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="cea8d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cea8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cea8d-107">*pCriteria* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cea8d-107">*pCriteria* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea8d-108">Un objeto [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) que se usa para evaluar si un objeto [**IContextNode**](icontextnode.md) cumple o no los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="cea8d-108">An [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) object that is used to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails its specified criteria.</span></span>

</dd> <dt>

<span data-ttu-id="cea8d-109">*ppContextNodesFound* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cea8d-109">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cea8d-110">Un puntero a la colección [**IContextNodes**](icontextnodes.md) que contiene todos los nodos que cumplen los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="cea8d-110">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all nodes that meet the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cea8d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cea8d-111">Return value</span></span>

<span data-ttu-id="cea8d-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cea8d-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cea8d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cea8d-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="cea8d-114">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppContextNodesFound* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="cea8d-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="cea8d-115">Si [**IInkAnalyzer**](iinkanalyzer.md) no contiene este [**IContextNode**](icontextnode.md), se devuelve una colección [**IContextNodes**](icontextnodes.md) vacía.</span><span class="sxs-lookup"><span data-stu-id="cea8d-115">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="cea8d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cea8d-116">Requirements</span></span>



| <span data-ttu-id="cea8d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cea8d-117">Requirement</span></span> | <span data-ttu-id="cea8d-118">Value</span><span class="sxs-lookup"><span data-stu-id="cea8d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cea8d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cea8d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cea8d-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cea8d-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cea8d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cea8d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cea8d-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cea8d-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cea8d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cea8d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cea8d-124"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cea8d-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cea8d-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cea8d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cea8d-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cea8d-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cea8d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="cea8d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea8d-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="cea8d-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="cea8d-129">**IInkAnalyzer:: FindInkLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="cea8d-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="cea8d-130">**IInkAnalyzer:: FindInkLeafNodesForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="cea8d-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="cea8d-131">**IInkAnalyzer:: FindLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="cea8d-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="cea8d-132">**IInkAnalyzer:: FindNode (método)**</span><span class="sxs-lookup"><span data-stu-id="cea8d-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="cea8d-133">**IInkAnalyzer:: FindNodesOfType (método)**</span><span class="sxs-lookup"><span data-stu-id="cea8d-133">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="cea8d-134">**IInkAnalyzer:: FindNodesOfTypeForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="cea8d-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="cea8d-135">**IInkAnalyzer:: FindNodesOfTypeInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="cea8d-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="cea8d-136">**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="cea8d-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="cea8d-137">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="cea8d-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

