---
description: Contiene datos binarios codificados para una imagen en el documento de diario, si está presente.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Elemento de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8437495a4c248a8e5bc68a0f7b75a2cf7d761387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697378"
---
# <a name="image-element"></a><span data-ttu-id="feaf6-103">Elemento de imagen</span><span class="sxs-lookup"><span data-stu-id="feaf6-103">Image Element</span></span>

<span data-ttu-id="feaf6-104">Contiene datos binarios codificados para una imagen en el documento de diario, si está presente.</span><span class="sxs-lookup"><span data-stu-id="feaf6-104">Contains encoded binary data for an image in the Journal document, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="feaf6-105">Definición</span><span class="sxs-lookup"><span data-stu-id="feaf6-105">Definition</span></span>

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a><span data-ttu-id="feaf6-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="feaf6-106">Parent Elements</span></span>

[<span data-ttu-id="feaf6-107">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="feaf6-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="feaf6-108">**Groupnode BizTalk**</span><span class="sxs-lookup"><span data-stu-id="feaf6-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="feaf6-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="feaf6-109">Child Elements</span></span>

<span data-ttu-id="feaf6-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="feaf6-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="feaf6-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="feaf6-111">Attributes</span></span>



| <span data-ttu-id="feaf6-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="feaf6-112">Attribute</span></span>  | <span data-ttu-id="feaf6-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="feaf6-113">Type</span></span>                      | <span data-ttu-id="feaf6-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="feaf6-114">Required</span></span> | <span data-ttu-id="feaf6-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="feaf6-115">Description</span></span>                                                                             | <span data-ttu-id="feaf6-116">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="feaf6-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="feaf6-117">**Left**</span><span class="sxs-lookup"><span data-stu-id="feaf6-117">**Left**</span></span>   | <span data-ttu-id="feaf6-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="feaf6-118">**xs:integer**</span></span>            | <span data-ttu-id="feaf6-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="feaf6-119">Required</span></span> | <span data-ttu-id="feaf6-120">Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="feaf6-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="feaf6-121">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="feaf6-121">Any integer.</span></span>              |
| <span data-ttu-id="feaf6-122">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="feaf6-122">**Top**</span></span>    | <span data-ttu-id="feaf6-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="feaf6-123">**xs:integer**</span></span>            | <span data-ttu-id="feaf6-124">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="feaf6-124">Required</span></span> | <span data-ttu-id="feaf6-125">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="feaf6-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="feaf6-126">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="feaf6-126">Any integer.</span></span>              |
| <span data-ttu-id="feaf6-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="feaf6-127">**Width**</span></span>  | <span data-ttu-id="feaf6-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="feaf6-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="feaf6-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="feaf6-129">Required</span></span> | <span data-ttu-id="feaf6-130">Ancho del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="feaf6-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="feaf6-131">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="feaf6-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="feaf6-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="feaf6-132">**Height**</span></span> | <span data-ttu-id="feaf6-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="feaf6-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="feaf6-134">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="feaf6-134">Required</span></span> | <span data-ttu-id="feaf6-135">Alto del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="feaf6-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="feaf6-136">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="feaf6-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="feaf6-137">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="feaf6-137">Element Information</span></span>



|              |                                                         |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="feaf6-138">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="feaf6-138">Element type</span></span> | <span data-ttu-id="feaf6-139">[**ImageType**](imagetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="feaf6-139">[**ImageType**](imagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="feaf6-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="feaf6-140">Namespace</span></span>    | <span data-ttu-id="feaf6-141">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="feaf6-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="feaf6-142">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="feaf6-142">Schema name</span></span>  | <span data-ttu-id="feaf6-143">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="feaf6-143">Journal Reader</span></span>                                          |



 

## <a name="see-also"></a><span data-ttu-id="feaf6-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="feaf6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feaf6-145">**Información previa**</span><span class="sxs-lookup"><span data-stu-id="feaf6-145">**Background**</span></span>](background-element.md)
</dt> </dl>

 

 



