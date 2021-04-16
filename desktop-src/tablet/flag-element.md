---
description: Contiene un mapa de bits con codificación Base64 de una marca asociada a la sección de una nota de Journal.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Elemento Flag
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b6eda9aeb29c07c0de05eadffb8ba8d60f81954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705703"
---
# <a name="flag-element"></a><span data-ttu-id="f9e98-103">Elemento Flag</span><span class="sxs-lookup"><span data-stu-id="f9e98-103">Flag Element</span></span>

<span data-ttu-id="f9e98-104">Contiene un mapa de bits con codificación Base64 de una marca asociada a la sección de una nota de Journal.</span><span class="sxs-lookup"><span data-stu-id="f9e98-104">Contains a base64 encoded bitmap of a flag associated with section of a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="f9e98-105">Definición</span><span class="sxs-lookup"><span data-stu-id="f9e98-105">Definition</span></span>

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="f9e98-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="f9e98-106">Parent Elements</span></span>

[<span data-ttu-id="f9e98-107">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="f9e98-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="f9e98-108">**Groupnode BizTalk**</span><span class="sxs-lookup"><span data-stu-id="f9e98-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="f9e98-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f9e98-109">Child Elements</span></span>

<span data-ttu-id="f9e98-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f9e98-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="f9e98-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="f9e98-111">Attributes</span></span>



| <span data-ttu-id="f9e98-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="f9e98-112">Attribute</span></span>  | <span data-ttu-id="f9e98-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9e98-113">Type</span></span>                      | <span data-ttu-id="f9e98-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f9e98-114">Required</span></span> | <span data-ttu-id="f9e98-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9e98-115">Description</span></span>                                                                             | <span data-ttu-id="f9e98-116">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="f9e98-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="f9e98-117">**Left**</span><span class="sxs-lookup"><span data-stu-id="f9e98-117">**Left**</span></span>   | <span data-ttu-id="f9e98-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="f9e98-118">**xs:integer**</span></span>            | <span data-ttu-id="f9e98-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f9e98-119">Required</span></span> | <span data-ttu-id="f9e98-120">Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="f9e98-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="f9e98-121">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="f9e98-121">Any integer.</span></span>              |
| <span data-ttu-id="f9e98-122">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="f9e98-122">**Top**</span></span>    | <span data-ttu-id="f9e98-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="f9e98-123">**xs:integer**</span></span>            | <span data-ttu-id="f9e98-124">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f9e98-124">Required</span></span> | <span data-ttu-id="f9e98-125">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="f9e98-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="f9e98-126">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="f9e98-126">Any integer.</span></span>              |
| <span data-ttu-id="f9e98-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="f9e98-127">**Width**</span></span>  | <span data-ttu-id="f9e98-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="f9e98-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="f9e98-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f9e98-129">Required</span></span> | <span data-ttu-id="f9e98-130">Ancho del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="f9e98-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="f9e98-131">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="f9e98-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="f9e98-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="f9e98-132">**Height**</span></span> | <span data-ttu-id="f9e98-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="f9e98-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="f9e98-134">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f9e98-134">Required</span></span> | <span data-ttu-id="f9e98-135">Alto del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="f9e98-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="f9e98-136">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="f9e98-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="f9e98-137">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="f9e98-137">Element Information</span></span>



|              |                                                       |
|--------------|-------------------------------------------------------|
| <span data-ttu-id="f9e98-138">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f9e98-138">Element type</span></span> | <span data-ttu-id="f9e98-139">[**FlagType**](flagtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="f9e98-139">[**FlagType**](flagtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="f9e98-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f9e98-140">Namespace</span></span>    | <span data-ttu-id="f9e98-141">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="f9e98-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>            |
| <span data-ttu-id="f9e98-142">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="f9e98-142">Schema name</span></span>  | <span data-ttu-id="f9e98-143">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="f9e98-143">Journal Reader</span></span>                                        |



 

 

 



