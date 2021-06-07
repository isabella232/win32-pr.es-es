---
description: Contiene información de texto de la nota de diario.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Elemento Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570f613a06f9fe814bfb1acbdbdba040dbc1119f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432335"
---
# <a name="text-element"></a><span data-ttu-id="5127a-103">Elemento Text</span><span class="sxs-lookup"><span data-stu-id="5127a-103">Text Element</span></span>

<span data-ttu-id="5127a-104">Contiene información de texto de la nota de diario.</span><span class="sxs-lookup"><span data-stu-id="5127a-104">Contains text information from the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="5127a-105">Definición</span><span class="sxs-lookup"><span data-stu-id="5127a-105">Definition</span></span>

<span data-ttu-id="5127a-106">Cuando se usa con [**contenido**](content-element--journal-reader.md):</span><span class="sxs-lookup"><span data-stu-id="5127a-106">When used with [**Content**](content-element--journal-reader.md):</span></span>

``` syntax
<xs:element name="Text" type="TextType" />
```

<span data-ttu-id="5127a-107">O bien, cuando se usa [**con TitleInfo**](titleinfo-element.md) [**y GroupNode**](groupnode-element.md):</span><span class="sxs-lookup"><span data-stu-id="5127a-107">Or, when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md):</span></span>

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a><span data-ttu-id="5127a-108">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="5127a-108">Parent Elements</span></span>

[<span data-ttu-id="5127a-109">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="5127a-109">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="5127a-110">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="5127a-110">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="5127a-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="5127a-111">**TitleInfo**</span></span>](titleinfo-element.md)

## <a name="child-elements"></a><span data-ttu-id="5127a-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5127a-112">Child Elements</span></span>

<span data-ttu-id="5127a-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5127a-113">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="5127a-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="5127a-114">Attributes</span></span>

<span data-ttu-id="5127a-115">No hay ningún atributo cuando se usa [**con TitleInfo**](titleinfo-element.md) y [**GroupNode**](groupnode-element.md).</span><span class="sxs-lookup"><span data-stu-id="5127a-115">There are no attributes when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md).</span></span> <span data-ttu-id="5127a-116">Cuando se usa [**con Content**](content-element--journal-reader.md), los atributos son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="5127a-116">When used with [**Content**](content-element--journal-reader.md), the attributes are as follows.</span></span>



| <span data-ttu-id="5127a-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="5127a-117">Attribute</span></span>  | <span data-ttu-id="5127a-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="5127a-118">Type</span></span>                      | <span data-ttu-id="5127a-119">Requerido</span><span class="sxs-lookup"><span data-stu-id="5127a-119">Required</span></span> | <span data-ttu-id="5127a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="5127a-120">Description</span></span>                                                                             | <span data-ttu-id="5127a-121">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="5127a-121">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="5127a-122">**Left**</span><span class="sxs-lookup"><span data-stu-id="5127a-122">**Left**</span></span>   | <span data-ttu-id="5127a-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="5127a-123">**xs:integer**</span></span>            | <span data-ttu-id="5127a-124">Requerido</span><span class="sxs-lookup"><span data-stu-id="5127a-124">Required</span></span> | <span data-ttu-id="5127a-125">Distancia desde el origen hasta el punto situado más a la izquierda en el cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="5127a-125">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="5127a-126">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="5127a-126">Any integer.</span></span>              |
| <span data-ttu-id="5127a-127">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="5127a-127">**Top**</span></span>    | <span data-ttu-id="5127a-128">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="5127a-128">**xs:integer**</span></span>            | <span data-ttu-id="5127a-129">Requerido</span><span class="sxs-lookup"><span data-stu-id="5127a-129">Required</span></span> | <span data-ttu-id="5127a-130">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="5127a-130">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="5127a-131">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="5127a-131">Any integer.</span></span>              |
| <span data-ttu-id="5127a-132">**Width**</span><span class="sxs-lookup"><span data-stu-id="5127a-132">**Width**</span></span>  | <span data-ttu-id="5127a-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5127a-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5127a-134">Requerido</span><span class="sxs-lookup"><span data-stu-id="5127a-134">Required</span></span> | <span data-ttu-id="5127a-135">Ancho del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="5127a-135">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="5127a-136">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="5127a-136">Any non-negative integer.</span></span> |
| <span data-ttu-id="5127a-137">**Height**</span><span class="sxs-lookup"><span data-stu-id="5127a-137">**Height**</span></span> | <span data-ttu-id="5127a-138">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5127a-138">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5127a-139">Requerido</span><span class="sxs-lookup"><span data-stu-id="5127a-139">Required</span></span> | <span data-ttu-id="5127a-140">Alto del cuadro de límite para el elemento.</span><span class="sxs-lookup"><span data-stu-id="5127a-140">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="5127a-141">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="5127a-141">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="5127a-142">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5127a-142">Element Information</span></span>



|   <span data-ttu-id="5127a-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="5127a-143">Element</span></span>           |   <span data-ttu-id="5127a-144">Value</span><span class="sxs-lookup"><span data-stu-id="5127a-144">Value</span></span>                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5127a-145">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5127a-145">Element type</span></span> | <span data-ttu-id="5127a-146">[**TextType**](texttype-complex-type.md) complexType (con el elemento Content) o **xs:string** (con [**elementos GroupNode**](groupnode-element.md) [**y TitleInfo)**](titleinfo-element.md)</span><span class="sxs-lookup"><span data-stu-id="5127a-146">[**TextType**](texttype-complex-type.md) complexType (with the Content element) or **xs:string** (with [**GroupNode**](groupnode-element.md) and [**TitleInfo**](titleinfo-element.md) elements)</span></span> |
| <span data-ttu-id="5127a-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5127a-147">Namespace</span></span>    | <span data-ttu-id="5127a-148">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="5127a-148">urn:schemas-microsoft-com:tabletpc:richink</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="5127a-149">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="5127a-149">Schema name</span></span>  | <span data-ttu-id="5127a-150">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="5127a-150">Journal Reader</span></span><br/>                                                                                                                                                                           |



 

 

 




