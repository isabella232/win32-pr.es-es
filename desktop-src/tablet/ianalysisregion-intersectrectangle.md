---
description: Restringe el área de este IAnalysisRegion al área creada por su intersección con el rectángulo especificado.
ms.assetid: de6b565f-34c1-4551-ab92-db6bacb8608d
title: 'IAnalysisRegion:: IntersectRectangle (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4ce0e514b24aba0331d9ea604333680db1c67c8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542099"
---
# <a name="ianalysisregionintersectrectangle-method"></a><span data-ttu-id="f5bdb-103">IAnalysisRegion:: IntersectRectangle (método)</span><span class="sxs-lookup"><span data-stu-id="f5bdb-103">IAnalysisRegion::IntersectRectangle method</span></span>

<span data-ttu-id="f5bdb-104">Restringe el área de este [**IAnalysisRegion**](ianalysisregion.md) al área creada por su intersección con el rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="f5bdb-104">Restricts the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its intersection with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5bdb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5bdb-105">Syntax</span></span>


```C++
HRESULT IntersectRectangle(
  [in] RECT *pIntersectingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="f5bdb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5bdb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5bdb-107">*pIntersectingRectangle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f5bdb-107">*pIntersectingRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5bdb-108">Puntero al rectángulo con el que se va a formar una intersección en las coordenadas del espacio de tinta.</span><span class="sxs-lookup"><span data-stu-id="f5bdb-108">A pointer to the rectangle with which to intersect, in ink-space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5bdb-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5bdb-109">Return value</span></span>

<span data-ttu-id="f5bdb-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f5bdb-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5bdb-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5bdb-111">Remarks</span></span>

<span data-ttu-id="f5bdb-112">Las coordenadas del rectángulo están en unidades de HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="f5bdb-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="f5bdb-113">Si las dos áreas no forman una intersección, el área nueva está vacía.</span><span class="sxs-lookup"><span data-stu-id="f5bdb-113">If the two areas do not intersect, the new area is empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5bdb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5bdb-114">Requirements</span></span>



| <span data-ttu-id="f5bdb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5bdb-115">Requirement</span></span> | <span data-ttu-id="f5bdb-116">Value</span><span class="sxs-lookup"><span data-stu-id="f5bdb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5bdb-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5bdb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f5bdb-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f5bdb-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f5bdb-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5bdb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f5bdb-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f5bdb-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f5bdb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5bdb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5bdb-122"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f5bdb-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f5bdb-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f5bdb-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5bdb-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5bdb-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f5bdb-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5bdb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5bdb-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="f5bdb-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="f5bdb-127">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="f5bdb-127">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="f5bdb-128">**IAnalysisRegion:: ExcludeRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="f5bdb-128">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="f5bdb-129">**IAnalysisRegion:: IntersectRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="f5bdb-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="f5bdb-130">**IAnalysisRegion:: UnionRectangle (método)**</span><span class="sxs-lookup"><span data-stu-id="f5bdb-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="f5bdb-131">**IAnalysisRegion:: UnionRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="f5bdb-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="f5bdb-132">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="f5bdb-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




