---
description: Especifica el control que se va a usar al editar la propiedad.
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: editControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966f9742082fd6b5f939941a956eaae1ac4e427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002046"
---
# <a name="editcontrol"></a><span data-ttu-id="05664-103">editControl</span><span class="sxs-lookup"><span data-stu-id="05664-103">editControl</span></span>

<span data-ttu-id="05664-104">Especifica el control que se va a usar al editar la propiedad.</span><span class="sxs-lookup"><span data-stu-id="05664-104">Specifies what control to use when editing the property.</span></span> <span data-ttu-id="05664-105">Solo debe haber un elemento [editControl]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="05664-105">There should be only one [editControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="05664-106">Si hay varios elementos, se usa el último.</span><span class="sxs-lookup"><span data-stu-id="05664-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="05664-107">Si no se proporciona ningún elemento [editControl]() , los valores de atributo predeterminados se aplican a la descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="05664-107">If no [editControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

<span data-ttu-id="05664-108">Si <typeInfo isInnate="true"> es, este elemento se omite porque no se puede editar una propiedad innate.</span><span class="sxs-lookup"><span data-stu-id="05664-108">If <typeInfo isInnate="true">, this element is ignored because an innate property cannot be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="05664-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05664-109">Syntax</span></span>


```
<!-- editControl -->
<xs:element name="editControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                    <xs:enumeration value="IconList"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="05664-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="05664-110">Element Information</span></span>



| <span data-ttu-id="05664-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="05664-111">Parent Element</span></span>                                   | <span data-ttu-id="05664-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="05664-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="05664-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="05664-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="05664-114">None</span><span class="sxs-lookup"><span data-stu-id="05664-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="05664-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="05664-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="05664-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="05664-116">Attribute</span></span></th>
<th><span data-ttu-id="05664-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="05664-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="05664-118">control</span><span class="sxs-lookup"><span data-stu-id="05664-118">control</span></span></td>
<td><span data-ttu-id="05664-119">Público.</span><span class="sxs-lookup"><span data-stu-id="05664-119">Public.</span></span> <span data-ttu-id="05664-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="05664-120">Optional.</span></span> <span data-ttu-id="05664-121">El valor predeterminado es &quot; default &quot; .</span><span class="sxs-lookup"><span data-stu-id="05664-121">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="05664-122">Estos son los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="05664-122">The following are valid values.</span></span> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="05664-123">Value</span><span class="sxs-lookup"><span data-stu-id="05664-123">Value</span></span></th>
<th><span data-ttu-id="05664-124">Significado</span><span class="sxs-lookup"><span data-stu-id="05664-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="05664-125">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="05664-125">Default</span></span></td>
<td><span data-ttu-id="05664-126">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="05664-126">Default.</span></span> <span data-ttu-id="05664-127">Utiliza el control predeterminado, basado en el <typeInfo type=&quot;&quot;> atributo.</span><span class="sxs-lookup"><span data-stu-id="05664-127">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="05664-128">A continuación se enumeran los tipos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="05664-128">The default types are listed below.</span></span> <span data-ttu-id="05664-129">Cualquier otro tipo da como resultado el uso del &quot; control de texto &quot; .</span><span class="sxs-lookup"><span data-stu-id="05664-129">Any other type results in using the &quot;Text&quot; control.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="05664-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="05664-130">Type</span></span></th>
<th><span data-ttu-id="05664-131">Control</span><span class="sxs-lookup"><span data-stu-id="05664-131">Control</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="05664-132">String</span><span class="sxs-lookup"><span data-stu-id="05664-132">String</span></span></td>
<td><span data-ttu-id="05664-133">Texto</span><span class="sxs-lookup"><span data-stu-id="05664-133">Text</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05664-134">Cadena (varios valores)</span><span class="sxs-lookup"><span data-stu-id="05664-134">String (multi-value)</span></span></td>
<td><span data-ttu-id="05664-135">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="05664-135">MultiValueText</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05664-136">DateTime</span><span class="sxs-lookup"><span data-stu-id="05664-136">DateTime</span></span></td>
<td><span data-ttu-id="05664-137">Calendario</span><span class="sxs-lookup"><span data-stu-id="05664-137">Calendar</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05664-138">Calendario</span><span class="sxs-lookup"><span data-stu-id="05664-138">Calendar</span></span></td>
<td><span data-ttu-id="05664-139">Usa el control de calendario.</span><span class="sxs-lookup"><span data-stu-id="05664-139">Uses the calendar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05664-140">CheckboxDropList</span><span class="sxs-lookup"><span data-stu-id="05664-140">CheckboxDropList</span></span></td>
<td><span data-ttu-id="05664-141">Utiliza el control de lista con las casillas.</span><span class="sxs-lookup"><span data-stu-id="05664-141">Uses the list control with checkboxes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05664-142">Plegable</span><span class="sxs-lookup"><span data-stu-id="05664-142">DropList</span></span></td>
<td><span data-ttu-id="05664-143">Utiliza el control de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="05664-143">Uses the dropdown list control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05664-144">MultiLineText</span><span class="sxs-lookup"><span data-stu-id="05664-144">MultiLineText</span></span></td>
<td><span data-ttu-id="05664-145">Usa el control de edición de texto de varias líneas.</span><span class="sxs-lookup"><span data-stu-id="05664-145">Uses the multi-line text edit control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05664-146">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="05664-146">MultiValueText</span></span></td>
<td><span data-ttu-id="05664-147">Usa el control de edición de texto de varios valores.</span><span class="sxs-lookup"><span data-stu-id="05664-147">Uses the multi-value text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05664-148">Rating</span><span class="sxs-lookup"><span data-stu-id="05664-148">Rating</span></span></td>
<td><span data-ttu-id="05664-149">Usa el control de clasificación de 5 estrellas.</span><span class="sxs-lookup"><span data-stu-id="05664-149">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05664-150">Texto</span><span class="sxs-lookup"><span data-stu-id="05664-150">Text</span></span></td>
<td><span data-ttu-id="05664-151">Usa el control de edición de texto.</span><span class="sxs-lookup"><span data-stu-id="05664-151">Uses the text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05664-152">IconList</span><span class="sxs-lookup"><span data-stu-id="05664-152">IconList</span></span></td>
<td><span data-ttu-id="05664-153"><strong>Windows 7 y versiones posteriores.</strong></span><span class="sxs-lookup"><span data-stu-id="05664-153"><strong>Windows 7 and later.</strong></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
