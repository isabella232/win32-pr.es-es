---
description: Define un grupo de atributos que se utiliza en una variedad de elementos de un archivo XML de diario. Contiene atributos que se usan para definir los límites (izquierda, superior, alto y ancho) de un elemento en el documento.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Grupo de atributos BoundsType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411a9d3ec30363e5c405cf27654330a0886f8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807981"
---
# <a name="boundstype-attribute-group"></a><span data-ttu-id="0c3be-104">Grupo de atributos BoundsType</span><span class="sxs-lookup"><span data-stu-id="0c3be-104">BoundsType Attribute Group</span></span>

<span data-ttu-id="0c3be-105">Define un grupo de atributos que se utiliza en una variedad de elementos de un archivo XML de diario.</span><span class="sxs-lookup"><span data-stu-id="0c3be-105">Defines an attribute group that is used by a variety of elements in a Journal XML file.</span></span> <span data-ttu-id="0c3be-106">Contiene atributos que se usan para definir los límites (izquierda, superior, alto y ancho) de un elemento en el documento.</span><span class="sxs-lookup"><span data-stu-id="0c3be-106">It contains attributes used to define the bounds (left, top, height, and width) of an element in the document.</span></span>

## <a name="definition"></a><span data-ttu-id="0c3be-107">Definición</span><span class="sxs-lookup"><span data-stu-id="0c3be-107">Definition</span></span>

``` syntax
<xs:attributeGroup name="BoundsType">
  <xs:attribute name="Left" use="required" type="xs:integer" />
  <xs:attribute name="Top" use="required" type="xs:integer" />
  <xs:attribute name="Width" use="required" type="xs:nonNegativeInteger" />
  <xs:attribute name="Height" use="required" type="xs: nonNegativeInteger" />
</xs:attributeGroup>
```

## <a name="child-elements"></a><span data-ttu-id="0c3be-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0c3be-108">Child Elements</span></span>

<span data-ttu-id="0c3be-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0c3be-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="0c3be-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="0c3be-110">Attributes</span></span>



| <span data-ttu-id="0c3be-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="0c3be-111">Attribute</span></span>  | <span data-ttu-id="0c3be-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c3be-112">Type</span></span>                      | <span data-ttu-id="0c3be-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="0c3be-113">Required</span></span> | <span data-ttu-id="0c3be-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c3be-114">Description</span></span>                                                                                        | <span data-ttu-id="0c3be-115">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="0c3be-115">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="0c3be-116">**Left**</span><span class="sxs-lookup"><span data-stu-id="0c3be-116">**Left**</span></span>   | <span data-ttu-id="0c3be-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="0c3be-117">**xs:integer**</span></span>            | <span data-ttu-id="0c3be-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="0c3be-118">Required</span></span> | <span data-ttu-id="0c3be-119">Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="0c3be-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="0c3be-120">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="0c3be-120">Any integer.</span></span><br/>              |
| <span data-ttu-id="0c3be-121">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="0c3be-121">**Top**</span></span>    | <span data-ttu-id="0c3be-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="0c3be-122">**xs:integer**</span></span>            | <span data-ttu-id="0c3be-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="0c3be-123">Required</span></span> | <span data-ttu-id="0c3be-124">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="0c3be-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="0c3be-125">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="0c3be-125">Any integer.</span></span><br/>              |
| <span data-ttu-id="0c3be-126">**Width**</span><span class="sxs-lookup"><span data-stu-id="0c3be-126">**Width**</span></span>  | <span data-ttu-id="0c3be-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="0c3be-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="0c3be-128">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="0c3be-128">Required</span></span> | <span data-ttu-id="0c3be-129">Ancho del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="0c3be-129">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="0c3be-130">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="0c3be-130">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="0c3be-131">**Height**</span><span class="sxs-lookup"><span data-stu-id="0c3be-131">**Height**</span></span> | <span data-ttu-id="0c3be-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="0c3be-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="0c3be-133">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="0c3be-133">Required</span></span> | <span data-ttu-id="0c3be-134">Alto del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="0c3be-134">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="0c3be-135">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="0c3be-135">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="0c3be-136">Información de tipo</span><span class="sxs-lookup"><span data-stu-id="0c3be-136">Type Information</span></span>



|             |                                            |
|-------------|--------------------------------------------|
| <span data-ttu-id="0c3be-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0c3be-137">Namespace</span></span>   | <span data-ttu-id="0c3be-138">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="0c3be-138">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="0c3be-139">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="0c3be-139">Schema name</span></span> | <span data-ttu-id="0c3be-140">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="0c3be-140">Journal Reader</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="0c3be-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c3be-141">Remarks</span></span>

<span data-ttu-id="0c3be-142">**Left** y **Top** pueden ser negativos porque el origen está definido por los márgenes, no por la página.</span><span class="sxs-lookup"><span data-stu-id="0c3be-142">**Left** and **Top** can be negative because the origin is defined by the margins, not the page.</span></span>

 

 




