---
description: Se produce después de que IInkAnalyzer actualice una o varias propiedades de un objeto IContextNode.
ms.assetid: f626c263-31a4-45ee-ae04-3251eac0d652
title: 'Evento _IAnalysisProxyEvents:: ContextNodePropertiesUpdated (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodePropertiesUpdated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fa035b89c531f3b2d230ab849ba20b945dd2d25c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707587"
---
# <a name="_ianalysisproxyeventscontextnodepropertiesupdated-event"></a><span data-ttu-id="ddc16-103">\_Evento IAnalysisProxyEvents:: ContextNodePropertiesUpdated</span><span class="sxs-lookup"><span data-stu-id="ddc16-103">\_IAnalysisProxyEvents::ContextNodePropertiesUpdated event</span></span>

<span data-ttu-id="ddc16-104">Se produce después de que [**IInkAnalyzer**](iinkanalyzer.md) actualice una o varias propiedades de un objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ddc16-104">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) updates one or more properties of an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddc16-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddc16-105">Syntax</span></span>


```C++
HRESULT ContextNodePropertiesUpdated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeUpdated
);
```



## <a name="parameters"></a><span data-ttu-id="ddc16-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ddc16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddc16-107">*pInkAnalyzer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ddc16-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc16-108">El objeto [**IInkAnalyzer**](iinkanalyzer.md) que actualiza las propiedades.</span><span class="sxs-lookup"><span data-stu-id="ddc16-108">The [**IInkAnalyzer**](iinkanalyzer.md) object updating the properties.</span></span>

</dd> <dt>

<span data-ttu-id="ddc16-109">*pContextNodeUpdated* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ddc16-109">*pContextNodeUpdated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc16-110">Objeto [**IContextNode**](icontextnode.md) cuyas propiedades se actualizan.</span><span class="sxs-lookup"><span data-stu-id="ddc16-110">The [**IContextNode**](icontextnode.md) object whose properties are updated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddc16-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ddc16-111">Return value</span></span>

<span data-ttu-id="ddc16-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ddc16-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ddc16-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddc16-113">Remarks</span></span>

<span data-ttu-id="ddc16-114">Utilice este evento cuando la aplicación mantiene su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="ddc16-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="ddc16-115">Este evento se produce durante la fase de conciliación del análisis de tinta o como respuesta a un método del analizador de tintas que cambia las propiedades de un [**IContextNode**](icontextnode.md) (vea [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)).</span><span class="sxs-lookup"><span data-stu-id="ddc16-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that changes the properties of an [**IContextNode**](icontextnode.md) (see [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)).</span></span>

<span data-ttu-id="ddc16-116">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ddc16-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ddc16-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddc16-117">Requirements</span></span>



| <span data-ttu-id="ddc16-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddc16-118">Requirement</span></span> | <span data-ttu-id="ddc16-119">Value</span><span class="sxs-lookup"><span data-stu-id="ddc16-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddc16-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddc16-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ddc16-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ddc16-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ddc16-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddc16-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ddc16-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ddc16-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ddc16-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ddc16-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddc16-125"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ddc16-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ddc16-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ddc16-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddc16-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddc16-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ddc16-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddc16-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddc16-129">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="ddc16-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="ddc16-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ddc16-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ddc16-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="ddc16-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ddc16-132">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="ddc16-132">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="ddc16-133">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="ddc16-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="ddc16-134">Propiedades del nodo de contexto</span><span class="sxs-lookup"><span data-stu-id="ddc16-134">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="ddc16-135">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="ddc16-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




