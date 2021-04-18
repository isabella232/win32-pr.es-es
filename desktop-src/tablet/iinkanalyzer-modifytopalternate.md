---
description: Cambia la alternativa superior actual a la alternativa especificada y borra el tipo de confirmación de todos los objetos IContextNode asociados con la alternativa.
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: 'IInkAnalyzer:: ModifyTopAlternate (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da2fcde7015e993e13e47673b271c560b6c3d72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715203"
---
# <a name="iinkanalyzermodifytopalternate-method"></a><span data-ttu-id="6fd1c-103">IInkAnalyzer:: ModifyTopAlternate (método)</span><span class="sxs-lookup"><span data-stu-id="6fd1c-103">IInkAnalyzer::ModifyTopAlternate method</span></span>

<span data-ttu-id="6fd1c-104">Cambia la alternativa superior actual a la alternativa especificada y borra el tipo de confirmación de todos los objetos [**IContextNode**](icontextnode.md) asociados con la alternativa.</span><span class="sxs-lookup"><span data-stu-id="6fd1c-104">Changes the current top alternate to the specified alternate and clears the confirmation type for all [**IContextNode**](icontextnode.md) objects associated with the alternate.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fd1c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6fd1c-105">Syntax</span></span>


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a><span data-ttu-id="6fd1c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6fd1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fd1c-107">*pAlternate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6fd1c-107">*pAlternate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fd1c-108">Objeto [**IAnalysisAlternate**](ianalysisalternate.md) que contiene el nuevo alternativo superior.</span><span class="sxs-lookup"><span data-stu-id="6fd1c-108">The [**IAnalysisAlternate**](ianalysisalternate.md) object containing the new top alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fd1c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6fd1c-109">Return value</span></span>

<span data-ttu-id="6fd1c-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6fd1c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6fd1c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6fd1c-111">Remarks</span></span>

<span data-ttu-id="6fd1c-112">Para obtener alternativas de análisis, use el método [**IInkAnalyzer:: GetAlternates**](iinkanalyzer-getalternates.md), el método [**IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)o [**IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="6fd1c-112">To get analysis alternates, use [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes Method**](iinkanalyzer-getalternatesforcontextnodes.md), or [**IInkAnalyzer::GetAlternatesForStrokes Method**](iinkanalyzer-getalternatesforstrokes.md).</span></span> <span data-ttu-id="6fd1c-113">Para obtener los objetos [**IContextNode**](icontextnode.md) asociados a una alternativa de análisis, use el [**método IAnalysisAlternate:: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).</span><span class="sxs-lookup"><span data-stu-id="6fd1c-113">To get the [**IContextNode**](icontextnode.md) objects associated with an analysis alternate, use [**IAnalysisAlternate::GetAlternateNodes Method**](ianalysisalternate-getalternatenodes.md).</span></span>

<span data-ttu-id="6fd1c-114">Para cambiar el tipo de confirmación de un nodo de contexto, use [**IContextNode:: CONFIRM**](icontextnode-confirm.md).</span><span class="sxs-lookup"><span data-stu-id="6fd1c-114">To change the confirmation type for a context node, use [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fd1c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fd1c-115">Requirements</span></span>



| <span data-ttu-id="6fd1c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fd1c-116">Requirement</span></span> | <span data-ttu-id="6fd1c-117">Value</span><span class="sxs-lookup"><span data-stu-id="6fd1c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd1c-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fd1c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6fd1c-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6fd1c-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6fd1c-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fd1c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6fd1c-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6fd1c-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6fd1c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6fd1c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fd1c-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6fd1c-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6fd1c-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6fd1c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fd1c-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fd1c-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6fd1c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6fd1c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fd1c-127">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="6fd1c-127">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="6fd1c-128">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="6fd1c-128">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="6fd1c-129">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="6fd1c-129">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="6fd1c-130">**ConfirmationType**</span><span class="sxs-lookup"><span data-stu-id="6fd1c-130">**ConfirmationType**</span></span>](confirmationtype.md)
</dt> <dt>

[<span data-ttu-id="6fd1c-131">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="6fd1c-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




