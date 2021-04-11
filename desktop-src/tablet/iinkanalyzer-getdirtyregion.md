---
description: Recupera el área que ha cambiado desde la última operación de análisis.
ms.assetid: 0cd62775-59c6-41f5-957e-709a53a8c257
title: 'IInkAnalyzer:: GetDirtyRegion (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 56f980189e22f50bb832be904933ef0b26d9b54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275467"
---
# <a name="iinkanalyzergetdirtyregion-method"></a><span data-ttu-id="cb1f7-103">IInkAnalyzer:: GetDirtyRegion (método)</span><span class="sxs-lookup"><span data-stu-id="cb1f7-103">IInkAnalyzer::GetDirtyRegion method</span></span>

<span data-ttu-id="cb1f7-104">Recupera el área que ha cambiado desde la última operación de análisis.</span><span class="sxs-lookup"><span data-stu-id="cb1f7-104">Retrieves the area that has changed since the last analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb1f7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb1f7-105">Syntax</span></span>


```C++
HRESULT GetDirtyRegion(
  [out] IAnalysisRegion **ppDirtyRegion
);
```



## <a name="parameters"></a><span data-ttu-id="cb1f7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb1f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb1f7-107">*ppDirtyRegion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cb1f7-107">*ppDirtyRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb1f7-108">[**IAnalysisRegion**](ianalysisregion.md) que describe el área que ha cambiado desde la última operación de análisis.</span><span class="sxs-lookup"><span data-stu-id="cb1f7-108">An [**IAnalysisRegion**](ianalysisregion.md) that describes the area that has changed since the last analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb1f7-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb1f7-109">Return value</span></span>

<span data-ttu-id="cb1f7-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cb1f7-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cb1f7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb1f7-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="cb1f7-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppDirtyRegion* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="cb1f7-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppDirtyRegion* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="cb1f7-113">Este método identifica las áreas que se deben analizar o volver a analizar.</span><span class="sxs-lookup"><span data-stu-id="cb1f7-113">This method identifies the areas that need to be analyzed or reanalyzed.</span></span> <span data-ttu-id="cb1f7-114">Todos los métodos de [**IInkAnalyzer**](iinkanalyzer.md) que agregan, actualizan o quitan datos de trazo actualizan la región desfasada.</span><span class="sxs-lookup"><span data-stu-id="cb1f7-114">All of the [**IInkAnalyzer**](iinkanalyzer.md) methods that add, update, or remove stroke data update the dirty region.</span></span> <span data-ttu-id="cb1f7-115">Para marcar manualmente un área para el análisis:</span><span class="sxs-lookup"><span data-stu-id="cb1f7-115">To manually mark an area for reanalysis:</span></span>

1.  <span data-ttu-id="cb1f7-116">Obtiene la región desfasada mediante el **método IInkAnalyzer:: GetDirtyRegion**.</span><span class="sxs-lookup"><span data-stu-id="cb1f7-116">Get the dirty region using **IInkAnalyzer::GetDirtyRegion Method**.</span></span>
2.  <span data-ttu-id="cb1f7-117">Use el método [**IAnalysisRegion:: UnionRegion**](ianalysisregion-unionregion.md) o [**IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md) para agregar el área a la región del paso 1.</span><span class="sxs-lookup"><span data-stu-id="cb1f7-117">Use [**IAnalysisRegion::UnionRegion Method**](ianalysisregion-unionregion.md) or [**IAnalysisRegion::UnionRectangle Method**](ianalysisregion-unionrectangle.md) to add the area to the region from step 1.</span></span>
3.  <span data-ttu-id="cb1f7-118">Use el [**método IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) para actualizar la región desfasada.</span><span class="sxs-lookup"><span data-stu-id="cb1f7-118">Use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to update the dirty region.</span></span>

<span data-ttu-id="cb1f7-119">El [**IInkAnalyzer**](iinkanalyzer.md) analiza la tinta dentro de su región desfasada durante una llamada al método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="cb1f7-119">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span> <span data-ttu-id="cb1f7-120">Sin embargo, el **IInkAnalyzer** puede expandir la operación de análisis para incluir las regiones vecinas.</span><span class="sxs-lookup"><span data-stu-id="cb1f7-120">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="cb1f7-121">Esta propiedad puede contener áreas no adyacentes.</span><span class="sxs-lookup"><span data-stu-id="cb1f7-121">This property may contain nonadjacent areas.</span></span>

<span data-ttu-id="cb1f7-122">Use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar memoria de la matriz de *ppDirtyRegion* cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="cb1f7-122">Use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory from the *ppDirtyRegion* array when you are finished with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb1f7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb1f7-123">Requirements</span></span>



| <span data-ttu-id="cb1f7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb1f7-124">Requirement</span></span> | <span data-ttu-id="cb1f7-125">Value</span><span class="sxs-lookup"><span data-stu-id="cb1f7-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb1f7-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb1f7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cb1f7-127">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cb1f7-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cb1f7-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb1f7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cb1f7-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cb1f7-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cb1f7-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb1f7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb1f7-131"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cb1f7-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cb1f7-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb1f7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb1f7-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb1f7-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cb1f7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb1f7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb1f7-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="cb1f7-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="cb1f7-136">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="cb1f7-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="cb1f7-137">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="cb1f7-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="cb1f7-138">**IInkAnalyzer:: AddStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="cb1f7-138">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="cb1f7-139">**IInkAnalyzer:: AddStrokeForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="cb1f7-139">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="cb1f7-140">**IInkAnalyzer:: AddStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="cb1f7-140">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="cb1f7-141">**IInkAnalyzer:: AddStrokesForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="cb1f7-141">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="cb1f7-142">**IInkAnalyzer:: RemoveStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="cb1f7-142">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="cb1f7-143">**IInkAnalyzer:: RemoveStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="cb1f7-143">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="cb1f7-144">**IInkAnalyzer:: UpdateStrokesData (método)**</span><span class="sxs-lookup"><span data-stu-id="cb1f7-144">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="cb1f7-145">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="cb1f7-145">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

