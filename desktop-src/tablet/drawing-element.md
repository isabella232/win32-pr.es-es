---
description: Contiene contenido clasificado por el analizador o el usuario como un dibujo.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Elemento Drawing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87c0a3d8879fb5f3146c46c9c88d83a6e658d8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432517"
---
# <a name="drawing-element"></a><span data-ttu-id="47b0e-103">Elemento Drawing</span><span class="sxs-lookup"><span data-stu-id="47b0e-103">Drawing Element</span></span>

<span data-ttu-id="47b0e-104">Contiene contenido clasificado por el analizador o el usuario como un dibujo.</span><span class="sxs-lookup"><span data-stu-id="47b0e-104">Contains content that has been classified by the analyzer or the user as a drawing.</span></span>

## <a name="definition"></a><span data-ttu-id="47b0e-105">Definición</span><span class="sxs-lookup"><span data-stu-id="47b0e-105">Definition</span></span>

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="47b0e-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="47b0e-106">Parent Elements</span></span>

[<span data-ttu-id="47b0e-107">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="47b0e-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="47b0e-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="47b0e-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="47b0e-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="47b0e-109">Child Elements</span></span>

[<span data-ttu-id="47b0e-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="47b0e-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="47b0e-111">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="47b0e-111">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="47b0e-112">**InkClass**</span><span class="sxs-lookup"><span data-stu-id="47b0e-112">**InkClass**</span></span>](inkclass-element.md)

[<span data-ttu-id="47b0e-113">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="47b0e-113">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="47b0e-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="47b0e-114">Attributes</span></span>



| <span data-ttu-id="47b0e-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="47b0e-115">Attribute</span></span>  | <span data-ttu-id="47b0e-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="47b0e-116">Type</span></span>                      | <span data-ttu-id="47b0e-117">Requerido</span><span class="sxs-lookup"><span data-stu-id="47b0e-117">Required</span></span> | <span data-ttu-id="47b0e-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="47b0e-118">Description</span></span>                                                                             | <span data-ttu-id="47b0e-119">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="47b0e-119">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="47b0e-120">**Left**</span><span class="sxs-lookup"><span data-stu-id="47b0e-120">**Left**</span></span>   | <span data-ttu-id="47b0e-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="47b0e-121">**xs:integer**</span></span>            | <span data-ttu-id="47b0e-122">Requerido</span><span class="sxs-lookup"><span data-stu-id="47b0e-122">Required</span></span> | <span data-ttu-id="47b0e-123">Distancia desde el origen hasta el punto situado más a la izquierda en el cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="47b0e-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="47b0e-124">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="47b0e-124">Any integer.</span></span>              |
| <span data-ttu-id="47b0e-125">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="47b0e-125">**Top**</span></span>    | <span data-ttu-id="47b0e-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="47b0e-126">**xs:integer**</span></span>            | <span data-ttu-id="47b0e-127">Requerido</span><span class="sxs-lookup"><span data-stu-id="47b0e-127">Required</span></span> | <span data-ttu-id="47b0e-128">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="47b0e-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="47b0e-129">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="47b0e-129">Any integer.</span></span>              |
| <span data-ttu-id="47b0e-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="47b0e-130">**Width**</span></span>  | <span data-ttu-id="47b0e-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="47b0e-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="47b0e-132">Requerido</span><span class="sxs-lookup"><span data-stu-id="47b0e-132">Required</span></span> | <span data-ttu-id="47b0e-133">Ancho del cuadro de límite para el elemento.</span><span class="sxs-lookup"><span data-stu-id="47b0e-133">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="47b0e-134">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="47b0e-134">Any non-negative integer.</span></span> |
| <span data-ttu-id="47b0e-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="47b0e-135">**Height**</span></span> | <span data-ttu-id="47b0e-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="47b0e-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="47b0e-137">Requerido</span><span class="sxs-lookup"><span data-stu-id="47b0e-137">Required</span></span> | <span data-ttu-id="47b0e-138">Alto del cuadro de límite para el elemento.</span><span class="sxs-lookup"><span data-stu-id="47b0e-138">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="47b0e-139">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="47b0e-139">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="47b0e-140">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="47b0e-140">Element Information</span></span>



|  <span data-ttu-id="47b0e-141">Elemento</span><span class="sxs-lookup"><span data-stu-id="47b0e-141">Element</span></span>     | <span data-ttu-id="47b0e-142">Value</span><span class="sxs-lookup"><span data-stu-id="47b0e-142">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="47b0e-143">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="47b0e-143">Element type</span></span> | <span data-ttu-id="47b0e-144">[**DrawingType**](drawingtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="47b0e-144">[**DrawingType**](drawingtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="47b0e-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="47b0e-145">Namespace</span></span>    | <span data-ttu-id="47b0e-146">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="47b0e-146">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="47b0e-147">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="47b0e-147">Schema name</span></span>  | <span data-ttu-id="47b0e-148">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="47b0e-148">Journal Reader</span></span>                                              |



 

 

 



