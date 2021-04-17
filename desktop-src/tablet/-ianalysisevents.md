---
description: Especifica eventos asociados a los pasos de análisis de un objeto IInkAnalyzer.
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: Interfaz _IAnalysisEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90e32669d8b542202f6166052c072f224bb2954a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697379"
---
# <a name="_ianalysisevents-interface"></a><span data-ttu-id="a372c-103">\_Interfaz IAnalysisEvents</span><span class="sxs-lookup"><span data-stu-id="a372c-103">\_IAnalysisEvents interface</span></span>

<span data-ttu-id="a372c-104">Especifica eventos asociados a los pasos de análisis de un objeto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="a372c-104">Specifies events associated with the analysis steps of an [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>

-   [<span data-ttu-id="a372c-105">Eventos</span><span class="sxs-lookup"><span data-stu-id="a372c-105">Events</span></span>](/windows)

### <a name="events"></a><span data-ttu-id="a372c-106">Events</span><span class="sxs-lookup"><span data-stu-id="a372c-106">Events</span></span>

<span data-ttu-id="a372c-107">La interfaz **\_ IAnalysisEvents** tiene estos eventos.</span><span class="sxs-lookup"><span data-stu-id="a372c-107">The **\_IAnalysisEvents** interface has these events.</span></span>



| <span data-ttu-id="a372c-108">Evento</span><span class="sxs-lookup"><span data-stu-id="a372c-108">Event</span></span>                                                               | <span data-ttu-id="a372c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a372c-109">Description</span></span>                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a372c-110">**Actividad**</span><span class="sxs-lookup"><span data-stu-id="a372c-110">**Activity**</span></span>](-ianalysisevents-activity.md)                       | <span data-ttu-id="a372c-111">Tiene lugar durante las llamadas al método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o al método [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) .</span><span class="sxs-lookup"><span data-stu-id="a372c-111">Occurs during calls to the [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) method.</span></span><br/> |
| [<span data-ttu-id="a372c-112">**IntermediateResults**</span><span class="sxs-lookup"><span data-stu-id="a372c-112">**IntermediateResults**</span></span>](-ianalysisevents-intermediateresults.md) | <span data-ttu-id="a372c-113">Se produce cuando finaliza la fase de análisis intermedio actual.</span><span class="sxs-lookup"><span data-stu-id="a372c-113">Occurs when the current intermediate analysis stage is finished.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="a372c-114">**ReadyToReconcile**</span><span class="sxs-lookup"><span data-stu-id="a372c-114">**ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)       | <span data-ttu-id="a372c-115">Se produce cuando [**IInkAnalyzer**](iinkanalyzer.md) está listo para conciliar los resultados del análisis de fondo con su estado actual.</span><span class="sxs-lookup"><span data-stu-id="a372c-115">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) is ready to reconcile its background analysis results with its current state.</span></span><br/>                                                  |
| [<span data-ttu-id="a372c-116">**Results**</span><span class="sxs-lookup"><span data-stu-id="a372c-116">**Results**</span></span>](-ianalysisevents-results.md)                         | <span data-ttu-id="a372c-117">Se produce cuando finaliza la fase de análisis final.</span><span class="sxs-lookup"><span data-stu-id="a372c-117">Occurs when the final analysis stage is finished.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="a372c-118">**UpdateStrokesCache**</span><span class="sxs-lookup"><span data-stu-id="a372c-118">**UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)   | <span data-ttu-id="a372c-119">Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) tenga acceso a los datos del trazo.</span><span class="sxs-lookup"><span data-stu-id="a372c-119">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) accesses stroke data.</span></span><br/>                                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="a372c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a372c-120">Requirements</span></span>



| <span data-ttu-id="a372c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a372c-121">Requirement</span></span> | <span data-ttu-id="a372c-122">Value</span><span class="sxs-lookup"><span data-stu-id="a372c-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a372c-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a372c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a372c-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a372c-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a372c-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a372c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a372c-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a372c-126">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="a372c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a372c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a372c-128">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="a372c-128">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="a372c-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a372c-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a372c-130">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="a372c-130">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="a372c-131">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="a372c-131">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="a372c-132">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="a372c-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

