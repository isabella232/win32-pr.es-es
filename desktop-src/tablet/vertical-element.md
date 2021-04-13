---
description: Contiene la información que describe el componente vertical de las líneas del diseño de fondo usado por la nota de Journal. Se utiliza, por ejemplo, cuando la nota tiene líneas de cuadrícula.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Elemento vertical
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 191a9c5cb3190cff9b1e379a68dbfab49ddc25a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360253"
---
# <a name="vertical-element"></a><span data-ttu-id="5468c-104">Elemento vertical</span><span class="sxs-lookup"><span data-stu-id="5468c-104">Vertical Element</span></span>

<span data-ttu-id="5468c-105">Contiene la información que describe el componente vertical de las líneas del diseño de fondo usado por la nota de Journal.</span><span class="sxs-lookup"><span data-stu-id="5468c-105">Contains the information that describes the vertical component of the lines in the stationery used by the Journal note.</span></span> <span data-ttu-id="5468c-106">Se utiliza, por ejemplo, cuando la nota tiene líneas de cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="5468c-106">Used, for example, when the note has grid lines.</span></span>

## <a name="definition"></a><span data-ttu-id="5468c-107">Definición</span><span class="sxs-lookup"><span data-stu-id="5468c-107">Definition</span></span>

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="5468c-108">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="5468c-108">Parent Elements</span></span>

[<span data-ttu-id="5468c-109">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="5468c-109">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="5468c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5468c-110">Child Elements</span></span>

<span data-ttu-id="5468c-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5468c-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="5468c-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="5468c-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5468c-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="5468c-113">Attribute</span></span></th>
<th><span data-ttu-id="5468c-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="5468c-114">Type</span></span></th>
<th><span data-ttu-id="5468c-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5468c-115">Required</span></span></th>
<th><span data-ttu-id="5468c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="5468c-116">Description</span></span></th>
<th><span data-ttu-id="5468c-117">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="5468c-117">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5468c-118"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="5468c-118"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="5468c-119">SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="5468c-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="5468c-120">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5468c-120">Required</span></span></td>
<td><span data-ttu-id="5468c-121">Especifica el tipo de línea que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="5468c-121">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="5468c-122">None</span><span class="sxs-lookup"><span data-stu-id="5468c-122">None</span></span></li>
<li><span data-ttu-id="5468c-123">Sólido</span><span class="sxs-lookup"><span data-stu-id="5468c-123">Solid</span></span></li>
<li><span data-ttu-id="5468c-124">Guión</span><span class="sxs-lookup"><span data-stu-id="5468c-124">Dash</span></span></li>
<li><span data-ttu-id="5468c-125">Punto</span><span class="sxs-lookup"><span data-stu-id="5468c-125">Dot</span></span></li>
<li><span data-ttu-id="5468c-126">DashDot</span><span class="sxs-lookup"><span data-stu-id="5468c-126">DashDot</span></span></li>
<li><span data-ttu-id="5468c-127">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="5468c-127">DashDotDot</span></span></li>
<li><span data-ttu-id="5468c-128">Doble</span><span class="sxs-lookup"><span data-stu-id="5468c-128">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5468c-129"><strong>Color</strong></span><span class="sxs-lookup"><span data-stu-id="5468c-129"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="5468c-130">SimpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="5468c-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="5468c-131">Opcionales</span><span class="sxs-lookup"><span data-stu-id="5468c-131">Optional</span></span></td>
<td><span data-ttu-id="5468c-132">Color del elemento.</span><span class="sxs-lookup"><span data-stu-id="5468c-132">Color of the element.</span></span></td>
<td><span data-ttu-id="5468c-133">Valor RGB hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="5468c-133">A hexadecimal RGB value.</span></span> <span data-ttu-id="5468c-134">Coincide con la siguiente expresión regular: # [0-9-9 a-Z-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="5468c-134">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="5468c-135">Por ejemplo, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="5468c-135">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5468c-136"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="5468c-136"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="5468c-137"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="5468c-137"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="5468c-138">Opcionales</span><span class="sxs-lookup"><span data-stu-id="5468c-138">Optional</span></span></td>
<td><span data-ttu-id="5468c-139">Espaciado antes del elemento.</span><span class="sxs-lookup"><span data-stu-id="5468c-139">Spacing before the element.</span></span></td>
<td><span data-ttu-id="5468c-140">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="5468c-140">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5468c-141"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="5468c-141"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="5468c-142"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="5468c-142"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="5468c-143">Opcionales</span><span class="sxs-lookup"><span data-stu-id="5468c-143">Optional</span></span></td>
<td><span data-ttu-id="5468c-144">Espaciado entre este elemento y los elementos circundantes.</span><span class="sxs-lookup"><span data-stu-id="5468c-144">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="5468c-145">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="5468c-145">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="5468c-146">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5468c-146">Element Information</span></span>



|              |                                                               |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="5468c-147">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5468c-147">Element type</span></span> | <span data-ttu-id="5468c-148">[**VerticalType**](verticaltype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="5468c-148">[**VerticalType**](verticaltype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="5468c-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5468c-149">Namespace</span></span>    | <span data-ttu-id="5468c-150">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="5468c-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="5468c-151">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="5468c-151">Schema name</span></span>  | <span data-ttu-id="5468c-152">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="5468c-152">Journal Reader</span></span>                                                |



 

 

 




