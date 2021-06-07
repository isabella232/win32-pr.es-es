---
description: Contiene el contenido de una página De diario.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Elemento Content [Lector de diario]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fec59601a91d63b09c703557b7c6cd28fd11620
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432157"
---
# <a name="content-element-journal-reader"></a><span data-ttu-id="0530a-103">Lector del diario \[ de elementos content\]</span><span class="sxs-lookup"><span data-stu-id="0530a-103">Content Element \[Journal Reader\]</span></span>

<span data-ttu-id="0530a-104">Contiene el contenido de una página De diario.</span><span class="sxs-lookup"><span data-stu-id="0530a-104">Contains the content for a Journal page.</span></span>

## <a name="definition"></a><span data-ttu-id="0530a-105">Definición</span><span class="sxs-lookup"><span data-stu-id="0530a-105">Definition</span></span>

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="0530a-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="0530a-106">Parent Elements</span></span>

[<span data-ttu-id="0530a-107">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="0530a-107">**JournalPage**</span></span>](journalpage-element.md)

## <a name="child-elements"></a><span data-ttu-id="0530a-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0530a-108">Child Elements</span></span>

[<span data-ttu-id="0530a-109">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="0530a-109">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="0530a-110">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="0530a-110">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="0530a-111">**Dibujo**</span><span class="sxs-lookup"><span data-stu-id="0530a-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="0530a-112">**Texto**</span><span class="sxs-lookup"><span data-stu-id="0530a-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="0530a-113">**Imagen**</span><span class="sxs-lookup"><span data-stu-id="0530a-113">**Image**</span></span>](image-element.md)

[<span data-ttu-id="0530a-114">**Marca**</span><span class="sxs-lookup"><span data-stu-id="0530a-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="0530a-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="0530a-115">Attributes</span></span>



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
<th><span data-ttu-id="0530a-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="0530a-116">Attribute</span></span></th>
<th><span data-ttu-id="0530a-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="0530a-117">Type</span></span></th>
<th><span data-ttu-id="0530a-118">Requerido</span><span class="sxs-lookup"><span data-stu-id="0530a-118">Required</span></span></th>
<th><span data-ttu-id="0530a-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="0530a-119">Description</span></span></th>
<th><span data-ttu-id="0530a-120">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="0530a-120">PossibleValues</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0530a-121"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="0530a-121"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="0530a-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span><span class="sxs-lookup"><span data-stu-id="0530a-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span></span></td>
<td><span data-ttu-id="0530a-123">Requerido</span><span class="sxs-lookup"><span data-stu-id="0530a-123">Required</span></span></td>
<td><span data-ttu-id="0530a-124">Si el tipo es &quot; Inert &quot; , no se puede modificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="0530a-124">If the type is &quot;Inert&quot;, then the content cannot be modified.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="0530a-125">Normal</span><span class="sxs-lookup"><span data-stu-id="0530a-125">Normal</span></span></li>
<li><span data-ttu-id="0530a-126">Inerte</span><span class="sxs-lookup"><span data-stu-id="0530a-126">Inert</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="0530a-127">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0530a-127">Element Information</span></span>



|  <span data-ttu-id="0530a-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="0530a-128">Element</span></span>     | <span data-ttu-id="0530a-129">Value</span><span class="sxs-lookup"><span data-stu-id="0530a-129">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="0530a-130">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0530a-130">Element type</span></span> | <span data-ttu-id="0530a-131">[**ContentType**](contenttype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="0530a-131">[**ContentType**](contenttype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="0530a-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0530a-132">Namespace</span></span>    | <span data-ttu-id="0530a-133">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="0530a-133">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="0530a-134">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="0530a-134">Schema name</span></span>  | <span data-ttu-id="0530a-135">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="0530a-135">Journal Reader</span></span>                                              |



 

 

 




