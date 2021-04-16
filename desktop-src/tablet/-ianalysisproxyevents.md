---
description: Especifica los eventos asociados con los pasos del proxy de datos de un objeto IInkAnalyzer.
ms.assetid: 57fee525-02e2-4721-b6e5-28112d53db2a
title: _IAnalysisProxyEvents interfaz (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b83019cafb6053b9f803c815289d9f9f64d32a5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105678661"
---
# <a name="_ianalysisproxyevents-interface"></a><span data-ttu-id="c31a9-103">\_Interfaz IAnalysisProxyEvents</span><span class="sxs-lookup"><span data-stu-id="c31a9-103">\_IAnalysisProxyEvents interface</span></span>

<span data-ttu-id="c31a9-104">Especifica los eventos asociados con los pasos del proxy de datos de un objeto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="c31a9-104">Specifies events associated with the data proxy steps of an [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>

-   [<span data-ttu-id="c31a9-105">Eventos</span><span class="sxs-lookup"><span data-stu-id="c31a9-105">Events</span></span>](/windows)

### <a name="events"></a><span data-ttu-id="c31a9-106">Events</span><span class="sxs-lookup"><span data-stu-id="c31a9-106">Events</span></span>

<span data-ttu-id="c31a9-107">La interfaz **\_ IAnalysisProxyEvents** tiene estos eventos.</span><span class="sxs-lookup"><span data-stu-id="c31a9-107">The **\_IAnalysisProxyEvents** interface has these events.</span></span>



| <span data-ttu-id="c31a9-108">Evento</span><span class="sxs-lookup"><span data-stu-id="c31a9-108">Event</span></span>                                                                                      | <span data-ttu-id="c31a9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c31a9-109">Description</span></span>                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c31a9-110">**ContextNodeCreated**</span><span class="sxs-lookup"><span data-stu-id="c31a9-110">**ContextNodeCreated**</span></span>](-ianalysisproxyevents-contextnodecreated.md)                     | <span data-ttu-id="c31a9-111">Se produce después de que [**IInkAnalyzer**](iinkanalyzer.md) cree un objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="c31a9-111">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                                                  |
| [<span data-ttu-id="c31a9-112">**ContextNodeDeleting**</span><span class="sxs-lookup"><span data-stu-id="c31a9-112">**ContextNodeDeleting**</span></span>](-ianalysisproxyevents-contextnodedeleting.md)                   | <span data-ttu-id="c31a9-113">Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) elimine un objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="c31a9-113">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                                                 |
| [<span data-ttu-id="c31a9-114">**ContextNodeLinkAdding**</span><span class="sxs-lookup"><span data-stu-id="c31a9-114">**ContextNodeLinkAdding**</span></span>](-ianalysisproxyevents-contextnodelinkadding.md)               | <span data-ttu-id="c31a9-115">Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) agregue un objeto [**IContextLink**](icontextlink.md) entre dos objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="c31a9-115">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) adds an [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>           |
| [<span data-ttu-id="c31a9-116">**ContextNodeLinkDeleting**</span><span class="sxs-lookup"><span data-stu-id="c31a9-116">**ContextNodeLinkDeleting**</span></span>](-ianalysisproxyevents-contextnodelinkdeleting.md)           | <span data-ttu-id="c31a9-117">Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) elimine un objeto [**IContextLink**](icontextlink.md) entre dos objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="c31a9-117">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes a [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>         |
| [<span data-ttu-id="c31a9-118">**ContextNodeMovingToPosition**</span><span class="sxs-lookup"><span data-stu-id="c31a9-118">**ContextNodeMovingToPosition**</span></span>](-ianalysisproxyevents-contextnodemovingtoposition.md)   | <span data-ttu-id="c31a9-119">Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) mueva un objeto [**IContextNode**](icontextnode.md) a una nueva posición dentro de la colección de subnodos de su nodo primario.</span><span class="sxs-lookup"><span data-stu-id="c31a9-119">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object to a new position within its parent node's collection of subnodes.</span></span><br/> |
| [<span data-ttu-id="c31a9-120">**ContextNodePropertiesUpdated**</span><span class="sxs-lookup"><span data-stu-id="c31a9-120">**ContextNodePropertiesUpdated**</span></span>](-ianalysisproxyevents-contextnodepropertiesupdated.md) | <span data-ttu-id="c31a9-121">Se produce después de que [**IInkAnalyzer**](iinkanalyzer.md) actualice una o varias propiedades de un objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="c31a9-121">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) updates one or more properties of an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                        |
| [<span data-ttu-id="c31a9-122">**ContextNodeReparenting**</span><span class="sxs-lookup"><span data-stu-id="c31a9-122">**ContextNodeReparenting**</span></span>](-ianalysisproxyevents-contextnodereparenting.md)             | <span data-ttu-id="c31a9-123">Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) mueva un objeto [**IContextNode**](icontextnode.md) cambiando su nodo primario.</span><span class="sxs-lookup"><span data-stu-id="c31a9-123">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object by changing its parent node.</span></span><br/>                                       |
| [<span data-ttu-id="c31a9-124">**InkAnalyzerStateChanging**</span><span class="sxs-lookup"><span data-stu-id="c31a9-124">**InkAnalyzerStateChanging**</span></span>](-ianalysisproxyevents-inkanalyzerstatechanging.md)         | <span data-ttu-id="c31a9-125">Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) reconcilia los resultados del análisis para que una aplicación pueda sincronizar los datos con **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="c31a9-125">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) reconciles analysis results so that an application can synchronize data with the **IInkAnalyzer**.</span></span><br/>                      |
| [<span data-ttu-id="c31a9-126">**PopulateContextNode**</span><span class="sxs-lookup"><span data-stu-id="c31a9-126">**PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)                   | <span data-ttu-id="c31a9-127">Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) realice el análisis dentro de la región de un objeto [**IContextNode**](icontextnode.md) parcialmente rellenado.</span><span class="sxs-lookup"><span data-stu-id="c31a9-127">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) performs analysis within the region of a partially populated [**IContextNode**](icontextnode.md) object.</span></span><br/>               |
| [<span data-ttu-id="c31a9-128">**StrokeReparented**</span><span class="sxs-lookup"><span data-stu-id="c31a9-128">**StrokeReparented**</span></span>](-ianalysisproxyevents-strokereparented.md)                         | <span data-ttu-id="c31a9-129">Se produce cuando el [**IInkAnalyzer**](iinkanalyzer.md) mueve un trazo de un objeto [**IContextNode**](icontextnode.md) a otro.</span><span class="sxs-lookup"><span data-stu-id="c31a9-129">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) moves a stroke from one [**IContextNode**](icontextnode.md) object to another.</span></span><br/>                                           |



 

## <a name="remarks"></a><span data-ttu-id="c31a9-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c31a9-130">Remarks</span></span>

<span data-ttu-id="c31a9-131">Utilice estos eventos cuando la aplicación mantiene su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="c31a9-131">Use these events when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="c31a9-132">Para obtener más información sobre cómo sincronizar los datos de la aplicación con **IInkAnalyzer**, vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c31a9-132">For more information about synchronizing your application data with the **IInkAnalyzer**, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c31a9-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c31a9-133">Requirements</span></span>



| <span data-ttu-id="c31a9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c31a9-134">Requirement</span></span> | <span data-ttu-id="c31a9-135">Value</span><span class="sxs-lookup"><span data-stu-id="c31a9-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c31a9-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c31a9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c31a9-137">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c31a9-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c31a9-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c31a9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c31a9-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c31a9-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c31a9-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c31a9-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c31a9-141"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c31a9-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c31a9-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c31a9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c31a9-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c31a9-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c31a9-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="c31a9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c31a9-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="c31a9-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c31a9-146">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="c31a9-146">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c31a9-147">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="c31a9-147">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="c31a9-148">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="c31a9-148">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="c31a9-149">\_IAnalysisEvents</span><span class="sxs-lookup"><span data-stu-id="c31a9-149">\_IAnalysisEvents</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="c31a9-150">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="c31a9-150">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

