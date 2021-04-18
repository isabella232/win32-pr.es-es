---
description: Se produce antes de que IInkAnalyzer reconcilia los resultados del análisis para que una aplicación pueda sincronizar los datos con IInkAnalyzer.
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: 'Evento _IAnalysisProxyEvents:: InkAnalyzerStateChanging (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.InkAnalyzerStateChanging
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 92535c34b5d107fb1e435e9abe229df46204f236
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707590"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a><span data-ttu-id="a33b9-103">\_Evento IAnalysisProxyEvents:: InkAnalyzerStateChanging</span><span class="sxs-lookup"><span data-stu-id="a33b9-103">\_IAnalysisProxyEvents::InkAnalyzerStateChanging event</span></span>

<span data-ttu-id="a33b9-104">Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) reconcilia los resultados del análisis para que una aplicación pueda sincronizar los datos con **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="a33b9-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) reconciles analysis results so that an application can synchronize data with the **IInkAnalyzer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a33b9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a33b9-105">Syntax</span></span>


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a><span data-ttu-id="a33b9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a33b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a33b9-107">*pInkAnalyzer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a33b9-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33b9-108">[**IInkAnalyzer**](iinkanalyzer.md) que está a punto de conciliar sus resultados de análisis.</span><span class="sxs-lookup"><span data-stu-id="a33b9-108">The [**IInkAnalyzer**](iinkanalyzer.md) that is about to reconcile its analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a33b9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a33b9-109">Return value</span></span>

<span data-ttu-id="a33b9-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a33b9-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a33b9-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a33b9-111">Remarks</span></span>

<span data-ttu-id="a33b9-112">Utilice este evento cuando la aplicación mantiene su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="a33b9-112">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="a33b9-113">Cuando **IInkAnalyzer** genera este evento, la aplicación debe rellenar los subnodos del nodo raíz del analizador de tinta (vea [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) y [**IInkAnalyzer:: GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="a33b9-113">When the **IInkAnalyzer** raises this event, your application should populate the subnodes of the ink analyzer's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

<span data-ttu-id="a33b9-114">[**IInkAnalyzer**](iinkanalyzer.md) genera este evento después de que se genere el evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="a33b9-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it raises the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span> <span data-ttu-id="a33b9-115">Genera este evento solo mientras se realiza el análisis en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a33b9-115">It raises this event only while performing background analysis.</span></span>

<span data-ttu-id="a33b9-116">Bloquee la estructura de datos cuando el [**IInkAnalyzer**](iinkanalyzer.md) provoque el evento **\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging** .</span><span class="sxs-lookup"><span data-stu-id="a33b9-116">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the **\_IAnalysisProxyEvents::InkAnalyzerStateChanging** event.</span></span> <span data-ttu-id="a33b9-117">Los cambios en la estructura de datos durante esta fase de análisis pueden provocar errores en el análisis y la sincronización de las entradas manuscritas.</span><span class="sxs-lookup"><span data-stu-id="a33b9-117">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="a33b9-118">Desbloquee la estructura de datos cuando el **IInkAnalyzer** genera el evento [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) o [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="a33b9-118">Unlock your data structure when the **IInkAnalyzer** raises the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="a33b9-119">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a33b9-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a33b9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a33b9-120">Requirements</span></span>



| <span data-ttu-id="a33b9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a33b9-121">Requirement</span></span> | <span data-ttu-id="a33b9-122">Value</span><span class="sxs-lookup"><span data-stu-id="a33b9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a33b9-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a33b9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a33b9-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a33b9-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a33b9-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a33b9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a33b9-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a33b9-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a33b9-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a33b9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a33b9-128"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a33b9-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a33b9-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a33b9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a33b9-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a33b9-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a33b9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a33b9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a33b9-132">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="a33b9-132">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="a33b9-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a33b9-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a33b9-134">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="a33b9-134">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="a33b9-135">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="a33b9-135">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="a33b9-136">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="a33b9-136">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="a33b9-137">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="a33b9-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




