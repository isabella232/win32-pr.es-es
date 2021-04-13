---
description: Cambia la alternativa superior actual al IAnalysisAlternate especificado.
ms.assetid: 0867a662-d172-4ca2-a41f-49c0ea454768
title: 'IInkAnalyzer:: ModifyTopAlternateWithConfirmation (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternateWithConfirmation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 60b0221e7d27cfd5d601dcf77e80a297045d39a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360337"
---
# <a name="iinkanalyzermodifytopalternatewithconfirmation-method"></a><span data-ttu-id="6b71a-103">IInkAnalyzer:: ModifyTopAlternateWithConfirmation (método)</span><span class="sxs-lookup"><span data-stu-id="6b71a-103">IInkAnalyzer::ModifyTopAlternateWithConfirmation method</span></span>

<span data-ttu-id="6b71a-104">Cambia la alternativa superior actual al [**IAnalysisAlternate**](ianalysisalternate.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="6b71a-104">Changes the current top alternate to the specified [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6b71a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b71a-105">Syntax</span></span>


```C++
HRESULT ModifyTopAlternateWithConfirmation(
  [in] IAnalysisAlternate *alternate,
  [in] VARIANT_BOOL       fconfirmAutomatically
);
```



## <a name="parameters"></a><span data-ttu-id="6b71a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b71a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b71a-107">*alternativa* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6b71a-107">*alternate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b71a-108">Alternativa de análisis que se va a establecer como la nueva alternativa superior.</span><span class="sxs-lookup"><span data-stu-id="6b71a-108">The analysis alternate to set as the new top alternate.</span></span>

</dd> <dt>

<span data-ttu-id="6b71a-109">*fconfirmAutomatically* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6b71a-109">*fconfirmAutomatically* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b71a-110">**Variante \_ TRUE** para establecer todos los nodos de contexto de hoja de tinta que corresponden al análisis alternativo a un tipo de confirmación de **ConfirmationType \_ NodeTypeAndProperties** (vea [**IContextNode:: IsConfirmed**](icontextnode-isconfirmed.md) y [**ConfirmationType**](confirmationtype.md)); **Variante \_ FALSE** para establecer todos los nodos de contexto de hoja de tinta que corresponden al análisis alternativo a un tipo de confirmación de **ConfirmationType \_ ninguno**.</span><span class="sxs-lookup"><span data-stu-id="6b71a-110">**VARIANT\_TRUE** to set all of the ink leaf context nodes that correspond to the analysis alternate to a confirmation type of **ConfirmationType\_NodeTypeAndProperties** (see [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md) and [**ConfirmationType**](confirmationtype.md)); **VARIANT\_FALSE** to set all of the ink leaf context nodes that correspond to the analysis alternate to a confirmation type of **ConfirmationType\_None**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b71a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b71a-111">Return value</span></span>

<span data-ttu-id="6b71a-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6b71a-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6b71a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b71a-113">Remarks</span></span>

<span data-ttu-id="6b71a-114">Para obtener alternativas de análisis, use el método [**IInkAnalyzer:: GetAlternates**](iinkanalyzer-getalternates.md), el método [**IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)o [**IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="6b71a-114">To get analysis alternates, use [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes Method**](iinkanalyzer-getalternatesforcontextnodes.md), or [**IInkAnalyzer::GetAlternatesForStrokes Method**](iinkanalyzer-getalternatesforstrokes.md).</span></span> <span data-ttu-id="6b71a-115">Para obtener los objetos de nodo de contexto asociados a una alternativa de análisis, use el [**método IAnalysisAlternate:: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).</span><span class="sxs-lookup"><span data-stu-id="6b71a-115">To get the context node objects associated with an analysis alternate, use [**IAnalysisAlternate::GetAlternateNodes Method**](ianalysisalternate-getalternatenodes.md).</span></span>

<span data-ttu-id="6b71a-116">Para cambiar el tipo de confirmación de un nodo de contexto, use [**IContextNode:: CONFIRM**](icontextnode-confirm.md).</span><span class="sxs-lookup"><span data-stu-id="6b71a-116">To change the confirmation type for a context node, use [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b71a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b71a-117">Requirements</span></span>



| <span data-ttu-id="6b71a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b71a-118">Requirement</span></span> | <span data-ttu-id="6b71a-119">Value</span><span class="sxs-lookup"><span data-stu-id="6b71a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b71a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b71a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6b71a-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6b71a-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6b71a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b71a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6b71a-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6b71a-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6b71a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b71a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b71a-125"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6b71a-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6b71a-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6b71a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b71a-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b71a-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6b71a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b71a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b71a-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="6b71a-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="6b71a-130">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="6b71a-130">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="6b71a-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="6b71a-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="6b71a-132">**ConfirmationType de análisis de tinta**</span><span class="sxs-lookup"><span data-stu-id="6b71a-132">**Ink Analysis ConfirmationType**</span></span>](confirmationtype.md)
</dt> <dt>

[<span data-ttu-id="6b71a-133">Referencia</span><span class="sxs-lookup"><span data-stu-id="6b71a-133">Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




