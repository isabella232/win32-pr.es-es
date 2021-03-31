---
description: Expone métodos y propiedades para una región que representa un área de un documento.
ms.assetid: ee823a9e-a144-4394-847e-abf390fb839a
title: Interfaz IAnalysisRegion (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c9c5e7653790e193c03b1cf4e0c489ea39c3eec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810045"
---
# <a name="ianalysisregion-interface"></a><span data-ttu-id="6c12e-103">Interfaz IAnalysisRegion</span><span class="sxs-lookup"><span data-stu-id="6c12e-103">IAnalysisRegion interface</span></span>

<span data-ttu-id="6c12e-104">Expone métodos y propiedades para una región que representa un área de un documento.</span><span class="sxs-lookup"><span data-stu-id="6c12e-104">Exposes methods and properties for a region that represents an area of a document.</span></span>

## <a name="members"></a><span data-ttu-id="6c12e-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c12e-105">Members</span></span>

<span data-ttu-id="6c12e-106">La interfaz **IAnalysisRegion** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6c12e-106">The **IAnalysisRegion** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6c12e-107">**IAnalysisRegion** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6c12e-107">**IAnalysisRegion** also has these types of members:</span></span>

-   [<span data-ttu-id="6c12e-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="6c12e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6c12e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="6c12e-109">Methods</span></span>

<span data-ttu-id="6c12e-110">La interfaz **IAnalysisRegion** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6c12e-110">The **IAnalysisRegion** interface has these methods.</span></span>



| <span data-ttu-id="6c12e-111">Método</span><span class="sxs-lookup"><span data-stu-id="6c12e-111">Method</span></span>                                                           | <span data-ttu-id="6c12e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c12e-112">Description</span></span>                                                                                                                                    |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c12e-113">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="6c12e-113">**Clone**</span></span>](ianalysisregion-clone.md)                           | <span data-ttu-id="6c12e-114">Crea una copia de **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="6c12e-114">Creates a copy of the **IAnalysisRegion**.</span></span><br/>                                                                                          |
| [<span data-ttu-id="6c12e-115">**ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="6c12e-115">**ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)     | <span data-ttu-id="6c12e-116">Restringe el área del **IAnalysisRegion** a la parte de su área que no forma una intersección con el rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="6c12e-116">Restricts the area of the **IAnalysisRegion** to the portion of its area that does not intersect the specified rectangle.</span></span><br/>           |
| [<span data-ttu-id="6c12e-117">**ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="6c12e-117">**ExcludeRegion**</span></span>](ianalysisregion-excluderegion.md)           | <span data-ttu-id="6c12e-118">Restringe el área del **IAnalysisRegion** a la parte de su área que no forma una intersección con el **IAnalysisRegion** especificado.</span><span class="sxs-lookup"><span data-stu-id="6c12e-118">Restricts the area of the **IAnalysisRegion** to the portion of its area that does not intersect the specified **IAnalysisRegion**.</span></span><br/> |
| [<span data-ttu-id="6c12e-119">**GetBounds**</span><span class="sxs-lookup"><span data-stu-id="6c12e-119">**GetBounds**</span></span>](ianalysisregion-getbounds.md)                   | <span data-ttu-id="6c12e-120">Recupera el rectángulo delimitador de **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="6c12e-120">Retrieves the bounding rectangle of the **IAnalysisRegion**.</span></span><br/>                                                                        |
| [<span data-ttu-id="6c12e-121">**GetRegionScans**</span><span class="sxs-lookup"><span data-stu-id="6c12e-121">**GetRegionScans**</span></span>](ianalysisregion-getregionscans.md)         | <span data-ttu-id="6c12e-122">Recupera una matriz de rectángulos que define el área de **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="6c12e-122">Retrieves an array of rectangles that defines the area of the **IAnalysisRegion**.</span></span><br/>                                                  |
| [<span data-ttu-id="6c12e-123">**IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="6c12e-123">**IntersectRectangle**</span></span>](ianalysisregion-intersectrectangle.md) | <span data-ttu-id="6c12e-124">Restringe el área de este **IAnalysisRegion** al área creada por su intersección con el rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="6c12e-124">Restricts the area of this **IAnalysisRegion** to the area created by its intersection with the specified rectangle.</span></span><br/>                |
| [<span data-ttu-id="6c12e-125">**IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="6c12e-125">**IntersectRegion**</span></span>](ianalysisregion-intersectregion.md)       | <span data-ttu-id="6c12e-126">Restringe el área de **IAnalysisRegion** al área creada por su intersección con el **IAnalysisRegion** especificado.</span><span class="sxs-lookup"><span data-stu-id="6c12e-126">Restricts the area of the **IAnalysisRegion** to the area created by its intersection with the specified **IAnalysisRegion**.</span></span><br/>       |
| [<span data-ttu-id="6c12e-127">**IntersectsWith**</span><span class="sxs-lookup"><span data-stu-id="6c12e-127">**IntersectsWith**</span></span>](ianalysisregion-intersectswith.md)         | <span data-ttu-id="6c12e-128">Determina si el área del **IAnalysisRegion** se corta con el rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="6c12e-128">Determines whether the area of the **IAnalysisRegion** intersects with the specified rectangle.</span></span><br/>                                     |
| [<span data-ttu-id="6c12e-129">**Vacío**</span><span class="sxs-lookup"><span data-stu-id="6c12e-129">**IsEmpty**</span></span>](ianalysisregion-isempty.md)                       | <span data-ttu-id="6c12e-130">Recupera un valor que indica si **IAnalysisRegion** representa una región vacía.</span><span class="sxs-lookup"><span data-stu-id="6c12e-130">Retrieves a value indicating whether the **IAnalysisRegion** represents an empty region.</span></span><br/>                                            |
| [<span data-ttu-id="6c12e-131">**IsInfinite**</span><span class="sxs-lookup"><span data-stu-id="6c12e-131">**IsInfinite**</span></span>](ianalysisregion-isinfinite.md)                 | <span data-ttu-id="6c12e-132">Recupera un valor que indica si **IAnalysisRegion** representa una región infinita.</span><span class="sxs-lookup"><span data-stu-id="6c12e-132">Retrieves a value indicating whether the **IAnalysisRegion** represents an infinite region.</span></span><br/>                                         |
| [<span data-ttu-id="6c12e-133">**MakeEmpty**</span><span class="sxs-lookup"><span data-stu-id="6c12e-133">**MakeEmpty**</span></span>](ianalysisregion-makeempty.md)                   | <span data-ttu-id="6c12e-134">Reduce el **IAnalysisRegion** para representar un área vacía.</span><span class="sxs-lookup"><span data-stu-id="6c12e-134">Reduces the **IAnalysisRegion** to represent an empty area.</span></span><br/>                                                                         |
| [<span data-ttu-id="6c12e-135">**MakeInfinite**</span><span class="sxs-lookup"><span data-stu-id="6c12e-135">**MakeInfinite**</span></span>](ianalysisregion-makeinfinite.md)             | <span data-ttu-id="6c12e-136">Expande el **IAnalysisRegion** para representar un área infinita.</span><span class="sxs-lookup"><span data-stu-id="6c12e-136">Expands the **IAnalysisRegion** to represent an infinite area.</span></span><br/>                                                                      |
| [<span data-ttu-id="6c12e-137">**UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="6c12e-137">**UnionRectangle**</span></span>](ianalysisregion-unionrectangle.md)         | <span data-ttu-id="6c12e-138">Expande el área de este **IAnalysisRegion** al área creada por su unión con el rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="6c12e-138">Expands the area of this **IAnalysisRegion** to the area created by its union with the specified rectangle.</span></span><br/>                         |
| [<span data-ttu-id="6c12e-139">**UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="6c12e-139">**UnionRegion**</span></span>](ianalysisregion-unionregion.md)               | <span data-ttu-id="6c12e-140">Expande el área de este **IAnalysisRegion** al área creada por su unión con el **IAnalysisRegion** especificado.</span><span class="sxs-lookup"><span data-stu-id="6c12e-140">Expands the area of this **IAnalysisRegion** to the area created by its union with the specified **IAnalysisRegion**.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="6c12e-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c12e-141">Remarks</span></span>

<span data-ttu-id="6c12e-142">Esta interfaz representa un área que se construye a partir de regiones rectangulares.</span><span class="sxs-lookup"><span data-stu-id="6c12e-142">This interface represents an area that is constructed from rectangular regions.</span></span> <span data-ttu-id="6c12e-143">[**IInkAnalyzer**](iinkanalyzer.md) devuelve o interpreta las coordenadas de un área en el espacio de coordenadas en el que recibe los datos del trazo.</span><span class="sxs-lookup"><span data-stu-id="6c12e-143">The [**IInkAnalyzer**](iinkanalyzer.md) returns or interprets an area's coordinates within the coordinate space in which it receives stroke data.</span></span>

<span data-ttu-id="6c12e-144">Para obtener los límites actuales del **IAnalysisRegion**, use el método [**IAnalysisRegion:: GetBounds**](ianalysisregion-getbounds.md) o [**IAnalysisRegion:: GetRegionScans**](ianalysisregion-getregionscans.md).</span><span class="sxs-lookup"><span data-stu-id="6c12e-144">To get the current bounds of the **IAnalysisRegion**, use [**IAnalysisRegion::GetBounds Method**](ianalysisregion-getbounds.md) or [**IAnalysisRegion::GetRegionScans Method**](ianalysisregion-getregionscans.md).</span></span>

<span data-ttu-id="6c12e-145">Para modificar el área de un **IAnalysisRegion** existente, use los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="6c12e-145">To modify the area of an existing **IAnalysisRegion**, use the following methods.</span></span>

-   [<span data-ttu-id="6c12e-146">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="6c12e-146">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
-   [<span data-ttu-id="6c12e-147">**IAnalysisRegion:: ExcludeRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="6c12e-147">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
-   [<span data-ttu-id="6c12e-148">**IAnalysisRegion:: IntersectRectangle (método)**</span><span class="sxs-lookup"><span data-stu-id="6c12e-148">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
-   [<span data-ttu-id="6c12e-149">**IAnalysisRegion:: IntersectRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="6c12e-149">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
-   [<span data-ttu-id="6c12e-150">**IAnalysisRegion:: MakeEmpty (método)**</span><span class="sxs-lookup"><span data-stu-id="6c12e-150">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
-   [<span data-ttu-id="6c12e-151">**IAnalysisRegion:: MakeInfinite (método)**</span><span class="sxs-lookup"><span data-stu-id="6c12e-151">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
-   [<span data-ttu-id="6c12e-152">**IAnalysisRegion:: UnionRectangle (método)**</span><span class="sxs-lookup"><span data-stu-id="6c12e-152">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
-   [<span data-ttu-id="6c12e-153">**IAnalysisRegion:: UnionRegion (método)**</span><span class="sxs-lookup"><span data-stu-id="6c12e-153">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)

<span data-ttu-id="6c12e-154">Esta interfaz es equivalente a la clase System. Windows. Ink. AnalysisCore. AnalysisRegionBase en el .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="6c12e-154">This interface is equivalent to the System.Windows.Ink.AnalysisCore.AnalysisRegionBase class in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c12e-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c12e-155">Requirements</span></span>



| <span data-ttu-id="6c12e-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c12e-156">Requirement</span></span> | <span data-ttu-id="6c12e-157">Value</span><span class="sxs-lookup"><span data-stu-id="6c12e-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c12e-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c12e-158">Minimum supported client</span></span><br/> | <span data-ttu-id="6c12e-159">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6c12e-159">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6c12e-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c12e-160">Minimum supported server</span></span><br/> | <span data-ttu-id="6c12e-161">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6c12e-161">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6c12e-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c12e-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c12e-163"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6c12e-163"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6c12e-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c12e-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c12e-165"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c12e-165"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6c12e-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c12e-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c12e-167">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="6c12e-167">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="6c12e-168">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="6c12e-168">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

