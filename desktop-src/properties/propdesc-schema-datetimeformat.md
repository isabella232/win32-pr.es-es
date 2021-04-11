---
description: 'Especifica cómo IPropertyDescription:: FormatForDisplay debe formatear el valor de la propiedad como una cadena. Esto solo es aplicable si <displayInfo displayType=&\#0034;DateTime&\#0034;> .'
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091898f77f4dcc37bbe65515f8606104a4d968bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276205"
---
# <a name="datetimeformat"></a><span data-ttu-id="9701b-104">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="9701b-104">dateTimeFormat</span></span>

<span data-ttu-id="9701b-105">Especifica cómo [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) debe formatear el valor de la propiedad como una cadena.</span><span class="sxs-lookup"><span data-stu-id="9701b-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="9701b-106">Esto solo es aplicable si <displayInfo displayType="DateTime"> .</span><span class="sxs-lookup"><span data-stu-id="9701b-106">This is applicable only if <displayInfo displayType="DateTime">.</span></span> <span data-ttu-id="9701b-107">Solo debe haber un elemento [DateTimeFormat]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="9701b-107">There should be only one [dateTimeFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="9701b-108">Si hay varios elementos, se usa el último.</span><span class="sxs-lookup"><span data-stu-id="9701b-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="9701b-109">Si no se proporciona ningún elemento [DateTimeFormat]() , se aplica la configuración de atributo predeterminada a la descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="9701b-109">If no [dateTimeFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="9701b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9701b-110">Syntax</span></span>


```
      <!-- dateTimeFormat -->
      <xs:element name="dateTimeFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Month"/>
                <xs:enumeration value="YearMonth"/>
                <xs:enumeration value="Year"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatTimeAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortTime"/>
                <xs:enumeration value="LongTime"/>
                <xs:enumeration value="HideTime"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDateAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortDate"/>
                <xs:enumeration value="LongDate"/>
                <xs:enumeration value="HideDate"/>
                <xs:enumeration value="RelativeShortDate"/>
                <xs:enumeration value="RelativeLongDate"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="9701b-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9701b-111">Element Information</span></span>



| <span data-ttu-id="9701b-112">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="9701b-112">Parent Element</span></span>                                   | <span data-ttu-id="9701b-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9701b-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="9701b-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="9701b-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="9701b-115">None</span><span class="sxs-lookup"><span data-stu-id="9701b-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="9701b-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="9701b-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9701b-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="9701b-117">Attribute</span></span></th>
<th><span data-ttu-id="9701b-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="9701b-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9701b-119">formatas</span><span class="sxs-lookup"><span data-stu-id="9701b-119">formatAs</span></span></td>
<td><span data-ttu-id="9701b-120">Público.</span><span class="sxs-lookup"><span data-stu-id="9701b-120">Public.</span></span> <span data-ttu-id="9701b-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9701b-121">Optional.</span></span> <span data-ttu-id="9701b-122">El valor predeterminado es &quot; General &quot; .</span><span class="sxs-lookup"><span data-stu-id="9701b-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="9701b-123">Estos son los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="9701b-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9701b-124">Value</span><span class="sxs-lookup"><span data-stu-id="9701b-124">Value</span></span></th>
<th><span data-ttu-id="9701b-125">Significado</span><span class="sxs-lookup"><span data-stu-id="9701b-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9701b-126">General</span><span class="sxs-lookup"><span data-stu-id="9701b-126">General</span></span></td>
<td><span data-ttu-id="9701b-127">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9701b-127">Default.</span></span> <span data-ttu-id="9701b-128">Da formato al valor de fecha y hora mediante <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9701b-128">Formats the date-time value using <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>.</span></span> <span data-ttu-id="9701b-129">Use los atributos <em>formatTimeAs</em> y <em>formatDateAs</em> para especificar cómo se da formato a la fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="9701b-129">Use the <em>formatTimeAs</em> and <em>formatDateAs</em> attributes to specify how the time and date are formatted.</span></span> <span data-ttu-id="9701b-130">Requiere que el tipo de propiedad sea DateTime.</span><span class="sxs-lookup"><span data-stu-id="9701b-130">Requires the property type to be DateTime.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9701b-131">Mes</span><span class="sxs-lookup"><span data-stu-id="9701b-131">Month</span></span></td>
<td><span data-ttu-id="9701b-132">Da formato al valor como uno de los meses del año.</span><span class="sxs-lookup"><span data-stu-id="9701b-132">Formats the value as one of the months of the year.</span></span> <span data-ttu-id="9701b-133">Requiere que el tipo de propiedad sea Int32.</span><span class="sxs-lookup"><span data-stu-id="9701b-133">Requires the property type to be Int32.</span></span> <span data-ttu-id="9701b-134">El valor debe almacenarse como un valor numérico con 1 que representa el primer mes del año.</span><span class="sxs-lookup"><span data-stu-id="9701b-134">The value must be stored as a numeric value with 1 representing the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9701b-135">YearMonth</span><span class="sxs-lookup"><span data-stu-id="9701b-135">YearMonth</span></span></td>
<td><span data-ttu-id="9701b-136">Da formato al valor como &quot; año-mes &quot; .</span><span class="sxs-lookup"><span data-stu-id="9701b-136">Formats the value as &quot;Year - Month&quot;.</span></span> <span data-ttu-id="9701b-137">Requiere que el tipo de propiedad sea Int32.</span><span class="sxs-lookup"><span data-stu-id="9701b-137">Requires the property type to be Int32.</span></span> <span data-ttu-id="9701b-138">El valor se debe almacenar de forma que los dos bytes más altos especifiquen el año y los dos bytes inferiores especifiquen el mes.</span><span class="sxs-lookup"><span data-stu-id="9701b-138">The value must be stored such that the two highest bytes specify the year and the lower two bytes specify the month.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9701b-139">Year</span><span class="sxs-lookup"><span data-stu-id="9701b-139">Year</span></span></td>
<td><span data-ttu-id="9701b-140">Da formato al valor como una cadena simple.</span><span class="sxs-lookup"><span data-stu-id="9701b-140">Formats the value as a simple string.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9701b-141">formatTimeAs</span><span class="sxs-lookup"><span data-stu-id="9701b-141">formatTimeAs</span></span></td>
<td><span data-ttu-id="9701b-142">Público.</span><span class="sxs-lookup"><span data-stu-id="9701b-142">Public.</span></span> <span data-ttu-id="9701b-143">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9701b-143">Optional.</span></span> <span data-ttu-id="9701b-144">El valor predeterminado es &quot; ShortTime &quot; .</span><span class="sxs-lookup"><span data-stu-id="9701b-144">Default is &quot;ShortTime&quot;.</span></span> <span data-ttu-id="9701b-145">Especifica el formato en el que se va a mostrar la hora.</span><span class="sxs-lookup"><span data-stu-id="9701b-145">Specifies the format in which to display time.</span></span> <span data-ttu-id="9701b-146">Se aplica cuando <strong>formatas &quot; = &quot; General</strong>.</span><span class="sxs-lookup"><span data-stu-id="9701b-146">Applies when <strong>formatAs=&quot;General&quot;</strong>.</span></span> <span data-ttu-id="9701b-147">Estos son los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="9701b-147">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9701b-148">Value</span><span class="sxs-lookup"><span data-stu-id="9701b-148">Value</span></span></th>
<th><span data-ttu-id="9701b-149">Significado</span><span class="sxs-lookup"><span data-stu-id="9701b-149">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9701b-150">ShortTime</span><span class="sxs-lookup"><span data-stu-id="9701b-150">ShortTime</span></span></td>
<td><span data-ttu-id="9701b-151">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9701b-151">Default.</span></span> <span data-ttu-id="9701b-152">Mostrar la hora como &quot; 7:48 PM &quot; .</span><span class="sxs-lookup"><span data-stu-id="9701b-152">Show the time like &quot;7:48 PM&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9701b-153">Sido</span><span class="sxs-lookup"><span data-stu-id="9701b-153">LongTime</span></span></td>
<td><span data-ttu-id="9701b-154">Mostrar la hora como &quot; 7:48:33 PM &quot; .</span><span class="sxs-lookup"><span data-stu-id="9701b-154">Show the time like &quot;7:48:33 PM&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9701b-155">HideTime</span><span class="sxs-lookup"><span data-stu-id="9701b-155">HideTime</span></span></td>
<td><span data-ttu-id="9701b-156">No muestra la parte de hora de la fecha.</span><span class="sxs-lookup"><span data-stu-id="9701b-156">Do not display the time portion of the date.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9701b-157">formatDateAs</span><span class="sxs-lookup"><span data-stu-id="9701b-157">formatDateAs</span></span></td>
<td><span data-ttu-id="9701b-158">Público.</span><span class="sxs-lookup"><span data-stu-id="9701b-158">Public.</span></span> <span data-ttu-id="9701b-159">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9701b-159">Optional.</span></span> <span data-ttu-id="9701b-160">El valor predeterminado es &quot; fechacorta &quot; .</span><span class="sxs-lookup"><span data-stu-id="9701b-160">Default is &quot;ShortDate&quot;.</span></span> <span data-ttu-id="9701b-161">Especifica el formato en el que se va a mostrar la fecha.</span><span class="sxs-lookup"><span data-stu-id="9701b-161">Specifies the format in which to display the date.</span></span> <span data-ttu-id="9701b-162">Se aplica cuando <strong>formatas &quot; = &quot; General</strong>.</span><span class="sxs-lookup"><span data-stu-id="9701b-162">Applies when <strong>formatAs=&quot;General&quot;</strong>.</span></span> <span data-ttu-id="9701b-163">Estos son los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="9701b-163">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9701b-164">Valor</span><span class="sxs-lookup"><span data-stu-id="9701b-164">Value</span></span></th>
<th><span data-ttu-id="9701b-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9701b-165">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9701b-166">Fechacorta</span><span class="sxs-lookup"><span data-stu-id="9701b-166">ShortDate</span></span></td>
<td><span data-ttu-id="9701b-167">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9701b-167">Default.</span></span> <span data-ttu-id="9701b-168">Muestra la fecha como &quot; 5/13/59 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9701b-168">Show the date like &quot;5/13/59&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9701b-169">LongDate</span><span class="sxs-lookup"><span data-stu-id="9701b-169">LongDate</span></span></td>
<td><span data-ttu-id="9701b-170">Mostrar la fecha como el &quot; miércoles, 13 de mayo de 1959 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9701b-170">Show the date like &quot;Wednesday, May 13, 1959&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9701b-171">HideDate</span><span class="sxs-lookup"><span data-stu-id="9701b-171">HideDate</span></span></td>
<td><span data-ttu-id="9701b-172">No mostrar la parte de la fecha.</span><span class="sxs-lookup"><span data-stu-id="9701b-172">Do not display the date portion.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9701b-173">RelativeShortDate</span><span class="sxs-lookup"><span data-stu-id="9701b-173">RelativeShortDate</span></span></td>
<td><span data-ttu-id="9701b-174">Muestre la fecha como &quot; fechacorta &quot; , pero use descripciones relativas, como &quot; ayer &quot; , siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="9701b-174">Show the date like &quot;ShortDate&quot;, but use relative descriptions, such as &quot;yesterday&quot;, whenever possible.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9701b-175">RelativeLongDate</span><span class="sxs-lookup"><span data-stu-id="9701b-175">RelativeLongDate</span></span></td>
<td><span data-ttu-id="9701b-176">Muestre la fecha como &quot; LongDate &quot; , pero use descripciones relativas, como &quot; ayer &quot; , siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="9701b-176">Show the date like &quot;LongDate&quot;, but use relative descriptions, such as &quot;yesterday&quot;, whenever possible.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
