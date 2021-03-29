---
description: Contiene información de formato para las líneas horizontales utilizadas para el diseño de fondo de una nota de Journal.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e380ca35f86ce1012084d31de732cd66c79363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810070"
---
# <a name="horizontal-element"></a><span data-ttu-id="53c65-103">Elemento horizontal</span><span class="sxs-lookup"><span data-stu-id="53c65-103">Horizontal Element</span></span>

<span data-ttu-id="53c65-104">Contiene información de formato para las líneas horizontales utilizadas para el diseño de fondo de una nota de Journal.</span><span class="sxs-lookup"><span data-stu-id="53c65-104">Contains formatting information for the horizontal lines used for the stationery in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="53c65-105">Definición</span><span class="sxs-lookup"><span data-stu-id="53c65-105">Definition</span></span>

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="53c65-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="53c65-106">Parent Elements</span></span>

[<span data-ttu-id="53c65-107">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="53c65-107">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="53c65-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="53c65-108">Child Elements</span></span>

<span data-ttu-id="53c65-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="53c65-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="53c65-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="53c65-110">Attributes</span></span>



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
<th><span data-ttu-id="53c65-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="53c65-111">Attribute</span></span></th>
<th><span data-ttu-id="53c65-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="53c65-112">Type</span></span></th>
<th><span data-ttu-id="53c65-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="53c65-113">Required</span></span></th>
<th><span data-ttu-id="53c65-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="53c65-114">Description</span></span></th>
<th><span data-ttu-id="53c65-115">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="53c65-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="53c65-116"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="53c65-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="53c65-117">SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="53c65-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="53c65-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="53c65-118">Required</span></span></td>
<td><span data-ttu-id="53c65-119">Especifica el tipo de línea que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="53c65-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="53c65-120">None</span><span class="sxs-lookup"><span data-stu-id="53c65-120">None</span></span></li>
<li><span data-ttu-id="53c65-121">Sólido</span><span class="sxs-lookup"><span data-stu-id="53c65-121">Solid</span></span></li>
<li><span data-ttu-id="53c65-122">Guión</span><span class="sxs-lookup"><span data-stu-id="53c65-122">Dash</span></span></li>
<li><span data-ttu-id="53c65-123">Punto</span><span class="sxs-lookup"><span data-stu-id="53c65-123">Dot</span></span></li>
<li><span data-ttu-id="53c65-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="53c65-124">DashDot</span></span></li>
<li><span data-ttu-id="53c65-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="53c65-125">DashDotDot</span></span></li>
<li><span data-ttu-id="53c65-126">Doble</span><span class="sxs-lookup"><span data-stu-id="53c65-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53c65-127"><strong>Color</strong></span><span class="sxs-lookup"><span data-stu-id="53c65-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="53c65-128">SimpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="53c65-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="53c65-129">Opcionales</span><span class="sxs-lookup"><span data-stu-id="53c65-129">Optional</span></span></td>
<td><span data-ttu-id="53c65-130">Color del elemento.</span><span class="sxs-lookup"><span data-stu-id="53c65-130">Color of the element.</span></span></td>
<td><span data-ttu-id="53c65-131">Valor RGB hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="53c65-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="53c65-132">Coincide con la siguiente expresión regular: # [0-9-9 a-Z-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="53c65-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="53c65-133">Por ejemplo, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="53c65-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53c65-134"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="53c65-134"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="53c65-135"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="53c65-135"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="53c65-136">Opcionales</span><span class="sxs-lookup"><span data-stu-id="53c65-136">Optional</span></span></td>
<td><span data-ttu-id="53c65-137">Espaciado antes del elemento.</span><span class="sxs-lookup"><span data-stu-id="53c65-137">Spacing before the element.</span></span></td>
<td><span data-ttu-id="53c65-138">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="53c65-138">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53c65-139"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="53c65-139"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="53c65-140"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="53c65-140"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="53c65-141">Opcionales</span><span class="sxs-lookup"><span data-stu-id="53c65-141">Optional</span></span></td>
<td><span data-ttu-id="53c65-142">Espaciado entre este elemento y los elementos circundantes.</span><span class="sxs-lookup"><span data-stu-id="53c65-142">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="53c65-143">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="53c65-143">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="53c65-144">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="53c65-144">Element Information</span></span>



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="53c65-145">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="53c65-145">Element type</span></span> | [<span data-ttu-id="53c65-146">**HorizontalType complexType**</span><span class="sxs-lookup"><span data-stu-id="53c65-146">**HorizontalType complexType**</span></span>](horizontaltype-complex-type.md) |
| <span data-ttu-id="53c65-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="53c65-147">Namespace</span></span>    | <span data-ttu-id="53c65-148">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="53c65-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="53c65-149">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="53c65-149">Schema name</span></span>  | <span data-ttu-id="53c65-150">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="53c65-150">Journal Reader</span></span>                                                    |



 

 

 




