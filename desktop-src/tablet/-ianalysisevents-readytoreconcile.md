---
description: Se produce cuando IInkAnalyzer está listo para conciliar los resultados del análisis de fondo con su estado actual.
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: 'Evento _IAnalysisEvents:: ReadyToReconcile (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.ReadyToReconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f3144f34dc680f9bc31f51b9e6b4284a70fb9bc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279855"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a><span data-ttu-id="1e73e-103">\_Evento IAnalysisEvents:: ReadyToReconcile</span><span class="sxs-lookup"><span data-stu-id="1e73e-103">\_IAnalysisEvents::ReadyToReconcile event</span></span>

<span data-ttu-id="1e73e-104">Se produce cuando [**IInkAnalyzer**](iinkanalyzer.md) está listo para conciliar los resultados del análisis de fondo con su estado actual.</span><span class="sxs-lookup"><span data-stu-id="1e73e-104">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) is ready to reconcile its background analysis results with its current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e73e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e73e-105">Syntax</span></span>


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a><span data-ttu-id="1e73e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e73e-106">Parameters</span></span>

<span data-ttu-id="1e73e-107">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1e73e-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e73e-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e73e-108">Return value</span></span>

<span data-ttu-id="1e73e-109">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1e73e-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1e73e-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e73e-110">Remarks</span></span>

<span data-ttu-id="1e73e-111">[**IInkAnalyzer**](iinkanalyzer.md) realiza la conciliación automática cuando se establece la **marca \_ AutomaticReconciliation AnalysisModes** del analizador de tinta (vea el [**método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="1e73e-111">The [**IInkAnalyzer**](iinkanalyzer.md) performs automatic reconciliation when the ink analyzer's **AnalysisModes\_AutomaticReconciliation** flag is set (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)).</span></span> <span data-ttu-id="1e73e-112">Cuando no se establece la marca **AnalysisModes \_ AutomaticReconciliation** , la aplicación debe conciliar los resultados del análisis de fondo manualmente.</span><span class="sxs-lookup"><span data-stu-id="1e73e-112">When the **AnalysisModes\_AutomaticReconciliation** flag is not set, your application needs to reconcile background analysis results manually.</span></span>

<span data-ttu-id="1e73e-113">Para realizar la reconciliación manual, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="1e73e-113">To perform manual reconciliation, follow these steps.</span></span>

1.  <span data-ttu-id="1e73e-114">Borre la marca **AnalysisModes \_ AutomaticReconciliation** del analizador de tinta.</span><span class="sxs-lookup"><span data-stu-id="1e73e-114">Clear the ink analyzer's **AnalysisModes\_AutomaticReconciliation** flag.</span></span>
2.  <span data-ttu-id="1e73e-115">Controle el evento **\_ IAnalysisEvents:: ReadyToReconcile** .</span><span class="sxs-lookup"><span data-stu-id="1e73e-115">Handle the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span>
3.  <span data-ttu-id="1e73e-116">Para conciliar los resultados del análisis, llame al método [**IInkAnalyzer:: Reconciliate**](iinkanalyzer-reconcile.md) del controlador de eventos para el evento **\_ IAnalysisEvents:: ReadyToReconcile** .</span><span class="sxs-lookup"><span data-stu-id="1e73e-116">To reconcile the analysis results, call the [**IInkAnalyzer::Reconcile Method**](iinkanalyzer-reconcile.md) method from the event handler for the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span> <span data-ttu-id="1e73e-117">Para cancelar la operación de análisis en segundo plano actual, llame al método [**IInkAnalyzer:: ABORT**](iinkanalyzer-abort.md) del controlador de eventos para el evento **\_ IAnalysisEvents:: ReadyToReconcile** .</span><span class="sxs-lookup"><span data-stu-id="1e73e-117">To cancel the current background analysis operation, call the [**IInkAnalyzer::Abort Method**](iinkanalyzer-abort.md) method from the event handler for the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span>

<span data-ttu-id="1e73e-118">[**IInkAnalyzer**](iinkanalyzer.md) genera este evento antes de generar el evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .</span><span class="sxs-lookup"><span data-stu-id="1e73e-118">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event before it raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span>

<span data-ttu-id="1e73e-119">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1e73e-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="1e73e-120">[**IInkAnalyzer**](iinkanalyzer.md) genera este evento durante el análisis en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="1e73e-120">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event during background analysis.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e73e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e73e-121">Requirements</span></span>



| <span data-ttu-id="1e73e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e73e-122">Requirement</span></span> | <span data-ttu-id="1e73e-123">Value</span><span class="sxs-lookup"><span data-stu-id="1e73e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e73e-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e73e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1e73e-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1e73e-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1e73e-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e73e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1e73e-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1e73e-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1e73e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e73e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e73e-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1e73e-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1e73e-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e73e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e73e-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e73e-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1e73e-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e73e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e73e-133">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="1e73e-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="1e73e-134">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="1e73e-134">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="1e73e-135">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="1e73e-135">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="1e73e-136">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="1e73e-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="1e73e-137">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="1e73e-137">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="1e73e-138">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="1e73e-138">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="1e73e-139">**IInkAnalyzer:: reconciliate (método)**</span><span class="sxs-lookup"><span data-stu-id="1e73e-139">**IInkAnalyzer::Reconcile Method**</span></span>](iinkanalyzer-reconcile.md)
</dt> <dt>

[<span data-ttu-id="1e73e-140">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="1e73e-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




