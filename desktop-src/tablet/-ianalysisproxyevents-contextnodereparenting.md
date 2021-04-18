---
description: Se produce antes de que IInkAnalyzer mueva un objeto IContextNode cambiando su nodo primario.
ms.assetid: 91261270-aa7c-4f0a-a790-1b2bf322a3ad
title: 'Evento _IAnalysisProxyEvents:: ContextNodeReparenting (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeReparenting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 084f971edc5adce0845fc7e1c3ea6ea59a066bb0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707605"
---
# <a name="_ianalysisproxyeventscontextnodereparenting-event"></a><span data-ttu-id="5b5af-103">\_Evento IAnalysisProxyEvents:: ContextNodeReparenting</span><span class="sxs-lookup"><span data-stu-id="5b5af-103">\_IAnalysisProxyEvents::ContextNodeReparenting event</span></span>

<span data-ttu-id="5b5af-104">Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) mueva un objeto [**IContextNode**](icontextnode.md) cambiando su nodo primario.</span><span class="sxs-lookup"><span data-stu-id="5b5af-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object by changing its parent node.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b5af-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b5af-105">Syntax</span></span>


```C++
HRESULT ContextNodeReparenting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pNewParentContextNode,
  [in] IContextNode *pContextNodeToBeReparented
);
```



## <a name="parameters"></a><span data-ttu-id="5b5af-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b5af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b5af-107">*pInkAnalyzer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b5af-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b5af-108">El objeto [**IInkAnalyzer**](iinkanalyzer.md) que mueve el objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="5b5af-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5b5af-109">*pNewParentContextNode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b5af-109">*pNewParentContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b5af-110">Nuevo objeto [**IContextNode**](icontextnode.md) primario.</span><span class="sxs-lookup"><span data-stu-id="5b5af-110">The new parent [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5b5af-111">*pContextNodeToBeReparented* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b5af-111">*pContextNodeToBeReparented* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b5af-112">Objeto [**IContextNode**](icontextnode.md) que se va a desplace.</span><span class="sxs-lookup"><span data-stu-id="5b5af-112">The [**IContextNode**](icontextnode.md) object to be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b5af-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b5af-113">Return value</span></span>

<span data-ttu-id="5b5af-114">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5b5af-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5b5af-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b5af-115">Remarks</span></span>

<span data-ttu-id="5b5af-116">Utilice este evento cuando la aplicación mantiene su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="5b5af-116">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="5b5af-117">Este evento se produce durante la fase de conciliación del análisis de tinta o en respuesta a un método que mueve un [**IContextNode**](icontextnode.md) de una colección de subnodos a otro (vea [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) y [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="5b5af-117">This event occurs during the reconcile phase of ink analysis, or in response to a method that moves an [**IContextNode**](icontextnode.md) from one collection of subnodes to another (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span>

<span data-ttu-id="5b5af-118">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5b5af-118">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b5af-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b5af-119">Requirements</span></span>



| <span data-ttu-id="5b5af-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b5af-120">Requirement</span></span> | <span data-ttu-id="5b5af-121">Value</span><span class="sxs-lookup"><span data-stu-id="5b5af-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5af-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b5af-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5b5af-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5b5af-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5b5af-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b5af-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5b5af-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5b5af-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5b5af-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b5af-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b5af-127"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5b5af-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5b5af-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b5af-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b5af-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b5af-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5b5af-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b5af-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b5af-131">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="5b5af-131">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="5b5af-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="5b5af-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="5b5af-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="5b5af-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="5b5af-134">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="5b5af-134">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="5b5af-135">**IContextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="5b5af-135">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="5b5af-136">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="5b5af-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="5b5af-137">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="5b5af-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="5b5af-138">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="5b5af-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




