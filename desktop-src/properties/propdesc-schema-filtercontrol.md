---
description: Especifica el control que se va a usar en el menú de filtro de encabezado.
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: filterControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c0de28eaa349b9a999ba39c1bad47aa01d43d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666863"
---
# <a name="filtercontrol"></a><span data-ttu-id="2a022-103">filterControl</span><span class="sxs-lookup"><span data-stu-id="2a022-103">filterControl</span></span>

<span data-ttu-id="2a022-104">Especifica el control que se va a usar en el menú de filtro de encabezado.</span><span class="sxs-lookup"><span data-stu-id="2a022-104">Specifies what control to use in the header filter menu.</span></span> <span data-ttu-id="2a022-105">Solo debe haber un elemento [filterControl]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="2a022-105">There should be only one [filterControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="2a022-106">Si hay varios elementos, se usa el último.</span><span class="sxs-lookup"><span data-stu-id="2a022-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="2a022-107">Si no se proporciona ningún elemento [filterControl]() , los valores de atributo predeterminados se aplican a la descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="2a022-107">If no [filterControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a022-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a022-108">Syntax</span></span>


```
      <!-- filterControl -->
      <xs:element name="filterControl"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="control">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="Default"/>
                <xs:enumeration value="Calendar"/>
                <xs:enumeration value="Rating"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="2a022-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2a022-109">Element Information</span></span>



| <span data-ttu-id="2a022-110">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="2a022-110">Parent Element</span></span>                                   | <span data-ttu-id="2a022-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2a022-111">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="2a022-112">displayInfo</span><span class="sxs-lookup"><span data-stu-id="2a022-112">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="2a022-113">None</span><span class="sxs-lookup"><span data-stu-id="2a022-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="2a022-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="2a022-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a022-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="2a022-115">Attribute</span></span></th>
<th><span data-ttu-id="2a022-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a022-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a022-117">control</span><span class="sxs-lookup"><span data-stu-id="2a022-117">control</span></span></td>
<td><span data-ttu-id="2a022-118">Público.</span><span class="sxs-lookup"><span data-stu-id="2a022-118">Public.</span></span> <span data-ttu-id="2a022-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2a022-119">Optional.</span></span> <span data-ttu-id="2a022-120">El valor predeterminado es &quot; default &quot; .</span><span class="sxs-lookup"><span data-stu-id="2a022-120">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="2a022-121">Estos son los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="2a022-121">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a022-122">Value</span><span class="sxs-lookup"><span data-stu-id="2a022-122">Value</span></span></th>
<th><span data-ttu-id="2a022-123">Significado</span><span class="sxs-lookup"><span data-stu-id="2a022-123">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a022-124">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2a022-124">Default</span></span></td>
<td><span data-ttu-id="2a022-125">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2a022-125">Default.</span></span> <span data-ttu-id="2a022-126">Utiliza el control predeterminado, basado en el <typeInfo type=&quot;&quot;> atributo.</span><span class="sxs-lookup"><span data-stu-id="2a022-126">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="2a022-127">El tipo predeterminado es &quot; DateTime &quot; y el control predeterminado es &quot; Calendar &quot; .</span><span class="sxs-lookup"><span data-stu-id="2a022-127">The default type is &quot;DateTime&quot; and the default control is &quot;Calendar&quot;.</span></span> <span data-ttu-id="2a022-128">Cualquier otro tipo da como resultado un control de filtro especial.</span><span class="sxs-lookup"><span data-stu-id="2a022-128">Any other type results in no special filter control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a022-129">Calendario</span><span class="sxs-lookup"><span data-stu-id="2a022-129">Calendar</span></span></td>
<td><span data-ttu-id="2a022-130">Usa el control de calendario.</span><span class="sxs-lookup"><span data-stu-id="2a022-130">Uses the calendar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a022-131">Rating</span><span class="sxs-lookup"><span data-stu-id="2a022-131">Rating</span></span></td>
<td><span data-ttu-id="2a022-132">Usa el control de clasificación de 5 estrellas.</span><span class="sxs-lookup"><span data-stu-id="2a022-132">Uses the 5-star rating control.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
