---
description: Contiene información de texto de la nota de Journal.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Elemento Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c72fe584d0e796d4a6f897297aa60bbeddc5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002878"
---
# <a name="text-element"></a><span data-ttu-id="1914d-103">Elemento Text</span><span class="sxs-lookup"><span data-stu-id="1914d-103">Text Element</span></span>

<span data-ttu-id="1914d-104">Contiene información de texto de la nota de Journal.</span><span class="sxs-lookup"><span data-stu-id="1914d-104">Contains text information from the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="1914d-105">Definición</span><span class="sxs-lookup"><span data-stu-id="1914d-105">Definition</span></span>

<span data-ttu-id="1914d-106">Cuando se usa con [**contenido**](content-element--journal-reader.md):</span><span class="sxs-lookup"><span data-stu-id="1914d-106">When used with [**Content**](content-element--journal-reader.md):</span></span>

``` syntax
<xs:element name="Text" type="TextType" />
```

<span data-ttu-id="1914d-107">O bien, cuando se usa con [**TitleInfo**](titleinfo-element.md) y [**groupnode BizTalk**](groupnode-element.md):</span><span class="sxs-lookup"><span data-stu-id="1914d-107">Or, when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md):</span></span>

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a><span data-ttu-id="1914d-108">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="1914d-108">Parent Elements</span></span>

[<span data-ttu-id="1914d-109">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="1914d-109">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="1914d-110">**Groupnode BizTalk**</span><span class="sxs-lookup"><span data-stu-id="1914d-110">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="1914d-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="1914d-111">**TitleInfo**</span></span>](titleinfo-element.md)

## <a name="child-elements"></a><span data-ttu-id="1914d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1914d-112">Child Elements</span></span>

<span data-ttu-id="1914d-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1914d-113">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="1914d-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="1914d-114">Attributes</span></span>

<span data-ttu-id="1914d-115">No hay ningún atributo cuando se usa con [**TitleInfo**](titleinfo-element.md) y [**groupnode BizTalk**](groupnode-element.md).</span><span class="sxs-lookup"><span data-stu-id="1914d-115">There are no attributes when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md).</span></span> <span data-ttu-id="1914d-116">Cuando se usa con [**contenido**](content-element--journal-reader.md), los atributos son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="1914d-116">When used with [**Content**](content-element--journal-reader.md), the attributes are as follows.</span></span>



| <span data-ttu-id="1914d-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="1914d-117">Attribute</span></span>  | <span data-ttu-id="1914d-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="1914d-118">Type</span></span>                      | <span data-ttu-id="1914d-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1914d-119">Required</span></span> | <span data-ttu-id="1914d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="1914d-120">Description</span></span>                                                                             | <span data-ttu-id="1914d-121">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="1914d-121">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="1914d-122">**Left**</span><span class="sxs-lookup"><span data-stu-id="1914d-122">**Left**</span></span>   | <span data-ttu-id="1914d-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="1914d-123">**xs:integer**</span></span>            | <span data-ttu-id="1914d-124">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1914d-124">Required</span></span> | <span data-ttu-id="1914d-125">Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="1914d-125">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="1914d-126">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="1914d-126">Any integer.</span></span>              |
| <span data-ttu-id="1914d-127">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="1914d-127">**Top**</span></span>    | <span data-ttu-id="1914d-128">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="1914d-128">**xs:integer**</span></span>            | <span data-ttu-id="1914d-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1914d-129">Required</span></span> | <span data-ttu-id="1914d-130">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="1914d-130">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="1914d-131">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="1914d-131">Any integer.</span></span>              |
| <span data-ttu-id="1914d-132">**Width**</span><span class="sxs-lookup"><span data-stu-id="1914d-132">**Width**</span></span>  | <span data-ttu-id="1914d-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="1914d-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="1914d-134">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1914d-134">Required</span></span> | <span data-ttu-id="1914d-135">Ancho del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="1914d-135">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="1914d-136">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="1914d-136">Any non-negative integer.</span></span> |
| <span data-ttu-id="1914d-137">**Height**</span><span class="sxs-lookup"><span data-stu-id="1914d-137">**Height**</span></span> | <span data-ttu-id="1914d-138">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="1914d-138">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="1914d-139">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1914d-139">Required</span></span> | <span data-ttu-id="1914d-140">Alto del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="1914d-140">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="1914d-141">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="1914d-141">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="1914d-142">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1914d-142">Element Information</span></span>



|              |                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1914d-143">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1914d-143">Element type</span></span> | <span data-ttu-id="1914d-144">[**TextType**](texttype-complex-type.md) complexType (con el elemento Content) o **xs: String** (con elementos [**groupnode BizTalk**](groupnode-element.md) y [**TitleInfo**](titleinfo-element.md) )</span><span class="sxs-lookup"><span data-stu-id="1914d-144">[**TextType**](texttype-complex-type.md) complexType (with the Content element) or **xs:string** (with [**GroupNode**](groupnode-element.md) and [**TitleInfo**](titleinfo-element.md) elements)</span></span> |
| <span data-ttu-id="1914d-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1914d-145">Namespace</span></span>    | <span data-ttu-id="1914d-146">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="1914d-146">urn:schemas-microsoft-com:tabletpc:richink</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="1914d-147">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="1914d-147">Schema name</span></span>  | <span data-ttu-id="1914d-148">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="1914d-148">Journal Reader</span></span><br/>                                                                                                                                                                           |



 

 

 




