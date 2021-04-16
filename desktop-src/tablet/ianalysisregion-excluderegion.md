---
description: Restringe el área del IAnalysisRegion a la parte de su área que no forma una intersección con el IAnalysisRegion especificado.
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: 'IAnalysisRegion:: ExcludeRegion (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13324d872a76a9184e6ea67b227dbd7444684bb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542102"
---
# <a name="ianalysisregionexcluderegion-method"></a><span data-ttu-id="4e74b-103">IAnalysisRegion:: ExcludeRegion (método)</span><span class="sxs-lookup"><span data-stu-id="4e74b-103">IAnalysisRegion::ExcludeRegion method</span></span>

<span data-ttu-id="4e74b-104">Restringe el área del [**IAnalysisRegion**](ianalysisregion.md) a la parte de su área que no forma una intersección con el **IAnalysisRegion** especificado.</span><span class="sxs-lookup"><span data-stu-id="4e74b-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the portion of its area that does not intersect the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e74b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e74b-105">Syntax</span></span>


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a><span data-ttu-id="4e74b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e74b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e74b-107">*pRegionToExclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e74b-107">*pRegionToExclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e74b-108">[**IAnalysisRegion**](ianalysisregion.md) que se va a excluir de este **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="4e74b-108">The [**IAnalysisRegion**](ianalysisregion.md) to exclude from this **IAnalysisRegion**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e74b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e74b-109">Return value</span></span>

<span data-ttu-id="4e74b-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4e74b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4e74b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e74b-111">Remarks</span></span>

<span data-ttu-id="4e74b-112">Si las dos áreas no forman una intersección, este [**IAnalysisRegion**](ianalysisregion.md) no cambia.</span><span class="sxs-lookup"><span data-stu-id="4e74b-112">If the two areas do not intersect, this [**IAnalysisRegion**](ianalysisregion.md) is unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e74b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e74b-113">Requirements</span></span>



| <span data-ttu-id="4e74b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e74b-114">Requirement</span></span> | <span data-ttu-id="4e74b-115">Value</span><span class="sxs-lookup"><span data-stu-id="4e74b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e74b-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e74b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4e74b-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4e74b-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4e74b-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e74b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4e74b-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4e74b-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4e74b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e74b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e74b-121"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4e74b-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4e74b-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e74b-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e74b-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e74b-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4e74b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e74b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e74b-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="4e74b-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="4e74b-126">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="4e74b-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="4e74b-127">**IAnalysisRegion:: IntersectRectangle (método)**</span><span class="sxs-lookup"><span data-stu-id="4e74b-127">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="4e74b-128">**IAnalysisRegion:: IntersectRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="4e74b-128">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="4e74b-129">**IAnalysisRegion:: UnionRectangle (método)**</span><span class="sxs-lookup"><span data-stu-id="4e74b-129">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="4e74b-130">**IAnalysisRegion:: UnionRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="4e74b-130">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="4e74b-131">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="4e74b-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




