---
description: Cuando se reemplaza en una clase derivada, evalúa si un objeto IContextNode especificado cumple los criterios.
ms.assetid: ade8e59c-6aeb-4a87-a95d-229f8f0b2223
title: 'IMatchesCriteriaCallBack:: EvaluateContextNode (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack.EvaluateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 554cf451396101de2238258de0a0706956f24a02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648181"
---
# <a name="imatchescriteriacallbackevaluatecontextnode-method"></a><span data-ttu-id="c8273-103">IMatchesCriteriaCallBack:: EvaluateContextNode (método)</span><span class="sxs-lookup"><span data-stu-id="c8273-103">IMatchesCriteriaCallBack::EvaluateContextNode method</span></span>

<span data-ttu-id="c8273-104">Cuando se reemplaza en una clase derivada, evalúa si un objeto [**IContextNode**](icontextnode.md) especificado cumple los criterios.</span><span class="sxs-lookup"><span data-stu-id="c8273-104">When overridden in a derived class, evaluates whether a specified [**IContextNode**](icontextnode.md) object meets the criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8273-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8273-105">Syntax</span></span>


```C++
HRESULT EvaluateContextNode(
  [in]  IContextNode *pContextNodeToEvaluate,
  [out] VARIANT_BOOL *pbResult
);
```



## <a name="parameters"></a><span data-ttu-id="c8273-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8273-107">*pContextNodeToEvaluate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8273-107">*pContextNodeToEvaluate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8273-108">Objeto [**IContextNode**](icontextnode.md) que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="c8273-108">The [**IContextNode**](icontextnode.md) object to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="c8273-109">*pbResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c8273-109">*pbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8273-110">**Variante \_ TRUE** si *pContextNodeToEvaluate* coincide con los criterios; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="c8273-110">**VARIANT\_TRUE** if *pContextNodeToEvaluate* matches the criteria; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8273-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8273-111">Return value</span></span>

<span data-ttu-id="c8273-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c8273-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c8273-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8273-113">Remarks</span></span>

<span data-ttu-id="c8273-114">Para usar el método [**IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) o [**IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), cree una clase que implemente [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md).</span><span class="sxs-lookup"><span data-stu-id="c8273-114">To use [**IInkAnalyzer::FindNodesWithCallBack Method**](iinkanalyzer-findnodeswithcallback.md) or [**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**](iinkanalyzer-findnodeswithcallbackinsubtree.md), create a class that implements [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md).</span></span> <span data-ttu-id="c8273-115">Implemente **IMatchesCriteriaCallBack:: EvaluateContextNode** para devolver **Variant \_ true** si el objeto [**IContextNode**](icontextnode.md) coincide con los criterios y **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c8273-115">Implement **IMatchesCriteriaCallBack::EvaluateContextNode** to return **VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object matches your criteria, and **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="c8273-116">En algunos criterios, puede que tenga que proporcionar un medio para inicializar o mantener el estado del objeto **IMatchesCriteriaCallBack** .</span><span class="sxs-lookup"><span data-stu-id="c8273-116">For some criteria, you may need to provide a means of initializing or maintaining the state of your **IMatchesCriteriaCallBack** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8273-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8273-117">Requirements</span></span>



| <span data-ttu-id="c8273-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8273-118">Requirement</span></span> | <span data-ttu-id="c8273-119">Value</span><span class="sxs-lookup"><span data-stu-id="c8273-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8273-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8273-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c8273-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c8273-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c8273-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8273-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c8273-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c8273-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c8273-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8273-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8273-125"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c8273-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c8273-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8273-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8273-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8273-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c8273-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8273-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8273-129">**IMatchesCriteriaCallBack**</span><span class="sxs-lookup"><span data-stu-id="c8273-129">**IMatchesCriteriaCallBack**</span></span>](imatchescriteriacallback.md)
</dt> <dt>

[<span data-ttu-id="c8273-130">**IInkAnalyzer:: FindNodesWithCallBack (método)**</span><span class="sxs-lookup"><span data-stu-id="c8273-130">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="c8273-131">**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="c8273-131">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="c8273-132">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="c8273-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




