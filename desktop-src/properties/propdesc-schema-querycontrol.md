---
description: No se admite en Windows 7 y versiones posteriores. Especifica el control que se va a usar en el generador de consultas.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: Consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448b47038f82afb9f860209bfe89eb9e6eecb890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666856"
---
# <a name="querycontrol"></a><span data-ttu-id="fe836-104">Consulta</span><span class="sxs-lookup"><span data-stu-id="fe836-104">queryControl</span></span>

<span data-ttu-id="fe836-105">No se admite en Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="fe836-105">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="fe836-106">Especifica el control que se va a usar en el generador de consultas.</span><span class="sxs-lookup"><span data-stu-id="fe836-106">Specifies what control to use in the query builder.</span></span> <span data-ttu-id="fe836-107">Solo debe haber un elemento [consulta]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="fe836-107">There should be only one [queryControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="fe836-108">Si hay varios elementos, se usa el último.</span><span class="sxs-lookup"><span data-stu-id="fe836-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="fe836-109">Si no se proporciona ningún elemento [consulta]() , los valores de atributo predeterminados se aplican a la descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="fe836-109">If no [queryControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe836-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe836-110">Syntax</span></span>


```
<!-- queryControl -->
<xs:element name="queryControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="NumericText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="fe836-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fe836-111">Element Information</span></span>



| <span data-ttu-id="fe836-112">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="fe836-112">Parent Element</span></span>                                   | <span data-ttu-id="fe836-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fe836-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="fe836-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="fe836-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="fe836-115">None</span><span class="sxs-lookup"><span data-stu-id="fe836-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="fe836-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="fe836-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe836-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="fe836-117">Attribute</span></span></th>
<th><span data-ttu-id="fe836-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe836-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe836-119">control</span><span class="sxs-lookup"><span data-stu-id="fe836-119">control</span></span></td>
<td><span data-ttu-id="fe836-120">Público.</span><span class="sxs-lookup"><span data-stu-id="fe836-120">Public.</span></span> <span data-ttu-id="fe836-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fe836-121">Optional.</span></span> <span data-ttu-id="fe836-122">El valor predeterminado es &quot; default &quot; .</span><span class="sxs-lookup"><span data-stu-id="fe836-122">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="fe836-123">Estos son los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="fe836-123">The following are valid values.</span></span> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe836-124">Value</span><span class="sxs-lookup"><span data-stu-id="fe836-124">Value</span></span></th>
<th><span data-ttu-id="fe836-125">Significado</span><span class="sxs-lookup"><span data-stu-id="fe836-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe836-126">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="fe836-126">Default</span></span></td>
<td><span data-ttu-id="fe836-127">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fe836-127">Default.</span></span> <span data-ttu-id="fe836-128">Utiliza el control predeterminado, basado en el <typeInfo type=&quot;&quot;> atributo.</span><span class="sxs-lookup"><span data-stu-id="fe836-128">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="fe836-129">A continuación se enumeran los tipos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="fe836-129">The default types are listed below.</span></span> <span data-ttu-id="fe836-130">Cualquier otro tipo da como resultado el uso del &quot; control de texto &quot; .</span><span class="sxs-lookup"><span data-stu-id="fe836-130">Any other type results in using the &quot;Text&quot; control.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="fe836-131">ConditionType</span><span class="sxs-lookup"><span data-stu-id="fe836-131">ConditionType</span></span></th>
<th><span data-ttu-id="fe836-132">Control</span><span class="sxs-lookup"><span data-stu-id="fe836-132">Control</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe836-133">String</span><span class="sxs-lookup"><span data-stu-id="fe836-133">String</span></span></td>
<td><span data-ttu-id="fe836-134">Texto</span><span class="sxs-lookup"><span data-stu-id="fe836-134">Text</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe836-135">Cadena (varios valores)</span><span class="sxs-lookup"><span data-stu-id="fe836-135">String (multi-value)</span></span></td>
<td><span data-ttu-id="fe836-136">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="fe836-136">MultiValueText</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe836-137">Número o tamaño</span><span class="sxs-lookup"><span data-stu-id="fe836-137">Number or Size</span></span></td>
<td><span data-ttu-id="fe836-138">NumericText</span><span class="sxs-lookup"><span data-stu-id="fe836-138">NumericText</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe836-139">Número o tamaño (enumeración)</span><span class="sxs-lookup"><span data-stu-id="fe836-139">Number or Size (enum)</span></span></td>
<td><span data-ttu-id="fe836-140">List</span><span class="sxs-lookup"><span data-stu-id="fe836-140">List</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe836-141">DateTime</span><span class="sxs-lookup"><span data-stu-id="fe836-141">DateTime</span></span></td>
<td><span data-ttu-id="fe836-142">Calendario</span><span class="sxs-lookup"><span data-stu-id="fe836-142">Calendar</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe836-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="fe836-143">Boolean</span></span></td>
<td><span data-ttu-id="fe836-144">Boolean</span><span class="sxs-lookup"><span data-stu-id="fe836-144">Boolean</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe836-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="fe836-145">Boolean</span></span></td>
<td><span data-ttu-id="fe836-146">Utiliza el control booleano.</span><span class="sxs-lookup"><span data-stu-id="fe836-146">Uses the boolean control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe836-147">Calendario</span><span class="sxs-lookup"><span data-stu-id="fe836-147">Calendar</span></span></td>
<td><span data-ttu-id="fe836-148">Usa el control de calendario desplegable.</span><span class="sxs-lookup"><span data-stu-id="fe836-148">Uses the dropdown calendar control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe836-149">CheckboxDropList</span><span class="sxs-lookup"><span data-stu-id="fe836-149">CheckboxDropList</span></span></td>
<td><span data-ttu-id="fe836-150">Utiliza el control de lista con las casillas.</span><span class="sxs-lookup"><span data-stu-id="fe836-150">Uses the list control with checkboxes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe836-151">Plegable</span><span class="sxs-lookup"><span data-stu-id="fe836-151">DropList</span></span></td>
<td><span data-ttu-id="fe836-152">Utiliza el control de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="fe836-152">Uses the dropdown list control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe836-153">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="fe836-153">MultiValueText</span></span></td>
<td><span data-ttu-id="fe836-154">Usa el control de edición de texto de varios valores.</span><span class="sxs-lookup"><span data-stu-id="fe836-154">Uses the multi-value text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe836-155">NumericText</span><span class="sxs-lookup"><span data-stu-id="fe836-155">NumericText</span></span></td>
<td><span data-ttu-id="fe836-156">Usa el control de edición de texto numérico.</span><span class="sxs-lookup"><span data-stu-id="fe836-156">Uses the numeric text edit control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe836-157">Rating</span><span class="sxs-lookup"><span data-stu-id="fe836-157">Rating</span></span></td>
<td><span data-ttu-id="fe836-158">Usa el control de clasificación de 5 estrellas.</span><span class="sxs-lookup"><span data-stu-id="fe836-158">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe836-159">Texto</span><span class="sxs-lookup"><span data-stu-id="fe836-159">Text</span></span></td>
<td><span data-ttu-id="fe836-160">Usa el control de edición de texto.</span><span class="sxs-lookup"><span data-stu-id="fe836-160">Uses the text edit control.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
