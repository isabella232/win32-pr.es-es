---
description: Cancela la operación de análisis actual.
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: 'IInkAnalyzer:: ABORT (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Abort
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eac96809bfbe41e7d6a070782da3ffd0f6407c60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715219"
---
# <a name="iinkanalyzerabort-method"></a><span data-ttu-id="d7756-103">IInkAnalyzer:: ABORT (método)</span><span class="sxs-lookup"><span data-stu-id="d7756-103">IInkAnalyzer::Abort method</span></span>

<span data-ttu-id="d7756-104">Cancela la operación de análisis actual.</span><span class="sxs-lookup"><span data-stu-id="d7756-104">Cancels the current analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7756-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7756-105">Syntax</span></span>


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a><span data-ttu-id="d7756-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7756-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7756-107">*ppAbortedRegion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d7756-107">*ppAbortedRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7756-108">Un puntero a un [**IAnalysisRegion**](ianalysisregion.md) que representa la región desfasada (vea [**IInkAnalyzer:: GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) de la operación de análisis actual.</span><span class="sxs-lookup"><span data-stu-id="d7756-108">A pointer to an [**IAnalysisRegion**](ianalysisregion.md) that represents the dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) of the current analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7756-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7756-109">Return value</span></span>

<span data-ttu-id="d7756-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d7756-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d7756-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7756-111">Remarks</span></span>

<span data-ttu-id="d7756-112">Llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppAbortedRegion* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="d7756-112">Call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAbortedRegion* when you no longer need to use the object.</span></span>

<span data-ttu-id="d7756-113">Este método cancela la operación de análisis actual.</span><span class="sxs-lookup"><span data-stu-id="d7756-113">This method cancels the current analysis operation.</span></span>

<span data-ttu-id="d7756-114">Cuando *ppAbortedRegion* es **null**, este método realiza la anulación como normal, porque esto indica que el autor de la llamada no tiene ningún interés en el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="d7756-114">When *ppAbortedRegion* is **NULL**, this method performs the abort as normal, because this indicates that the caller has no interest in the return value.</span></span>

<span data-ttu-id="d7756-115">**IInkAnalyzer:: ABORT (método** ) silencia los eventos [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) y [**\_ IAnalysisEvents:: Activity**](-ianalysisevents-activity.md) para la operación de análisis actual.</span><span class="sxs-lookup"><span data-stu-id="d7756-115">**IInkAnalyzer::Abort Method** silences the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) and [**\_IAnalysisEvents::Activity**](-ianalysisevents-activity.md) events for the current analysis operation.</span></span>

<span data-ttu-id="d7756-116">**IInkAnalyzer:: ABORT el método** se ejecuta de forma asincrónica hasta que se cancela la operación de análisis en segundo plano actual.</span><span class="sxs-lookup"><span data-stu-id="d7756-116">**IInkAnalyzer::Abort Method** runs asynchronously until the current background analysis operation is canceled.</span></span> <span data-ttu-id="d7756-117">Dado que el proceso de cancelación es asincrónico, la aplicación puede realizar otras tareas mientras se cancela el opertions de análisis actual.</span><span class="sxs-lookup"><span data-stu-id="d7756-117">Because the cancellation process is asynchronous, the application can perform other tasks while the current analysis opertions is canceled.</span></span>

<span data-ttu-id="d7756-118">Si no hay operaciones de análisis en curso, este método devuelve una región de análisis vacía.</span><span class="sxs-lookup"><span data-stu-id="d7756-118">If no analysis operations are in progress, this method returns an empty analysis region.</span></span>

<span data-ttu-id="d7756-119">Si una operación de análisis está en curso, este método cancela la operación.</span><span class="sxs-lookup"><span data-stu-id="d7756-119">If one analysis operation is in progress, this method cancels the operation.</span></span>

<span data-ttu-id="d7756-120">Si hay operaciones de análisis sincrónicas y asincrónicas en curso, este método cancela la operación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="d7756-120">If both synchronous and asynchronous analysis operations are in progress, this method cancels the synchronous operation.</span></span>

<span data-ttu-id="d7756-121">Si se llama a este método más de una vez para la misma operación de análisis, la primera llamada devuelve la región desfasada de la operación y las llamadas subsiguientes devuelven una región vacía.</span><span class="sxs-lookup"><span data-stu-id="d7756-121">If this method is called more than once for the same analysis operation, the first call returns the dirty region for the operation, and the subsequent calls return an empty region.</span></span>

<span data-ttu-id="d7756-122">Si la aplicación mantiene su propia estructura de datos que está sincronizada con la del [**IInkAnalyzer**](iinkanalyzer.md), la llamada al **método IInkAnalyzer:: ABORT** puede dejar el documento con resultados parciales.</span><span class="sxs-lookup"><span data-stu-id="d7756-122">If your application maintains its own data structure that is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), calling **IInkAnalyzer::Abort Method** can leave your document with partial results.</span></span> <span data-ttu-id="d7756-123">Para evitar esto, no llame al **método IInkAnalyzer:: ABORT** entre el momento en que **IInkAnalyzer** recibe el evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) y la hora en que el **IInkAnalyzer** recibe el evento [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) o [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="d7756-123">To avoid this, do not call **IInkAnalyzer::Abort Method** between the time the **IInkAnalyzer** receives the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event and the time the **IInkAnalyzer** receives the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="d7756-124">Para obtener más información acerca de cómo sincronizar los datos de aplicación con el analizador de tinta, consulte [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d7756-124">For more information about synchronizing your application data with the ink analyzer, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7756-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7756-125">Requirements</span></span>



| <span data-ttu-id="d7756-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7756-126">Requirement</span></span> | <span data-ttu-id="d7756-127">Value</span><span class="sxs-lookup"><span data-stu-id="d7756-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7756-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7756-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d7756-129">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d7756-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d7756-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7756-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d7756-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d7756-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d7756-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7756-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7756-133"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d7756-133"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d7756-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d7756-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7756-135"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7756-135"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d7756-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7756-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7756-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="d7756-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d7756-138">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="d7756-138">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="d7756-139">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="d7756-139">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="d7756-140">**IInkAnalyzer:: GetDirtyRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="d7756-140">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="d7756-141">**IInkAnalyzer:: SetDirtyRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="d7756-141">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="d7756-142">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="d7756-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

