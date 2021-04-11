---
description: Cambia el tipo del trazo especificado.
ms.assetid: 1608fed1-cd6c-46c3-a35f-3d262279ec2e
title: 'IInkAnalyzer:: SetStrokeType (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8a5f77cbefb200bad973c0f2cf28fea5d3efe1da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154405"
---
# <a name="iinkanalyzersetstroketype-method"></a><span data-ttu-id="489cf-103">IInkAnalyzer:: SetStrokeType (método)</span><span class="sxs-lookup"><span data-stu-id="489cf-103">IInkAnalyzer::SetStrokeType method</span></span>

<span data-ttu-id="489cf-104">Cambia el tipo del trazo especificado.</span><span class="sxs-lookup"><span data-stu-id="489cf-104">Changes the type of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="489cf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="489cf-105">Syntax</span></span>


```C++
HRESULT SetStrokeType(
  [in] LONG       lStrokeId,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="489cf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="489cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="489cf-107">*lStrokeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="489cf-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="489cf-108">Identificador de trazo del trazo al que se va a asignar *StrokeType*.</span><span class="sxs-lookup"><span data-stu-id="489cf-108">The stroke identifier of the stroke to which to assign *StrokeType*.</span></span>

</dd> <dt>

<span data-ttu-id="489cf-109">*StrokeType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="489cf-109">*StrokeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="489cf-110">Valor de [**StrokeType**](stroketype.md) que se va a asignar al trazo.</span><span class="sxs-lookup"><span data-stu-id="489cf-110">The [**StrokeType**](stroketype.md) value to assign to the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="489cf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="489cf-111">Return value</span></span>

<span data-ttu-id="489cf-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="489cf-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="489cf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="489cf-113">Remarks</span></span>

<span data-ttu-id="489cf-114">Si el tipo del trazo es el valor de [**StrokeType**](stroketype.md) **StrokeType sin \_ clasificar**, el [**IInkAnalyzer**](iinkanalyzer.md) clasifica el trazo durante el análisis de la tinta.</span><span class="sxs-lookup"><span data-stu-id="489cf-114">If the stroke's type is the [**StrokeType**](stroketype.md) value **StrokeType\_Unclassified**, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="489cf-115">De lo contrario, **IInkAnalyzer** usa el tipo establecido en el trazo.</span><span class="sxs-lookup"><span data-stu-id="489cf-115">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="489cf-116">[**IInkAnalyzer**](iinkanalyzer.md) no establece el valor de tipo de trazo como parte del análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="489cf-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="489cf-117">Para especificar o cambiar el tipo de trazo, use el método **IInkAnalyzer:: SetStrokeType** o [**IInkAnalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md).</span><span class="sxs-lookup"><span data-stu-id="489cf-117">To specify or change the stroke type, use **IInkAnalyzer::SetStrokeType Method** or [**IInkAnalyzer::SetStrokesType Method**](iinkanalyzer-setstrokestype.md).</span></span>

<span data-ttu-id="489cf-118">Si un trazo está asociado a un [**IContextNode**](icontextnode.md) que no es un nodo de tinta sin clasificar (vea [**IContextNode:: GetType**](icontextnode-gettype.md)), este método mueve el trazo a un nodo de tinta sin clasificar que contiene trazos del mismo idioma.</span><span class="sxs-lookup"><span data-stu-id="489cf-118">If a stroke is associated with an [**IContextNode**](icontextnode.md) that is not an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)), this method moves the stroke to an unclassified ink node that contains strokes of the same language.</span></span> <span data-ttu-id="489cf-119">Si no existe tal nodo de contexto, este método crea un nuevo nodo de entrada sin clasificar y le agrega el trazo.</span><span class="sxs-lookup"><span data-stu-id="489cf-119">If no such context node exists, this method creates a new unclassified ink node and adds the stroke to it.</span></span> <span data-ttu-id="489cf-120">Un nodo de tinta sin clasificar es un **IContextNode** de tipo UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="489cf-120">An unclassified ink node is an **IContextNode** that is of type UnclassifiedInk.</span></span>

<span data-ttu-id="489cf-121">Si este método mueve un trazo desde un [**IContextNode**](icontextnode.md) que no es un nodo de tinta no clasificado, este método también agrega el rectángulo de selección del trazo a la región desfasada del analizador de tinta (vea el [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="489cf-121">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="489cf-122">Este método no mueve un trazo si el parámetro *StrokeType* coincide con el tipo actual del trazo.</span><span class="sxs-lookup"><span data-stu-id="489cf-122">This method does not move a stroke if the *StrokeType* parameter matches the stroke's current type.</span></span>

<span data-ttu-id="489cf-123">Al establecer el tipo de trazo en los trazos que están asociados a un ContextNode que tiene NodeTypeAndProperties confirmada, se producirá una excepción InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="489cf-123">Setting the stroke type on strokes that are associated with a ContextNode that has NodeTypeAndProperties confirmed will raise an InvalidOperationException.</span></span>

<span data-ttu-id="489cf-124">Si el trazo especificado no está asociado al [**IInkAnalyzer**](iinkanalyzer.md), este método devuelve sin actualizar **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="489cf-124">If the specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="489cf-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="489cf-125">Requirements</span></span>



| <span data-ttu-id="489cf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="489cf-126">Requirement</span></span> | <span data-ttu-id="489cf-127">Value</span><span class="sxs-lookup"><span data-stu-id="489cf-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="489cf-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="489cf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="489cf-129">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="489cf-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="489cf-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="489cf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="489cf-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="489cf-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="489cf-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="489cf-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="489cf-133"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="489cf-133"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="489cf-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="489cf-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="489cf-135"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="489cf-135"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="489cf-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="489cf-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="489cf-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="489cf-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="489cf-138">**IInkAnalyzer:: GetStrokeType (método)**</span><span class="sxs-lookup"><span data-stu-id="489cf-138">**IInkAnalyzer::GetStrokeType Method**</span></span>](iinkanalyzer-getstroketype.md)
</dt> <dt>

[<span data-ttu-id="489cf-139">**IInkAnalyzer:: SetStrokesType (método)**</span><span class="sxs-lookup"><span data-stu-id="489cf-139">**IInkAnalyzer::SetStrokesType Method**</span></span>](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[<span data-ttu-id="489cf-140">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="489cf-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




