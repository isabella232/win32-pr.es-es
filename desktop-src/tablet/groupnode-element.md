---
description: Contiene un conjunto de elementos&\# 8212; Paragraph, InkWord, Drawing, Text, Image o Flag&\# 8212; que se agrupan en la nota de Journal.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Elemento Groupnode BizTalk
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ee141691ef58d14e6c08a49544e9cf3ecf7540b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648208"
---
# <a name="groupnode-element"></a><span data-ttu-id="6e7ea-103">Elemento Groupnode BizTalk</span><span class="sxs-lookup"><span data-stu-id="6e7ea-103">GroupNode Element</span></span>

<span data-ttu-id="6e7ea-104">Contiene un conjunto de elementos ([**paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md)o [**Flag**](flag-element.md)) que se agrupan en la nota de Journal.</span><span class="sxs-lookup"><span data-stu-id="6e7ea-104">Contains a set of elements—[**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md), or [**Flag**](flag-element.md)—that are grouped together in the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="6e7ea-105">Definición</span><span class="sxs-lookup"><span data-stu-id="6e7ea-105">Definition</span></span>

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a><span data-ttu-id="6e7ea-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="6e7ea-106">Parent Elements</span></span>

[<span data-ttu-id="6e7ea-107">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="6e7ea-107">**Content**</span></span>](content-element--journal-reader.md)

## <a name="child-elements"></a><span data-ttu-id="6e7ea-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6e7ea-108">Child Elements</span></span>

[<span data-ttu-id="6e7ea-109">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="6e7ea-109">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="6e7ea-110">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="6e7ea-110">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="6e7ea-111">**Dibujo**</span><span class="sxs-lookup"><span data-stu-id="6e7ea-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="6e7ea-112">**Texto**</span><span class="sxs-lookup"><span data-stu-id="6e7ea-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="6e7ea-113">**Impresión**</span><span class="sxs-lookup"><span data-stu-id="6e7ea-113">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="6e7ea-114">**Marca**</span><span class="sxs-lookup"><span data-stu-id="6e7ea-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="6e7ea-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="6e7ea-115">Attributes</span></span>



| <span data-ttu-id="6e7ea-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="6e7ea-116">Attribute</span></span>  | <span data-ttu-id="6e7ea-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e7ea-117">Type</span></span>                      | <span data-ttu-id="6e7ea-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e7ea-118">Required</span></span> | <span data-ttu-id="6e7ea-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e7ea-119">Description</span></span>                                                                             | <span data-ttu-id="6e7ea-120">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="6e7ea-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="6e7ea-121">**Left**</span><span class="sxs-lookup"><span data-stu-id="6e7ea-121">**Left**</span></span>   | <span data-ttu-id="6e7ea-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="6e7ea-122">**xs:integer**</span></span>            | <span data-ttu-id="6e7ea-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e7ea-123">Required</span></span> | <span data-ttu-id="6e7ea-124">Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="6e7ea-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="6e7ea-125">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="6e7ea-125">Any integer.</span></span>              |
| <span data-ttu-id="6e7ea-126">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="6e7ea-126">**Top**</span></span>    | <span data-ttu-id="6e7ea-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="6e7ea-127">**xs:integer**</span></span>            | <span data-ttu-id="6e7ea-128">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e7ea-128">Required</span></span> | <span data-ttu-id="6e7ea-129">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="6e7ea-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="6e7ea-130">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="6e7ea-130">Any integer.</span></span>              |
| <span data-ttu-id="6e7ea-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="6e7ea-131">**Width**</span></span>  | <span data-ttu-id="6e7ea-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="6e7ea-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="6e7ea-133">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e7ea-133">Required</span></span> | <span data-ttu-id="6e7ea-134">Ancho del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="6e7ea-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="6e7ea-135">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="6e7ea-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="6e7ea-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="6e7ea-136">**Height**</span></span> | <span data-ttu-id="6e7ea-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="6e7ea-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="6e7ea-138">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e7ea-138">Required</span></span> | <span data-ttu-id="6e7ea-139">Alto del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="6e7ea-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="6e7ea-140">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="6e7ea-140">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="6e7ea-141">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6e7ea-141">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="6e7ea-142">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="6e7ea-142">Element type</span></span> | <span data-ttu-id="6e7ea-143">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="6e7ea-143">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="6e7ea-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6e7ea-144">Namespace</span></span>    | <span data-ttu-id="6e7ea-145">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="6e7ea-145">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="6e7ea-146">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="6e7ea-146">Schema name</span></span>  | <span data-ttu-id="6e7ea-147">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="6e7ea-147">Journal Reader</span></span>                                                  |



 

 

 



