---
description: Se produce antes de que IInkAnalyzer elimine un objeto IContextNode.
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: 'Evento _IAnalysisProxyEvents:: ContextNodeDeleting (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 26488c5657b6d2765534f82b6eacae774adcf561
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707595"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a><span data-ttu-id="66dd0-103">\_Evento IAnalysisProxyEvents:: ContextNodeDeleting</span><span class="sxs-lookup"><span data-stu-id="66dd0-103">\_IAnalysisProxyEvents::ContextNodeDeleting event</span></span>

<span data-ttu-id="66dd0-104">Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) elimine un objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="66dd0-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="66dd0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66dd0-105">Syntax</span></span>


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a><span data-ttu-id="66dd0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66dd0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66dd0-107">*pInkAnalyzer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66dd0-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66dd0-108">El objeto [**IInkAnalyzer**](iinkanalyzer.md) que elimina el objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="66dd0-108">The [**IInkAnalyzer**](iinkanalyzer.md) object deleting the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="66dd0-109">*pContextNodeToBeDeleted* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66dd0-109">*pContextNodeToBeDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66dd0-110">El objeto [**IContextNode**](icontextnode.md) que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="66dd0-110">The [**IContextNode**](icontextnode.md) object to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66dd0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66dd0-111">Return value</span></span>

<span data-ttu-id="66dd0-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="66dd0-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="66dd0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66dd0-113">Remarks</span></span>

<span data-ttu-id="66dd0-114">Utilice este evento cuando la aplicación mantiene su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="66dd0-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="66dd0-115">Este evento se produce durante la fase de conciliación del análisis de tinta o como respuesta a un método del analizador de tintas que elimina un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="66dd0-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that deletes an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="66dd0-116">Antes de que [**IInkAnalyzer**](iinkanalyzer.md) elimine un [**IContextNode**](icontextnode.md), el **IInkAnalyzer** quita todos los trazos del nodo de contexto y quita todos los vínculos a otros nodos de contexto.</span><span class="sxs-lookup"><span data-stu-id="66dd0-116">Before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md), the **IInkAnalyzer** removes all of the strokes from the context node and removes all of the links to other context nodes.</span></span> <span data-ttu-id="66dd0-117">Antes de que se quite el nodo de contexto, el **IInkAnalyzer** puede generar los siguientes eventos.</span><span class="sxs-lookup"><span data-stu-id="66dd0-117">Before the context node is removed, the **IInkAnalyzer** may raise the following events.</span></span>

-   <span data-ttu-id="66dd0-118">El evento [**\_ IAnalysisProxyEvents:: StrokeReparented**](-ianalysisproxyevents-strokereparented.md) cuando mueve un trazo desde [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="66dd0-118">The [**\_IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) event when it moves a stroke from the [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="66dd0-119">El evento [**\_ IAnalysisProxyEvents:: ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) antes de quitar un [**IContextLink**](icontextlink.md) de [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="66dd0-119">The [**\_IAnalysisProxyEvents::ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) event before it removes a [**IContextLink**](icontextlink.md) from the [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="66dd0-120">El evento **\_ IAnalysisProxyEvents:: ContextNodeDeleting** antes de quitar un nodo de contexto primario que ya no tiene nodos secundarios.</span><span class="sxs-lookup"><span data-stu-id="66dd0-120">The **\_IAnalysisProxyEvents::ContextNodeDeleting** event before it removes a parent context node that no longer has child nodes.</span></span>

<span data-ttu-id="66dd0-121">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="66dd0-121">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66dd0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66dd0-122">Requirements</span></span>



| <span data-ttu-id="66dd0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="66dd0-123">Requirement</span></span> | <span data-ttu-id="66dd0-124">Value</span><span class="sxs-lookup"><span data-stu-id="66dd0-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66dd0-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66dd0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="66dd0-126">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="66dd0-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="66dd0-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66dd0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="66dd0-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="66dd0-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="66dd0-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66dd0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="66dd0-130"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="66dd0-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="66dd0-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="66dd0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66dd0-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66dd0-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="66dd0-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="66dd0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66dd0-134">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="66dd0-134">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="66dd0-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="66dd0-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="66dd0-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="66dd0-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="66dd0-137">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="66dd0-137">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="66dd0-138">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="66dd0-138">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="66dd0-139">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="66dd0-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




