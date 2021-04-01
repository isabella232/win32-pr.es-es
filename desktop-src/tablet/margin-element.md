---
description: Define las líneas de margen dibujadas en la página.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Margin, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0500d4db165012393cb600c1e118089b68c76695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279167"
---
# <a name="margin-element"></a><span data-ttu-id="d00dc-103">Margin, elemento</span><span class="sxs-lookup"><span data-stu-id="d00dc-103">Margin Element</span></span>

<span data-ttu-id="d00dc-104">Define las líneas de margen dibujadas en la página.</span><span class="sxs-lookup"><span data-stu-id="d00dc-104">Defines the margin lines drawn on the page.</span></span>

## <a name="definition"></a><span data-ttu-id="d00dc-105">Definición</span><span class="sxs-lookup"><span data-stu-id="d00dc-105">Definition</span></span>

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a><span data-ttu-id="d00dc-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="d00dc-106">Parent Elements</span></span>

<span data-ttu-id="d00dc-107">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d00dc-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d00dc-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d00dc-108">Child Elements</span></span>

<span data-ttu-id="d00dc-109">Ninguno...</span><span class="sxs-lookup"><span data-stu-id="d00dc-109">None..</span></span>

## <a name="attributes"></a><span data-ttu-id="d00dc-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="d00dc-110">Attributes</span></span>



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
<th><span data-ttu-id="d00dc-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="d00dc-111">Attribute</span></span></th>
<th><span data-ttu-id="d00dc-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="d00dc-112">Type</span></span></th>
<th><span data-ttu-id="d00dc-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d00dc-113">Required</span></span></th>
<th><span data-ttu-id="d00dc-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d00dc-114">Description</span></span></th>
<th><span data-ttu-id="d00dc-115">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="d00dc-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d00dc-116"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="d00dc-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="d00dc-117">SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00dc-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="d00dc-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d00dc-118">Required</span></span></td>
<td><span data-ttu-id="d00dc-119">Especifica el tipo de línea que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="d00dc-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="d00dc-120">None</span><span class="sxs-lookup"><span data-stu-id="d00dc-120">None</span></span></li>
<li><span data-ttu-id="d00dc-121">Sólido</span><span class="sxs-lookup"><span data-stu-id="d00dc-121">Solid</span></span></li>
<li><span data-ttu-id="d00dc-122">Guión</span><span class="sxs-lookup"><span data-stu-id="d00dc-122">Dash</span></span></li>
<li><span data-ttu-id="d00dc-123">Punto</span><span class="sxs-lookup"><span data-stu-id="d00dc-123">Dot</span></span></li>
<li><span data-ttu-id="d00dc-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="d00dc-124">DashDot</span></span></li>
<li><span data-ttu-id="d00dc-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="d00dc-125">DashDotDot</span></span></li>
<li><span data-ttu-id="d00dc-126">Doble</span><span class="sxs-lookup"><span data-stu-id="d00dc-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00dc-127"><strong>Color</strong></span><span class="sxs-lookup"><span data-stu-id="d00dc-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="d00dc-128">SimpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00dc-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="d00dc-129">Opcionales</span><span class="sxs-lookup"><span data-stu-id="d00dc-129">Optional</span></span></td>
<td><span data-ttu-id="d00dc-130">Color del elemento.</span><span class="sxs-lookup"><span data-stu-id="d00dc-130">Color of the element.</span></span></td>
<td><span data-ttu-id="d00dc-131">Valor RGB hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="d00dc-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="d00dc-132">Coincide con la siguiente expresión regular: # [0-9-9 a-Z-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="d00dc-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="d00dc-133">Por ejemplo, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="d00dc-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00dc-134"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="d00dc-134"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="d00dc-135">SimpleType <a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a></span><span class="sxs-lookup"><span data-stu-id="d00dc-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="d00dc-136">Opcionales</span><span class="sxs-lookup"><span data-stu-id="d00dc-136">Optional</span></span></td>
<td><span data-ttu-id="d00dc-137">Indica el margen izquierdo o derecho.</span><span class="sxs-lookup"><span data-stu-id="d00dc-137">Indicates Left or Right margin.</span></span></td>
<td><ul>
<li><span data-ttu-id="d00dc-138">Left</span><span class="sxs-lookup"><span data-stu-id="d00dc-138">Left</span></span></li>
<li><span data-ttu-id="d00dc-139">Right</span><span class="sxs-lookup"><span data-stu-id="d00dc-139">Right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00dc-140"><strong>Espaciado</strong></span><span class="sxs-lookup"><span data-stu-id="d00dc-140"><strong>Spacing</strong></span></span></td>
<td><span data-ttu-id="d00dc-141"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="d00dc-141"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="d00dc-142">Opcionales</span><span class="sxs-lookup"><span data-stu-id="d00dc-142">Optional</span></span></td>
<td><span data-ttu-id="d00dc-143">Espaciado entre el borde de la página y el margen.</span><span class="sxs-lookup"><span data-stu-id="d00dc-143">Spacing between edge of page and margin.</span></span></td>
<td><span data-ttu-id="d00dc-144">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="d00dc-144">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="d00dc-145">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d00dc-145">Element Information</span></span>



|              |                                                           |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="d00dc-146">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d00dc-146">Element type</span></span> | <span data-ttu-id="d00dc-147">[**MarginType**](margintype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="d00dc-147">[**MarginType**](margintype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="d00dc-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d00dc-148">Namespace</span></span>    | <span data-ttu-id="d00dc-149">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="d00dc-149">urn:schemas-microsoft-com:tabletpc:richink</span></span>                |
| <span data-ttu-id="d00dc-150">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="d00dc-150">Schema name</span></span>  | <span data-ttu-id="d00dc-151">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="d00dc-151">Journal Reader</span></span>                                            |



 

 

 




