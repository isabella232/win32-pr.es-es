---
description: Contiene un conjunto de elementos&\# 8212; Paragraph, InkWord, Drawing, Text, Image o Flag&8212; que se agrupan en \# la nota del diario.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Elemento GroupNode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc4d39a592b5b6328bd31ff37761cfd3f0138c0
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432577"
---
# <a name="groupnode-element"></a><span data-ttu-id="b7ba3-103">Elemento GroupNode</span><span class="sxs-lookup"><span data-stu-id="b7ba3-103">GroupNode Element</span></span>

<span data-ttu-id="b7ba3-104">Contiene un conjunto de elementos ([**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md)o [**Flag)**](flag-element.md)que se agrupan en la nota del diario.</span><span class="sxs-lookup"><span data-stu-id="b7ba3-104">Contains a set of elements—[**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md), or [**Flag**](flag-element.md)—that are grouped together in the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="b7ba3-105">Definición</span><span class="sxs-lookup"><span data-stu-id="b7ba3-105">Definition</span></span>

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a><span data-ttu-id="b7ba3-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b7ba3-106">Parent Elements</span></span>

[<span data-ttu-id="b7ba3-107">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="b7ba3-107">**Content**</span></span>](content-element--journal-reader.md)

## <a name="child-elements"></a><span data-ttu-id="b7ba3-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b7ba3-108">Child Elements</span></span>

[<span data-ttu-id="b7ba3-109">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="b7ba3-109">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="b7ba3-110">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="b7ba3-110">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="b7ba3-111">**Dibujo**</span><span class="sxs-lookup"><span data-stu-id="b7ba3-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="b7ba3-112">**Texto**</span><span class="sxs-lookup"><span data-stu-id="b7ba3-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="b7ba3-113">**Imagen**</span><span class="sxs-lookup"><span data-stu-id="b7ba3-113">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="b7ba3-114">**Marca**</span><span class="sxs-lookup"><span data-stu-id="b7ba3-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="b7ba3-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="b7ba3-115">Attributes</span></span>



| <span data-ttu-id="b7ba3-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="b7ba3-116">Attribute</span></span>  | <span data-ttu-id="b7ba3-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="b7ba3-117">Type</span></span>                      | <span data-ttu-id="b7ba3-118">Requerido</span><span class="sxs-lookup"><span data-stu-id="b7ba3-118">Required</span></span> | <span data-ttu-id="b7ba3-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7ba3-119">Description</span></span>                                                                             | <span data-ttu-id="b7ba3-120">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="b7ba3-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="b7ba3-121">**Left**</span><span class="sxs-lookup"><span data-stu-id="b7ba3-121">**Left**</span></span>   | <span data-ttu-id="b7ba3-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="b7ba3-122">**xs:integer**</span></span>            | <span data-ttu-id="b7ba3-123">Requerido</span><span class="sxs-lookup"><span data-stu-id="b7ba3-123">Required</span></span> | <span data-ttu-id="b7ba3-124">Distancia desde el origen hasta el punto más a la izquierda en el cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="b7ba3-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="b7ba3-125">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="b7ba3-125">Any integer.</span></span>              |
| <span data-ttu-id="b7ba3-126">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="b7ba3-126">**Top**</span></span>    | <span data-ttu-id="b7ba3-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="b7ba3-127">**xs:integer**</span></span>            | <span data-ttu-id="b7ba3-128">Requerido</span><span class="sxs-lookup"><span data-stu-id="b7ba3-128">Required</span></span> | <span data-ttu-id="b7ba3-129">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="b7ba3-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="b7ba3-130">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="b7ba3-130">Any integer.</span></span>              |
| <span data-ttu-id="b7ba3-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="b7ba3-131">**Width**</span></span>  | <span data-ttu-id="b7ba3-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="b7ba3-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="b7ba3-133">Requerido</span><span class="sxs-lookup"><span data-stu-id="b7ba3-133">Required</span></span> | <span data-ttu-id="b7ba3-134">Ancho del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="b7ba3-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="b7ba3-135">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="b7ba3-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="b7ba3-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="b7ba3-136">**Height**</span></span> | <span data-ttu-id="b7ba3-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="b7ba3-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="b7ba3-138">Requerido</span><span class="sxs-lookup"><span data-stu-id="b7ba3-138">Required</span></span> | <span data-ttu-id="b7ba3-139">Alto del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="b7ba3-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="b7ba3-140">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="b7ba3-140">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="b7ba3-141">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b7ba3-141">Element Information</span></span>



|  <span data-ttu-id="b7ba3-142">Elemento</span><span class="sxs-lookup"><span data-stu-id="b7ba3-142">Element</span></span>     | <span data-ttu-id="b7ba3-143">Value</span><span class="sxs-lookup"><span data-stu-id="b7ba3-143">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="b7ba3-144">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="b7ba3-144">Element type</span></span> | <span data-ttu-id="b7ba3-145">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="b7ba3-145">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="b7ba3-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b7ba3-146">Namespace</span></span>    | <span data-ttu-id="b7ba3-147">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="b7ba3-147">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="b7ba3-148">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="b7ba3-148">Schema name</span></span>  | <span data-ttu-id="b7ba3-149">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="b7ba3-149">Journal Reader</span></span>                                                  |



 

 

 



