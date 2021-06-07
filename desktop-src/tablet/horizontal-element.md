---
description: Contiene información de formato para las líneas horizontales usadas para la papelería en una nota de diario.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento Horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de08008d0243d27f8a8c5f64d6aeac5ddbcc1c
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432387"
---
# <a name="horizontal-element"></a><span data-ttu-id="094ab-103">Elemento Horizontal</span><span class="sxs-lookup"><span data-stu-id="094ab-103">Horizontal Element</span></span>

<span data-ttu-id="094ab-104">Contiene información de formato para las líneas horizontales usadas para la papelería en una nota de diario.</span><span class="sxs-lookup"><span data-stu-id="094ab-104">Contains formatting information for the horizontal lines used for the stationery in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="094ab-105">Definición</span><span class="sxs-lookup"><span data-stu-id="094ab-105">Definition</span></span>

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="094ab-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="094ab-106">Parent Elements</span></span>

[<span data-ttu-id="094ab-107">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="094ab-107">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="094ab-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="094ab-108">Child Elements</span></span>

<span data-ttu-id="094ab-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="094ab-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="094ab-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="094ab-110">Attributes</span></span>



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
<th><span data-ttu-id="094ab-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="094ab-111">Attribute</span></span></th>
<th><span data-ttu-id="094ab-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="094ab-112">Type</span></span></th>
<th><span data-ttu-id="094ab-113">Requerido</span><span class="sxs-lookup"><span data-stu-id="094ab-113">Required</span></span></th>
<th><span data-ttu-id="094ab-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="094ab-114">Description</span></span></th>
<th><span data-ttu-id="094ab-115">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="094ab-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="094ab-116"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="094ab-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="094ab-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="094ab-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="094ab-118">Requerido</span><span class="sxs-lookup"><span data-stu-id="094ab-118">Required</span></span></td>
<td><span data-ttu-id="094ab-119">Especifica el tipo de línea que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="094ab-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="094ab-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="094ab-120">None</span></span></li>
<li><span data-ttu-id="094ab-121">Sólido</span><span class="sxs-lookup"><span data-stu-id="094ab-121">Solid</span></span></li>
<li><span data-ttu-id="094ab-122">Guión</span><span class="sxs-lookup"><span data-stu-id="094ab-122">Dash</span></span></li>
<li><span data-ttu-id="094ab-123">Punto</span><span class="sxs-lookup"><span data-stu-id="094ab-123">Dot</span></span></li>
<li><span data-ttu-id="094ab-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="094ab-124">DashDot</span></span></li>
<li><span data-ttu-id="094ab-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="094ab-125">DashDotDot</span></span></li>
<li><span data-ttu-id="094ab-126">Double</span><span class="sxs-lookup"><span data-stu-id="094ab-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="094ab-127"><strong>Color</strong></span><span class="sxs-lookup"><span data-stu-id="094ab-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="094ab-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="094ab-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="094ab-129">Opcionales</span><span class="sxs-lookup"><span data-stu-id="094ab-129">Optional</span></span></td>
<td><span data-ttu-id="094ab-130">Color del elemento.</span><span class="sxs-lookup"><span data-stu-id="094ab-130">Color of the element.</span></span></td>
<td><span data-ttu-id="094ab-131">Valor RGB hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="094ab-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="094ab-132">Coincide con la siguiente expresión regular: #[0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="094ab-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="094ab-133">Por ejemplo, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="094ab-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="094ab-134"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="094ab-134"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="094ab-135"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="094ab-135"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="094ab-136">Opcionales</span><span class="sxs-lookup"><span data-stu-id="094ab-136">Optional</span></span></td>
<td><span data-ttu-id="094ab-137">Espaciado delante del elemento.</span><span class="sxs-lookup"><span data-stu-id="094ab-137">Spacing before the element.</span></span></td>
<td><span data-ttu-id="094ab-138">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="094ab-138">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="094ab-139"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="094ab-139"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="094ab-140"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="094ab-140"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="094ab-141">Opcionales</span><span class="sxs-lookup"><span data-stu-id="094ab-141">Optional</span></span></td>
<td><span data-ttu-id="094ab-142">Espaciado entre este elemento y los elementos circundantes.</span><span class="sxs-lookup"><span data-stu-id="094ab-142">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="094ab-143">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="094ab-143">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="094ab-144">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="094ab-144">Element Information</span></span>



|  <span data-ttu-id="094ab-145">Elemento</span><span class="sxs-lookup"><span data-stu-id="094ab-145">Element</span></span>     | <span data-ttu-id="094ab-146">Value</span><span class="sxs-lookup"><span data-stu-id="094ab-146">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="094ab-147">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="094ab-147">Element type</span></span> | [<span data-ttu-id="094ab-148">**HorizontalType complexType**</span><span class="sxs-lookup"><span data-stu-id="094ab-148">**HorizontalType complexType**</span></span>](horizontaltype-complex-type.md) |
| <span data-ttu-id="094ab-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="094ab-149">Namespace</span></span>    | <span data-ttu-id="094ab-150">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="094ab-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="094ab-151">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="094ab-151">Schema name</span></span>  | <span data-ttu-id="094ab-152">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="094ab-152">Journal Reader</span></span>                                                    |



 

 

 




