---
description: Expande el área de este IAnalysisRegion al área creada por su unión con el rectángulo especificado.
ms.assetid: 9b12f509-4f6a-43b0-9639-bef060fd6d50
title: 'IAnalysisRegion:: UnionRectangle (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3a28a60eae95641225dd9c01791d89a9c38ada82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696546"
---
# <a name="ianalysisregionunionrectangle-method"></a><span data-ttu-id="85f5c-103">IAnalysisRegion:: UnionRectangle (método)</span><span class="sxs-lookup"><span data-stu-id="85f5c-103">IAnalysisRegion::UnionRectangle method</span></span>

<span data-ttu-id="85f5c-104">Expande el área de este [**IAnalysisRegion**](ianalysisregion.md) al área creada por su unión con el rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="85f5c-104">Expands the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its union with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="85f5c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85f5c-105">Syntax</span></span>


```C++
HRESULT UnionRectangle(
  [in] RECT *pRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="85f5c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85f5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85f5c-107">*pRectangle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85f5c-107">*pRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85f5c-108">Puntero al rectángulo con el que se va a combinar, en coordenadas de espacio de tinta.</span><span class="sxs-lookup"><span data-stu-id="85f5c-108">A pointer to the rectangle with which to combine, in ink-space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85f5c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85f5c-109">Return value</span></span>

<span data-ttu-id="85f5c-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="85f5c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="85f5c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85f5c-111">Remarks</span></span>

<span data-ttu-id="85f5c-112">Las coordenadas del rectángulo están en unidades de HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="85f5c-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="85f5c-113">Si alguna de las áreas es infinita, la nueva área también es infinita.</span><span class="sxs-lookup"><span data-stu-id="85f5c-113">If either area is infinite, the new area is also infinite.</span></span>

## <a name="requirements"></a><span data-ttu-id="85f5c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85f5c-114">Requirements</span></span>



| <span data-ttu-id="85f5c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="85f5c-115">Requirement</span></span> | <span data-ttu-id="85f5c-116">Value</span><span class="sxs-lookup"><span data-stu-id="85f5c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85f5c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85f5c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="85f5c-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="85f5c-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="85f5c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85f5c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="85f5c-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="85f5c-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="85f5c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85f5c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="85f5c-122"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="85f5c-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="85f5c-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85f5c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85f5c-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85f5c-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="85f5c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="85f5c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85f5c-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="85f5c-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="85f5c-127">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="85f5c-127">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="85f5c-128">**IAnalysisRegion:: ExcludeRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="85f5c-128">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="85f5c-129">**IAnalysisRegion:: IntersectRectangle (método)**</span><span class="sxs-lookup"><span data-stu-id="85f5c-129">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="85f5c-130">**IAnalysisRegion:: IntersectRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="85f5c-130">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="85f5c-131">**IAnalysisRegion:: UnionRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="85f5c-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="85f5c-132">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="85f5c-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




