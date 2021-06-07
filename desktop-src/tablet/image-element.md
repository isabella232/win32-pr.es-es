---
description: Contiene datos binarios codificados para una imagen en el documento Journal, si está presente.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Elemento de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9dd3b37a39ce45ee0294f46922fbab376523b64
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432587"
---
# <a name="image-element"></a><span data-ttu-id="078a3-103">Elemento de imagen</span><span class="sxs-lookup"><span data-stu-id="078a3-103">Image Element</span></span>

<span data-ttu-id="078a3-104">Contiene datos binarios codificados para una imagen en el documento Journal, si está presente.</span><span class="sxs-lookup"><span data-stu-id="078a3-104">Contains encoded binary data for an image in the Journal document, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="078a3-105">Definición</span><span class="sxs-lookup"><span data-stu-id="078a3-105">Definition</span></span>

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a><span data-ttu-id="078a3-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="078a3-106">Parent Elements</span></span>

[<span data-ttu-id="078a3-107">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="078a3-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="078a3-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="078a3-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="078a3-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="078a3-109">Child Elements</span></span>

<span data-ttu-id="078a3-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="078a3-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="078a3-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="078a3-111">Attributes</span></span>



| <span data-ttu-id="078a3-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="078a3-112">Attribute</span></span>  | <span data-ttu-id="078a3-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="078a3-113">Type</span></span>                      | <span data-ttu-id="078a3-114">Requerido</span><span class="sxs-lookup"><span data-stu-id="078a3-114">Required</span></span> | <span data-ttu-id="078a3-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="078a3-115">Description</span></span>                                                                             | <span data-ttu-id="078a3-116">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="078a3-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="078a3-117">**Left**</span><span class="sxs-lookup"><span data-stu-id="078a3-117">**Left**</span></span>   | <span data-ttu-id="078a3-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="078a3-118">**xs:integer**</span></span>            | <span data-ttu-id="078a3-119">Requerido</span><span class="sxs-lookup"><span data-stu-id="078a3-119">Required</span></span> | <span data-ttu-id="078a3-120">Distancia desde el origen hasta el punto más a la izquierda en el cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="078a3-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="078a3-121">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="078a3-121">Any integer.</span></span>              |
| <span data-ttu-id="078a3-122">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="078a3-122">**Top**</span></span>    | <span data-ttu-id="078a3-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="078a3-123">**xs:integer**</span></span>            | <span data-ttu-id="078a3-124">Requerido</span><span class="sxs-lookup"><span data-stu-id="078a3-124">Required</span></span> | <span data-ttu-id="078a3-125">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="078a3-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="078a3-126">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="078a3-126">Any integer.</span></span>              |
| <span data-ttu-id="078a3-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="078a3-127">**Width**</span></span>  | <span data-ttu-id="078a3-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="078a3-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="078a3-129">Requerido</span><span class="sxs-lookup"><span data-stu-id="078a3-129">Required</span></span> | <span data-ttu-id="078a3-130">Ancho del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="078a3-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="078a3-131">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="078a3-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="078a3-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="078a3-132">**Height**</span></span> | <span data-ttu-id="078a3-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="078a3-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="078a3-134">Requerido</span><span class="sxs-lookup"><span data-stu-id="078a3-134">Required</span></span> | <span data-ttu-id="078a3-135">Alto del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="078a3-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="078a3-136">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="078a3-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="078a3-137">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="078a3-137">Element Information</span></span>



|  <span data-ttu-id="078a3-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="078a3-138">Element</span></span>     | <span data-ttu-id="078a3-139">Value</span><span class="sxs-lookup"><span data-stu-id="078a3-139">Value</span></span>                                                     |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="078a3-140">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="078a3-140">Element type</span></span> | <span data-ttu-id="078a3-141">[**ImageType**](imagetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="078a3-141">[**ImageType**](imagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="078a3-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="078a3-142">Namespace</span></span>    | <span data-ttu-id="078a3-143">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="078a3-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="078a3-144">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="078a3-144">Schema name</span></span>  | <span data-ttu-id="078a3-145">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="078a3-145">Journal Reader</span></span>                                          |



 

## <a name="see-also"></a><span data-ttu-id="078a3-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="078a3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="078a3-147">**Información previa**</span><span class="sxs-lookup"><span data-stu-id="078a3-147">**Background**</span></span>](background-element.md)
</dt> </dl>

 

 



