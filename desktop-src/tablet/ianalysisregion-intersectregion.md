---
description: Restringe el área de IAnalysisRegion al área creada por su intersección con el IAnalysisRegion especificado.
ms.assetid: 02b3049f-ada9-4de3-a7a2-f9ff8313fbab
title: 'IAnalysisRegion:: IntersectRegion (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7ff3caad382e54f41685f6102edafdeb86b813c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715243"
---
# <a name="ianalysisregionintersectregion-method"></a><span data-ttu-id="431e1-103">IAnalysisRegion:: IntersectRegion (método)</span><span class="sxs-lookup"><span data-stu-id="431e1-103">IAnalysisRegion::IntersectRegion method</span></span>

<span data-ttu-id="431e1-104">Restringe el área de [**IAnalysisRegion**](ianalysisregion.md) al área creada por su intersección con el **IAnalysisRegion** especificado.</span><span class="sxs-lookup"><span data-stu-id="431e1-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the area created by its intersection with the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="431e1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="431e1-105">Syntax</span></span>


```C++
HRESULT IntersectRegion(
  [in] IAnalysisRegion *pRegionToIntersect
);
```



## <a name="parameters"></a><span data-ttu-id="431e1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="431e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="431e1-107">*pRegionToIntersect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="431e1-107">*pRegionToIntersect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="431e1-108">[**IAnalysisRegion**](ianalysisregion.md) con el que se va a formar una intersección.</span><span class="sxs-lookup"><span data-stu-id="431e1-108">The [**IAnalysisRegion**](ianalysisregion.md) with which to intersect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="431e1-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="431e1-109">Return value</span></span>

<span data-ttu-id="431e1-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="431e1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="431e1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="431e1-111">Remarks</span></span>

<span data-ttu-id="431e1-112">Si las dos áreas no forman una intersección, el área nueva está vacía.</span><span class="sxs-lookup"><span data-stu-id="431e1-112">If the two areas do not intersect, the new area is empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="431e1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="431e1-113">Requirements</span></span>



| <span data-ttu-id="431e1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="431e1-114">Requirement</span></span> | <span data-ttu-id="431e1-115">Value</span><span class="sxs-lookup"><span data-stu-id="431e1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="431e1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="431e1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="431e1-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="431e1-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="431e1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="431e1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="431e1-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="431e1-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="431e1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="431e1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="431e1-121"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="431e1-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="431e1-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="431e1-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="431e1-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="431e1-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="431e1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="431e1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="431e1-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="431e1-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="431e1-126">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="431e1-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="431e1-127">**IAnalysisRegion:: ExcludeRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="431e1-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="431e1-128">**IAnalysisRegion:: IntersectRectangle (método)**</span><span class="sxs-lookup"><span data-stu-id="431e1-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="431e1-129">**IAnalysisRegion:: UnionRectangle (método)**</span><span class="sxs-lookup"><span data-stu-id="431e1-129">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="431e1-130">**IAnalysisRegion:: UnionRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="431e1-130">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="431e1-131">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="431e1-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




