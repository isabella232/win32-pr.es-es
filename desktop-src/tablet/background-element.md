---
description: Contiene el fondo de un elemento JournalDocument o un elemento JournalPage.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Background (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e58a836c7cfd13130779c1cd6b017105bcaa6321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716591"
---
# <a name="background-element"></a><span data-ttu-id="faf32-103">Background (elemento)</span><span class="sxs-lookup"><span data-stu-id="faf32-103">Background Element</span></span>

<span data-ttu-id="faf32-104">Contiene el fondo de un elemento [**JournalDocument**](journaldocument-element.md) o un elemento [**JournalPage**](journalpage-element.md) .</span><span class="sxs-lookup"><span data-stu-id="faf32-104">Contains the background for a [**JournalDocument**](journaldocument-element.md) element or [**JournalPage**](journalpage-element.md) element.</span></span>

## <a name="definition"></a><span data-ttu-id="faf32-105">Definición</span><span class="sxs-lookup"><span data-stu-id="faf32-105">Definition</span></span>

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="faf32-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="faf32-106">Parent Elements</span></span>

[<span data-ttu-id="faf32-107">**Diseño de fondo**</span><span class="sxs-lookup"><span data-stu-id="faf32-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="faf32-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="faf32-108">Child Elements</span></span>

[<span data-ttu-id="faf32-109">**Impresión**</span><span class="sxs-lookup"><span data-stu-id="faf32-109">**Image**</span></span>](image-element.md)

## <a name="attributes"></a><span data-ttu-id="faf32-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="faf32-110">Attributes</span></span>



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
<th><span data-ttu-id="faf32-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="faf32-111">Attribute</span></span></th>
<th><span data-ttu-id="faf32-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf32-112">Type</span></span></th>
<th><span data-ttu-id="faf32-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="faf32-113">Required</span></span></th>
<th><span data-ttu-id="faf32-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="faf32-114">Description</span></span></th>
<th><span data-ttu-id="faf32-115">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="faf32-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="faf32-116"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="faf32-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="faf32-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="faf32-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="faf32-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="faf32-118">Required</span></span></td>
<td><span data-ttu-id="faf32-119">Especifica el estilo del fondo.</span><span class="sxs-lookup"><span data-stu-id="faf32-119">Specifies the style of the background.</span></span></td>
<td><ul>
<li><span data-ttu-id="faf32-120">None</span><span class="sxs-lookup"><span data-stu-id="faf32-120">None</span></span></li>
<li><span data-ttu-id="faf32-121">Sólido</span><span class="sxs-lookup"><span data-stu-id="faf32-121">Solid</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf32-122"><strong>Color</strong></span><span class="sxs-lookup"><span data-stu-id="faf32-122"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="faf32-123">SimpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf32-123"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="faf32-124">Opcionales</span><span class="sxs-lookup"><span data-stu-id="faf32-124">Optional</span></span></td>
<td><span data-ttu-id="faf32-125">Especifica el color del fondo.</span><span class="sxs-lookup"><span data-stu-id="faf32-125">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="faf32-126">Consulte <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</span><span class="sxs-lookup"><span data-stu-id="faf32-126">See <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="faf32-127">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="faf32-127">Element Information</span></span>



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="faf32-128">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="faf32-128">Element type</span></span> | <span data-ttu-id="faf32-129">[**BackgroundType**](backgroundtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="faf32-129">[**BackgroundType**](backgroundtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="faf32-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="faf32-130">Namespace</span></span>    | <span data-ttu-id="faf32-131">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="faf32-131">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="faf32-132">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="faf32-132">Schema name</span></span>  | <span data-ttu-id="faf32-133">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="faf32-133">Journal Reader</span></span>                                                    |



 

 

 



