---
description: Define las líneas de margen dibujadas en la página.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Elemento Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547177a10fc3724f3b9bf3dde65f857d03f0f2a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432137"
---
# <a name="margin-element"></a><span data-ttu-id="f9711-103">Elemento Margin</span><span class="sxs-lookup"><span data-stu-id="f9711-103">Margin Element</span></span>

<span data-ttu-id="f9711-104">Define las líneas de margen dibujadas en la página.</span><span class="sxs-lookup"><span data-stu-id="f9711-104">Defines the margin lines drawn on the page.</span></span>

## <a name="definition"></a><span data-ttu-id="f9711-105">Definición</span><span class="sxs-lookup"><span data-stu-id="f9711-105">Definition</span></span>

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a><span data-ttu-id="f9711-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="f9711-106">Parent Elements</span></span>

<span data-ttu-id="f9711-107">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f9711-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f9711-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f9711-108">Child Elements</span></span>

<span data-ttu-id="f9711-109">Ninguno..</span><span class="sxs-lookup"><span data-stu-id="f9711-109">None..</span></span>

## <a name="attributes"></a><span data-ttu-id="f9711-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="f9711-110">Attributes</span></span>



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
<th><span data-ttu-id="f9711-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="f9711-111">Attribute</span></span></th>
<th><span data-ttu-id="f9711-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9711-112">Type</span></span></th>
<th><span data-ttu-id="f9711-113">Requerido</span><span class="sxs-lookup"><span data-stu-id="f9711-113">Required</span></span></th>
<th><span data-ttu-id="f9711-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9711-114">Description</span></span></th>
<th><span data-ttu-id="f9711-115">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="f9711-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9711-116"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="f9711-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="f9711-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="f9711-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="f9711-118">Requerido</span><span class="sxs-lookup"><span data-stu-id="f9711-118">Required</span></span></td>
<td><span data-ttu-id="f9711-119">Especifica el tipo de línea que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="f9711-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="f9711-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f9711-120">None</span></span></li>
<li><span data-ttu-id="f9711-121">Sólido</span><span class="sxs-lookup"><span data-stu-id="f9711-121">Solid</span></span></li>
<li><span data-ttu-id="f9711-122">Guión</span><span class="sxs-lookup"><span data-stu-id="f9711-122">Dash</span></span></li>
<li><span data-ttu-id="f9711-123">Punto</span><span class="sxs-lookup"><span data-stu-id="f9711-123">Dot</span></span></li>
<li><span data-ttu-id="f9711-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="f9711-124">DashDot</span></span></li>
<li><span data-ttu-id="f9711-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="f9711-125">DashDotDot</span></span></li>
<li><span data-ttu-id="f9711-126">Double</span><span class="sxs-lookup"><span data-stu-id="f9711-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9711-127"><strong>Color</strong></span><span class="sxs-lookup"><span data-stu-id="f9711-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="f9711-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="f9711-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="f9711-129">Opcionales</span><span class="sxs-lookup"><span data-stu-id="f9711-129">Optional</span></span></td>
<td><span data-ttu-id="f9711-130">Color del elemento.</span><span class="sxs-lookup"><span data-stu-id="f9711-130">Color of the element.</span></span></td>
<td><span data-ttu-id="f9711-131">Valor RGB hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="f9711-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="f9711-132">Coincide con la siguiente expresión regular: #[0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="f9711-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="f9711-133">Por ejemplo, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="f9711-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9711-134"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="f9711-134"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="f9711-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="f9711-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="f9711-136">Opcionales</span><span class="sxs-lookup"><span data-stu-id="f9711-136">Optional</span></span></td>
<td><span data-ttu-id="f9711-137">Indica el margen izquierdo o derecho.</span><span class="sxs-lookup"><span data-stu-id="f9711-137">Indicates Left or Right margin.</span></span></td>
<td><ul>
<li><span data-ttu-id="f9711-138">Left</span><span class="sxs-lookup"><span data-stu-id="f9711-138">Left</span></span></li>
<li><span data-ttu-id="f9711-139">Right</span><span class="sxs-lookup"><span data-stu-id="f9711-139">Right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9711-140"><strong>Espaciado</strong></span><span class="sxs-lookup"><span data-stu-id="f9711-140"><strong>Spacing</strong></span></span></td>
<td><span data-ttu-id="f9711-141"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="f9711-141"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="f9711-142">Opcionales</span><span class="sxs-lookup"><span data-stu-id="f9711-142">Optional</span></span></td>
<td><span data-ttu-id="f9711-143">Espaciado entre el borde de la página y el margen.</span><span class="sxs-lookup"><span data-stu-id="f9711-143">Spacing between edge of page and margin.</span></span></td>
<td><span data-ttu-id="f9711-144">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="f9711-144">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="f9711-145">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="f9711-145">Element Information</span></span>



|  <span data-ttu-id="f9711-146">Elemento</span><span class="sxs-lookup"><span data-stu-id="f9711-146">Element</span></span>     | <span data-ttu-id="f9711-147">Value</span><span class="sxs-lookup"><span data-stu-id="f9711-147">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="f9711-148">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f9711-148">Element type</span></span> | <span data-ttu-id="f9711-149">[**MarginType**](margintype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="f9711-149">[**MarginType**](margintype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="f9711-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f9711-150">Namespace</span></span>    | <span data-ttu-id="f9711-151">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="f9711-151">urn:schemas-microsoft-com:tabletpc:richink</span></span>                |
| <span data-ttu-id="f9711-152">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="f9711-152">Schema name</span></span>  | <span data-ttu-id="f9711-153">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="f9711-153">Journal Reader</span></span>                                            |



 

 

 




