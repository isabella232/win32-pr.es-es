---
description: Se produce antes de que IInkAnalyzer tenga acceso a los datos del trazo.
ms.assetid: fed46476-4531-4516-9375-d7b654efb3be
title: 'Evento _IAnalysisEvents:: UpdateStrokesCache (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.UpdateStrokesCache
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5d16011d8c5fe571d228b632fecb7a973bafcbf5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105697996"
---
# <a name="_ianalysiseventsupdatestrokescache-event"></a><span data-ttu-id="080bc-103">\_Evento IAnalysisEvents:: UpdateStrokesCache</span><span class="sxs-lookup"><span data-stu-id="080bc-103">\_IAnalysisEvents::UpdateStrokesCache event</span></span>

<span data-ttu-id="080bc-104">Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) tenga acceso a los datos del trazo.</span><span class="sxs-lookup"><span data-stu-id="080bc-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) accesses stroke data.</span></span>

## <a name="syntax"></a><span data-ttu-id="080bc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="080bc-105">Syntax</span></span>


```C++
HRESULT UpdateStrokesCache(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="080bc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="080bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="080bc-107">*ulStrokeIdsCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="080bc-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="080bc-108">Número de identificadores de trazo en *plStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="080bc-108">The number of stroke identifiers in *plStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="080bc-109">*plStrokeIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="080bc-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="080bc-110">Los identificadores de los trazos cuyos datos de paquetes se han borrado.</span><span class="sxs-lookup"><span data-stu-id="080bc-110">The identifiers of the strokes whose packet data has been cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="080bc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="080bc-111">Return value</span></span>

<span data-ttu-id="080bc-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="080bc-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="080bc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="080bc-113">Remarks</span></span>

<span data-ttu-id="080bc-114">El [**IInkAnalyzer**](iinkanalyzer.md) genera este evento durante el análisis de tinta cuando tiene acceso a uno o varios trazos para los que se han borrado los datos del paquete.</span><span class="sxs-lookup"><span data-stu-id="080bc-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event during ink analysis when it accesses one or more strokes for which the packet data has been cleared.</span></span> <span data-ttu-id="080bc-115">Para actualizar los datos del paquete de trazos, utilice el método [**IInkAnalyzer:: UpdateStrokesData Method**](iinkanalyzer-updatestrokesdata.md) .</span><span class="sxs-lookup"><span data-stu-id="080bc-115">To update the stroke packet data, use the [**IInkAnalyzer::UpdateStrokesData Method**](iinkanalyzer-updatestrokesdata.md) method.</span></span>

<span data-ttu-id="080bc-116">El [**IInkAnalyzer**](iinkanalyzer.md) no genera este evento cuando se tiene acceso a un nodo de hoja de tinta parcialmente rellenado cuando el **IInkAnalyzer** no ha establecido la ubicación del nodo.</span><span class="sxs-lookup"><span data-stu-id="080bc-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not raise this event when accessing a partially populated ink leaf node when the location of the node has not been set by the **IInkAnalyzer**.</span></span>

<span data-ttu-id="080bc-117">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="080bc-117">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="080bc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="080bc-118">Requirements</span></span>



| <span data-ttu-id="080bc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="080bc-119">Requirement</span></span> | <span data-ttu-id="080bc-120">Value</span><span class="sxs-lookup"><span data-stu-id="080bc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="080bc-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="080bc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="080bc-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="080bc-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="080bc-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="080bc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="080bc-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="080bc-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="080bc-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="080bc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="080bc-126"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="080bc-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="080bc-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="080bc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="080bc-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="080bc-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="080bc-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="080bc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="080bc-130">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="080bc-130">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="080bc-131">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="080bc-131">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="080bc-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="080bc-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="080bc-133">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="080bc-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="080bc-134">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="080bc-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="080bc-135">**IInkAnalyzer:: UpdateStrokesData (método)**</span><span class="sxs-lookup"><span data-stu-id="080bc-135">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="080bc-136">**IContextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="080bc-136">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="080bc-137">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="080bc-137">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="080bc-138">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="080bc-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




