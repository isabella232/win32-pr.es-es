---
description: Contiene un párrafo.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Elemento Paragraph (Windows.ui.xaml.documents. h)
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
ms.openlocfilehash: bfe3752541bb54571e9802f557e83dcc7632f845
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660157"
---
# <a name="paragraph-element"></a><span data-ttu-id="87617-103">Elemento Paragraph</span><span class="sxs-lookup"><span data-stu-id="87617-103">Paragraph Element</span></span>

<span data-ttu-id="87617-104">Contiene un párrafo.</span><span class="sxs-lookup"><span data-stu-id="87617-104">Contains a paragraph.</span></span>

## <a name="definition"></a><span data-ttu-id="87617-105">Definición</span><span class="sxs-lookup"><span data-stu-id="87617-105">Definition</span></span>

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="87617-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="87617-106">Parent Elements</span></span>

[<span data-ttu-id="87617-107">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="87617-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="87617-108">**Groupnode BizTalk**</span><span class="sxs-lookup"><span data-stu-id="87617-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="87617-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="87617-109">Child Elements</span></span>

[<span data-ttu-id="87617-110">**Línea**</span><span class="sxs-lookup"><span data-stu-id="87617-110">**Line**</span></span>](line-element.md)

[<span data-ttu-id="87617-111">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="87617-111">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="attributes"></a><span data-ttu-id="87617-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="87617-112">Attributes</span></span>



| <span data-ttu-id="87617-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="87617-113">Attribute</span></span>       | <span data-ttu-id="87617-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="87617-114">Type</span></span>                      | <span data-ttu-id="87617-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="87617-115">Required</span></span> | <span data-ttu-id="87617-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="87617-116">Description</span></span>                                                                             | <span data-ttu-id="87617-117">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="87617-117">Possible Values</span></span>           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="87617-118">**Left**</span><span class="sxs-lookup"><span data-stu-id="87617-118">**Left**</span></span>        | <span data-ttu-id="87617-119">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="87617-119">**xs:integer**</span></span>            | <span data-ttu-id="87617-120">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="87617-120">Required</span></span> | <span data-ttu-id="87617-121">Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="87617-121">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="87617-122">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="87617-122">Any integer.</span></span>              |
| <span data-ttu-id="87617-123">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="87617-123">**Top**</span></span>         | <span data-ttu-id="87617-124">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="87617-124">**xs:integer**</span></span>            | <span data-ttu-id="87617-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="87617-125">Required</span></span> | <span data-ttu-id="87617-126">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="87617-126">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="87617-127">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="87617-127">Any integer.</span></span>              |
| <span data-ttu-id="87617-128">**Width**</span><span class="sxs-lookup"><span data-stu-id="87617-128">**Width**</span></span>       | <span data-ttu-id="87617-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="87617-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="87617-130">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="87617-130">Required</span></span> | <span data-ttu-id="87617-131">Ancho del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="87617-131">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="87617-132">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="87617-132">Any non-negative integer.</span></span> |
| <span data-ttu-id="87617-133">**Height**</span><span class="sxs-lookup"><span data-stu-id="87617-133">**Height**</span></span>      | <span data-ttu-id="87617-134">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="87617-134">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="87617-135">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="87617-135">Required</span></span> | <span data-ttu-id="87617-136">Alto del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="87617-136">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="87617-137">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="87617-137">Any non-negative integer.</span></span> |
| <span data-ttu-id="87617-138">**BlockNumber**</span><span class="sxs-lookup"><span data-stu-id="87617-138">**BlockNumber**</span></span> | <span data-ttu-id="87617-139">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="87617-139">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="87617-140">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="87617-140">Required</span></span> | <span data-ttu-id="87617-141">Número de bloque.</span><span class="sxs-lookup"><span data-stu-id="87617-141">Block number.</span></span>                                                                           | <span data-ttu-id="87617-142">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="87617-142">Any non-negative integer.</span></span> |
| <span data-ttu-id="87617-143">**LineNumber**</span><span class="sxs-lookup"><span data-stu-id="87617-143">**LineNumber**</span></span>  | <span data-ttu-id="87617-144">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="87617-144">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="87617-145">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="87617-145">Required</span></span> | <span data-ttu-id="87617-146">Línea en la que comienza el párrafo.</span><span class="sxs-lookup"><span data-stu-id="87617-146">The line on which the paragraph begins.</span></span>                                                 | <span data-ttu-id="87617-147">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="87617-147">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="87617-148">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="87617-148">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="87617-149">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="87617-149">Element type</span></span> | <span data-ttu-id="87617-150">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="87617-150">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="87617-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="87617-151">Namespace</span></span>    | <span data-ttu-id="87617-152">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="87617-152">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="87617-153">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="87617-153">Schema name</span></span>  | <span data-ttu-id="87617-154">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="87617-154">Journal Reader</span></span>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="87617-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87617-155">Requirements</span></span>



| <span data-ttu-id="87617-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="87617-156">Requirement</span></span> | <span data-ttu-id="87617-157">Value</span><span class="sxs-lookup"><span data-stu-id="87617-157">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87617-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87617-158">Header</span></span><br/> | <dl> <span data-ttu-id="87617-159"><dt>Windows.ui.xaml.documents. h</dt></span><span class="sxs-lookup"><span data-stu-id="87617-159"><dt>Windows.ui.xaml.documents.h</dt></span></span> </dl> |



 

 




