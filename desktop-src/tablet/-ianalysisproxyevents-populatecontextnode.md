---
description: Se produce antes de que IInkAnalyzer realice el análisis dentro de la región de un objeto IContextNode parcialmente rellenado.
ms.assetid: c24e8adb-672f-444a-bccb-1e9e55bea432
title: _IAnalysisProxyEvents::P evento opulateContextNode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.PopulateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e8aebe4ba777d62f90aa00c45ea0f1644e2b8183
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279862"
---
# <a name="_ianalysisproxyeventspopulatecontextnode-event"></a><span data-ttu-id="e80e1-103">\_IAnalysisProxyEvents::P evento opulateContextNode</span><span class="sxs-lookup"><span data-stu-id="e80e1-103">\_IAnalysisProxyEvents::PopulateContextNode event</span></span>

<span data-ttu-id="e80e1-104">Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) realice el análisis dentro de la región de un objeto [**IContextNode**](icontextnode.md) parcialmente rellenado.</span><span class="sxs-lookup"><span data-stu-id="e80e1-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) performs analysis within the region of a partially populated [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e80e1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e80e1-105">Syntax</span></span>


```C++
HRESULT PopulateContextNode(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToPopulate
);
```



## <a name="parameters"></a><span data-ttu-id="e80e1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e80e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e80e1-107">*pInkAnalyzer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e80e1-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e80e1-108">Objeto [**IInkAnalyzer**](iinkanalyzer.md) sobre el que se va a realizar el análisis.</span><span class="sxs-lookup"><span data-stu-id="e80e1-108">The [**IInkAnalyzer**](iinkanalyzer.md) object about to perform analysis.</span></span>

</dd> <dt>

<span data-ttu-id="e80e1-109">*pContextNodeToPopulate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e80e1-109">*pContextNodeToPopulate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e80e1-110">Objeto [**IContextNode**](icontextnode.md) parcialmente rellenado.</span><span class="sxs-lookup"><span data-stu-id="e80e1-110">The partially populated [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e80e1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e80e1-111">Return value</span></span>

<span data-ttu-id="e80e1-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e80e1-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e80e1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e80e1-113">Remarks</span></span>

<span data-ttu-id="e80e1-114">Utilice este evento cuando la aplicación mantiene su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="e80e1-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="e80e1-115">Cuando **IInkAnalyzer** genera este evento, la aplicación debe rellenar el *pContextNodeToPopulate*.</span><span class="sxs-lookup"><span data-stu-id="e80e1-115">When the **IInkAnalyzer** raises this event, your application should populate the *pContextNodeToPopulate*.</span></span> <span data-ttu-id="e80e1-116">Durante la fase de análisis, el **IInkAnalyzer** genera este evento para obtener información sobre las áreas en las que está analizando la tinta.</span><span class="sxs-lookup"><span data-stu-id="e80e1-116">During the analysis phase, the **IInkAnalyzer** raises this event to get information for areas in which it is analyzing ink.</span></span>

<span data-ttu-id="e80e1-117">Si el documento contiene vínculos para *pContextNodeToPopulate*, la aplicación debe crear y agregar estos vínculos.</span><span class="sxs-lookup"><span data-stu-id="e80e1-117">If the document contains links for the *pContextNodeToPopulate*, your application should create and add these links.</span></span> <span data-ttu-id="e80e1-118">Este proceso requiere que los nodos de origen y de destino, incluidos sus antecesores, se rellenen por completo antes de que se cierre el controlador de eventos para este evento (vea [**IContextLink:: GetSourceNode**](icontextlink-getsourcenode.md) y [**IContextLink:: GetDestinationNode**](icontextlink-getdestinationnode.md)).</span><span class="sxs-lookup"><span data-stu-id="e80e1-118">This process requires that both the source and destination nodes, including their ancestors, are fully populated before the event handler for this event exits (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) and [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)).</span></span>

<span data-ttu-id="e80e1-119">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e80e1-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="e80e1-120">Durante el análisis en segundo plano, [**IInkAnalyzer**](iinkanalyzer.md) genera este evento después de que se genere el evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="e80e1-120">During background analysis, the [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it raises the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="e80e1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e80e1-121">Requirements</span></span>



| <span data-ttu-id="e80e1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e80e1-122">Requirement</span></span> | <span data-ttu-id="e80e1-123">Value</span><span class="sxs-lookup"><span data-stu-id="e80e1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e80e1-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e80e1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e80e1-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e80e1-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e80e1-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e80e1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e80e1-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e80e1-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e80e1-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e80e1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e80e1-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e80e1-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e80e1-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e80e1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e80e1-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e80e1-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e80e1-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e80e1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e80e1-133">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="e80e1-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="e80e1-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="e80e1-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e80e1-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="e80e1-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e80e1-136">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="e80e1-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="e80e1-137">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="e80e1-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="e80e1-138">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="e80e1-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




