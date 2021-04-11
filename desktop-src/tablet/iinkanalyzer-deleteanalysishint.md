---
description: Quita una sugerencia de análisis de IInkAnalyzer.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: IInkAnalyzer::D método eleteAnalysisHint (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.DeleteAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f84f718701abd5bc76b55427aab9df072f758c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154421"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a><span data-ttu-id="3e534-103">IInkAnalyzer::D método eleteAnalysisHint</span><span class="sxs-lookup"><span data-stu-id="3e534-103">IInkAnalyzer::DeleteAnalysisHint method</span></span>

<span data-ttu-id="3e534-104">Quita una sugerencia de análisis de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="3e534-104">Removes an analysis hint from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e534-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e534-105">Syntax</span></span>


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="3e534-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e534-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e534-107">*pHintToDelete* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e534-107">*pHintToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e534-108">La sugerencia de análisis desde [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="3e534-108">The analysis hint from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e534-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e534-109">Return value</span></span>

<span data-ttu-id="3e534-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3e534-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3e534-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e534-111">Remarks</span></span>

<span data-ttu-id="3e534-112">Al quitar una sugerencia de análisis no se marca el área de la sugerencia para su análisis.</span><span class="sxs-lookup"><span data-stu-id="3e534-112">Removing an analysis hint does not mark the hint's area for reanalysis.</span></span> <span data-ttu-id="3e534-113">Para marcar el área dentro de la sugerencia para su reanálisis, use el [**método IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) para establecer la región desfasada en la Unión de la región desfasada actual y el área de la sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="3e534-113">To mark the area within the hint for reanalysis, use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to set the dirty region to the union of the current dirty region and area of the analysis hint.</span></span>

<span data-ttu-id="3e534-114">La sugerencia se quita del analizador; sin embargo, el propio [**IContextNode**](icontextnode.md) no se elimina.</span><span class="sxs-lookup"><span data-stu-id="3e534-114">The hint is removed from the analyzer; however, the [**IContextNode**](icontextnode.md) itself is not deleted.</span></span>

<span data-ttu-id="3e534-115">Este método devuelve un código de error cuando *pHintToDelete* es un [**IContextNode**](icontextnode.md) que no es de tipo AnalysisHint (vea [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="3e534-115">This method returns an error code when *pHintToDelete* is a [**IContextNode**](icontextnode.md) that is not of type AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e534-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e534-116">Requirements</span></span>



| <span data-ttu-id="3e534-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e534-117">Requirement</span></span> | <span data-ttu-id="3e534-118">Value</span><span class="sxs-lookup"><span data-stu-id="3e534-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e534-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e534-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3e534-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3e534-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3e534-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e534-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3e534-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3e534-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3e534-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e534-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e534-124"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3e534-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3e534-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e534-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e534-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e534-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3e534-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e534-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e534-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="3e534-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="3e534-129">**IInkAnalyzer:: CreateAnalysisHint (método)**</span><span class="sxs-lookup"><span data-stu-id="3e534-129">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="3e534-130">**IInkAnalyzer:: GetAnalysisHints (método)**</span><span class="sxs-lookup"><span data-stu-id="3e534-130">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="3e534-131">**IInkAnalyzer:: GetAnalysisHintsByName (método)**</span><span class="sxs-lookup"><span data-stu-id="3e534-131">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="3e534-132">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="3e534-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




