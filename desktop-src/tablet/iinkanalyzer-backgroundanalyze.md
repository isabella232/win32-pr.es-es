---
description: Realiza el análisis de tinta asincrónica.
ms.assetid: 36427b80-5e3b-4c9a-bb49-e6b7f9301cbd
title: 'IInkAnalyzer:: BackgroundAnalyze (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.BackgroundAnalyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 606e1444f66884564a6b9f2007adfc26b2eb2ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542030"
---
# <a name="iinkanalyzerbackgroundanalyze-method"></a><span data-ttu-id="776ce-103">IInkAnalyzer:: BackgroundAnalyze (método)</span><span class="sxs-lookup"><span data-stu-id="776ce-103">IInkAnalyzer::BackgroundAnalyze method</span></span>

<span data-ttu-id="776ce-104">Realiza el análisis de tinta asincrónica.</span><span class="sxs-lookup"><span data-stu-id="776ce-104">Performs asynchronous ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="776ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="776ce-105">Syntax</span></span>


```C++
HRESULT BackgroundAnalyze();
```



## <a name="parameters"></a><span data-ttu-id="776ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="776ce-106">Parameters</span></span>

<span data-ttu-id="776ce-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="776ce-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="776ce-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="776ce-108">Return value</span></span>

<span data-ttu-id="776ce-109">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="776ce-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="776ce-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="776ce-110">Remarks</span></span>

<span data-ttu-id="776ce-111">Cuando se llama a este método, el [**IInkAnalyzer**](iinkanalyzer.md) realiza el análisis de tinta en un subproceso en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="776ce-111">When this method is called, the [**IInkAnalyzer**](iinkanalyzer.md) performs the ink analysis on a background thread.</span></span>

<span data-ttu-id="776ce-112">Este método devuelve **S \_ false** y no inicia una nueva operación de análisis en segundo plano en las siguientes circunstancias.</span><span class="sxs-lookup"><span data-stu-id="776ce-112">This method returns **S\_FALSE** and does not start a new background analysis operation under the following circumstances.</span></span>

-   <span data-ttu-id="776ce-113">El [**IInkAnalyzer**](iinkanalyzer.md) está realizando el análisis en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="776ce-113">The [**IInkAnalyzer**](iinkanalyzer.md) is currently performing background analysis.</span></span>
-   <span data-ttu-id="776ce-114">la región desfasada (vea [**IInkAnalyzer:: GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) representa un área vacía.</span><span class="sxs-lookup"><span data-stu-id="776ce-114">the dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) represents an empty area.</span></span>

<span data-ttu-id="776ce-115">El [**IInkAnalyzer**](iinkanalyzer.md) analiza la tinta dentro de su región desfasada durante una llamada al método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o **IInkAnalyzer:: BackgroundAnalyze**.</span><span class="sxs-lookup"><span data-stu-id="776ce-115">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or **IInkAnalyzer::BackgroundAnalyze Method**.</span></span> <span data-ttu-id="776ce-116">Sin embargo, el **IInkAnalyzer** puede expandir la operación de análisis para incluir las regiones vecinas.</span><span class="sxs-lookup"><span data-stu-id="776ce-116">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="776ce-117">Este método establece la región desfasada en una región vacía.</span><span class="sxs-lookup"><span data-stu-id="776ce-117">This method sets the dirty region to an empty region.</span></span>

<span data-ttu-id="776ce-118">Si los datos de trazo se agregaron al [**IInkAnalyzer**](iinkanalyzer.md) después de la llamada al **método IInkAnalyzer:: BackgroundAnalyze**, el **IInkAnalyzer** puede actualizar la región desfasada durante la fase de conciliación del análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="776ce-118">If stroke data was added to the [**IInkAnalyzer**](iinkanalyzer.md) after the call to **IInkAnalyzer::BackgroundAnalyze Method**, the **IInkAnalyzer** may update the dirty region during the reconcile phase of ink analysis.</span></span>

<span data-ttu-id="776ce-119">La configuración de modos de análisis (vea [**IInkAnalyzer:: GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)) especifica cómo realiza el [**IInkAnalyzer**](iinkanalyzer.md) el análisis en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="776ce-119">The analysis modes setting (see [**IInkAnalyzer::GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)) specifies how the [**IInkAnalyzer**](iinkanalyzer.md) performs background analysis.</span></span> <span data-ttu-id="776ce-120">Para obtener más información sobre el análisis de tinta, consulte [información general del análisis de tinta](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="776ce-120">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

<span data-ttu-id="776ce-121">Este método devuelve un código de error en las siguientes circunstancias.</span><span class="sxs-lookup"><span data-stu-id="776ce-121">This method returns an error code under the following circumstances.</span></span>

-   <span data-ttu-id="776ce-122">La aplicación tiene establecido el valor [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ IntermediateResults** en [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IInkAnalyzer:: SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) y no controla el evento [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) .</span><span class="sxs-lookup"><span data-stu-id="776ce-122">Your application has set [**AnalysisModes**](analysismodes.md) value **AnalysisModes\_IntermediateResults** in the [**IInkAnalyzer**](iinkanalyzer.md) (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) and does not handle the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) event.</span></span>
-   <span data-ttu-id="776ce-123">La aplicación ha borrado el valor de [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ AutomaticReconciliation** en [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IInkAnalyzer:: SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) y no controla el evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="776ce-123">Your application has cleared [**AnalysisModes**](analysismodes.md) value **AnalysisModes\_AutomaticReconciliation** in the [**IInkAnalyzer**](iinkanalyzer.md) (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) and does not handle the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span>
-   <span data-ttu-id="776ce-124">La aplicación no controla el evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="776ce-124">Your application does not handle the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>
-   <span data-ttu-id="776ce-125">La aplicación no controla el evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .</span><span class="sxs-lookup"><span data-stu-id="776ce-125">Your application does not handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span>

## <a name="examples"></a><span data-ttu-id="776ce-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="776ce-126">Examples</span></span>

<span data-ttu-id="776ce-127">En el ejemplo siguiente se comprueba la región desfasada del analizador de tinta y, a continuación, se inicia el análisis de tinta de fondo si la región desfasada no está vacía.</span><span class="sxs-lookup"><span data-stu-id="776ce-127">The following example checks the ink analyzer's dirty region, and then initiates background ink analysis if the dirty region is not empty.</span></span>


```C++
// Check that the ink analyzer's dirty region is not empty.
IAnalysisRegion *pDirtyRegion;
hr = this->m_spIInkAnalyzer->GetDirtyRegion(&pDirtyRegion);

if (SUCCEEDED(hr))
{
    VARIANT_BOOL bIsEmpty;
    hr = pDirtyRegion->IsEmpty(&bIsEmpty);

    if (SUCCEEDED(hr))
    {
        if (!bIsEmpty)
        {
            // Insert code that prepares the application for background
            // ink analysis here.

            // Start background ink analysis. The _IAnalysisEvents::Results
            // event signals when background ink analysis is complete.
            hr = this->m_spIInkAnalyzer->BackgroundAnalyze();
        }
    }
}

// Free the memory for the dirty region.
if (pDirtyRegion != NULL)
{
    pDirtyRegion->Release();
}
```



## <a name="requirements"></a><span data-ttu-id="776ce-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="776ce-128">Requirements</span></span>



| <span data-ttu-id="776ce-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="776ce-129">Requirement</span></span> | <span data-ttu-id="776ce-130">Value</span><span class="sxs-lookup"><span data-stu-id="776ce-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="776ce-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="776ce-131">Minimum supported client</span></span><br/> | <span data-ttu-id="776ce-132">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="776ce-132">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="776ce-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="776ce-133">Minimum supported server</span></span><br/> | <span data-ttu-id="776ce-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="776ce-134">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="776ce-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="776ce-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="776ce-136"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="776ce-136"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="776ce-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="776ce-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="776ce-138"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="776ce-138"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="776ce-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="776ce-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="776ce-140">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="776ce-140">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="776ce-141">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="776ce-141">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="776ce-142">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="776ce-142">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="776ce-143">**IInkAnalyzer:: GetAnalysisModes (método)**</span><span class="sxs-lookup"><span data-stu-id="776ce-143">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="776ce-144">**IInkAnalyzer:: SetAnalysisModes (método)**</span><span class="sxs-lookup"><span data-stu-id="776ce-144">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="776ce-145">**IInkAnalyzer:: GetDirtyRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="776ce-145">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="776ce-146">**IInkAnalyzer:: SetDirtyRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="776ce-146">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="776ce-147">**IInkAnalyzer:: GetRootNode (método)**</span><span class="sxs-lookup"><span data-stu-id="776ce-147">**IInkAnalyzer::GetRootNode Method**</span></span>](iinkanalyzer-getrootnode.md)
</dt> <dt>

[<span data-ttu-id="776ce-148">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="776ce-148">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




