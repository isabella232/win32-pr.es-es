---
description: Asocia los trazos especificados a este IContextNode.
ms.assetid: 5ce8893a-da59-4cec-a349-d5ffc4f43905
title: 'IContextNode:: SetStrokes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be7fd1645af70e34c747894bc8ab4317b08e2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715227"
---
# <a name="icontextnodesetstrokes-method"></a><span data-ttu-id="d7bcb-103">IContextNode:: SetStrokes (método)</span><span class="sxs-lookup"><span data-stu-id="d7bcb-103">IContextNode::SetStrokes method</span></span>

<span data-ttu-id="d7bcb-104">Asocia los trazos especificados a este [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="d7bcb-104">Associates the specified strokes with this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7bcb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7bcb-105">Syntax</span></span>


```C++
HRESULT SetStrokes(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="d7bcb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7bcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7bcb-107">*ulStrokeIdsCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7bcb-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7bcb-108">Número de identificadores de trazo en *plStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="d7bcb-108">The number of stroke identifiers in *plStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="d7bcb-109">*plStrokeIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7bcb-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7bcb-110">Los identificadores de los trazos que se van a asociar a este [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="d7bcb-110">The identifiers of the strokes to associate with this [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7bcb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7bcb-111">Return value</span></span>

<span data-ttu-id="d7bcb-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d7bcb-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d7bcb-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7bcb-113">Remarks</span></span>

<span data-ttu-id="d7bcb-114">Este método no actualiza la región desfasada del analizador de tinta (consulte el [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="d7bcb-114">This method does not update the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="d7bcb-115">Use este método cuando la aplicación mantenga su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="d7bcb-115">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="d7bcb-116">Utilice este método para asignar datos de trazo a un nodo de contexto específico.</span><span class="sxs-lookup"><span data-stu-id="d7bcb-116">Use this method to assign stroke data to a specific context node.</span></span> <span data-ttu-id="d7bcb-117">Para obtener más información sobre cómo sincronizar los datos de la aplicación con **IInkAnalyzer**, vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d7bcb-117">For more information about synchronizing your application data with the **IInkAnalyzer**, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="d7bcb-118">Si alguno de los trazos especificados ya está asociado a [**IInkAnalyzer**](iinkanalyzer.md), este método devuelve **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="d7bcb-118">If any of the specified strokes are already associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7bcb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7bcb-119">Requirements</span></span>



| <span data-ttu-id="d7bcb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7bcb-120">Requirement</span></span> | <span data-ttu-id="d7bcb-121">Value</span><span class="sxs-lookup"><span data-stu-id="d7bcb-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7bcb-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7bcb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d7bcb-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d7bcb-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d7bcb-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7bcb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d7bcb-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d7bcb-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d7bcb-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7bcb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7bcb-127"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d7bcb-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d7bcb-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d7bcb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7bcb-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7bcb-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d7bcb-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7bcb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7bcb-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="d7bcb-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="d7bcb-132">**IInkAnalyzer:: AddStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="d7bcb-132">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="d7bcb-133">**IInkAnalyzer:: AddStrokeForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="d7bcb-133">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="d7bcb-134">**IInkAnalyzer:: AddStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="d7bcb-134">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="d7bcb-135">**IInkAnalyzer:: AddStrokesForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="d7bcb-135">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="d7bcb-136">**IInkAnalyzer:: AddStrokesToCustomRecognizer (método)**</span><span class="sxs-lookup"><span data-stu-id="d7bcb-136">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="d7bcb-137">**IInkAnalyzer:: AddStrokeToCustomRecognizer (método)**</span><span class="sxs-lookup"><span data-stu-id="d7bcb-137">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="d7bcb-138">**IInkAnalyzer:: RemoveStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="d7bcb-138">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="d7bcb-139">**IInkAnalyzer:: RemoveStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="d7bcb-139">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="d7bcb-140">**IContextNode::GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="d7bcb-140">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="d7bcb-141">**IContextNode::GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="d7bcb-141">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="d7bcb-142">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="d7bcb-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




