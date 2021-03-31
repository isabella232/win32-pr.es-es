---
description: Quita los trazos especificados de IInkAnalyzer.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: 'IInkAnalyzer:: RemoveStrokes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 00f065e01f9a4ff1459988d76fc9393ba24aa894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154412"
---
# <a name="iinkanalyzerremovestrokes-method"></a><span data-ttu-id="729d2-103">IInkAnalyzer:: RemoveStrokes (método)</span><span class="sxs-lookup"><span data-stu-id="729d2-103">IInkAnalyzer::RemoveStrokes method</span></span>

<span data-ttu-id="729d2-104">Quita los trazos especificados de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="729d2-104">Removes the specified strokes from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="729d2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="729d2-105">Syntax</span></span>


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a><span data-ttu-id="729d2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="729d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="729d2-107">*ulStrokeIdCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="729d2-107">*ulStrokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="729d2-108">Número de identificadores de trazo en *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="729d2-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="729d2-109">*plStrokes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="729d2-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="729d2-110">Los identificadores de los trazos que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="729d2-110">The identifiers for the strokes to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="729d2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="729d2-111">Return value</span></span>

<span data-ttu-id="729d2-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="729d2-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="729d2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="729d2-113">Remarks</span></span>

<span data-ttu-id="729d2-114">Este método quita los datos de paquete de y las referencias a los trazos especificados de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="729d2-114">This method removes the packet data for and references to the specified strokes from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="729d2-115">Este método quita los trazos del nodo de contexto hoja que hace referencia a los trazos.</span><span class="sxs-lookup"><span data-stu-id="729d2-115">This method removes the strokes from the leaf context node that references the strokes.</span></span> <span data-ttu-id="729d2-116">Si alguna [**IContextNode**](icontextnode.md) ya no hace referencia a ningún trazo, este método elimina los objetos **IContextNode** y **IContextNode** antecesor que ya no tienen ningún nodo secundario.</span><span class="sxs-lookup"><span data-stu-id="729d2-116">If any [**IContextNode**](icontextnode.md) no longer references any strokes, this method deletes the **IContextNode** and any ancestor **IContextNode** objects that no longer have any child nodes.</span></span>

<span data-ttu-id="729d2-117">Después de que este método quita los trazos de [**IContextNode**](icontextnode.md), actualiza la región desfasada del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IInkAnalyzer:: GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) para incluir el rectángulo de selección de los trazos que se han quitado.</span><span class="sxs-lookup"><span data-stu-id="729d2-117">After this method removes the strokes from the [**IContextNode**](icontextnode.md), it updates the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) to include the bounding box of the removed strokes.</span></span>

<span data-ttu-id="729d2-118">Si un trazo identificado en *plStrokes* no está asociado a [**IInkAnalyzer**](iinkanalyzer.md), este método omite el identificador.</span><span class="sxs-lookup"><span data-stu-id="729d2-118">If a stroke identified in *plStrokes* is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="729d2-119">Si ninguno de los trazos identificados en *plStrokes* están asociados al analizador de tinta, este método devuelve sin actualizar [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="729d2-119">If none of the strokes identified in *plStrokes* are associated with the ink analyzer, this method returns without updating the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="729d2-120">Este método devuelve y el código de error cuando *plStrokes* es NULL.</span><span class="sxs-lookup"><span data-stu-id="729d2-120">This method returns and error code when *plStrokes* is null.</span></span>

## <a name="requirements"></a><span data-ttu-id="729d2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="729d2-121">Requirements</span></span>



| <span data-ttu-id="729d2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="729d2-122">Requirement</span></span> | <span data-ttu-id="729d2-123">Value</span><span class="sxs-lookup"><span data-stu-id="729d2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="729d2-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="729d2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="729d2-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="729d2-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="729d2-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="729d2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="729d2-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="729d2-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="729d2-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="729d2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="729d2-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="729d2-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="729d2-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="729d2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="729d2-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="729d2-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="729d2-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="729d2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="729d2-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="729d2-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="729d2-134">**IInkAnalyzer:: AddStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="729d2-134">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="729d2-135">**IInkAnalyzer:: AddStrokeForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="729d2-135">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="729d2-136">**IInkAnalyzer:: AddStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="729d2-136">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="729d2-137">**IInkAnalyzer:: AddStrokesForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="729d2-137">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="729d2-138">**IInkAnalyzer:: RemoveStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="729d2-138">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="729d2-139">**IInkAnalyzer:: GetDirtyRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="729d2-139">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="729d2-140">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="729d2-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




