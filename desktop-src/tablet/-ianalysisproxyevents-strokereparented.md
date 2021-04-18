---
description: Se produce cuando el IInkAnalyzer mueve un trazo de un objeto IContextNode a otro.
ms.assetid: a90214af-c3ea-4e2a-94b4-bb5746a2b476
title: 'Evento _IAnalysisProxyEvents:: StrokeReparented (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.StrokeReparented
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a587acb6534641d5d64981ab25247b0e23e4f347
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707589"
---
# <a name="_ianalysisproxyeventsstrokereparented-event"></a><span data-ttu-id="25531-103">\_Evento IAnalysisProxyEvents:: StrokeReparented</span><span class="sxs-lookup"><span data-stu-id="25531-103">\_IAnalysisProxyEvents::StrokeReparented event</span></span>

<span data-ttu-id="25531-104">Se produce cuando el [**IInkAnalyzer**](iinkanalyzer.md) mueve un trazo de un objeto [**IContextNode**](icontextnode.md) a otro.</span><span class="sxs-lookup"><span data-stu-id="25531-104">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) moves a stroke from one [**IContextNode**](icontextnode.md) object to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="25531-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25531-105">Syntax</span></span>


```C++
HRESULT StrokeReparented(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] LONG         lStrokeIdToMove,
  [in] IContextNode *pSourceContextNode,
  [in] IContextNode *pDestinationContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="25531-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25531-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25531-107">*pInkAnalyzer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="25531-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25531-108">El objeto [**IInkAnalyzer**](iinkanalyzer.md) que mueve el trazo.</span><span class="sxs-lookup"><span data-stu-id="25531-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="25531-109">*lStrokeIdToMove* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="25531-109">*lStrokeIdToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25531-110">Identificador del trazo que se va a desplace.</span><span class="sxs-lookup"><span data-stu-id="25531-110">The identifier of the stroke to move.</span></span>

</dd> <dt>

<span data-ttu-id="25531-111">*pSourceContextNode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="25531-111">*pSourceContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25531-112">Objeto [**IContextNode**](icontextnode.md) desde el que se mueve el trazo.</span><span class="sxs-lookup"><span data-stu-id="25531-112">The [**IContextNode**](icontextnode.md) object from which the stroke is moved.</span></span>

</dd> <dt>

<span data-ttu-id="25531-113">*pDestinationContextNode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="25531-113">*pDestinationContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25531-114">Objeto [**IContextNode**](icontextnode.md) al que se mueve el trazo.</span><span class="sxs-lookup"><span data-stu-id="25531-114">The [**IContextNode**](icontextnode.md) object to which the stroke is moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25531-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25531-115">Return value</span></span>

<span data-ttu-id="25531-116">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="25531-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="25531-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25531-117">Remarks</span></span>

<span data-ttu-id="25531-118">Utilice este evento cuando la aplicación mantiene su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="25531-118">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="25531-119">Este evento se produce durante la fase de conciliación del análisis de tinta o en respuesta a un método **IInkAnalyzer** que mueve los datos de trazo de un [**IContextNode**](icontextnode.md) a otro.</span><span class="sxs-lookup"><span data-stu-id="25531-119">This event occurs during the reconcile phase of ink analysis, or in response to an **IInkAnalyzer** method that moves stroke data from one [**IContextNode**](icontextnode.md) to another.</span></span>

<span data-ttu-id="25531-120">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="25531-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25531-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25531-121">Requirements</span></span>



| <span data-ttu-id="25531-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="25531-122">Requirement</span></span> | <span data-ttu-id="25531-123">Value</span><span class="sxs-lookup"><span data-stu-id="25531-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25531-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25531-124">Minimum supported client</span></span><br/> | <span data-ttu-id="25531-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="25531-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="25531-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25531-126">Minimum supported server</span></span><br/> | <span data-ttu-id="25531-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="25531-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="25531-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25531-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="25531-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="25531-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="25531-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="25531-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25531-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25531-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="25531-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="25531-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25531-133">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="25531-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="25531-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="25531-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="25531-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="25531-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="25531-136">**IInkAnalyzer:: Analyze (método)**</span><span class="sxs-lookup"><span data-stu-id="25531-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="25531-137">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="25531-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="25531-138">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="25531-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




