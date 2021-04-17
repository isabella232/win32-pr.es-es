---
description: Se produce cuando finaliza la fase de análisis final.
ms.assetid: 97318c2d-980e-436c-b97d-e064bace5bf0
title: '_IAnalysisEvents:: Results (evento) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Results
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd52a5ce4563827fb22a00f79113fe1e80e852b3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105697997"
---
# <a name="_ianalysiseventsresults-event"></a><span data-ttu-id="49602-103">\_IAnalysisEvents:: Results (evento)</span><span class="sxs-lookup"><span data-stu-id="49602-103">\_IAnalysisEvents::Results event</span></span>

<span data-ttu-id="49602-104">Se produce cuando finaliza la fase de análisis final.</span><span class="sxs-lookup"><span data-stu-id="49602-104">Occurs when the final analysis stage is finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="49602-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49602-105">Syntax</span></span>


```C++
HRESULT Results(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a><span data-ttu-id="49602-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49602-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49602-107">*pInkAnalyzer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49602-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49602-108">[**IInkAnalyzer**](iinkanalyzer.md) que genera los resultados del análisis.</span><span class="sxs-lookup"><span data-stu-id="49602-108">The [**IInkAnalyzer**](iinkanalyzer.md) that produces the analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="49602-109">*pAnalysisStatus* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49602-109">*pAnalysisStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49602-110">Objeto [**IAnalysisStatus**](ianalysisstatus.md) que representa el estado del análisis.</span><span class="sxs-lookup"><span data-stu-id="49602-110">The [**IAnalysisStatus**](ianalysisstatus.md) object that represents the status of the analysis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49602-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49602-111">Return value</span></span>

<span data-ttu-id="49602-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="49602-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="49602-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49602-113">Remarks</span></span>

<span data-ttu-id="49602-114">[**IInkAnalyzer**](iinkanalyzer.md) genera este evento una vez que se han reconciliado los resultados de la fase de análisis final.</span><span class="sxs-lookup"><span data-stu-id="49602-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it has reconciled the results for the final analysis stage.</span></span>

<span data-ttu-id="49602-115">Si la aplicación llama al [**método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), este evento señala cuándo los resultados del análisis están listos.</span><span class="sxs-lookup"><span data-stu-id="49602-115">If your application calls [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md), this event signals when analysis results are ready.</span></span>

<span data-ttu-id="49602-116">Si la aplicación mantiene su propia estructura de datos, que está sincronizada con la del [**IInkAnalyzer**](iinkanalyzer.md), este evento indica que el **IInkAnalyzer** ha terminado de realizar cambios en sus datos internos para esta fase de análisis.</span><span class="sxs-lookup"><span data-stu-id="49602-116">If your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), this event indicates that the **IInkAnalyzer** has finished making changes to its internal data for this analysis stage.</span></span>

<span data-ttu-id="49602-117">Bloquee la estructura de datos cuando el [**IInkAnalyzer**](iinkanalyzer.md) provoque el evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .</span><span class="sxs-lookup"><span data-stu-id="49602-117">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span> <span data-ttu-id="49602-118">Los cambios en la estructura de datos durante esta fase de análisis pueden provocar errores en el análisis y la sincronización de las entradas manuscritas.</span><span class="sxs-lookup"><span data-stu-id="49602-118">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="49602-119">Desbloquee la estructura de datos cuando el **IInkAnalyzer** genera el evento [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) o **\_ IAnalysisEvents:: Results** .</span><span class="sxs-lookup"><span data-stu-id="49602-119">Unlock your data structure when the **IInkAnalyzer** raises the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or **\_IAnalysisEvents::Results** event.</span></span>

<span data-ttu-id="49602-120">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="49602-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="49602-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49602-121">Requirements</span></span>



| <span data-ttu-id="49602-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="49602-122">Requirement</span></span> | <span data-ttu-id="49602-123">Value</span><span class="sxs-lookup"><span data-stu-id="49602-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49602-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49602-124">Minimum supported client</span></span><br/> | <span data-ttu-id="49602-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="49602-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="49602-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49602-126">Minimum supported server</span></span><br/> | <span data-ttu-id="49602-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="49602-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="49602-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49602-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="49602-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="49602-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="49602-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49602-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49602-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49602-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="49602-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="49602-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49602-133">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="49602-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="49602-134">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="49602-134">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="49602-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="49602-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="49602-136">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="49602-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="49602-137">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="49602-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="49602-138">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="49602-138">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="49602-139">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="49602-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




