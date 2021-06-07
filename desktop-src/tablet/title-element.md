---
description: Contiene información de título sobre la nota de diario.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Elemento Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef687f809aae5c3722cdad84ee63d79c7bfcfb21
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432227"
---
# <a name="title-element"></a><span data-ttu-id="e974f-103">Elemento Title</span><span class="sxs-lookup"><span data-stu-id="e974f-103">Title Element</span></span>

<span data-ttu-id="e974f-104">Contiene información de título sobre la nota de diario.</span><span class="sxs-lookup"><span data-stu-id="e974f-104">Contains title information about the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="e974f-105">Definición</span><span class="sxs-lookup"><span data-stu-id="e974f-105">Definition</span></span>

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="e974f-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="e974f-106">Parent Elements</span></span>

[<span data-ttu-id="e974f-107">**Diseño de fondo**</span><span class="sxs-lookup"><span data-stu-id="e974f-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="e974f-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e974f-108">Child Elements</span></span>

[<span data-ttu-id="e974f-109">**TitleArea**</span><span class="sxs-lookup"><span data-stu-id="e974f-109">**TitleArea**</span></span>](titlearea-element.md)

## <a name="attributes"></a><span data-ttu-id="e974f-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="e974f-110">Attributes</span></span>



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
<th><span data-ttu-id="e974f-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="e974f-111">Attribute</span></span></th>
<th><span data-ttu-id="e974f-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="e974f-112">Type</span></span></th>
<th><span data-ttu-id="e974f-113">Requerido</span><span class="sxs-lookup"><span data-stu-id="e974f-113">Required</span></span></th>
<th><span data-ttu-id="e974f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e974f-114">Description</span></span></th>
<th><span data-ttu-id="e974f-115">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="e974f-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e974f-116"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="e974f-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="e974f-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="e974f-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="e974f-118">Requerido</span><span class="sxs-lookup"><span data-stu-id="e974f-118">Required</span></span></td>
<td><span data-ttu-id="e974f-119">Especifica el tipo de borde que rodea el título de la nota.</span><span class="sxs-lookup"><span data-stu-id="e974f-119">Specifies the type of border surrounding the title of the note.</span></span></td>
<td><ul>
<li><span data-ttu-id="e974f-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e974f-120">None</span></span></li>
<li><span data-ttu-id="e974f-121">SolidSquare</span><span class="sxs-lookup"><span data-stu-id="e974f-121">SolidSquare</span></span></li>
<li><span data-ttu-id="e974f-122">OutlineSquare</span><span class="sxs-lookup"><span data-stu-id="e974f-122">OutlineSquare</span></span></li>
<li><span data-ttu-id="e974f-123">SolidRoundRect</span><span class="sxs-lookup"><span data-stu-id="e974f-123">SolidRoundRect</span></span></li>
<li><span data-ttu-id="e974f-124">OutlineRoundRect</span><span class="sxs-lookup"><span data-stu-id="e974f-124">OutlineRoundRect</span></span></li>
<li><span data-ttu-id="e974f-125">SolidRoundRectDottedBaseline</span><span class="sxs-lookup"><span data-stu-id="e974f-125">SolidRoundRectDottedBaseline</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e974f-126"><strong>DateStyle</strong></span><span class="sxs-lookup"><span data-stu-id="e974f-126"><strong>DateStyle</strong></span></span></td>
<td><span data-ttu-id="e974f-127"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="e974f-127"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="e974f-128">Requerido</span><span class="sxs-lookup"><span data-stu-id="e974f-128">Required</span></span></td>
<td><span data-ttu-id="e974f-129">Define si el título incluye una fecha o no.</span><span class="sxs-lookup"><span data-stu-id="e974f-129">Defines whether the title includes a date or not.</span></span></td>
<td><ul>
<li><span data-ttu-id="e974f-130">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e974f-130">None</span></span></li>
<li><span data-ttu-id="e974f-131">Short</span><span class="sxs-lookup"><span data-stu-id="e974f-131">Short</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e974f-132"><strong>Color</strong></span><span class="sxs-lookup"><span data-stu-id="e974f-132"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="e974f-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="e974f-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span></span></td>
<td><span data-ttu-id="e974f-134">Opcionales</span><span class="sxs-lookup"><span data-stu-id="e974f-134">Optional</span></span></td>
<td><span data-ttu-id="e974f-135">Especifica el color del fondo.</span><span class="sxs-lookup"><span data-stu-id="e974f-135">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="e974f-136">Vea <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e974f-136">See <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="e974f-137">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e974f-137">Element Information</span></span>



| <span data-ttu-id="e974f-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="e974f-138">Element</span></span>      | <span data-ttu-id="e974f-139">Value</span><span class="sxs-lookup"><span data-stu-id="e974f-139">Value</span></span>                                                   |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="e974f-140">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e974f-140">Element type</span></span> | <span data-ttu-id="e974f-141">[**TitleType**](titletype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="e974f-141">[**TitleType**](titletype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="e974f-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e974f-142">Namespace</span></span>    | <span data-ttu-id="e974f-143">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="e974f-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="e974f-144">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="e974f-144">Schema name</span></span>  | <span data-ttu-id="e974f-145">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="e974f-145">Journal Reader</span></span>                                          |



 

 

 



