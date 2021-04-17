---
description: Contiene información sobre una palabra de tinta determinada en la nota de Journal, incluida la posición, los alternativos y los datos de tinta reales.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Elemento InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fb5e2bcce2e01f684f0b39d662e8538c7d27e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706508"
---
# <a name="inkword-element"></a><span data-ttu-id="04ee3-103">Elemento InkWord</span><span class="sxs-lookup"><span data-stu-id="04ee3-103">InkWord Element</span></span>

<span data-ttu-id="04ee3-104">Contiene información sobre una palabra de tinta determinada en la nota de Journal, incluida la posición, los alternativos y los datos de tinta reales.</span><span class="sxs-lookup"><span data-stu-id="04ee3-104">Contains information about a given ink word in the Journal note, including position, alternates, and the actual ink data.</span></span>

## <a name="definition"></a><span data-ttu-id="04ee3-105">Definición</span><span class="sxs-lookup"><span data-stu-id="04ee3-105">Definition</span></span>

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a><span data-ttu-id="04ee3-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="04ee3-106">Parent Elements</span></span>

[<span data-ttu-id="04ee3-107">**Groupnode BizTalk**</span><span class="sxs-lookup"><span data-stu-id="04ee3-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="04ee3-108">**Línea**</span><span class="sxs-lookup"><span data-stu-id="04ee3-108">**Line**</span></span>](line-element.md)

## <a name="child-elements"></a><span data-ttu-id="04ee3-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="04ee3-109">Child Elements</span></span>

[<span data-ttu-id="04ee3-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="04ee3-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="04ee3-111">**AlternateList**</span><span class="sxs-lookup"><span data-stu-id="04ee3-111">**AlternateList**</span></span>](alternatelist-element.md)

[<span data-ttu-id="04ee3-112">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="04ee3-112">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="04ee3-113">**Confianza**</span><span class="sxs-lookup"><span data-stu-id="04ee3-113">**Confidence**</span></span>](confidence-element.md)

[<span data-ttu-id="04ee3-114">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="04ee3-114">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="04ee3-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="04ee3-115">Attributes</span></span>



| <span data-ttu-id="04ee3-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="04ee3-116">Attribute</span></span>  | <span data-ttu-id="04ee3-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="04ee3-117">Type</span></span>                      | <span data-ttu-id="04ee3-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="04ee3-118">Required</span></span> | <span data-ttu-id="04ee3-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="04ee3-119">Description</span></span>                                                                             | <span data-ttu-id="04ee3-120">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="04ee3-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="04ee3-121">**Left**</span><span class="sxs-lookup"><span data-stu-id="04ee3-121">**Left**</span></span>   | <span data-ttu-id="04ee3-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="04ee3-122">**xs:integer**</span></span>            | <span data-ttu-id="04ee3-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="04ee3-123">Required</span></span> | <span data-ttu-id="04ee3-124">Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="04ee3-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="04ee3-125">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="04ee3-125">Any integer.</span></span>              |
| <span data-ttu-id="04ee3-126">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="04ee3-126">**Top**</span></span>    | <span data-ttu-id="04ee3-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="04ee3-127">**xs:integer**</span></span>            | <span data-ttu-id="04ee3-128">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="04ee3-128">Required</span></span> | <span data-ttu-id="04ee3-129">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="04ee3-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="04ee3-130">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="04ee3-130">Any integer.</span></span>              |
| <span data-ttu-id="04ee3-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="04ee3-131">**Width**</span></span>  | <span data-ttu-id="04ee3-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="04ee3-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="04ee3-133">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="04ee3-133">Required</span></span> | <span data-ttu-id="04ee3-134">Ancho del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="04ee3-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="04ee3-135">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="04ee3-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="04ee3-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="04ee3-136">**Height**</span></span> | <span data-ttu-id="04ee3-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="04ee3-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="04ee3-138">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="04ee3-138">Required</span></span> | <span data-ttu-id="04ee3-139">Alto del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="04ee3-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="04ee3-140">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="04ee3-140">Any non-negative integer.</span></span> |



 

> [!WARNING]
> <span data-ttu-id="04ee3-141">La asignación de coordenadas interna de la palabra de tinta es una unidad de métricas en inglés y la aplicación debe usar un multiplicador de 2,54 para convertir los valores de ancho y alto en las unidades de HIMETRIC utilizadas por las API de la plataforma de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="04ee3-141">The ink word's internal coordinate mapping is English Metric Units and a multiplier of 2.54 will need to be used by your application to convert the Width and Height values to the HIMETRIC units used by the Tablet PC platform APIs.</span></span>

 

## <a name="element-information"></a><span data-ttu-id="04ee3-142">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="04ee3-142">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="04ee3-143">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="04ee3-143">Element type</span></span> | <span data-ttu-id="04ee3-144">[**InkWordType**](inkwordtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="04ee3-144">[**InkWordType**](inkwordtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="04ee3-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="04ee3-145">Namespace</span></span>    | <span data-ttu-id="04ee3-146">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="04ee3-146">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="04ee3-147">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="04ee3-147">Schema name</span></span>  | <span data-ttu-id="04ee3-148">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="04ee3-148">Journal Reader</span></span>                                              |



 

 

 



