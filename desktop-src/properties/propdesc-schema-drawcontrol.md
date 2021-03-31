---
description: Especifica el control que se va a usar al mostrar simplemente la propiedad.
ms.assetid: 0fb8afc4-d16b-4c2e-80b3-da9935b11bb5
title: drawControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5318fdebc995ff45932f75b4000ceda6e74068e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082422"
---
# <a name="drawcontrol"></a><span data-ttu-id="98f4d-103">drawControl</span><span class="sxs-lookup"><span data-stu-id="98f4d-103">drawControl</span></span>

<span data-ttu-id="98f4d-104">Especifica el control que se va a usar al mostrar simplemente la propiedad.</span><span class="sxs-lookup"><span data-stu-id="98f4d-104">Specifies what control to use when simply displaying the property.</span></span> <span data-ttu-id="98f4d-105">Solo debe haber un elemento [drawControl]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="98f4d-105">There should be only one [drawControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="98f4d-106">Si hay varios elementos, se usa el último.</span><span class="sxs-lookup"><span data-stu-id="98f4d-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="98f4d-107">Si no se proporciona ningún elemento [drawControl]() , los valores de atributo predeterminados se aplican a la descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="98f4d-107">If no [drawControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

<span data-ttu-id="98f4d-108">Este formulario del control no permite la edición de propiedades.</span><span class="sxs-lookup"><span data-stu-id="98f4d-108">This form of the control does not allow for property editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="98f4d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98f4d-109">Syntax</span></span>


```
<!-- drawControl -->
<xs:element name="drawControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="PercentBar"/>
                    <xs:enumeration value="ProgressBar"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="StaticText"/>
                    <xs:enumeration value="IconList"/>
                    <xs:enumeration value="BooleanCheckMark"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="98f4d-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="98f4d-110">Element Information</span></span>



| <span data-ttu-id="98f4d-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="98f4d-111">Parent Element</span></span>                                   | <span data-ttu-id="98f4d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="98f4d-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="98f4d-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="98f4d-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="98f4d-114">None</span><span class="sxs-lookup"><span data-stu-id="98f4d-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="98f4d-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="98f4d-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98f4d-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="98f4d-116">Attribute</span></span></th>
<th><span data-ttu-id="98f4d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="98f4d-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98f4d-118">control</span><span class="sxs-lookup"><span data-stu-id="98f4d-118">control</span></span></td>
<td><span data-ttu-id="98f4d-119">Público.</span><span class="sxs-lookup"><span data-stu-id="98f4d-119">Public.</span></span> <span data-ttu-id="98f4d-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="98f4d-120">Optional.</span></span> <span data-ttu-id="98f4d-121">El valor predeterminado es &quot; default &quot; .</span><span class="sxs-lookup"><span data-stu-id="98f4d-121">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="98f4d-122">Estos son los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="98f4d-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="98f4d-123">Value</span><span class="sxs-lookup"><span data-stu-id="98f4d-123">Value</span></span></th>
<th><span data-ttu-id="98f4d-124">Significado</span><span class="sxs-lookup"><span data-stu-id="98f4d-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98f4d-125">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="98f4d-125">Default</span></span></td>
<td><span data-ttu-id="98f4d-126">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="98f4d-126">Default.</span></span> <span data-ttu-id="98f4d-127">Utiliza el control predeterminado, basado en el <typeInfo type=&quot;&quot;> atributo.</span><span class="sxs-lookup"><span data-stu-id="98f4d-127">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="98f4d-128">El tipo predeterminado es &quot; String &quot; (varios valores) y el control predeterminado es &quot; MultiValueText &quot; .</span><span class="sxs-lookup"><span data-stu-id="98f4d-128">The default type is &quot;String&quot; (multi-value) and the default control is &quot;MultiValueText&quot;.</span></span> <span data-ttu-id="98f4d-129">Cualquier otro tipo da como resultado el uso del &quot; &quot; control StaticText.</span><span class="sxs-lookup"><span data-stu-id="98f4d-129">Any other type results in using the &quot;StaticText&quot; control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98f4d-130">MultiLineText</span><span class="sxs-lookup"><span data-stu-id="98f4d-130">MultiLineText</span></span></td>
<td><span data-ttu-id="98f4d-131">Usa el control de texto de varias líneas.</span><span class="sxs-lookup"><span data-stu-id="98f4d-131">Uses the multi-line text control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98f4d-132">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="98f4d-132">MultiValueText</span></span></td>
<td><span data-ttu-id="98f4d-133">Usa el control de texto de varios valores.</span><span class="sxs-lookup"><span data-stu-id="98f4d-133">Uses the multi-value text control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98f4d-134">PercentBar</span><span class="sxs-lookup"><span data-stu-id="98f4d-134">PercentBar</span></span></td>
<td><span data-ttu-id="98f4d-135">Usa el control de barra de porcentaje.</span><span class="sxs-lookup"><span data-stu-id="98f4d-135">Uses the percent bar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98f4d-136">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="98f4d-136">ProgressBar</span></span></td>
<td><span data-ttu-id="98f4d-137">Usa el control de barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="98f4d-137">Uses the progress bar control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98f4d-138">Rating</span><span class="sxs-lookup"><span data-stu-id="98f4d-138">Rating</span></span></td>
<td><span data-ttu-id="98f4d-139">Usa el control de clasificación de 5 estrellas.</span><span class="sxs-lookup"><span data-stu-id="98f4d-139">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98f4d-140">StaticText</span><span class="sxs-lookup"><span data-stu-id="98f4d-140">StaticText</span></span></td>
<td><span data-ttu-id="98f4d-141">Usa <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription:: FormatForDisplay</strong></a> para mostrar el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="98f4d-141">Uses <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription::FormatForDisplay</strong></a> to display the property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98f4d-142">IconList</span><span class="sxs-lookup"><span data-stu-id="98f4d-142">IconList</span></span></td>
<td><span data-ttu-id="98f4d-143"><strong>Windows 7 y versiones posteriores.</strong></span><span class="sxs-lookup"><span data-stu-id="98f4d-143"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="98f4d-144">Una enumeración de iconos.</span><span class="sxs-lookup"><span data-stu-id="98f4d-144">An enumeration of icons.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98f4d-145">BooleanCheckMark</span><span class="sxs-lookup"><span data-stu-id="98f4d-145">BooleanCheckMark</span></span></td>
<td><span data-ttu-id="98f4d-146"><strong>Windows 7 y versiones posteriores.</strong></span><span class="sxs-lookup"><span data-stu-id="98f4d-146"><strong>Windows 7 and later.</strong></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
