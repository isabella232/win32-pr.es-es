---
description: Quita el trazo especificado de IInkAnalyzer.
ms.assetid: e182ae35-854e-401d-8e26-aee645c05430
title: 'IInkAnalyzer:: RemoveStroke (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 03952e6e14679c53f7b65f21463fc0457f302b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542006"
---
# <a name="iinkanalyzerremovestroke-method"></a><span data-ttu-id="c4942-103">IInkAnalyzer:: RemoveStroke (método)</span><span class="sxs-lookup"><span data-stu-id="c4942-103">IInkAnalyzer::RemoveStroke method</span></span>

<span data-ttu-id="c4942-104">Quita el trazo especificado de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="c4942-104">Removes the specified stroke from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4942-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4942-105">Syntax</span></span>


```C++
HRESULT RemoveStroke(
  [in] LONG *plStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="c4942-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4942-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4942-107">*plStrokeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4942-107">*plStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4942-108">Identificador del trazo.</span><span class="sxs-lookup"><span data-stu-id="c4942-108">The stroke identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4942-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4942-109">Return value</span></span>

<span data-ttu-id="c4942-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c4942-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c4942-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4942-111">Remarks</span></span>

<span data-ttu-id="c4942-112">Este método quita del [**IInkAnalyzer**](iinkanalyzer.md)los datos del paquete y las referencias a, el trazo especificado.</span><span class="sxs-lookup"><span data-stu-id="c4942-112">This method removes the packet data for, and references to, the specified stroke from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="c4942-113">Este método quita el trazo del nodo de contexto hoja que hace referencia al trazo.</span><span class="sxs-lookup"><span data-stu-id="c4942-113">This method removes the stroke from the leaf context node that references the stroke.</span></span> <span data-ttu-id="c4942-114">Si [**IContextNode**](icontextnode.md) ya no hace referencia a ningún trazo, este método elimina los objetos **IContextNode** y **IContextNode** antecesor que ya no tienen ningún nodo secundario.</span><span class="sxs-lookup"><span data-stu-id="c4942-114">If the [**IContextNode**](icontextnode.md) no longer references any strokes, this method deletes the **IContextNode** and any ancestor **IContextNode** objects that no longer have any child nodes.</span></span>

<span data-ttu-id="c4942-115">Después de que este método quita el trazo del [**IContextNode**](icontextnode.md), actualiza la región desfasada del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IInkAnalyzer:: GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) para incluir el rectángulo de selección del trazo que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="c4942-115">After this method removes the stroke from the [**IContextNode**](icontextnode.md), it updates the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) to include the bounding box of the removed stroke.</span></span>

<span data-ttu-id="c4942-116">Si *plStrokeId* no identifica un trazo asociado a [**IInkAnalyzer**](iinkanalyzer.md), este método devuelve sin actualizar el analizador de tinta.</span><span class="sxs-lookup"><span data-stu-id="c4942-116">If *plStrokeId* does not identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the ink analyzer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4942-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4942-117">Requirements</span></span>



| <span data-ttu-id="c4942-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4942-118">Requirement</span></span> | <span data-ttu-id="c4942-119">Value</span><span class="sxs-lookup"><span data-stu-id="c4942-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4942-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4942-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c4942-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c4942-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c4942-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4942-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c4942-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c4942-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c4942-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4942-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4942-125"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c4942-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c4942-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c4942-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4942-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4942-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c4942-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4942-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4942-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="c4942-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c4942-130">**IInkAnalyzer:: AddStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="c4942-130">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="c4942-131">**IInkAnalyzer:: AddStrokeForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="c4942-131">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="c4942-132">**IInkAnalyzer:: AddStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="c4942-132">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="c4942-133">**IInkAnalyzer:: AddStrokesForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="c4942-133">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="c4942-134">**IInkAnalyzer:: RemoveStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="c4942-134">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="c4942-135">**IInkAnalyzer:: GetDirtyRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="c4942-135">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="c4942-136">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="c4942-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




