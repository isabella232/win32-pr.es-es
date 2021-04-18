---
description: Especifica la información de presentación de una propiedad.
ms.assetid: 27c03ced-a5fa-4ab4-b88e-5b78701da878
title: displayInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fff0bb441b4535c0b6c6f3183671fbe8ade09183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648399"
---
# <a name="displayinfo"></a><span data-ttu-id="2709b-103">displayInfo</span><span class="sxs-lookup"><span data-stu-id="2709b-103">displayInfo</span></span>

<span data-ttu-id="2709b-104">Especifica la información de presentación de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="2709b-104">Specifies a property's display information.</span></span> <span data-ttu-id="2709b-105">Solo debe haber un elemento [displayInfo]() para cada [propertyDescription](./propdesc-schema-propertydescription.md).</span><span class="sxs-lookup"><span data-stu-id="2709b-105">There should be only one [displayInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md).</span></span>

<span data-ttu-id="2709b-106">Si hay varios elementos, se usa el último.</span><span class="sxs-lookup"><span data-stu-id="2709b-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="2709b-107">Si no se proporciona ningún elemento [displayInfo]() , los valores de atributo predeterminados se aplican a la descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="2709b-107">If no [displayInfo]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="2709b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2709b-108">Syntax</span></span>


```
<!-- displayInfo -->
<xs:element name="displayInfo">
    <xs:complexType>
        <xs:all>
            <xs:element name="stringFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="General"/>
                                <xs:enumeration value="FileName"/>
                                <xs:enumeration value="FilePath"/>
                                <xs:enumeration value="Hyperlink"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="booleanFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="YesNo"/>
                                <xs:enumeration value="OnOff"/>
                                <xs:enumeration value="TrueFalse"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="numberFormat" minOccurs="0" maxOccurs="1">
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
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="hh:mm"/>
                                <xs:enumeration value="hh:mm:ss"/>
                                <xs:enumeration value="hh:mm:ss.fff"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="dateTimeFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="enumeratedList" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="value" type="xs:string" use="required"/>
                                <xs:attribute name="text" type="xs:string" use="required"/>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="minValue" type="xs:string" use="required"/>
                                <xs:attribute name="setValue" type="xs:string"/>
                                <xs:attribute name="text" type="xs:string"/>
                            </xs:complexType>
                        </xs:element>
                    </xs:sequence>

                    <xs:attribute name="defaultText" type="xs:string"/>
                    <xs:attribute name="useValueForDefault" type="xs:boolean"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="drawControl" minOccurs="0" maxOccurs="1">
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
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="editControl" minOccurs="0" maxOccurs="1">
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
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="filterControl" minOccurs="0" maxOccurs="1">
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
            <xs:element name="queryControl" minOccurs="0" maxOccurs="1">
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
        </xs:all>

        <xs:attribute name="defaultColumnWidth" type="xs:nonNegativeInteger" default="20"/>
        <xs:attribute name="displayType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        
        <xs:attribute name="alignment" default="Left">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Left"/>
                    <xs:enumeration value="Center"/>
                    <xs:enumeration value="Right"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="relativeDescriptionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Count"/>
                    <xs:enumeration value="Revision"/>
                    <xs:enumeration value="Length"/>
                    <xs:enumeration value="Duration"/>
                    <xs:enumeration value="Speed"/>
                    <xs:enumeration value="Rate"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Priority"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultSortDirection" default="Ascending">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                  <xs:enumeration value="Ascending"/>
                  <xs:enumeration value="Descending"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="2709b-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2709b-109">Element Information</span></span>



| <span data-ttu-id="2709b-110">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="2709b-110">Parent Element</span></span>                                                   | <span data-ttu-id="2709b-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2709b-111">Child Elements</span></span>                                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2709b-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="2709b-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | [<span data-ttu-id="2709b-113">stringFormat</span><span class="sxs-lookup"><span data-stu-id="2709b-113">stringFormat</span></span>](./propdesc-schema-stringformat.md)                                                             |
|                                                                  | [<span data-ttu-id="2709b-114">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="2709b-114">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)                                                           |
|                                                                  | [<span data-ttu-id="2709b-115">Numérico</span><span class="sxs-lookup"><span data-stu-id="2709b-115">numberFormat</span></span>](./propdesc-schema-numberformat.md)                                                             |
|                                                                  | [<span data-ttu-id="2709b-116">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2709b-116">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)                                                         |
|                                                                  | [<span data-ttu-id="2709b-117">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="2709b-117">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)                                                         |
|                                                                  | [<span data-ttu-id="2709b-118">drawControl</span><span class="sxs-lookup"><span data-stu-id="2709b-118">drawControl</span></span>](./propdesc-schema-drawcontrol.md)                                                               |
|                                                                  | [<span data-ttu-id="2709b-119">editControl</span><span class="sxs-lookup"><span data-stu-id="2709b-119">editControl</span></span>](./propdesc-schema-editcontrol.md)                                                               |
|                                                                  | [<span data-ttu-id="2709b-120">filterControl</span><span class="sxs-lookup"><span data-stu-id="2709b-120">filterControl</span></span>](./propdesc-schema-filtercontrol.md)                                                           |
|                                                                  | <span data-ttu-id="2709b-121">[consulta](./propdesc-schema-querycontrol.md) (solo Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="2709b-121">[queryControl](./propdesc-schema-querycontrol.md) (Windows Vista only.</span></span> <span data-ttu-id="2709b-122">No se admite en Windows 7 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="2709b-122">Not supported in Windows 7 and later.)</span></span> |



 

## <a name="attributes"></a><span data-ttu-id="2709b-123">Atributos</span><span class="sxs-lookup"><span data-stu-id="2709b-123">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2709b-124">Atributo</span><span class="sxs-lookup"><span data-stu-id="2709b-124">Attribute</span></span></th>
<th><span data-ttu-id="2709b-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="2709b-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2709b-126">defaultColumnWidth</span><span class="sxs-lookup"><span data-stu-id="2709b-126">defaultColumnWidth</span></span></td>
<td><span data-ttu-id="2709b-127">Público.</span><span class="sxs-lookup"><span data-stu-id="2709b-127">Public.</span></span> <span data-ttu-id="2709b-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2709b-128">Optional.</span></span> <span data-ttu-id="2709b-129">El valor predeterminado es &quot; 20 &quot; .</span><span class="sxs-lookup"><span data-stu-id="2709b-129">Default is &quot;20&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2709b-130">TipoDePresentación</span><span class="sxs-lookup"><span data-stu-id="2709b-130">displayType</span></span></td>
<td><span data-ttu-id="2709b-131">Público.</span><span class="sxs-lookup"><span data-stu-id="2709b-131">Public.</span></span> <span data-ttu-id="2709b-132">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2709b-132">Optional.</span></span> <span data-ttu-id="2709b-133">El valor predeterminado es &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="2709b-133">Default is &quot;String&quot;.</span></span> <span data-ttu-id="2709b-134">Especifica el tipo de la cadena de presentación.</span><span class="sxs-lookup"><span data-stu-id="2709b-134">Specifies the type of the display string.</span></span> <span data-ttu-id="2709b-135">Una vez establecido aquí, <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription:: GetDisplayType</strong></a>recupera los valores de <strong>PROPDESC_DISPLAYTYPE</strong> asociados.</span><span class="sxs-lookup"><span data-stu-id="2709b-135">Once set here, the associated <strong>PROPDESC_DISPLAYTYPE</strong> values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription::GetDisplayType</strong></a>.</span></span> <span data-ttu-id="2709b-136">Los tipos válidos son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="2709b-136">The following are valid types.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2709b-137">Value</span><span class="sxs-lookup"><span data-stu-id="2709b-137">Value</span></span></th>
<th><span data-ttu-id="2709b-138">Significado</span><span class="sxs-lookup"><span data-stu-id="2709b-138">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2709b-139">String</span><span class="sxs-lookup"><span data-stu-id="2709b-139">String</span></span></td>
<td><span data-ttu-id="2709b-140">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2709b-140">Default.</span></span> <span data-ttu-id="2709b-141">El valor se muestra como una cadena.</span><span class="sxs-lookup"><span data-stu-id="2709b-141">Value is displayed as a string.</span></span> <span data-ttu-id="2709b-142">Use &quot; StringFormat &quot; para dar formato.</span><span class="sxs-lookup"><span data-stu-id="2709b-142">Use &quot;stringFormat&quot; to format.</span></span> <span data-ttu-id="2709b-143">El método devuelve PDDT_STRING.</span><span class="sxs-lookup"><span data-stu-id="2709b-143">Method returns PDDT_STRING.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2709b-144">Number</span><span class="sxs-lookup"><span data-stu-id="2709b-144">Number</span></span></td>
<td><span data-ttu-id="2709b-145">Valor predeterminado para las propiedades numéricas.</span><span class="sxs-lookup"><span data-stu-id="2709b-145">Default for numeric properties.</span></span> <span data-ttu-id="2709b-146">El valor se muestra como un número.</span><span class="sxs-lookup"><span data-stu-id="2709b-146">Value is displayed as a number.</span></span> <span data-ttu-id="2709b-147">Use &quot; NumberFormat &quot; para dar formato.</span><span class="sxs-lookup"><span data-stu-id="2709b-147">Use &quot;numberFormat&quot; to format.</span></span> <span data-ttu-id="2709b-148">El método devuelve PDDT_NUMBER.</span><span class="sxs-lookup"><span data-stu-id="2709b-148">Method returns PDDT_NUMBER.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2709b-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="2709b-149">Boolean</span></span></td>
<td><span data-ttu-id="2709b-150">Valor predeterminado si <typeInfo type=&quot;Boolean&quot;> .</span><span class="sxs-lookup"><span data-stu-id="2709b-150">Default if <typeInfo type=&quot;Boolean&quot;>.</span></span> <span data-ttu-id="2709b-151">El valor se muestra como booleano.</span><span class="sxs-lookup"><span data-stu-id="2709b-151">Value is displayed as a boolean.</span></span> <span data-ttu-id="2709b-152">Use &quot; booleanFormat &quot; para dar formato.</span><span class="sxs-lookup"><span data-stu-id="2709b-152">Use &quot;booleanFormat&quot; to format.</span></span> <span data-ttu-id="2709b-153">El método devuelve PDDT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="2709b-153">Method returns PDDT_BOOLEAN.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2709b-154">DateTime</span><span class="sxs-lookup"><span data-stu-id="2709b-154">DateTime</span></span></td>
<td><span data-ttu-id="2709b-155">Valor predeterminado si <typeInfo type=&quot;DateTime&quot;> .</span><span class="sxs-lookup"><span data-stu-id="2709b-155">Default if <typeInfo type=&quot;DateTime&quot;>.</span></span> <span data-ttu-id="2709b-156">El valor se muestra como una fecha o una hora.</span><span class="sxs-lookup"><span data-stu-id="2709b-156">Value is displayed as a date or time.</span></span> <span data-ttu-id="2709b-157">Use &quot; DateTimeFormat &quot; para dar formato.</span><span class="sxs-lookup"><span data-stu-id="2709b-157">Use &quot;dateTimeFormat&quot; to format.</span></span> <span data-ttu-id="2709b-158">El método devuelve PDDT_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="2709b-158">Method returns PDDT_DATETIME.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2709b-159">Enumeración</span><span class="sxs-lookup"><span data-stu-id="2709b-159">Enumeration</span></span></td>
<td><span data-ttu-id="2709b-160">El valor se muestra como una asignación de cadena de presentación proporcionada por el &quot; &quot; elemento enumeratedList.</span><span class="sxs-lookup"><span data-stu-id="2709b-160">Value is displayed as a display string mapping provided by the &quot;enumeratedList&quot; element.</span></span> <span data-ttu-id="2709b-161">El método devuelve PDDT_ENUMERATED.</span><span class="sxs-lookup"><span data-stu-id="2709b-161">Method returns PDDT_ENUMERATED.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2709b-162">alineación</span><span class="sxs-lookup"><span data-stu-id="2709b-162">alignment</span></span></td>
<td><span data-ttu-id="2709b-163">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2709b-163">Optional.</span></span> <span data-ttu-id="2709b-164">El valor predeterminado es &quot; left &quot; .</span><span class="sxs-lookup"><span data-stu-id="2709b-164">Default is &quot;Left&quot;.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2709b-165">Value</span><span class="sxs-lookup"><span data-stu-id="2709b-165">Value</span></span></th>
<th><span data-ttu-id="2709b-166">Significado</span><span class="sxs-lookup"><span data-stu-id="2709b-166">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2709b-167">Left</span><span class="sxs-lookup"><span data-stu-id="2709b-167">Left</span></span></td>
<td><span data-ttu-id="2709b-168">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2709b-168">Default.</span></span> <span data-ttu-id="2709b-169">Alinear a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="2709b-169">Align left.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2709b-170">Center</span><span class="sxs-lookup"><span data-stu-id="2709b-170">Center</span></span></td>
<td><span data-ttu-id="2709b-171">Alinear el centro.</span><span class="sxs-lookup"><span data-stu-id="2709b-171">Align center.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2709b-172">Right</span><span class="sxs-lookup"><span data-stu-id="2709b-172">Right</span></span></td>
<td><span data-ttu-id="2709b-173">Alinear a la derecha.</span><span class="sxs-lookup"><span data-stu-id="2709b-173">Align right.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2709b-174">relativeDescriptionType</span><span class="sxs-lookup"><span data-stu-id="2709b-174">relativeDescriptionType</span></span></td>
<td><span data-ttu-id="2709b-175">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2709b-175">Optional.</span></span> <span data-ttu-id="2709b-176">El valor predeterminado es &quot; General &quot; .</span><span class="sxs-lookup"><span data-stu-id="2709b-176">Default is &quot;General&quot;.</span></span> <span data-ttu-id="2709b-177">Especifica cómo deben describirse dos valores de esta propiedad cuando se comparan entre sí.</span><span class="sxs-lookup"><span data-stu-id="2709b-177">Specifies how two values of this property should be described when they are compared with one another.</span></span> <span data-ttu-id="2709b-178">En el caso de la equivalencia, &quot; &quot; siempre se usa el mismo.</span><span class="sxs-lookup"><span data-stu-id="2709b-178">In the case of equivalency, &quot;Same&quot; is always used.</span></span> <span data-ttu-id="2709b-179"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription:: GetRelativeDescription</strong></a> y <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription:: GetRelativeDescriptionType</strong></a> usan este valor para determinar qué nombres para mostrar de descripción relativa usar.</span><span class="sxs-lookup"><span data-stu-id="2709b-179"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription::GetRelativeDescription</strong></a> and <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription::GetRelativeDescriptionType</strong></a> use this value to determine what relative description display names to use.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2709b-180">Value</span><span class="sxs-lookup"><span data-stu-id="2709b-180">Value</span></span></th>
<th><span data-ttu-id="2709b-181">Significado</span><span class="sxs-lookup"><span data-stu-id="2709b-181">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2709b-182">General</span><span class="sxs-lookup"><span data-stu-id="2709b-182">General</span></span></td>
<td><span data-ttu-id="2709b-183">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2709b-183">Default.</span></span> <span data-ttu-id="2709b-184">Usa &quot; diferentes &quot;  /  &quot; &quot;  /  &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="2709b-184">Uses &quot;Different&quot; / &quot;Same&quot; / &quot;Different&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2709b-185">Fecha</span><span class="sxs-lookup"><span data-stu-id="2709b-185">Date</span></span></td>
<td><span data-ttu-id="2709b-186">Valor predeterminado si <typeInfo type=&quot;DateTime&quot;> .</span><span class="sxs-lookup"><span data-stu-id="2709b-186">Default if <typeInfo type=&quot;DateTime&quot;>.</span></span> <span data-ttu-id="2709b-187">Usa la &quot; misma versión anterior &quot;  /  &quot; &quot;  /  &quot; &quot; , o usa la misma versión más &quot; antigua &quot;  /  &quot; , o lo hace &quot;  /  &quot; &quot; &quot; antes &quot;  /  &quot; &quot;  /  &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="2709b-187">Uses &quot;Earlier&quot; / &quot;Same&quot; / &quot;Later&quot;, or uses &quot;Older&quot; / &quot;Same&quot; / &quot;Newer&quot;, or uses &quot;Sooner&quot; / &quot;Same&quot; / &quot;Later&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2709b-188">Tamaño</span><span class="sxs-lookup"><span data-stu-id="2709b-188">Size</span></span></td>
<td><span data-ttu-id="2709b-189">Usa &quot; el &quot;  /  &quot; mismo &quot;  /  &quot; tamaño más pequeño&quot;</span><span class="sxs-lookup"><span data-stu-id="2709b-189">Uses &quot;Smaller&quot; / &quot;Same&quot; / &quot;Larger&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2709b-190">Count</span><span class="sxs-lookup"><span data-stu-id="2709b-190">Count</span></span></td>
<td><span data-ttu-id="2709b-191">Usa &quot; el &quot;  /  &quot; mismo &quot;  /  &quot; tamaño más pequeño&quot;</span><span class="sxs-lookup"><span data-stu-id="2709b-191">Uses &quot;Smaller&quot; / &quot;Same&quot; / &quot;Larger&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2709b-192">Revisión</span><span class="sxs-lookup"><span data-stu-id="2709b-192">Revision</span></span></td>
<td><span data-ttu-id="2709b-193">Se usa con &quot; anterioridad &quot;  /  &quot; &quot;  /  &quot; más adelante&quot;</span><span class="sxs-lookup"><span data-stu-id="2709b-193">Uses &quot;Earlier&quot; / &quot;Same&quot; / &quot;Later&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2709b-194">Length</span><span class="sxs-lookup"><span data-stu-id="2709b-194">Length</span></span></td>
<td><span data-ttu-id="2709b-195">Usa el &quot; &quot;  /  &quot; mismo &quot;  /  &quot; tiempo más corto&quot;</span><span class="sxs-lookup"><span data-stu-id="2709b-195">Uses &quot;Shorter&quot; / &quot;Same&quot; / &quot;Longer&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2709b-196">Duration</span><span class="sxs-lookup"><span data-stu-id="2709b-196">Duration</span></span></td>
<td><span data-ttu-id="2709b-197">Usa el &quot; &quot;  /  &quot; mismo &quot;  /  &quot; tiempo más corto&quot;</span><span class="sxs-lookup"><span data-stu-id="2709b-197">Uses &quot;Shorter&quot; / &quot;Same&quot; / &quot;Longer&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2709b-198">Velocidad</span><span class="sxs-lookup"><span data-stu-id="2709b-198">Speed</span></span></td>
<td><span data-ttu-id="2709b-199">Usa &quot; el &quot;  /  &quot; mismo &quot;  /  &quot; de forma más lenta&quot;</span><span class="sxs-lookup"><span data-stu-id="2709b-199">Uses &quot;Slower&quot; / &quot;Same&quot; / &quot;Faster&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2709b-200">Tarifa</span><span class="sxs-lookup"><span data-stu-id="2709b-200">Rate</span></span></td>
<td><span data-ttu-id="2709b-201">Usa &quot; el &quot;  /  &quot; mismo &quot;  /  &quot; de forma más lenta&quot;</span><span class="sxs-lookup"><span data-stu-id="2709b-201">Uses &quot;Slower&quot; / &quot;Same&quot; / &quot;Faster&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2709b-202">Rating</span><span class="sxs-lookup"><span data-stu-id="2709b-202">Rating</span></span></td>
<td><span data-ttu-id="2709b-203">Usa &quot; el &quot;  /  &quot; mismo &quot;  /  &quot; nivel más bajo&quot;</span><span class="sxs-lookup"><span data-stu-id="2709b-203">Uses &quot;Lower&quot; / &quot;Same&quot; / &quot;Higher&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2709b-204">Prioridad</span><span class="sxs-lookup"><span data-stu-id="2709b-204">Priority</span></span></td>
<td><span data-ttu-id="2709b-205">Usa &quot; el &quot;  /  &quot; mismo &quot;  /  &quot; nivel más bajo&quot;</span><span class="sxs-lookup"><span data-stu-id="2709b-205">Uses &quot;Lower&quot; / &quot;Same&quot; / &quot;Higher&quot;</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2709b-206">defaultSortDirection</span><span class="sxs-lookup"><span data-stu-id="2709b-206">defaultSortDirection</span></span></td>
<td><span data-ttu-id="2709b-207">Especifica la dirección de ordenación.</span><span class="sxs-lookup"><span data-stu-id="2709b-207">Specifies sort direction.</span></span> <span data-ttu-id="2709b-208">El valor predeterminado es &quot; Ascending &quot; .</span><span class="sxs-lookup"><span data-stu-id="2709b-208">Default is &quot;Ascending&quot;.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2709b-209">Value</span><span class="sxs-lookup"><span data-stu-id="2709b-209">Value</span></span></th>
<th><span data-ttu-id="2709b-210">Significado</span><span class="sxs-lookup"><span data-stu-id="2709b-210">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2709b-211">Ascendente</span><span class="sxs-lookup"><span data-stu-id="2709b-211">Ascending</span></span></td>
<td><span data-ttu-id="2709b-212">Ordena de forma ascendente.</span><span class="sxs-lookup"><span data-stu-id="2709b-212">Sorts ascending.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2709b-213">Descendente</span><span class="sxs-lookup"><span data-stu-id="2709b-213">Descending</span></span></td>
<td><span data-ttu-id="2709b-214">Ordena de forma descendente.</span><span class="sxs-lookup"><span data-stu-id="2709b-214">Sorts descending.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
