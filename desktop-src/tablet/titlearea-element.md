---
description: Contiene información de ubicación y delimitación para el título de la nota, si está presente.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Elemento TitleArea
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c009d817af9679edda618dd0262c7cbb85a612ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002977"
---
# <a name="titlearea-element"></a><span data-ttu-id="29dc4-103">Elemento TitleArea</span><span class="sxs-lookup"><span data-stu-id="29dc4-103">TitleArea Element</span></span>

<span data-ttu-id="29dc4-104">Contiene información de ubicación y delimitación para el título de la nota, si está presente.</span><span class="sxs-lookup"><span data-stu-id="29dc4-104">Contains location and bounding information for the note Title, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="29dc4-105">Definición</span><span class="sxs-lookup"><span data-stu-id="29dc4-105">Definition</span></span>

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="29dc4-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="29dc4-106">Parent Elements</span></span>

[<span data-ttu-id="29dc4-107">**Title**</span><span class="sxs-lookup"><span data-stu-id="29dc4-107">**Title**</span></span>](title-element.md)

## <a name="child-elements"></a><span data-ttu-id="29dc4-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="29dc4-108">Child Elements</span></span>

<span data-ttu-id="29dc4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="29dc4-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="29dc4-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="29dc4-110">Attributes</span></span>



| <span data-ttu-id="29dc4-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="29dc4-111">Attribute</span></span>  | <span data-ttu-id="29dc4-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="29dc4-112">Type</span></span>                      | <span data-ttu-id="29dc4-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="29dc4-113">Required</span></span> | <span data-ttu-id="29dc4-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="29dc4-114">Description</span></span>                                                                             | <span data-ttu-id="29dc4-115">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="29dc4-115">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="29dc4-116">**Left**</span><span class="sxs-lookup"><span data-stu-id="29dc4-116">**Left**</span></span>   | <span data-ttu-id="29dc4-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="29dc4-117">**xs:integer**</span></span>            | <span data-ttu-id="29dc4-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="29dc4-118">Required</span></span> | <span data-ttu-id="29dc4-119">Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="29dc4-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="29dc4-120">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="29dc4-120">Any integer.</span></span>              |
| <span data-ttu-id="29dc4-121">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="29dc4-121">**Top**</span></span>    | <span data-ttu-id="29dc4-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="29dc4-122">**xs:integer**</span></span>            | <span data-ttu-id="29dc4-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="29dc4-123">Required</span></span> | <span data-ttu-id="29dc4-124">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="29dc4-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="29dc4-125">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="29dc4-125">Any integer.</span></span>              |
| <span data-ttu-id="29dc4-126">**Width**</span><span class="sxs-lookup"><span data-stu-id="29dc4-126">**Width**</span></span>  | <span data-ttu-id="29dc4-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="29dc4-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="29dc4-128">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="29dc4-128">Required</span></span> | <span data-ttu-id="29dc4-129">Ancho del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="29dc4-129">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="29dc4-130">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="29dc4-130">Any non-negative integer.</span></span> |
| <span data-ttu-id="29dc4-131">**Height**</span><span class="sxs-lookup"><span data-stu-id="29dc4-131">**Height**</span></span> | <span data-ttu-id="29dc4-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="29dc4-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="29dc4-133">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="29dc4-133">Required</span></span> | <span data-ttu-id="29dc4-134">Alto del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="29dc4-134">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="29dc4-135">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="29dc4-135">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="29dc4-136">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="29dc4-136">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="29dc4-137">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="29dc4-137">Element type</span></span> | <span data-ttu-id="29dc4-138">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="29dc4-138">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="29dc4-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="29dc4-139">Namespace</span></span>    | <span data-ttu-id="29dc4-140">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="29dc4-140">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="29dc4-141">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="29dc4-141">Schema name</span></span>  | <span data-ttu-id="29dc4-142">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="29dc4-142">Journal Reader</span></span>                                                  |



 

 

 



