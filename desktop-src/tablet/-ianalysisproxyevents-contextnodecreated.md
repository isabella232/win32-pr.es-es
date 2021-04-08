---
description: Se produce después de que IInkAnalyzer cree un objeto IContextNode.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: 'Evento _IAnalysisProxyEvents:: ContextNodeCreated (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeCreated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac06a7fc45604e93408b1bb144ee7e884efd351e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104003455"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a><span data-ttu-id="d5c04-103">\_Evento IAnalysisProxyEvents:: ContextNodeCreated</span><span class="sxs-lookup"><span data-stu-id="d5c04-103">\_IAnalysisProxyEvents::ContextNodeCreated event</span></span>

<span data-ttu-id="d5c04-104">Se produce después de que [**IInkAnalyzer**](iinkanalyzer.md) cree un objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="d5c04-104">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c04-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5c04-105">Syntax</span></span>


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="d5c04-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5c04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c04-107">*pInkAnalyzer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5c04-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c04-108">[**IInkAnalyzer**](iinkanalyzer.md) que crea el objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="d5c04-108">The [**IInkAnalyzer**](iinkanalyzer.md) creating the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="d5c04-109">*pContextNodeCreated* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5c04-109">*pContextNodeCreated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c04-110">Nuevo objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="d5c04-110">The new [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5c04-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5c04-111">Return value</span></span>

<span data-ttu-id="d5c04-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d5c04-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d5c04-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5c04-113">Remarks</span></span>

<span data-ttu-id="d5c04-114">Utilice este evento cuando la aplicación mantiene su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="d5c04-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="d5c04-115">Este evento se produce durante la fase de conciliación del análisis de tinta o como respuesta a un método del analizador de tinta que crea un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="d5c04-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that creates an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="d5c04-116">Cuando el [**IInkAnalyzer**](iinkanalyzer.md) crea un [**IContextNode**](icontextnode.md), el nuevo **IContextNode** no contiene ningún trazo, no contiene vínculos a otros objetos **IContextNode** y es posible que no tenga todas sus propiedades establecidas.</span><span class="sxs-lookup"><span data-stu-id="d5c04-116">When the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md), the new **IContextNode** does not contain any strokes, does not contain links to other **IContextNode** objects, and may not have all of its properties set.</span></span> <span data-ttu-id="d5c04-117">Además, el nuevo **IContextNode** se agrega al final de la colección de subnodos de su nodo primario (vea [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) y [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="d5c04-117">Also, the new **IContextNode** is added to the end of its parent node's collection of subnodes (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="d5c04-118">Después de este evento, **IInkAnalyzer** puede generar los siguientes eventos.</span><span class="sxs-lookup"><span data-stu-id="d5c04-118">After this event, the **IInkAnalyzer** may raise the following events.</span></span>

-   <span data-ttu-id="d5c04-119">El evento [**\_ IAnalysisProxyEvents:: StrokeReparented**](-ianalysisproxyevents-strokereparented.md) cuando mueve un trazo de un nodo de contexto a otro.</span><span class="sxs-lookup"><span data-stu-id="d5c04-119">The [**\_IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) event when it moves a stroke from one context node to another.</span></span>
-   <span data-ttu-id="d5c04-120">El evento [**\_ IAnalysisProxyEvents:: ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) cuando agrega un [**IContextLink**](icontextlink.md) a un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="d5c04-120">The [**\_IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) event when it adds an [**IContextLink**](icontextlink.md) to an [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="d5c04-121">El evento [**\_ IAnalysisProxyEvents:: ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) cuando cambia el orden de una [**IContextNode**](icontextnode.md) dentro de la colección de subnodos de su nodo primario.</span><span class="sxs-lookup"><span data-stu-id="d5c04-121">The [**\_IAnalysisProxyEvents::ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) event when it changes the order of an [**IContextNode**](icontextnode.md) within its parent node's collection of subnodes.</span></span>
-   <span data-ttu-id="d5c04-122">[**IInkAnalyzer**](iinkanalyzer.md) genera el evento [**\_ IAnalysisProxyEvents:: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) después de resolver el estado de [**IContextNode**](icontextnode.md) para esta fase de análisis.</span><span class="sxs-lookup"><span data-stu-id="d5c04-122">The [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) event after it resolves the state of the [**IContextNode**](icontextnode.md) for this analysis phase.</span></span>

<span data-ttu-id="d5c04-123">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d5c04-123">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5c04-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5c04-124">Requirements</span></span>



| <span data-ttu-id="d5c04-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5c04-125">Requirement</span></span> | <span data-ttu-id="d5c04-126">Value</span><span class="sxs-lookup"><span data-stu-id="d5c04-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c04-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5c04-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d5c04-128">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d5c04-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d5c04-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5c04-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d5c04-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d5c04-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d5c04-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5c04-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5c04-132"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d5c04-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d5c04-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d5c04-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5c04-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5c04-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d5c04-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5c04-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c04-136">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="d5c04-136">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="d5c04-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="d5c04-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d5c04-138">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="d5c04-138">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="d5c04-139">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="d5c04-139">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="d5c04-140">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="d5c04-140">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="d5c04-141">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="d5c04-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




