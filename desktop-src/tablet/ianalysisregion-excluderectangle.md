---
description: Restringe el área del IAnalysisRegion a la parte de su área que no forma una intersección con el rectángulo especificado.
ms.assetid: a35b8bfc-a87a-4e9a-908f-2b13a128d222
title: 'IAnalysisRegion:: ExcludeRectangle (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 684ce2ceb57c7954c732fb2816aca50fcbae5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715244"
---
# <a name="ianalysisregionexcluderectangle-method"></a><span data-ttu-id="297e9-103">IAnalysisRegion:: ExcludeRectangle (método)</span><span class="sxs-lookup"><span data-stu-id="297e9-103">IAnalysisRegion::ExcludeRectangle method</span></span>

<span data-ttu-id="297e9-104">Restringe el área del [**IAnalysisRegion**](ianalysisregion.md) a la parte de su área que no forma una intersección con el rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="297e9-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the portion of its area that does not intersect the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="297e9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="297e9-105">Syntax</span></span>


```C++
HRESULT ExcludeRectangle(
  [in] RECT *pExcludingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="297e9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="297e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="297e9-107">*pExcludingRectangle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="297e9-107">*pExcludingRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="297e9-108">Rectángulo que se va a excluir de este [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="297e9-108">The rectangle to exclude from this [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="297e9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="297e9-109">Return value</span></span>

<span data-ttu-id="297e9-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="297e9-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="297e9-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="297e9-111">Remarks</span></span>

<span data-ttu-id="297e9-112">Las coordenadas del rectángulo están en unidades de HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="297e9-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="297e9-113">Si las dos áreas no forman una intersección, el [**IAnalysisRegion**](ianalysisregion.md) no cambia.</span><span class="sxs-lookup"><span data-stu-id="297e9-113">If the two areas do not intersect, the [**IAnalysisRegion**](ianalysisregion.md) is unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="297e9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="297e9-114">Requirements</span></span>



| <span data-ttu-id="297e9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="297e9-115">Requirement</span></span> | <span data-ttu-id="297e9-116">Value</span><span class="sxs-lookup"><span data-stu-id="297e9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="297e9-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="297e9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="297e9-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="297e9-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="297e9-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="297e9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="297e9-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="297e9-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="297e9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="297e9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="297e9-122"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="297e9-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="297e9-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="297e9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="297e9-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="297e9-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="297e9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="297e9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="297e9-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="297e9-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="297e9-127">**IAnalysisRegion:: ExcludeRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="297e9-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="297e9-128">**IAnalysisRegion:: IntersectRectangle (método)**</span><span class="sxs-lookup"><span data-stu-id="297e9-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="297e9-129">**IAnalysisRegion:: IntersectRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="297e9-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="297e9-130">**IAnalysisRegion:: UnionRectangle (método)**</span><span class="sxs-lookup"><span data-stu-id="297e9-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="297e9-131">**IAnalysisRegion:: UnionRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="297e9-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="297e9-132">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="297e9-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




