---
description: Contiene un párrafo.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Elemento Paragraph (Windows.ui.xaml.documents.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Paragraph
api_type:
- HeaderDef
api_location:
- windows.ui.xaml.documents.h
ms.openlocfilehash: 2f246294c80814ec809c0a1ca035fcb4741c30c5
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432237"
---
# <a name="paragraph-element"></a><span data-ttu-id="003c2-103">Elemento Paragraph</span><span class="sxs-lookup"><span data-stu-id="003c2-103">Paragraph Element</span></span>

<span data-ttu-id="003c2-104">Contiene un párrafo.</span><span class="sxs-lookup"><span data-stu-id="003c2-104">Contains a paragraph.</span></span>

## <a name="definition"></a><span data-ttu-id="003c2-105">Definición</span><span class="sxs-lookup"><span data-stu-id="003c2-105">Definition</span></span>

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="003c2-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="003c2-106">Parent Elements</span></span>

[<span data-ttu-id="003c2-107">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="003c2-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="003c2-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="003c2-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="003c2-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="003c2-109">Child Elements</span></span>

[<span data-ttu-id="003c2-110">**Línea**</span><span class="sxs-lookup"><span data-stu-id="003c2-110">**Line**</span></span>](line-element.md)

[<span data-ttu-id="003c2-111">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="003c2-111">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="attributes"></a><span data-ttu-id="003c2-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="003c2-112">Attributes</span></span>



| <span data-ttu-id="003c2-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="003c2-113">Attribute</span></span>       | <span data-ttu-id="003c2-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="003c2-114">Type</span></span>                      | <span data-ttu-id="003c2-115">Requerido</span><span class="sxs-lookup"><span data-stu-id="003c2-115">Required</span></span> | <span data-ttu-id="003c2-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="003c2-116">Description</span></span>                                                                             | <span data-ttu-id="003c2-117">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="003c2-117">Possible Values</span></span>           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="003c2-118">**Left**</span><span class="sxs-lookup"><span data-stu-id="003c2-118">**Left**</span></span>        | <span data-ttu-id="003c2-119">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="003c2-119">**xs:integer**</span></span>            | <span data-ttu-id="003c2-120">Requerido</span><span class="sxs-lookup"><span data-stu-id="003c2-120">Required</span></span> | <span data-ttu-id="003c2-121">Distancia desde el origen hasta el punto situado más a la izquierda en el cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="003c2-121">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="003c2-122">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="003c2-122">Any integer.</span></span>              |
| <span data-ttu-id="003c2-123">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="003c2-123">**Top**</span></span>         | <span data-ttu-id="003c2-124">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="003c2-124">**xs:integer**</span></span>            | <span data-ttu-id="003c2-125">Requerido</span><span class="sxs-lookup"><span data-stu-id="003c2-125">Required</span></span> | <span data-ttu-id="003c2-126">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="003c2-126">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="003c2-127">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="003c2-127">Any integer.</span></span>              |
| <span data-ttu-id="003c2-128">**Width**</span><span class="sxs-lookup"><span data-stu-id="003c2-128">**Width**</span></span>       | <span data-ttu-id="003c2-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="003c2-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="003c2-130">Requerido</span><span class="sxs-lookup"><span data-stu-id="003c2-130">Required</span></span> | <span data-ttu-id="003c2-131">Ancho del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="003c2-131">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="003c2-132">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="003c2-132">Any non-negative integer.</span></span> |
| <span data-ttu-id="003c2-133">**Height**</span><span class="sxs-lookup"><span data-stu-id="003c2-133">**Height**</span></span>      | <span data-ttu-id="003c2-134">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="003c2-134">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="003c2-135">Requerido</span><span class="sxs-lookup"><span data-stu-id="003c2-135">Required</span></span> | <span data-ttu-id="003c2-136">Alto del cuadro de límite para el elemento.</span><span class="sxs-lookup"><span data-stu-id="003c2-136">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="003c2-137">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="003c2-137">Any non-negative integer.</span></span> |
| <span data-ttu-id="003c2-138">**BlockNumber**</span><span class="sxs-lookup"><span data-stu-id="003c2-138">**BlockNumber**</span></span> | <span data-ttu-id="003c2-139">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="003c2-139">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="003c2-140">Requerido</span><span class="sxs-lookup"><span data-stu-id="003c2-140">Required</span></span> | <span data-ttu-id="003c2-141">Número de bloque.</span><span class="sxs-lookup"><span data-stu-id="003c2-141">Block number.</span></span>                                                                           | <span data-ttu-id="003c2-142">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="003c2-142">Any non-negative integer.</span></span> |
| <span data-ttu-id="003c2-143">**LineNumber**</span><span class="sxs-lookup"><span data-stu-id="003c2-143">**LineNumber**</span></span>  | <span data-ttu-id="003c2-144">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="003c2-144">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="003c2-145">Requerido</span><span class="sxs-lookup"><span data-stu-id="003c2-145">Required</span></span> | <span data-ttu-id="003c2-146">Línea en la que comienza el párrafo.</span><span class="sxs-lookup"><span data-stu-id="003c2-146">The line on which the paragraph begins.</span></span>                                                 | <span data-ttu-id="003c2-147">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="003c2-147">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="003c2-148">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="003c2-148">Element Information</span></span>



|  <span data-ttu-id="003c2-149">Elemento</span><span class="sxs-lookup"><span data-stu-id="003c2-149">Element</span></span>     | <span data-ttu-id="003c2-150">Value</span><span class="sxs-lookup"><span data-stu-id="003c2-150">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="003c2-151">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="003c2-151">Element type</span></span> | <span data-ttu-id="003c2-152">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="003c2-152">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="003c2-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="003c2-153">Namespace</span></span>    | <span data-ttu-id="003c2-154">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="003c2-154">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="003c2-155">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="003c2-155">Schema name</span></span>  | <span data-ttu-id="003c2-156">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="003c2-156">Journal Reader</span></span>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="003c2-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="003c2-157">Requirements</span></span>



| <span data-ttu-id="003c2-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="003c2-158">Requirement</span></span> | <span data-ttu-id="003c2-159">Value</span><span class="sxs-lookup"><span data-stu-id="003c2-159">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="003c2-160">Encabezado</span><span class="sxs-lookup"><span data-stu-id="003c2-160">Header</span></span><br/> | <dl> <span data-ttu-id="003c2-161"><dt>Windows.ui.xaml.documents.h</dt></span><span class="sxs-lookup"><span data-stu-id="003c2-161"><dt>Windows.ui.xaml.documents.h</dt></span></span> </dl> |



 

 




