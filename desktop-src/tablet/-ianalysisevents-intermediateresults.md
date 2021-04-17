---
description: Se produce cuando finaliza la fase de análisis intermedio actual.
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: 'Evento _IAnalysisEvents:: IntermediateResults (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.IntermediateResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33430225746ddd1a4099f89112f14f99f2b6da84
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105697994"
---
# <a name="_ianalysiseventsintermediateresults-event"></a><span data-ttu-id="57a84-103">\_Evento IAnalysisEvents:: IntermediateResults</span><span class="sxs-lookup"><span data-stu-id="57a84-103">\_IAnalysisEvents::IntermediateResults event</span></span>

<span data-ttu-id="57a84-104">Se produce cuando finaliza la fase de análisis intermedio actual.</span><span class="sxs-lookup"><span data-stu-id="57a84-104">Occurs when the current intermediate analysis stage is finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="57a84-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57a84-105">Syntax</span></span>


```C++
HRESULT IntermediateResults(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a><span data-ttu-id="57a84-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57a84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57a84-107">*pInkAnalyzer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="57a84-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57a84-108">[**IInkAnalyzer**](iinkanalyzer.md) que realiza el análisis.</span><span class="sxs-lookup"><span data-stu-id="57a84-108">The [**IInkAnalyzer**](iinkanalyzer.md) that is performing the analysis.</span></span>

</dd> <dt>

<span data-ttu-id="57a84-109">*pAnalysisStatus* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="57a84-109">*pAnalysisStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57a84-110">Objeto [**IAnalysisStatus**](ianalysisstatus.md) que representa el estado de los resultados intermedios.</span><span class="sxs-lookup"><span data-stu-id="57a84-110">The [**IAnalysisStatus**](ianalysisstatus.md) object representing the status of the intermediate results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57a84-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57a84-111">Return value</span></span>

<span data-ttu-id="57a84-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="57a84-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="57a84-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57a84-113">Remarks</span></span>

<span data-ttu-id="57a84-114">[**IInkAnalyzer**](iinkanalyzer.md) genera este evento después de haber reconciliado los resultados intermedios de la fase de análisis actual.</span><span class="sxs-lookup"><span data-stu-id="57a84-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it has reconciled the intermediate results for the current analysis stage.</span></span>

<span data-ttu-id="57a84-115">Si la aplicación mantiene su propia estructura de datos, que está sincronizada con la del [**IInkAnalyzer**](iinkanalyzer.md), este evento indica que el **IInkAnalyzer** ha terminado de realizar cambios en sus datos internos para esta fase de análisis.</span><span class="sxs-lookup"><span data-stu-id="57a84-115">If your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), this event indicates that the **IInkAnalyzer** has finished making changes to its internal data for this analysis stage.</span></span>

<span data-ttu-id="57a84-116">Bloquee la estructura de datos cuando el [**IInkAnalyzer**](iinkanalyzer.md) provoque el evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .</span><span class="sxs-lookup"><span data-stu-id="57a84-116">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span> <span data-ttu-id="57a84-117">Los cambios en la estructura de datos durante esta fase de análisis pueden provocar errores en el análisis y la sincronización de las entradas manuscritas.</span><span class="sxs-lookup"><span data-stu-id="57a84-117">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="57a84-118">Puede desbloquear la estructura de datos cuando el **IInkAnalyzer** genera el evento **\_ IAnalysisEvents:: IntermediateResults** o [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="57a84-118">You can unlock your data structure when the **IInkAnalyzer** raises the **\_IAnalysisEvents::IntermediateResults** or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="57a84-119">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="57a84-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="57a84-120">[**IInkAnalyzer**](iinkanalyzer.md) genera resultados intermedios solo cuando sus modos de análisis tienen establecida la marca **\_ IntermediateResults de AnalysisModes** (vea el [**método IInkAnalyzer:: GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="57a84-120">The [**IInkAnalyzer**](iinkanalyzer.md) generates intermediate results only when its analysis modes has the **AnalysisModes\_IntermediateResults** flag set (see [**IInkAnalyzer::GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="57a84-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57a84-121">Requirements</span></span>



| <span data-ttu-id="57a84-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="57a84-122">Requirement</span></span> | <span data-ttu-id="57a84-123">Value</span><span class="sxs-lookup"><span data-stu-id="57a84-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57a84-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57a84-124">Minimum supported client</span></span><br/> | <span data-ttu-id="57a84-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="57a84-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="57a84-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57a84-126">Minimum supported server</span></span><br/> | <span data-ttu-id="57a84-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="57a84-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="57a84-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57a84-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="57a84-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="57a84-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="57a84-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="57a84-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57a84-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57a84-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="57a84-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="57a84-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a84-133">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="57a84-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="57a84-134">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="57a84-134">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="57a84-135">**\_IAnalysisEvents:: results**</span><span class="sxs-lookup"><span data-stu-id="57a84-135">**\_IAnalysisEvents::Results**</span></span>](-ianalysisevents-results.md)
</dt> <dt>

[<span data-ttu-id="57a84-136">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="57a84-136">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="57a84-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="57a84-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="57a84-138">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="57a84-138">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="57a84-139">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="57a84-139">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="57a84-140">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="57a84-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>
