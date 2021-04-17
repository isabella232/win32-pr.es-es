---
description: Contiene contenido que ha sido clasificado por el analizador o por el usuario como un dibujo.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Elemento de dibujo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe516a4ba33e6e597b17ce8365d792f19468c3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697858"
---
# <a name="drawing-element"></a><span data-ttu-id="58e83-103">Elemento de dibujo</span><span class="sxs-lookup"><span data-stu-id="58e83-103">Drawing Element</span></span>

<span data-ttu-id="58e83-104">Contiene contenido que ha sido clasificado por el analizador o por el usuario como un dibujo.</span><span class="sxs-lookup"><span data-stu-id="58e83-104">Contains content that has been classified by the analyzer or the user as a drawing.</span></span>

## <a name="definition"></a><span data-ttu-id="58e83-105">Definición</span><span class="sxs-lookup"><span data-stu-id="58e83-105">Definition</span></span>

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="58e83-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="58e83-106">Parent Elements</span></span>

[<span data-ttu-id="58e83-107">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="58e83-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="58e83-108">**Groupnode BizTalk**</span><span class="sxs-lookup"><span data-stu-id="58e83-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="58e83-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="58e83-109">Child Elements</span></span>

[<span data-ttu-id="58e83-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="58e83-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="58e83-111">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="58e83-111">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="58e83-112">**InkClass**</span><span class="sxs-lookup"><span data-stu-id="58e83-112">**InkClass**</span></span>](inkclass-element.md)

[<span data-ttu-id="58e83-113">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="58e83-113">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="58e83-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="58e83-114">Attributes</span></span>



| <span data-ttu-id="58e83-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="58e83-115">Attribute</span></span>  | <span data-ttu-id="58e83-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="58e83-116">Type</span></span>                      | <span data-ttu-id="58e83-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="58e83-117">Required</span></span> | <span data-ttu-id="58e83-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="58e83-118">Description</span></span>                                                                             | <span data-ttu-id="58e83-119">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="58e83-119">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="58e83-120">**Left**</span><span class="sxs-lookup"><span data-stu-id="58e83-120">**Left**</span></span>   | <span data-ttu-id="58e83-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="58e83-121">**xs:integer**</span></span>            | <span data-ttu-id="58e83-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="58e83-122">Required</span></span> | <span data-ttu-id="58e83-123">Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="58e83-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="58e83-124">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="58e83-124">Any integer.</span></span>              |
| <span data-ttu-id="58e83-125">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="58e83-125">**Top**</span></span>    | <span data-ttu-id="58e83-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="58e83-126">**xs:integer**</span></span>            | <span data-ttu-id="58e83-127">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="58e83-127">Required</span></span> | <span data-ttu-id="58e83-128">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="58e83-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="58e83-129">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="58e83-129">Any integer.</span></span>              |
| <span data-ttu-id="58e83-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="58e83-130">**Width**</span></span>  | <span data-ttu-id="58e83-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="58e83-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="58e83-132">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="58e83-132">Required</span></span> | <span data-ttu-id="58e83-133">Ancho del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="58e83-133">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="58e83-134">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="58e83-134">Any non-negative integer.</span></span> |
| <span data-ttu-id="58e83-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="58e83-135">**Height**</span></span> | <span data-ttu-id="58e83-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="58e83-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="58e83-137">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="58e83-137">Required</span></span> | <span data-ttu-id="58e83-138">Alto del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="58e83-138">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="58e83-139">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="58e83-139">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="58e83-140">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="58e83-140">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="58e83-141">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="58e83-141">Element type</span></span> | <span data-ttu-id="58e83-142">[**DrawingType**](drawingtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="58e83-142">[**DrawingType**](drawingtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="58e83-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="58e83-143">Namespace</span></span>    | <span data-ttu-id="58e83-144">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="58e83-144">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="58e83-145">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="58e83-145">Schema name</span></span>  | <span data-ttu-id="58e83-146">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="58e83-146">Journal Reader</span></span>                                              |



 

 

 



