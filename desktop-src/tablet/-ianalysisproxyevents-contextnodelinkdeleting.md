---
description: Se produce antes de que IInkAnalyzer elimine un objeto IContextLink entre dos objetos IContextNode.
ms.assetid: bc9716b8-8793-4886-aff4-d880024129a6
title: 'Evento _IAnalysisProxyEvents:: ContextNodeLinkDeleting (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc4ba9586fc4c520b9ee44b039bd56f8ef2ade3c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279853"
---
# <a name="_ianalysisproxyeventscontextnodelinkdeleting-event"></a><span data-ttu-id="752ef-103">\_Evento IAnalysisProxyEvents:: ContextNodeLinkDeleting</span><span class="sxs-lookup"><span data-stu-id="752ef-103">\_IAnalysisProxyEvents::ContextNodeLinkDeleting event</span></span>

<span data-ttu-id="752ef-104">Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) elimine un objeto [**IContextLink**](icontextlink.md) entre dos objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="752ef-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes a [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="752ef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="752ef-105">Syntax</span></span>


```C++
HRESULT ContextNodeLinkDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeDeleted
);
```



## <a name="parameters"></a><span data-ttu-id="752ef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="752ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="752ef-107">*pInkAnalyzer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="752ef-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752ef-108">[**IInkAnalyzer**](iinkanalyzer.md) que elimina el vínculo.</span><span class="sxs-lookup"><span data-stu-id="752ef-108">The [**IInkAnalyzer**](iinkanalyzer.md) deleting the link.</span></span>

</dd> <dt>

<span data-ttu-id="752ef-109">*pContextLinkToBeDeleted* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="752ef-109">*pContextLinkToBeDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752ef-110">El objeto [**IContextLink**](icontextlink.md) que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="752ef-110">The [**IContextLink**](icontextlink.md) object to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="752ef-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="752ef-111">Return value</span></span>

<span data-ttu-id="752ef-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="752ef-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="752ef-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="752ef-113">Remarks</span></span>

<span data-ttu-id="752ef-114">Utilice este evento cuando la aplicación mantiene su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="752ef-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="752ef-115">Este evento se produce durante la fase de conciliación del análisis de tinta o en respuesta a un método **IInkAnalyzer** que quita un [**IContextLink**](icontextlink.md) de un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="752ef-115">This event occurs during the reconcile phase of ink analysis, or in response to an **IInkAnalyzer** method that removes an [**IContextLink**](icontextlink.md) from an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="752ef-116">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="752ef-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="752ef-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="752ef-117">Requirements</span></span>



| <span data-ttu-id="752ef-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="752ef-118">Requirement</span></span> | <span data-ttu-id="752ef-119">Value</span><span class="sxs-lookup"><span data-stu-id="752ef-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="752ef-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="752ef-120">Minimum supported client</span></span><br/> | <span data-ttu-id="752ef-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="752ef-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="752ef-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="752ef-122">Minimum supported server</span></span><br/> | <span data-ttu-id="752ef-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="752ef-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="752ef-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="752ef-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="752ef-125"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="752ef-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="752ef-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="752ef-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="752ef-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="752ef-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="752ef-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="752ef-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="752ef-129">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="752ef-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="752ef-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="752ef-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="752ef-131">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="752ef-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="752ef-132">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="752ef-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="752ef-133">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="752ef-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="752ef-134">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="752ef-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="752ef-135">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="752ef-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




