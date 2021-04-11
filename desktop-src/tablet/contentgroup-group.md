---
description: Define un grupo que contiene un conjunto de contenido agrupado en una nota de Journal.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Grupo ContentGroup
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbbc13a3dee796646b6d61ac9ba0bde50880f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083012"
---
# <a name="contentgroup-group"></a><span data-ttu-id="21eb7-103">Grupo ContentGroup</span><span class="sxs-lookup"><span data-stu-id="21eb7-103">ContentGroup Group</span></span>

<span data-ttu-id="21eb7-104">Define un grupo que contiene un conjunto de contenido agrupado en una nota de Journal.</span><span class="sxs-lookup"><span data-stu-id="21eb7-104">Defines a group that contains a set of grouped content in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="21eb7-105">Definición</span><span class="sxs-lookup"><span data-stu-id="21eb7-105">Definition</span></span>

``` syntax
<xs:group name="ContentGroup" >
  <xs:choice>
    <xs:element name="GroupNode" type="GroupNodeType" />
    <xs:element name="Paragraph" type="ParagraphType" />
    <xs:element name="InkWord" type="InkWordType" />
    <xs:element name="Drawing" type="DrawingType" />
    <xs:element name="Text" type="TextType" />
    <xs:element name="Image" type="ImageType" />
    <xs:element name="Flag" type="FlagType" />
    <xs:element name="Reflow" type="ReflowType" />
  </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="21eb7-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="21eb7-106">Child Elements</span></span>

[<span data-ttu-id="21eb7-107">**Groupnode BizTalk**</span><span class="sxs-lookup"><span data-stu-id="21eb7-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="21eb7-108">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="21eb7-108">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="21eb7-109">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="21eb7-109">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="21eb7-110">**Dibujo**</span><span class="sxs-lookup"><span data-stu-id="21eb7-110">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="21eb7-111">**Texto**</span><span class="sxs-lookup"><span data-stu-id="21eb7-111">**Text**</span></span>](text-element.md)

[<span data-ttu-id="21eb7-112">**Impresión**</span><span class="sxs-lookup"><span data-stu-id="21eb7-112">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="21eb7-113">**Marca**</span><span class="sxs-lookup"><span data-stu-id="21eb7-113">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="21eb7-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="21eb7-114">Attributes</span></span>



| <span data-ttu-id="21eb7-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="21eb7-115">Attribute</span></span>  | <span data-ttu-id="21eb7-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="21eb7-116">Type</span></span>                      | <span data-ttu-id="21eb7-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="21eb7-117">Required</span></span> | <span data-ttu-id="21eb7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="21eb7-118">Description</span></span>                                                                                        | <span data-ttu-id="21eb7-119">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="21eb7-119">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="21eb7-120">**Left**</span><span class="sxs-lookup"><span data-stu-id="21eb7-120">**Left**</span></span>   | <span data-ttu-id="21eb7-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="21eb7-121">**xs:integer**</span></span>            | <span data-ttu-id="21eb7-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="21eb7-122">Required</span></span> | <span data-ttu-id="21eb7-123">Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="21eb7-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="21eb7-124">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="21eb7-124">Any integer.</span></span><br/>              |
| <span data-ttu-id="21eb7-125">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="21eb7-125">**Top**</span></span>    | <span data-ttu-id="21eb7-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="21eb7-126">**xs:integer**</span></span>            | <span data-ttu-id="21eb7-127">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="21eb7-127">Required</span></span> | <span data-ttu-id="21eb7-128">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="21eb7-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="21eb7-129">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="21eb7-129">Any integer.</span></span><br/>              |
| <span data-ttu-id="21eb7-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="21eb7-130">**Width**</span></span>  | <span data-ttu-id="21eb7-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="21eb7-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="21eb7-132">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="21eb7-132">Required</span></span> | <span data-ttu-id="21eb7-133">Ancho del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="21eb7-133">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="21eb7-134">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="21eb7-134">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="21eb7-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="21eb7-135">**Height**</span></span> | <span data-ttu-id="21eb7-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="21eb7-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="21eb7-137">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="21eb7-137">Required</span></span> | <span data-ttu-id="21eb7-138">Alto del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="21eb7-138">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="21eb7-139">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="21eb7-139">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="21eb7-140">Información de tipo</span><span class="sxs-lookup"><span data-stu-id="21eb7-140">Type Information</span></span>



|             |                                            |
|-------------|--------------------------------------------|
| <span data-ttu-id="21eb7-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="21eb7-141">Namespace</span></span>   | <span data-ttu-id="21eb7-142">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="21eb7-142">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="21eb7-143">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="21eb7-143">Schema name</span></span> | <span data-ttu-id="21eb7-144">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="21eb7-144">Journal Reader</span></span>                             |



 

 

 




