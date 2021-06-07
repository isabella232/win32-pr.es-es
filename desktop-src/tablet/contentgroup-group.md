---
description: Define un grupo que contiene un conjunto de contenido agrupado en una nota de diario.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Grupo contentgroup
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e4291da1912c43674871c06fb803e1936f7178
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432617"
---
# <a name="contentgroup-group"></a><span data-ttu-id="503a5-103">Grupo contentgroup</span><span class="sxs-lookup"><span data-stu-id="503a5-103">ContentGroup Group</span></span>

<span data-ttu-id="503a5-104">Define un grupo que contiene un conjunto de contenido agrupado en una nota de diario.</span><span class="sxs-lookup"><span data-stu-id="503a5-104">Defines a group that contains a set of grouped content in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="503a5-105">Definición</span><span class="sxs-lookup"><span data-stu-id="503a5-105">Definition</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="503a5-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="503a5-106">Child Elements</span></span>

[<span data-ttu-id="503a5-107">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="503a5-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="503a5-108">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="503a5-108">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="503a5-109">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="503a5-109">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="503a5-110">**Dibujo**</span><span class="sxs-lookup"><span data-stu-id="503a5-110">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="503a5-111">**Texto**</span><span class="sxs-lookup"><span data-stu-id="503a5-111">**Text**</span></span>](text-element.md)

[<span data-ttu-id="503a5-112">**Imagen**</span><span class="sxs-lookup"><span data-stu-id="503a5-112">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="503a5-113">**Marca**</span><span class="sxs-lookup"><span data-stu-id="503a5-113">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="503a5-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="503a5-114">Attributes</span></span>



| <span data-ttu-id="503a5-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="503a5-115">Attribute</span></span>  | <span data-ttu-id="503a5-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="503a5-116">Type</span></span>                      | <span data-ttu-id="503a5-117">Requerido</span><span class="sxs-lookup"><span data-stu-id="503a5-117">Required</span></span> | <span data-ttu-id="503a5-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="503a5-118">Description</span></span>                                                                                        | <span data-ttu-id="503a5-119">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="503a5-119">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="503a5-120">**Left**</span><span class="sxs-lookup"><span data-stu-id="503a5-120">**Left**</span></span>   | <span data-ttu-id="503a5-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="503a5-121">**xs:integer**</span></span>            | <span data-ttu-id="503a5-122">Requerido</span><span class="sxs-lookup"><span data-stu-id="503a5-122">Required</span></span> | <span data-ttu-id="503a5-123">Distancia desde el origen hasta el punto situado más a la izquierda en el cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="503a5-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="503a5-124">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="503a5-124">Any integer.</span></span><br/>              |
| <span data-ttu-id="503a5-125">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="503a5-125">**Top**</span></span>    | <span data-ttu-id="503a5-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="503a5-126">**xs:integer**</span></span>            | <span data-ttu-id="503a5-127">Requerido</span><span class="sxs-lookup"><span data-stu-id="503a5-127">Required</span></span> | <span data-ttu-id="503a5-128">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="503a5-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="503a5-129">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="503a5-129">Any integer.</span></span><br/>              |
| <span data-ttu-id="503a5-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="503a5-130">**Width**</span></span>  | <span data-ttu-id="503a5-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="503a5-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="503a5-132">Requerido</span><span class="sxs-lookup"><span data-stu-id="503a5-132">Required</span></span> | <span data-ttu-id="503a5-133">Ancho del cuadro de límite para el elemento.</span><span class="sxs-lookup"><span data-stu-id="503a5-133">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="503a5-134">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="503a5-134">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="503a5-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="503a5-135">**Height**</span></span> | <span data-ttu-id="503a5-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="503a5-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="503a5-137">Requerido</span><span class="sxs-lookup"><span data-stu-id="503a5-137">Required</span></span> | <span data-ttu-id="503a5-138">Alto del cuadro de límite para el elemento.</span><span class="sxs-lookup"><span data-stu-id="503a5-138">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="503a5-139">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="503a5-139">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="503a5-140">Información de tipo</span><span class="sxs-lookup"><span data-stu-id="503a5-140">Type Information</span></span>



|  <span data-ttu-id="503a5-141">Elemento</span><span class="sxs-lookup"><span data-stu-id="503a5-141">Element</span></span>     | <span data-ttu-id="503a5-142">Value</span><span class="sxs-lookup"><span data-stu-id="503a5-142">Value</span></span>                                                     |
|-------------|--------------------------------------------|
| <span data-ttu-id="503a5-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="503a5-143">Namespace</span></span>   | <span data-ttu-id="503a5-144">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="503a5-144">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="503a5-145">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="503a5-145">Schema name</span></span> | <span data-ttu-id="503a5-146">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="503a5-146">Journal Reader</span></span>                             |



 

 

 




