---
description: Incluye el contenido de una página de diario.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Content (elemento) [Journal Reader]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b5a7c9631cd69d38b8db54e2a2f8e69636f7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697380"
---
# <a name="content-element-journal-reader"></a><span data-ttu-id="83a1d-103">Lector del diario de elementos de contenido \[\]</span><span class="sxs-lookup"><span data-stu-id="83a1d-103">Content Element \[Journal Reader\]</span></span>

<span data-ttu-id="83a1d-104">Incluye el contenido de una página de diario.</span><span class="sxs-lookup"><span data-stu-id="83a1d-104">Contains the content for a Journal page.</span></span>

## <a name="definition"></a><span data-ttu-id="83a1d-105">Definición</span><span class="sxs-lookup"><span data-stu-id="83a1d-105">Definition</span></span>

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="83a1d-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="83a1d-106">Parent Elements</span></span>

[<span data-ttu-id="83a1d-107">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="83a1d-107">**JournalPage**</span></span>](journalpage-element.md)

## <a name="child-elements"></a><span data-ttu-id="83a1d-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="83a1d-108">Child Elements</span></span>

[<span data-ttu-id="83a1d-109">**Groupnode BizTalk**</span><span class="sxs-lookup"><span data-stu-id="83a1d-109">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="83a1d-110">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="83a1d-110">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="83a1d-111">**Dibujo**</span><span class="sxs-lookup"><span data-stu-id="83a1d-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="83a1d-112">**Texto**</span><span class="sxs-lookup"><span data-stu-id="83a1d-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="83a1d-113">**Impresión**</span><span class="sxs-lookup"><span data-stu-id="83a1d-113">**Image**</span></span>](image-element.md)

[<span data-ttu-id="83a1d-114">**Marca**</span><span class="sxs-lookup"><span data-stu-id="83a1d-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="83a1d-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="83a1d-115">Attributes</span></span>



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
<th><span data-ttu-id="83a1d-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="83a1d-116">Attribute</span></span></th>
<th><span data-ttu-id="83a1d-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="83a1d-117">Type</span></span></th>
<th><span data-ttu-id="83a1d-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="83a1d-118">Required</span></span></th>
<th><span data-ttu-id="83a1d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="83a1d-119">Description</span></span></th>
<th><span data-ttu-id="83a1d-120">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="83a1d-120">PossibleValues</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="83a1d-121"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="83a1d-121"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="83a1d-122"><a href="contenttype-complex-type.md"><strong>ComplexType de ContentType</strong></a></span><span class="sxs-lookup"><span data-stu-id="83a1d-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span></span></td>
<td><span data-ttu-id="83a1d-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="83a1d-123">Required</span></span></td>
<td><span data-ttu-id="83a1d-124">Si el tipo es &quot; inerte &quot; , no se puede modificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="83a1d-124">If the type is &quot;Inert&quot;, then the content cannot be modified.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="83a1d-125">Normal</span><span class="sxs-lookup"><span data-stu-id="83a1d-125">Normal</span></span></li>
<li><span data-ttu-id="83a1d-126">Inert</span><span class="sxs-lookup"><span data-stu-id="83a1d-126">Inert</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="83a1d-127">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="83a1d-127">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="83a1d-128">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="83a1d-128">Element type</span></span> | <span data-ttu-id="83a1d-129">ComplexType de [**ContentType**](contenttype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="83a1d-129">[**ContentType**](contenttype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="83a1d-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="83a1d-130">Namespace</span></span>    | <span data-ttu-id="83a1d-131">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="83a1d-131">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="83a1d-132">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="83a1d-132">Schema name</span></span>  | <span data-ttu-id="83a1d-133">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="83a1d-133">Journal Reader</span></span>                                              |



 

 

 




