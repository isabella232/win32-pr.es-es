---
description: Cambia el tipo de los trazos especificados.
ms.assetid: 8d954a7d-c987-41cf-9933-b2e6bacc9489
title: 'IInkAnalyzer:: SetStrokesType (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de3f4e56b24226c2f74c6572561082c1d00afc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715201"
---
# <a name="iinkanalyzersetstrokestype-method"></a><span data-ttu-id="b6e5e-103">IInkAnalyzer:: SetStrokesType (método)</span><span class="sxs-lookup"><span data-stu-id="b6e5e-103">IInkAnalyzer::SetStrokesType method</span></span>

<span data-ttu-id="b6e5e-104">Cambia el tipo de los trazos especificados.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-104">Changes the type of the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6e5e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6e5e-105">Syntax</span></span>


```C++
HRESULT SetStrokesType(
  [in] ULONG      strokeIdCount,
  [in] LONG       *plStrokes,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="b6e5e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6e5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6e5e-107">*strokeIdCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b6e5e-107">*strokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6e5e-108">Número de identificadores de trazo en *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="b6e5e-109">*plStrokes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b6e5e-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6e5e-110">Una matriz que contiene los identificadores de trazo de los trazos a los que se asigna *StrokeType*.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-110">An array containing the stroke identifiers of the strokes to which to assign *StrokeType*.</span></span>

</dd> <dt>

<span data-ttu-id="b6e5e-111">*StrokeType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b6e5e-111">*StrokeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6e5e-112">Valor de [**StrokeType**](stroketype.md) que se va a asignar a los trazos.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-112">The [**StrokeType**](stroketype.md) value to assign to the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6e5e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6e5e-113">Return value</span></span>

<span data-ttu-id="b6e5e-114">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b6e5e-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b6e5e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6e5e-115">Remarks</span></span>

<span data-ttu-id="b6e5e-116">Si el tipo del trazo es el valor de [**StrokeType**](stroketype.md) **StrokeType sin \_ clasificar**, el [**IInkAnalyzer**](iinkanalyzer.md) clasifica el trazo durante el análisis de la tinta.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-116">If the stroke's type is the [**StrokeType**](stroketype.md) value **StrokeType\_Unclassified**, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="b6e5e-117">De lo contrario, **IInkAnalyzer** usa el tipo establecido en el trazo.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-117">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="b6e5e-118">[**IInkAnalyzer**](iinkanalyzer.md) no establece el valor de tipo de trazo como parte del análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-118">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="b6e5e-119">Para especificar o cambiar el tipo de trazo, use el método [**IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) o **IInkAnalyzer:: SetStrokesType**.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-119">To specify or change the stroke type, use [**IInkAnalyzer::SetStrokeType Method**](iinkanalyzer-setstroketype.md) or **IInkAnalyzer::SetStrokesType Method**.</span></span>

<span data-ttu-id="b6e5e-120">Si un trazo está asociado a un [**IContextNode**](icontextnode.md) que no es un nodo de tinta sin clasificar (vea [**IContextNode:: GetType**](icontextnode-gettype.md)), este método mueve el trazo a un nodo de tinta sin clasificar que contiene trazos del mismo idioma.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-120">If a stroke is associated with an [**IContextNode**](icontextnode.md) that is not an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)), this method moves the stroke to an unclassified ink node that contains strokes of the same language.</span></span> <span data-ttu-id="b6e5e-121">Si no existe tal nodo de contexto, este método crea un nuevo nodo de entrada sin clasificar y le agrega el trazo.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-121">If no such context node exists, this method creates a new unclassified ink node and adds the stroke to it.</span></span> <span data-ttu-id="b6e5e-122">Un nodo de tinta sin clasificar es un **IContextNode** de tipo UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-122">An unclassified ink node is an **IContextNode** that is of type UnclassifiedInk.</span></span>

<span data-ttu-id="b6e5e-123">Si este método mueve un trazo desde un [**IContextNode**](icontextnode.md) que no es un nodo de tinta no clasificado, este método también agrega el rectángulo de selección del trazo a la región desfasada del analizador de tinta (vea el [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="b6e5e-123">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="b6e5e-124">Este método no mueve un trazo si el parámetro *StrokeType* coincide con el tipo actual del trazo.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-124">This method does not move a stroke if the *StrokeType* parameter matches the stroke's current type.</span></span>

<span data-ttu-id="b6e5e-125">Si un trazo identificado en *strokeIds* no está asociado a [**IInkAnalyzer**](iinkanalyzer.md), este método omite el identificador.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-125">If a stroke identified in *strokeIds* is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="b6e5e-126">Si ninguno de los trazos especificados identifica un trazo asociado al [**IInkAnalyzer**](iinkanalyzer.md), este método devuelve sin actualizar **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-126">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="b6e5e-127">Al establecer el tipo de trazo en los trazos que están asociados a un ContextNode que tiene NodeTypeAndProperties confirmada, se producirá una excepción InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-127">Setting the stroke type on strokes that are associated with a ContextNode that has NodeTypeAndProperties confirmed will raise an InvalidOperationException.</span></span>

<span data-ttu-id="b6e5e-128">Este método devuelve un código de error cuando *plStrokes* es **null**.</span><span class="sxs-lookup"><span data-stu-id="b6e5e-128">This method returns an error code when *plStrokes* is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6e5e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6e5e-129">Requirements</span></span>



| <span data-ttu-id="b6e5e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6e5e-130">Requirement</span></span> | <span data-ttu-id="b6e5e-131">Value</span><span class="sxs-lookup"><span data-stu-id="b6e5e-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e5e-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6e5e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b6e5e-133">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b6e5e-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b6e5e-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6e5e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b6e5e-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b6e5e-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b6e5e-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6e5e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6e5e-137"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b6e5e-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b6e5e-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b6e5e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6e5e-139"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6e5e-139"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b6e5e-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6e5e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6e5e-141">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b6e5e-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b6e5e-142">**IInkAnalyzer:: GetStrokeType (método)**</span><span class="sxs-lookup"><span data-stu-id="b6e5e-142">**IInkAnalyzer::GetStrokeType Method**</span></span>](iinkanalyzer-getstroketype.md)
</dt> <dt>

[<span data-ttu-id="b6e5e-143">**IInkAnalyzer:: SetStrokeType (método)**</span><span class="sxs-lookup"><span data-stu-id="b6e5e-143">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> <dt>

[<span data-ttu-id="b6e5e-144">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="b6e5e-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




