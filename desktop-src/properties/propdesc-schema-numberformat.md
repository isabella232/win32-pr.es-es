---
description: 'Especifica cómo IPropertyDescription:: FormatForDisplay debe formatear el valor de la propiedad como una cadena. Esto solo es aplicable si <displayInfo displayType=&\#0034;Number&\#0034;> .'
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: Numérico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750a9fb4dcf6a7a56c350fccf80241644b956da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666860"
---
# <a name="numberformat"></a><span data-ttu-id="26906-104">Numérico</span><span class="sxs-lookup"><span data-stu-id="26906-104">numberFormat</span></span>

<span data-ttu-id="26906-105">Especifica cómo [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) debe formatear el valor de la propiedad como una cadena.</span><span class="sxs-lookup"><span data-stu-id="26906-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="26906-106">Esto solo es aplicable si <displayInfo displayType="Number"> .</span><span class="sxs-lookup"><span data-stu-id="26906-106">This is applicable only if <displayInfo displayType="Number">.</span></span> <span data-ttu-id="26906-107">Solo debe haber un elemento [NumberFormat]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="26906-107">There should be only one [numberFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="26906-108">Si hay varios elementos, se usa el último.</span><span class="sxs-lookup"><span data-stu-id="26906-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="26906-109">Si no se proporciona ningún elemento [NumberFormat]() , se aplica la configuración de atributo predeterminada a la descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="26906-109">If no [numberFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="26906-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26906-110">Syntax</span></span>


```
      <!-- numberFormat -->
      <xs:element name="numberFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Percentage"/>
                <xs:enumeration value="ByteSize"/>
                <xs:enumeration value="KBSize"/>
                <xs:enumeration value="SampleSize"/>
                <xs:enumeration value="Bitrate"/>
                <xs:enumeration value="SampleRate"/>
                <xs:enumeration value="FrameRate"/>
                <xs:enumeration value="Pixels"/>
                <xs:enumeration value="DPI"/>
                <xs:enumeration value="Duration"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDurationAs">
              <xs:restriction base="xs:string">
                <xs:enumeration value="hh:mm"/>
                <xs:enumeration value="hh:mm:ss"/>
                <xs:enumeration value="hh:mm:ss.fff"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="26906-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="26906-111">Element Information</span></span>



| <span data-ttu-id="26906-112">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="26906-112">Parent Element</span></span>                                   | <span data-ttu-id="26906-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="26906-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="26906-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="26906-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="26906-115">None</span><span class="sxs-lookup"><span data-stu-id="26906-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="26906-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="26906-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26906-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="26906-117">Attribute</span></span></th>
<th><span data-ttu-id="26906-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="26906-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26906-119">formatas</span><span class="sxs-lookup"><span data-stu-id="26906-119">formatAs</span></span></td>
<td><span data-ttu-id="26906-120">Público.</span><span class="sxs-lookup"><span data-stu-id="26906-120">Public.</span></span> <span data-ttu-id="26906-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="26906-121">Optional.</span></span> <span data-ttu-id="26906-122">El valor predeterminado es &quot; General &quot; .</span><span class="sxs-lookup"><span data-stu-id="26906-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="26906-123">Especifica el formato de presentación.</span><span class="sxs-lookup"><span data-stu-id="26906-123">Specifies the display format.</span></span> <span data-ttu-id="26906-124">Estos son los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="26906-124">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="26906-125">Value</span><span class="sxs-lookup"><span data-stu-id="26906-125">Value</span></span></th>
<th><span data-ttu-id="26906-126">Significado</span><span class="sxs-lookup"><span data-stu-id="26906-126">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26906-127">General</span><span class="sxs-lookup"><span data-stu-id="26906-127">General</span></span></td>
<td><span data-ttu-id="26906-128">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="26906-128">Default.</span></span> <span data-ttu-id="26906-129">Muestra el valor como un número sin formato.</span><span class="sxs-lookup"><span data-stu-id="26906-129">Displays the value as an unformatted number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26906-130">Porcentaje</span><span class="sxs-lookup"><span data-stu-id="26906-130">Percentage</span></span></td>
<td><span data-ttu-id="26906-131">Da formato al valor como un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="26906-131">Formats the value as a percentage.</span></span> <span data-ttu-id="26906-132">Requiere que la propiedad sea UInt32.</span><span class="sxs-lookup"><span data-stu-id="26906-132">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26906-133">ByteSize</span><span class="sxs-lookup"><span data-stu-id="26906-133">ByteSize</span></span></td>
<td><span data-ttu-id="26906-134">Da formato al valor como un byte, &quot; KB &quot; , &quot; MB &quot; o &quot; GB &quot; según corresponda.</span><span class="sxs-lookup"><span data-stu-id="26906-134">Formats the value as a byte, &quot;KB&quot;, &quot;MB&quot;, or &quot;GB&quot; as appropriate.</span></span> <span data-ttu-id="26906-135">Requiere que la propiedad sea UInt64.</span><span class="sxs-lookup"><span data-stu-id="26906-135">Requires the property to be UInt64.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26906-136">KBSize</span><span class="sxs-lookup"><span data-stu-id="26906-136">KBSize</span></span></td>
<td><span data-ttu-id="26906-137">Da formato a un valor de &quot; KB &quot; , independientemente de cuál sea el valor.</span><span class="sxs-lookup"><span data-stu-id="26906-137">Formats the value as a &quot;KB&quot;, no matter what the value is.</span></span> <span data-ttu-id="26906-138">Requiere que la propiedad sea UInt64.</span><span class="sxs-lookup"><span data-stu-id="26906-138">Requires the property to be UInt64.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26906-139">SampleSize</span><span class="sxs-lookup"><span data-stu-id="26906-139">SampleSize</span></span></td>
<td><span data-ttu-id="26906-140">Da formato al valor como un número de bits.</span><span class="sxs-lookup"><span data-stu-id="26906-140">Formats the value as a number of bits.</span></span> <span data-ttu-id="26906-141">Requiere que la propiedad sea UInt32.</span><span class="sxs-lookup"><span data-stu-id="26906-141">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26906-142">Velocidad de bits</span><span class="sxs-lookup"><span data-stu-id="26906-142">BitRate</span></span></td>
<td><span data-ttu-id="26906-143">Da formato al valor en &quot; Kbps &quot; .</span><span class="sxs-lookup"><span data-stu-id="26906-143">Formats the value in &quot;Kbps&quot;.</span></span> <span data-ttu-id="26906-144">Requiere que la propiedad sea UInt32.</span><span class="sxs-lookup"><span data-stu-id="26906-144">Requires the property to be UInt32.</span></span> <span data-ttu-id="26906-145">El valor debe almacenarse en &quot; unidades de bits por segundo &quot; .</span><span class="sxs-lookup"><span data-stu-id="26906-145">The value must be stored in &quot;bits-per-second&quot; units.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26906-146">SampleRate</span><span class="sxs-lookup"><span data-stu-id="26906-146">SampleRate</span></span></td>
<td><span data-ttu-id="26906-147">Da formato al valor en &quot; kHz &quot; .</span><span class="sxs-lookup"><span data-stu-id="26906-147">Formats the value in &quot;KHz&quot;.</span></span> <span data-ttu-id="26906-148">Requiere que la propiedad sea UInt32.</span><span class="sxs-lookup"><span data-stu-id="26906-148">Requires the property to be UInt32.</span></span> <span data-ttu-id="26906-149">El valor debe almacenarse en &quot; unidades de hercios &quot; .</span><span class="sxs-lookup"><span data-stu-id="26906-149">The value must be stored in &quot;Hertz&quot; units.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26906-150">FrameRate</span><span class="sxs-lookup"><span data-stu-id="26906-150">FrameRate</span></span></td>
<td><span data-ttu-id="26906-151">Da formato al valor en fotogramas/segundo.</span><span class="sxs-lookup"><span data-stu-id="26906-151">Formats the value in frames/second.</span></span> <span data-ttu-id="26906-152">Requiere que la propiedad sea UInt32.</span><span class="sxs-lookup"><span data-stu-id="26906-152">Requires the property to be UInt32.</span></span> <span data-ttu-id="26906-153">El valor debe almacenarse en &quot; unidades de kilo-fotogramas por segundo &quot; .</span><span class="sxs-lookup"><span data-stu-id="26906-153">The value must be stored in &quot;kilo-frames-per-second&quot; units.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26906-154">píxeles</span><span class="sxs-lookup"><span data-stu-id="26906-154">Pixels</span></span></td>
<td><span data-ttu-id="26906-155">Da formato al valor en unidades de píxeles.</span><span class="sxs-lookup"><span data-stu-id="26906-155">Formats the value in pixel units.</span></span> <span data-ttu-id="26906-156">Requiere que la propiedad sea UInt32.</span><span class="sxs-lookup"><span data-stu-id="26906-156">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26906-157">ppp</span><span class="sxs-lookup"><span data-stu-id="26906-157">DPI</span></span></td>
<td><span data-ttu-id="26906-158">Da formato al valor en puntos por pulgada.</span><span class="sxs-lookup"><span data-stu-id="26906-158">Formats the value in dots-per-inch.</span></span> <span data-ttu-id="26906-159">Requiere que la propiedad sea UInt32.</span><span class="sxs-lookup"><span data-stu-id="26906-159">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26906-160">Duration</span><span class="sxs-lookup"><span data-stu-id="26906-160">Duration</span></span></td>
<td><span data-ttu-id="26906-161">Da formato al valor como una duración.</span><span class="sxs-lookup"><span data-stu-id="26906-161">Formats the value as a duration.</span></span> <span data-ttu-id="26906-162"><formatDurationAs>Se usa para especificar el formato de duración.</span><span class="sxs-lookup"><span data-stu-id="26906-162">Use <formatDurationAs> to specify the duration format.</span></span> <span data-ttu-id="26906-163">Requiere que la propiedad sea UInt64.</span><span class="sxs-lookup"><span data-stu-id="26906-163">Requires the property to be UInt64.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26906-164">formatDurationAs</span><span class="sxs-lookup"><span data-stu-id="26906-164">formatDurationAs</span></span></td>
<td><span data-ttu-id="26906-165">Público.</span><span class="sxs-lookup"><span data-stu-id="26906-165">Public.</span></span> <span data-ttu-id="26906-166">Opcional.</span><span class="sxs-lookup"><span data-stu-id="26906-166">Optional.</span></span> <span data-ttu-id="26906-167">El valor predeterminado es &quot; HH: mm: SS &quot; .</span><span class="sxs-lookup"><span data-stu-id="26906-167">Default is &quot;hh:mm:ss&quot;.</span></span> <span data-ttu-id="26906-168">Solo se aplica si <em>formatas &quot; = &quot; Duration</em>.</span><span class="sxs-lookup"><span data-stu-id="26906-168">Only applies if <em>formatAs=&quot;Duration&quot;</em>.</span></span> <span data-ttu-id="26906-169">Requiere que la propiedad sea UInt64.</span><span class="sxs-lookup"><span data-stu-id="26906-169">Requires the property to be UInt64.</span></span> <span data-ttu-id="26906-170">Estos son los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="26906-170">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="26906-171">Value</span><span class="sxs-lookup"><span data-stu-id="26906-171">Value</span></span></th>
<th><span data-ttu-id="26906-172">Significado</span><span class="sxs-lookup"><span data-stu-id="26906-172">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26906-173">hh:mm</span><span class="sxs-lookup"><span data-stu-id="26906-173">hh:mm</span></span></td>
<td><span data-ttu-id="26906-174">Da formato al valor en horas y minutos.</span><span class="sxs-lookup"><span data-stu-id="26906-174">Formats the value in hours and minutes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26906-175">hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="26906-175">hh:mm:ss</span></span></td>
<td><span data-ttu-id="26906-176">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="26906-176">Default.</span></span> <span data-ttu-id="26906-177">Da formato al valor en horas, minutos y segundos.</span><span class="sxs-lookup"><span data-stu-id="26906-177">Formats the value in hours, minutes, and seconds.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26906-178">HH: mm: SS. FFF</span><span class="sxs-lookup"><span data-stu-id="26906-178">hh:mm:ss.fff</span></span></td>
<td><span data-ttu-id="26906-179">Da formato al valor en horas, minutos, segundos y milisegundos.</span><span class="sxs-lookup"><span data-stu-id="26906-179">Formats the value in hours, minutes, seconds, and milliseconds.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
