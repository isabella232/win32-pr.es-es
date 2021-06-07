---
description: Contiene la información que describe el componente vertical de las líneas de la papelería usada por la nota de diario. Se usa, por ejemplo, cuando la nota tiene líneas de cuadrícula.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Elemento Vertical
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42565e6f2828c4ef27d1b28830502303a03e6f13
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432127"
---
# <a name="vertical-element"></a><span data-ttu-id="99211-104">Elemento Vertical</span><span class="sxs-lookup"><span data-stu-id="99211-104">Vertical Element</span></span>

<span data-ttu-id="99211-105">Contiene la información que describe el componente vertical de las líneas de la papelería usada por la nota de diario.</span><span class="sxs-lookup"><span data-stu-id="99211-105">Contains the information that describes the vertical component of the lines in the stationery used by the Journal note.</span></span> <span data-ttu-id="99211-106">Se usa, por ejemplo, cuando la nota tiene líneas de cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="99211-106">Used, for example, when the note has grid lines.</span></span>

## <a name="definition"></a><span data-ttu-id="99211-107">Definición</span><span class="sxs-lookup"><span data-stu-id="99211-107">Definition</span></span>

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="99211-108">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="99211-108">Parent Elements</span></span>

[<span data-ttu-id="99211-109">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="99211-109">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="99211-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="99211-110">Child Elements</span></span>

<span data-ttu-id="99211-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="99211-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="99211-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="99211-112">Attributes</span></span>



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
<th><span data-ttu-id="99211-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="99211-113">Attribute</span></span></th>
<th><span data-ttu-id="99211-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="99211-114">Type</span></span></th>
<th><span data-ttu-id="99211-115">Requerido</span><span class="sxs-lookup"><span data-stu-id="99211-115">Required</span></span></th>
<th><span data-ttu-id="99211-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="99211-116">Description</span></span></th>
<th><span data-ttu-id="99211-117">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="99211-117">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="99211-118"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="99211-118"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="99211-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="99211-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="99211-120">Requerido</span><span class="sxs-lookup"><span data-stu-id="99211-120">Required</span></span></td>
<td><span data-ttu-id="99211-121">Especifica el tipo de línea que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="99211-121">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="99211-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="99211-122">None</span></span></li>
<li><span data-ttu-id="99211-123">Sólido</span><span class="sxs-lookup"><span data-stu-id="99211-123">Solid</span></span></li>
<li><span data-ttu-id="99211-124">Guión</span><span class="sxs-lookup"><span data-stu-id="99211-124">Dash</span></span></li>
<li><span data-ttu-id="99211-125">Punto</span><span class="sxs-lookup"><span data-stu-id="99211-125">Dot</span></span></li>
<li><span data-ttu-id="99211-126">DashDot</span><span class="sxs-lookup"><span data-stu-id="99211-126">DashDot</span></span></li>
<li><span data-ttu-id="99211-127">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="99211-127">DashDotDot</span></span></li>
<li><span data-ttu-id="99211-128">Double</span><span class="sxs-lookup"><span data-stu-id="99211-128">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99211-129"><strong>Color</strong></span><span class="sxs-lookup"><span data-stu-id="99211-129"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="99211-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="99211-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="99211-131">Opcionales</span><span class="sxs-lookup"><span data-stu-id="99211-131">Optional</span></span></td>
<td><span data-ttu-id="99211-132">Color del elemento.</span><span class="sxs-lookup"><span data-stu-id="99211-132">Color of the element.</span></span></td>
<td><span data-ttu-id="99211-133">Valor RGB hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="99211-133">A hexadecimal RGB value.</span></span> <span data-ttu-id="99211-134">Coincide con la siguiente expresión regular: #[0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="99211-134">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="99211-135">Por ejemplo, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="99211-135">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99211-136"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="99211-136"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="99211-137"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="99211-137"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="99211-138">Opcionales</span><span class="sxs-lookup"><span data-stu-id="99211-138">Optional</span></span></td>
<td><span data-ttu-id="99211-139">Espaciado delante del elemento.</span><span class="sxs-lookup"><span data-stu-id="99211-139">Spacing before the element.</span></span></td>
<td><span data-ttu-id="99211-140">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="99211-140">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99211-141"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="99211-141"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="99211-142"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="99211-142"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="99211-143">Opcionales</span><span class="sxs-lookup"><span data-stu-id="99211-143">Optional</span></span></td>
<td><span data-ttu-id="99211-144">Espaciado entre este elemento y los elementos circundantes.</span><span class="sxs-lookup"><span data-stu-id="99211-144">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="99211-145">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="99211-145">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="99211-146">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="99211-146">Element Information</span></span>



|  <span data-ttu-id="99211-147">Elemento</span><span class="sxs-lookup"><span data-stu-id="99211-147">Element</span></span>     | <span data-ttu-id="99211-148">Value</span><span class="sxs-lookup"><span data-stu-id="99211-148">Value</span></span>                                                         |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="99211-149">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="99211-149">Element type</span></span> | <span data-ttu-id="99211-150">[**VerticalType**](verticaltype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="99211-150">[**VerticalType**](verticaltype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="99211-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="99211-151">Namespace</span></span>    | <span data-ttu-id="99211-152">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="99211-152">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="99211-153">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="99211-153">Schema name</span></span>  | <span data-ttu-id="99211-154">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="99211-154">Journal Reader</span></span>                                                |



 

 

 




