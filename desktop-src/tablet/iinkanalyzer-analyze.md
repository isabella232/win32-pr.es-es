---
description: Realiza análisis sincrónicos de tinta.
ms.assetid: 957845f3-96b4-4184-aaec-e266cbe47e46
title: 'Método IInkAnalyzer:: Analyze (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Analyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2867064067b902105508a7742c6fec88fdcd58be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715212"
---
# <a name="iinkanalyzeranalyze-method"></a><span data-ttu-id="605e2-103">IInkAnalyzer:: Analyze (método)</span><span class="sxs-lookup"><span data-stu-id="605e2-103">IInkAnalyzer::Analyze method</span></span>

<span data-ttu-id="605e2-104">Realiza análisis sincrónicos de tinta.</span><span class="sxs-lookup"><span data-stu-id="605e2-104">Performs synchronous ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="605e2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="605e2-105">Syntax</span></span>


```C++
HRESULT Analyze(
  [out] IAnalysisStatus **ppStatus
);
```



## <a name="parameters"></a><span data-ttu-id="605e2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="605e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="605e2-107">*ppStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="605e2-107">*ppStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="605e2-108">Un puntero a un [**IAnalysisStatus**](ianalysisstatus.md) que describe el estado de la operación de análisis.</span><span class="sxs-lookup"><span data-stu-id="605e2-108">A pointer to an [**IAnalysisStatus**](ianalysisstatus.md) that describes the status of the analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="605e2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="605e2-109">Return value</span></span>

<span data-ttu-id="605e2-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="605e2-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="605e2-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="605e2-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="605e2-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppStatus* cuando ya no necesite usar el estado del análisis.</span><span class="sxs-lookup"><span data-stu-id="605e2-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppStatus* when you no longer need to use the analysis status.</span></span>

 

<span data-ttu-id="605e2-113">Este método inicia una operación sincrónica de análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="605e2-113">This method starts a synchronous ink analysis operation.</span></span> <span data-ttu-id="605e2-114">El análisis de tinta incluye el análisis de diseño, la clasificación de escritura y dibujo y el reconocimiento de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="605e2-114">Ink analysis includes layout analysis, writing and drawing classification, and handwriting recognition.</span></span> <span data-ttu-id="605e2-115">Este método devuelve una vez completada la operación de análisis.</span><span class="sxs-lookup"><span data-stu-id="605e2-115">This method returns after the analysis operation is complete.</span></span>

<span data-ttu-id="605e2-116">Este método devuelve **el \_ puntero E** si *ppStatus* es **null**.</span><span class="sxs-lookup"><span data-stu-id="605e2-116">This method returns **E\_POINTER** if *ppStatus* is **NULL**.</span></span>

<span data-ttu-id="605e2-117">Durante una llamada a un método **IInkAnalyzer:: Analyze** o [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), el [**IInkAnalyzer**](iinkanalyzer.md) analiza la tinta dentro de su región desfasada (vea [**IInkAnalyzer:: GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="605e2-117">During a call to **IInkAnalyzer::Analyze Method** or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md), the [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span> <span data-ttu-id="605e2-118">Sin embargo, el **IInkAnalyzer** puede expandir la operación de análisis para incluir las regiones vecinas.</span><span class="sxs-lookup"><span data-stu-id="605e2-118">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="605e2-119">Este método establece la región desfasada del objeto [**IInkAnalyzer**](iinkanalyzer.md) en una región vacía.</span><span class="sxs-lookup"><span data-stu-id="605e2-119">This method sets the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region to an empty region.</span></span> <span data-ttu-id="605e2-120">Si otro subproceso ha agregado datos de trazo que no se han analizado, el **IInkAnalyzer** agrega el rectángulo de selección de los trazos sin analizar a su región desfasada durante la fase de conciliación del análisis.</span><span class="sxs-lookup"><span data-stu-id="605e2-120">If another thread has added stroke data that has not been analyzed, the **IInkAnalyzer** adds the bounding box of the unanalyzed strokes to its dirty region during the reconcile phase of the analysis.</span></span>

<span data-ttu-id="605e2-121">Este método devuelve un error si la aplicación no controla el evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .</span><span class="sxs-lookup"><span data-stu-id="605e2-121">This method returns an error if your application does not handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span>

<span data-ttu-id="605e2-122">[**IInkAnalyzer**](iinkanalyzer.md) no genera los eventos [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) y [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) en respuesta a este método.</span><span class="sxs-lookup"><span data-stu-id="605e2-122">The [**IInkAnalyzer**](iinkanalyzer.md) does not raise the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) and [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) events in response to this method.</span></span>

<span data-ttu-id="605e2-123">Para modificar la forma en que se realiza el análisis de tinta, use el [**método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md).</span><span class="sxs-lookup"><span data-stu-id="605e2-123">To modify the way ink analysis is performed, use [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md).</span></span>

<span data-ttu-id="605e2-124">Para obtener más información sobre el análisis de tinta, consulte [información general del análisis de tinta](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="605e2-124">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="605e2-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="605e2-125">Examples</span></span>

<span data-ttu-id="605e2-126">En el ejemplo siguiente se realiza el análisis de tinta de primer plano.</span><span class="sxs-lookup"><span data-stu-id="605e2-126">The following example performs foreground ink analysis.</span></span>


```C++
// Perform synchronous ink analysis.
IAnalysisStatus *pAnalysisStatus = NULL;
hr = this->m_spIInkAnalyzer->Analyze(&pAnalysisStatus);

if (SUCCEEDED(hr))
{
    // Insert code that processes the analysis results.
}

// Release this reference to the analysis status.
if (pAnalysisStatus != NULL)
{
    pAnalysisStatus->Release();
    pAnalysisStatus = NULL;
}
```



## <a name="requirements"></a><span data-ttu-id="605e2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="605e2-127">Requirements</span></span>



| <span data-ttu-id="605e2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="605e2-128">Requirement</span></span> | <span data-ttu-id="605e2-129">Value</span><span class="sxs-lookup"><span data-stu-id="605e2-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="605e2-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="605e2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="605e2-131">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="605e2-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="605e2-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="605e2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="605e2-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="605e2-133">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="605e2-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="605e2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="605e2-135"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="605e2-135"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="605e2-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="605e2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="605e2-137"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="605e2-137"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="605e2-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="605e2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="605e2-139">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="605e2-139">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="605e2-140">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="605e2-140">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="605e2-141">**IInkAnalyzer:: GetDirtyRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="605e2-141">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="605e2-142">**IInkAnalyzer:: SetDirtyRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="605e2-142">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="605e2-143">**IInkAnalyzer:: GetRootNode (método)**</span><span class="sxs-lookup"><span data-stu-id="605e2-143">**IInkAnalyzer::GetRootNode Method**</span></span>](iinkanalyzer-getrootnode.md)
</dt> <dt>

[<span data-ttu-id="605e2-144">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="605e2-144">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> </dl>

 

