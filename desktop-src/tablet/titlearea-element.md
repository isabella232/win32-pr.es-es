---
description: Contiene la ubicación y la información de límite de la nota Title, si está presente.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Elemento TitleArea
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88d563e8d7f6fc0107bc3302d3f8d94d29dfbfb8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432197"
---
# <a name="titlearea-element"></a><span data-ttu-id="076a4-103">Elemento TitleArea</span><span class="sxs-lookup"><span data-stu-id="076a4-103">TitleArea Element</span></span>

<span data-ttu-id="076a4-104">Contiene la ubicación y la información de límite de la nota Title, si está presente.</span><span class="sxs-lookup"><span data-stu-id="076a4-104">Contains location and bounding information for the note Title, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="076a4-105">Definición</span><span class="sxs-lookup"><span data-stu-id="076a4-105">Definition</span></span>

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="076a4-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="076a4-106">Parent Elements</span></span>

[<span data-ttu-id="076a4-107">**Título**</span><span class="sxs-lookup"><span data-stu-id="076a4-107">**Title**</span></span>](title-element.md)

## <a name="child-elements"></a><span data-ttu-id="076a4-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="076a4-108">Child Elements</span></span>

<span data-ttu-id="076a4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="076a4-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="076a4-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="076a4-110">Attributes</span></span>



| <span data-ttu-id="076a4-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="076a4-111">Attribute</span></span>  | <span data-ttu-id="076a4-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="076a4-112">Type</span></span>                      | <span data-ttu-id="076a4-113">Requerido</span><span class="sxs-lookup"><span data-stu-id="076a4-113">Required</span></span> | <span data-ttu-id="076a4-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="076a4-114">Description</span></span>                                                                             | <span data-ttu-id="076a4-115">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="076a4-115">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="076a4-116">**Left**</span><span class="sxs-lookup"><span data-stu-id="076a4-116">**Left**</span></span>   | <span data-ttu-id="076a4-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="076a4-117">**xs:integer**</span></span>            | <span data-ttu-id="076a4-118">Requerido</span><span class="sxs-lookup"><span data-stu-id="076a4-118">Required</span></span> | <span data-ttu-id="076a4-119">Distancia desde el origen hasta el punto más a la izquierda en el cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="076a4-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="076a4-120">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="076a4-120">Any integer.</span></span>              |
| <span data-ttu-id="076a4-121">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="076a4-121">**Top**</span></span>    | <span data-ttu-id="076a4-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="076a4-122">**xs:integer**</span></span>            | <span data-ttu-id="076a4-123">Requerido</span><span class="sxs-lookup"><span data-stu-id="076a4-123">Required</span></span> | <span data-ttu-id="076a4-124">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="076a4-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="076a4-125">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="076a4-125">Any integer.</span></span>              |
| <span data-ttu-id="076a4-126">**Width**</span><span class="sxs-lookup"><span data-stu-id="076a4-126">**Width**</span></span>  | <span data-ttu-id="076a4-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="076a4-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="076a4-128">Requerido</span><span class="sxs-lookup"><span data-stu-id="076a4-128">Required</span></span> | <span data-ttu-id="076a4-129">Ancho del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="076a4-129">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="076a4-130">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="076a4-130">Any non-negative integer.</span></span> |
| <span data-ttu-id="076a4-131">**Height**</span><span class="sxs-lookup"><span data-stu-id="076a4-131">**Height**</span></span> | <span data-ttu-id="076a4-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="076a4-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="076a4-133">Requerido</span><span class="sxs-lookup"><span data-stu-id="076a4-133">Required</span></span> | <span data-ttu-id="076a4-134">Alto del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="076a4-134">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="076a4-135">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="076a4-135">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="076a4-136">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="076a4-136">Element Information</span></span>



|   <span data-ttu-id="076a4-137">Elemento</span><span class="sxs-lookup"><span data-stu-id="076a4-137">Element</span></span>    | <span data-ttu-id="076a4-138">Value</span><span class="sxs-lookup"><span data-stu-id="076a4-138">Value</span></span>                                                           |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="076a4-139">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="076a4-139">Element type</span></span> | <span data-ttu-id="076a4-140">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="076a4-140">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="076a4-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="076a4-141">Namespace</span></span>    | <span data-ttu-id="076a4-142">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="076a4-142">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="076a4-143">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="076a4-143">Schema name</span></span>  | <span data-ttu-id="076a4-144">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="076a4-144">Journal Reader</span></span>                                                  |



 

 

 



