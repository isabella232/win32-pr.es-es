---
description: Modifica el área que ha cambiado desde la última operación de análisis.
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: 'IInkAnalyzer:: SetDirtyRegion (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 72278dd9fe1d772d4ef340d25694d42f9c48ed7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154407"
---
# <a name="iinkanalyzersetdirtyregion-method"></a><span data-ttu-id="db9b6-103">IInkAnalyzer:: SetDirtyRegion (método)</span><span class="sxs-lookup"><span data-stu-id="db9b6-103">IInkAnalyzer::SetDirtyRegion method</span></span>

<span data-ttu-id="db9b6-104">Modifica el área que ha cambiado desde la última operación de análisis.</span><span class="sxs-lookup"><span data-stu-id="db9b6-104">Modifies the area that has changed since the last analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="db9b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db9b6-105">Syntax</span></span>


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a><span data-ttu-id="db9b6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db9b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db9b6-107">*pDirtyRegion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="db9b6-107">*pDirtyRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db9b6-108">[**IAnalysisRegion**](ianalysisregion.md) que describe el área que ha cambiado desde la última operación de análisis.</span><span class="sxs-lookup"><span data-stu-id="db9b6-108">An [**IAnalysisRegion**](ianalysisregion.md) that describes the area that has changed since the last analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db9b6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db9b6-109">Return value</span></span>

<span data-ttu-id="db9b6-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="db9b6-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="db9b6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db9b6-111">Remarks</span></span>

<span data-ttu-id="db9b6-112">Este método identifica las áreas que se deben analizar o volver a analizar.</span><span class="sxs-lookup"><span data-stu-id="db9b6-112">This method identifies the areas that need to be analyzed or reanalyzed.</span></span> <span data-ttu-id="db9b6-113">Todos los métodos de [**IInkAnalyzer**](iinkanalyzer.md) que agregan, actualizan o quitan datos de trazo actualizan la región desfasada.</span><span class="sxs-lookup"><span data-stu-id="db9b6-113">All of the [**IInkAnalyzer**](iinkanalyzer.md) methods that add, update, or remove stroke data update the dirty region.</span></span> <span data-ttu-id="db9b6-114">Para marcar manualmente un área para el análisis:</span><span class="sxs-lookup"><span data-stu-id="db9b6-114">To manually mark an area for reanalysis:</span></span>

1.  <span data-ttu-id="db9b6-115">Obtiene la región desfasada mediante el [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md).</span><span class="sxs-lookup"><span data-stu-id="db9b6-115">Get the dirty region using [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md).</span></span>
2.  <span data-ttu-id="db9b6-116">Use el método [**IAnalysisRegion:: UnionRegion**](ianalysisregion-unionregion.md) o [**IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md) para agregar el área a la región del paso 1.</span><span class="sxs-lookup"><span data-stu-id="db9b6-116">Use [**IAnalysisRegion::UnionRegion Method**](ianalysisregion-unionregion.md) or [**IAnalysisRegion::UnionRectangle Method**](ianalysisregion-unionrectangle.md) to add the area to the region from step 1.</span></span>
3.  <span data-ttu-id="db9b6-117">Use el **método IInkAnalyzer:: SetDirtyRegion** para actualizar la región desfasada.</span><span class="sxs-lookup"><span data-stu-id="db9b6-117">Use **IInkAnalyzer::SetDirtyRegion Method** to update the dirty region.</span></span>

<span data-ttu-id="db9b6-118">El [**IInkAnalyzer**](iinkanalyzer.md) analiza la tinta dentro de su región desfasada durante una llamada al método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="db9b6-118">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span> <span data-ttu-id="db9b6-119">Sin embargo, el **IInkAnalyzer** puede expandir la operación de análisis para incluir las regiones vecinas.</span><span class="sxs-lookup"><span data-stu-id="db9b6-119">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

## <a name="requirements"></a><span data-ttu-id="db9b6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db9b6-120">Requirements</span></span>



| <span data-ttu-id="db9b6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="db9b6-121">Requirement</span></span> | <span data-ttu-id="db9b6-122">Value</span><span class="sxs-lookup"><span data-stu-id="db9b6-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db9b6-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db9b6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="db9b6-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="db9b6-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="db9b6-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db9b6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="db9b6-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="db9b6-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="db9b6-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db9b6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="db9b6-128"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="db9b6-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="db9b6-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="db9b6-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db9b6-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db9b6-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="db9b6-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="db9b6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db9b6-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="db9b6-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="db9b6-133">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="db9b6-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="db9b6-134">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="db9b6-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="db9b6-135">**IInkAnalyzer:: AddStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="db9b6-135">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="db9b6-136">**IInkAnalyzer:: AddStrokeForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="db9b6-136">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="db9b6-137">**IInkAnalyzer:: AddStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="db9b6-137">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="db9b6-138">**IInkAnalyzer:: AddStrokesForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="db9b6-138">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="db9b6-139">**IInkAnalyzer:: RemoveStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="db9b6-139">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="db9b6-140">**IInkAnalyzer:: RemoveStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="db9b6-140">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="db9b6-141">**IInkAnalyzer:: UpdateStrokesData (método)**</span><span class="sxs-lookup"><span data-stu-id="db9b6-141">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="db9b6-142">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="db9b6-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




