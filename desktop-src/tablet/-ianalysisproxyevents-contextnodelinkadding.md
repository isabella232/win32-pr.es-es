---
description: Se produce antes de que el analizador de tinta agregue un objeto IContextLink entre dos objetos IContextNode.
ms.assetid: ec56cb8e-5154-45ee-911d-e2a240d19dc3
title: 'Evento _IAnalysisProxyEvents:: ContextNodeLinkAdding (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkAdding
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 341c551064869532e8b51ddecdbe1d5a78878abd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707596"
---
# <a name="_ianalysisproxyeventscontextnodelinkadding-event"></a><span data-ttu-id="b8293-103">\_Evento IAnalysisProxyEvents:: ContextNodeLinkAdding</span><span class="sxs-lookup"><span data-stu-id="b8293-103">\_IAnalysisProxyEvents::ContextNodeLinkAdding event</span></span>

<span data-ttu-id="b8293-104">Se produce antes de que el analizador de tinta agregue un objeto [**IContextLink**](icontextlink.md) entre dos objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b8293-104">Occurs before the ink analyzer adds an [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8293-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8293-105">Syntax</span></span>


```C++
HRESULT ContextNodeLinkAdding(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeAdded
);
```



## <a name="parameters"></a><span data-ttu-id="b8293-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8293-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8293-107">*pInkAnalyzer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8293-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8293-108">[**IInkAnalyzer**](iinkanalyzer.md) que agrega el vínculo.</span><span class="sxs-lookup"><span data-stu-id="b8293-108">The [**IInkAnalyzer**](iinkanalyzer.md) adding the link.</span></span>

</dd> <dt>

<span data-ttu-id="b8293-109">*pContextLinkToBeAdded* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8293-109">*pContextLinkToBeAdded* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8293-110">Objeto [**IContextLink**](icontextlink.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="b8293-110">The [**IContextLink**](icontextlink.md) object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8293-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8293-111">Return value</span></span>

<span data-ttu-id="b8293-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b8293-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b8293-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8293-113">Remarks</span></span>

<span data-ttu-id="b8293-114">Utilice este evento cuando la aplicación mantiene su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="b8293-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="b8293-115">Este evento se produce durante la fase de conciliación del análisis de tinta o en respuesta a un método del analizador de tintas que agrega un nuevo [**IContextLink**](icontextlink.md) a un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="b8293-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that adds a new [**IContextLink**](icontextlink.md) to an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="b8293-116">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b8293-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8293-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8293-117">Requirements</span></span>



| <span data-ttu-id="b8293-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8293-118">Requirement</span></span> | <span data-ttu-id="b8293-119">Value</span><span class="sxs-lookup"><span data-stu-id="b8293-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8293-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8293-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b8293-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b8293-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b8293-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8293-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b8293-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b8293-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b8293-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8293-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8293-125"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b8293-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b8293-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8293-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8293-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8293-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b8293-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8293-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8293-129">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="b8293-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="b8293-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b8293-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b8293-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="b8293-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b8293-132">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="b8293-132">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="b8293-133">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="b8293-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="b8293-134">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="b8293-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="b8293-135">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="b8293-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




