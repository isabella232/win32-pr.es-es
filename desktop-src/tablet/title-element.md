---
description: Contiene información de título sobre la nota de Journal.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Elemento Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2362e286482b329c50788b8eae4b4a30cbd1a125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697752"
---
# <a name="title-element"></a><span data-ttu-id="168ae-103">Elemento Title</span><span class="sxs-lookup"><span data-stu-id="168ae-103">Title Element</span></span>

<span data-ttu-id="168ae-104">Contiene información de título sobre la nota de Journal.</span><span class="sxs-lookup"><span data-stu-id="168ae-104">Contains title information about the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="168ae-105">Definición</span><span class="sxs-lookup"><span data-stu-id="168ae-105">Definition</span></span>

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="168ae-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="168ae-106">Parent Elements</span></span>

[<span data-ttu-id="168ae-107">**Diseño de fondo**</span><span class="sxs-lookup"><span data-stu-id="168ae-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="168ae-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="168ae-108">Child Elements</span></span>

[<span data-ttu-id="168ae-109">**TitleArea**</span><span class="sxs-lookup"><span data-stu-id="168ae-109">**TitleArea**</span></span>](titlearea-element.md)

## <a name="attributes"></a><span data-ttu-id="168ae-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="168ae-110">Attributes</span></span>



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
<th><span data-ttu-id="168ae-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="168ae-111">Attribute</span></span></th>
<th><span data-ttu-id="168ae-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="168ae-112">Type</span></span></th>
<th><span data-ttu-id="168ae-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="168ae-113">Required</span></span></th>
<th><span data-ttu-id="168ae-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="168ae-114">Description</span></span></th>
<th><span data-ttu-id="168ae-115">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="168ae-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="168ae-116"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="168ae-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="168ae-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="168ae-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="168ae-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="168ae-118">Required</span></span></td>
<td><span data-ttu-id="168ae-119">Especifica el tipo de borde que rodea el título de la nota.</span><span class="sxs-lookup"><span data-stu-id="168ae-119">Specifies the type of border surrounding the title of the note.</span></span></td>
<td><ul>
<li><span data-ttu-id="168ae-120">None</span><span class="sxs-lookup"><span data-stu-id="168ae-120">None</span></span></li>
<li><span data-ttu-id="168ae-121">SolidSquare</span><span class="sxs-lookup"><span data-stu-id="168ae-121">SolidSquare</span></span></li>
<li><span data-ttu-id="168ae-122">OutlineSquare</span><span class="sxs-lookup"><span data-stu-id="168ae-122">OutlineSquare</span></span></li>
<li><span data-ttu-id="168ae-123">SolidRoundRect</span><span class="sxs-lookup"><span data-stu-id="168ae-123">SolidRoundRect</span></span></li>
<li><span data-ttu-id="168ae-124">OutlineRoundRect</span><span class="sxs-lookup"><span data-stu-id="168ae-124">OutlineRoundRect</span></span></li>
<li><span data-ttu-id="168ae-125">SolidRoundRectDottedBaseline</span><span class="sxs-lookup"><span data-stu-id="168ae-125">SolidRoundRectDottedBaseline</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="168ae-126"><strong>DateStyle</strong></span><span class="sxs-lookup"><span data-stu-id="168ae-126"><strong>DateStyle</strong></span></span></td>
<td><span data-ttu-id="168ae-127"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="168ae-127"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="168ae-128">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="168ae-128">Required</span></span></td>
<td><span data-ttu-id="168ae-129">Define si el título incluye o no una fecha.</span><span class="sxs-lookup"><span data-stu-id="168ae-129">Defines whether the title includes a date or not.</span></span></td>
<td><ul>
<li><span data-ttu-id="168ae-130">None</span><span class="sxs-lookup"><span data-stu-id="168ae-130">None</span></span></li>
<li><span data-ttu-id="168ae-131">Short</span><span class="sxs-lookup"><span data-stu-id="168ae-131">Short</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="168ae-132"><strong>Color</strong></span><span class="sxs-lookup"><span data-stu-id="168ae-132"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="168ae-133"><a href="colortype-simple-type.md"><strong>SimpleType de ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="168ae-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span></span></td>
<td><span data-ttu-id="168ae-134">Opcionales</span><span class="sxs-lookup"><span data-stu-id="168ae-134">Optional</span></span></td>
<td><span data-ttu-id="168ae-135">Especifica el color del fondo.</span><span class="sxs-lookup"><span data-stu-id="168ae-135">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="168ae-136">Consulte <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="168ae-136">See <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="168ae-137">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="168ae-137">Element Information</span></span>



|              |                                                         |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="168ae-138">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="168ae-138">Element type</span></span> | <span data-ttu-id="168ae-139">[**TitleType**](titletype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="168ae-139">[**TitleType**](titletype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="168ae-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="168ae-140">Namespace</span></span>    | <span data-ttu-id="168ae-141">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="168ae-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="168ae-142">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="168ae-142">Schema name</span></span>  | <span data-ttu-id="168ae-143">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="168ae-143">Journal Reader</span></span>                                          |



 

 

 



