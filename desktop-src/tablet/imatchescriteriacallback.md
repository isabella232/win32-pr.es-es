---
description: Expone un método para evaluar si un objeto IContextNode cumple o no los criterios especificados.
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: Interfaz IMatchesCriteriaCallBack (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 960bd221bdd1f621f6ec4deb5ea167f5bf9ee4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540451"
---
# <a name="imatchescriteriacallback-interface"></a><span data-ttu-id="1987b-103">Interfaz IMatchesCriteriaCallBack</span><span class="sxs-lookup"><span data-stu-id="1987b-103">IMatchesCriteriaCallBack interface</span></span>

<span data-ttu-id="1987b-104">Expone un método para evaluar si un objeto [**IContextNode**](icontextnode.md) cumple o no los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="1987b-104">Exposes a method to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails a specified criteria.</span></span>

## <a name="members"></a><span data-ttu-id="1987b-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="1987b-105">Members</span></span>

<span data-ttu-id="1987b-106">La interfaz **IMatchesCriteriaCallBack** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1987b-106">The **IMatchesCriteriaCallBack** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1987b-107">**IMatchesCriteriaCallBack** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1987b-107">**IMatchesCriteriaCallBack** also has these types of members:</span></span>

-   [<span data-ttu-id="1987b-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="1987b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1987b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="1987b-109">Methods</span></span>

<span data-ttu-id="1987b-110">La interfaz **IMatchesCriteriaCallBack** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1987b-110">The **IMatchesCriteriaCallBack** interface has these methods.</span></span>



| <span data-ttu-id="1987b-111">Método</span><span class="sxs-lookup"><span data-stu-id="1987b-111">Method</span></span>                                                                      | <span data-ttu-id="1987b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1987b-112">Description</span></span>                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1987b-113">**EvaluateContextNode**</span><span class="sxs-lookup"><span data-stu-id="1987b-113">**EvaluateContextNode**</span></span>](imatchescriteriacallback-evaluatecontextnode.md) | <span data-ttu-id="1987b-114">Cuando se reemplaza en una clase derivada, evalúa si un objeto [**IContextNode**](icontextnode.md) especificado cumple los criterios.</span><span class="sxs-lookup"><span data-stu-id="1987b-114">When overridden in a derived class, evaluates whether a specified [**IContextNode**](icontextnode.md) object meets the criteria.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1987b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1987b-115">Remarks</span></span>

<span data-ttu-id="1987b-116">Para usar el método [**IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) o [**IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), cree una clase que implemente **IMatchesCriteriaCallBack**.</span><span class="sxs-lookup"><span data-stu-id="1987b-116">To use [**IInkAnalyzer::FindNodesWithCallBack Method**](iinkanalyzer-findnodeswithcallback.md) or [**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**](iinkanalyzer-findnodeswithcallbackinsubtree.md), create a class that implements **IMatchesCriteriaCallBack**.</span></span> <span data-ttu-id="1987b-117">Implemente [**IMatchesCriteriaCallBack:: EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) para devolver **Variant \_ true** si el objeto [**IContextNode**](icontextnode.md) coincide con los criterios y **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1987b-117">Implement [**IMatchesCriteriaCallBack::EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) to return **VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object matches your criteria, and **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="1987b-118">En algunos criterios, puede que tenga que proporcionar un medio para inicializar o mantener el estado del objeto **IMatchesCriteriaCallBack** .</span><span class="sxs-lookup"><span data-stu-id="1987b-118">For some criteria, you may need to provide a means of initializing or maintaining the state of your **IMatchesCriteriaCallBack** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1987b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1987b-119">Requirements</span></span>



| <span data-ttu-id="1987b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1987b-120">Requirement</span></span> | <span data-ttu-id="1987b-121">Value</span><span class="sxs-lookup"><span data-stu-id="1987b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1987b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1987b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1987b-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1987b-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1987b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1987b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1987b-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1987b-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1987b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1987b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1987b-127"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1987b-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1987b-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1987b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1987b-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1987b-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1987b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="1987b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1987b-131">**IInkAnalyzer:: FindNodesWithCallBack (método)**</span><span class="sxs-lookup"><span data-stu-id="1987b-131">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="1987b-132">**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="1987b-132">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="1987b-133">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="1987b-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

