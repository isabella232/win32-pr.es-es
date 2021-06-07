---
description: Contiene un mapa de bits codificado en Base64 de una marca asociada a la sección de una nota de diario.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Elemento Flag
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46508f9821379fbedb3291ba45d16dbdd0fb316f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432337"
---
# <a name="flag-element"></a><span data-ttu-id="53e6e-103">Elemento Flag</span><span class="sxs-lookup"><span data-stu-id="53e6e-103">Flag Element</span></span>

<span data-ttu-id="53e6e-104">Contiene un mapa de bits codificado en Base64 de una marca asociada a la sección de una nota de diario.</span><span class="sxs-lookup"><span data-stu-id="53e6e-104">Contains a base64 encoded bitmap of a flag associated with section of a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="53e6e-105">Definición</span><span class="sxs-lookup"><span data-stu-id="53e6e-105">Definition</span></span>

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="53e6e-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="53e6e-106">Parent Elements</span></span>

[<span data-ttu-id="53e6e-107">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="53e6e-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="53e6e-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="53e6e-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="53e6e-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="53e6e-109">Child Elements</span></span>

<span data-ttu-id="53e6e-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="53e6e-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="53e6e-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="53e6e-111">Attributes</span></span>



| <span data-ttu-id="53e6e-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="53e6e-112">Attribute</span></span>  | <span data-ttu-id="53e6e-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="53e6e-113">Type</span></span>                      | <span data-ttu-id="53e6e-114">Requerido</span><span class="sxs-lookup"><span data-stu-id="53e6e-114">Required</span></span> | <span data-ttu-id="53e6e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="53e6e-115">Description</span></span>                                                                             | <span data-ttu-id="53e6e-116">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="53e6e-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="53e6e-117">**Left**</span><span class="sxs-lookup"><span data-stu-id="53e6e-117">**Left**</span></span>   | <span data-ttu-id="53e6e-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="53e6e-118">**xs:integer**</span></span>            | <span data-ttu-id="53e6e-119">Requerido</span><span class="sxs-lookup"><span data-stu-id="53e6e-119">Required</span></span> | <span data-ttu-id="53e6e-120">Distancia desde el origen hasta el punto situado más a la izquierda en el cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="53e6e-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="53e6e-121">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="53e6e-121">Any integer.</span></span>              |
| <span data-ttu-id="53e6e-122">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="53e6e-122">**Top**</span></span>    | <span data-ttu-id="53e6e-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="53e6e-123">**xs:integer**</span></span>            | <span data-ttu-id="53e6e-124">Requerido</span><span class="sxs-lookup"><span data-stu-id="53e6e-124">Required</span></span> | <span data-ttu-id="53e6e-125">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="53e6e-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="53e6e-126">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="53e6e-126">Any integer.</span></span>              |
| <span data-ttu-id="53e6e-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="53e6e-127">**Width**</span></span>  | <span data-ttu-id="53e6e-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="53e6e-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="53e6e-129">Requerido</span><span class="sxs-lookup"><span data-stu-id="53e6e-129">Required</span></span> | <span data-ttu-id="53e6e-130">Ancho del cuadro de límite para el elemento.</span><span class="sxs-lookup"><span data-stu-id="53e6e-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="53e6e-131">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="53e6e-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="53e6e-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="53e6e-132">**Height**</span></span> | <span data-ttu-id="53e6e-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="53e6e-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="53e6e-134">Requerido</span><span class="sxs-lookup"><span data-stu-id="53e6e-134">Required</span></span> | <span data-ttu-id="53e6e-135">Alto del cuadro de límite para el elemento.</span><span class="sxs-lookup"><span data-stu-id="53e6e-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="53e6e-136">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="53e6e-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="53e6e-137">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="53e6e-137">Element Information</span></span>



|  <span data-ttu-id="53e6e-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="53e6e-138">Element</span></span>     | <span data-ttu-id="53e6e-139">Value</span><span class="sxs-lookup"><span data-stu-id="53e6e-139">Value</span></span>                                                     |
|--------------|-------------------------------------------------------|
| <span data-ttu-id="53e6e-140">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="53e6e-140">Element type</span></span> | <span data-ttu-id="53e6e-141">[**FlagType**](flagtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="53e6e-141">[**FlagType**](flagtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="53e6e-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="53e6e-142">Namespace</span></span>    | <span data-ttu-id="53e6e-143">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="53e6e-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>            |
| <span data-ttu-id="53e6e-144">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="53e6e-144">Schema name</span></span>  | <span data-ttu-id="53e6e-145">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="53e6e-145">Journal Reader</span></span>                                        |



 

 

 



