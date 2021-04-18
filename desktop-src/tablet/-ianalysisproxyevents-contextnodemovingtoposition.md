---
description: Se produce antes de que IInkAnalyzer mueva un objeto IContextNode a una nueva posición dentro de la colección de subnodos de su nodo primario.
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: 'Evento _IAnalysisProxyEvents:: ContextNodeMovingToPosition (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeMovingToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 462e7428fb43fd998d769dd152e19f8109b04158
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707591"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a><span data-ttu-id="309c6-103">\_Evento IAnalysisProxyEvents:: ContextNodeMovingToPosition</span><span class="sxs-lookup"><span data-stu-id="309c6-103">\_IAnalysisProxyEvents::ContextNodeMovingToPosition event</span></span>

<span data-ttu-id="309c6-104">Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) mueva un objeto [**IContextNode**](icontextnode.md) a una nueva posición dentro de la colección de subnodos de su nodo primario.</span><span class="sxs-lookup"><span data-stu-id="309c6-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object to a new position within its parent node's collection of subnodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="309c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="309c6-105">Syntax</span></span>


```C++
HRESULT ContextNodeMovingToPosition(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pISubNodeToMove,
  [in] IContextNode *pParentContextNode,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a><span data-ttu-id="309c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="309c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="309c6-107">*pInkAnalyzer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="309c6-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="309c6-108">El objeto [**IInkAnalyzer**](iinkanalyzer.md) que mueve el objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="309c6-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="309c6-109">*pISubNodeToMove* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="309c6-109">*pISubNodeToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="309c6-110">Objeto [**IContextNode**](icontextnode.md) que se va a desplace.</span><span class="sxs-lookup"><span data-stu-id="309c6-110">The [**IContextNode**](icontextnode.md) object to move.</span></span>

</dd> <dt>

<span data-ttu-id="309c6-111">*pParentContextNode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="309c6-111">*pParentContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="309c6-112">Objeto primario [**IContextNode**](icontextnode.md) de *pISubNodeToMove*.</span><span class="sxs-lookup"><span data-stu-id="309c6-112">The parent [**IContextNode**](icontextnode.md) object of *pISubNodeToMove*.</span></span>

</dd> <dt>

<span data-ttu-id="309c6-113">*ulNewIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="309c6-113">*ulNewIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="309c6-114">La nueva ubicación de *pISubNodeToMove* en la colección de subnodos de su nodo primario.</span><span class="sxs-lookup"><span data-stu-id="309c6-114">The new location of *pISubNodeToMove* in its parent node's collection of subnodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="309c6-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="309c6-115">Return value</span></span>

<span data-ttu-id="309c6-116">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="309c6-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="309c6-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="309c6-117">Remarks</span></span>

<span data-ttu-id="309c6-118">Utilice este evento cuando la aplicación mantiene su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="309c6-118">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="309c6-119">Este evento se produce durante la fase de conciliación del análisis de tinta o en respuesta a un método del analizador de tinta que mueve un [**IContextNode**](icontextnode.md) dentro de la colección de subnodos de su nodo primario (vea [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) y [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="309c6-119">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that moves an [**IContextNode**](icontextnode.md) within its parent node's collection of subnodes (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span>

<span data-ttu-id="309c6-120">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="309c6-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="309c6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="309c6-121">Requirements</span></span>



| <span data-ttu-id="309c6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="309c6-122">Requirement</span></span> | <span data-ttu-id="309c6-123">Value</span><span class="sxs-lookup"><span data-stu-id="309c6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="309c6-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="309c6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="309c6-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="309c6-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="309c6-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="309c6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="309c6-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="309c6-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="309c6-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="309c6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="309c6-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="309c6-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="309c6-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="309c6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="309c6-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="309c6-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="309c6-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="309c6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="309c6-133">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="309c6-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="309c6-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="309c6-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="309c6-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="309c6-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="309c6-136">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="309c6-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="309c6-137">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="309c6-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="309c6-138">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="309c6-138">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="309c6-139">**IContextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="309c6-139">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="309c6-140">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="309c6-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




