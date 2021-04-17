---
description: Especifica la información de tipo de una propiedad.
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: Requerida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa783a606066163fd8b17f53ef8a0fe2da44e539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666850"
---
# <a name="typeinfo"></a><span data-ttu-id="52fa5-103">Requerida</span><span class="sxs-lookup"><span data-stu-id="52fa5-103">typeInfo</span></span>

<span data-ttu-id="52fa5-104">Especifica la información de tipo de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="52fa5-104">Specifies a property's type information.</span></span> <span data-ttu-id="52fa5-105">Solo debe haber un elemento [typeInfo]() para cada [propertyDescription](./propdesc-schema-propertydescription.md).</span><span class="sxs-lookup"><span data-stu-id="52fa5-105">There should be only one [typeInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md).</span></span> <span data-ttu-id="52fa5-106">Este elemento ha cambiado para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="52fa5-106">This element has changed for Windows 7.</span></span>

<span data-ttu-id="52fa5-107">Si hay varios elementos, se usa el último.</span><span class="sxs-lookup"><span data-stu-id="52fa5-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="52fa5-108">Si no se proporciona ningún elemento [typeInfo]() , se aplica la configuración de atributo predeterminada a la descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="52fa5-108">If no [typeInfo]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="52fa5-109">Sintaxis para Windows 7</span><span class="sxs-lookup"><span data-stu-id="52fa5-109">Syntax for Windows 7</span></span>


```
<!-- typeInfo for Windows 7-->
<xs:element name="typeInfo">
    <xs:complexType>
        <xs:attribute name="type" default="Any">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Any"/>
                    <xs:enumeration value="Null"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Byte"/>
                    <xs:enumeration value="Buffer"/>
                    <xs:enumeration value="Int16"/>
                    <xs:enumeration value="UInt16"/>
                    <xs:enumeration value="Int32"/>
                    <xs:enumeration value="UInt32"/>
                    <xs:enumeration value="Int64"/>
                    <xs:enumeration value="UInt64"/>
                    <xs:enumeration value="Double"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Guid"/>
                    <xs:enumeration value="Blob"/>
                    <xs:enumeration value="Stream"/>
                    <xs:enumeration value="Clipboard"/>
                    <xs:enumeration value="Object"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="groupingRange">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Discrete"/>
                    <xs:enumeration value="Alphanumeric"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Dynamic"/>
                    <xs:enumeration value="Percent"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isInnate" type="xs:boolean" default="false"/>
        <xs:attribute name="canBePurged" type="xs:boolean"/>
        <xs:attribute name="multipleValues" type="xs:boolean" default="false"/>
        <xs:attribute name="isGroup" type="xs:boolean" default="false"/>
        <xs:attribute name="aggregationType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="First"/>
                    <xs:enumeration value="Sum"/>
                    <xs:enumeration value="Average"/>
                    <xs:enumeration value="DateRange"/>
                    <xs:enumeration value="Union"/>
                    <xs:enumeration value="Maximum"/>
                    <xs:enumeration value="Minimum"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isTreeProperty" type="xs:boolean" default="false"/>
        <xs:attribute name="isViewable" type="xs:boolean" default="false"/>
        <xs:attribute name="isQueryable" type="xs:boolean" default="false"/>
        <xs:attribute name="includeInFullTextQuery" type="xs:boolean" default="false"/>
        <xs:attribute name="searchRawValue" type="xs:boolean" default="false"/>
        <xs:attribute name="conditionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="None"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Size"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultOperation">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Equal"/>
                    <xs:enumeration value="NotEqual"/>
                    <xs:enumeration value="LessThan"/>
                    <xs:enumeration value="GreaterThan"/>
                    <xs:enumeration value="Contains"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="52fa5-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="52fa5-110">Element Information</span></span>



| <span data-ttu-id="52fa5-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="52fa5-111">Parent Element</span></span>                                                   | <span data-ttu-id="52fa5-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="52fa5-112">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="52fa5-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="52fa5-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="52fa5-114">None</span><span class="sxs-lookup"><span data-stu-id="52fa5-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="52fa5-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="52fa5-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="52fa5-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="52fa5-116">Attribute</span></span></th>
<th><span data-ttu-id="52fa5-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="52fa5-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52fa5-118">type</span><span class="sxs-lookup"><span data-stu-id="52fa5-118">type</span></span></td>
<td><span data-ttu-id="52fa5-119">Público.</span><span class="sxs-lookup"><span data-stu-id="52fa5-119">Public.</span></span> <span data-ttu-id="52fa5-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="52fa5-120">Optional.</span></span> <span data-ttu-id="52fa5-121">El valor predeterminado es &quot; any &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-121">Default is &quot;Any&quot;.</span></span> <span data-ttu-id="52fa5-122">Indica el tipo de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="52fa5-122">Indicates the type of the property.</span></span> <span data-ttu-id="52fa5-123">Los siguientes son tipos válidos y sus tipos de variante asociados se recuperan mediante <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: GetPropertyType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="52fa5-123">The following are valid types and their associated variant types are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a>.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="52fa5-124">Value</span><span class="sxs-lookup"><span data-stu-id="52fa5-124">Value</span></span></th>
<th><span data-ttu-id="52fa5-125">Significado</span><span class="sxs-lookup"><span data-stu-id="52fa5-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52fa5-126">Any</span><span class="sxs-lookup"><span data-stu-id="52fa5-126">Any</span></span></td>
<td><span data-ttu-id="52fa5-127">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="52fa5-127">Default.</span></span> <span data-ttu-id="52fa5-128">El subsistema de propiedades no aplicará ni convertirá el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="52fa5-128">The property subsystem will not enforce or coerce the property value.</span></span> <span data-ttu-id="52fa5-129"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: GetPropertyType</strong></a> devuelve VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="52fa5-129"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> returns VT_NULL.</span></span> <span data-ttu-id="52fa5-130">Se recomienda encarecidamente a los fabricantes de software independientes (ISV) que proporcionen un tipo en lugar de revertir a este valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="52fa5-130">Independent software vendors (ISVs) are strongly encouraged to provide a type rather than fall back on this default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-131">Null</span><span class="sxs-lookup"><span data-stu-id="52fa5-131">Null</span></span></td>
<td><span data-ttu-id="52fa5-132">No hay ningún valor para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="52fa5-132">There is no value for this property.</span></span> <span data-ttu-id="52fa5-133"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: GetPropertyType</strong></a> devuelve VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="52fa5-133"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> returns VT_NULL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-134">String</span><span class="sxs-lookup"><span data-stu-id="52fa5-134">String</span></span></td>
<td><span data-ttu-id="52fa5-135">El valor debe ser un VT_LPWSTR, que es una cadena Unicode que termina en una referencia nula.</span><span class="sxs-lookup"><span data-stu-id="52fa5-135">The value must be a VT_LPWSTR, which is a Unicode string terminated by a null reference.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-136">Boolean</span><span class="sxs-lookup"><span data-stu-id="52fa5-136">Boolean</span></span></td>
<td><span data-ttu-id="52fa5-137">El valor debe ser un VT_BOOL, que es un booleano.</span><span class="sxs-lookup"><span data-stu-id="52fa5-137">The value must be a VT_BOOL, which is a boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-138">Byte</span><span class="sxs-lookup"><span data-stu-id="52fa5-138">Byte</span></span></td>
<td><span data-ttu-id="52fa5-139">El valor debe ser un VT_UI1, que es un byte.</span><span class="sxs-lookup"><span data-stu-id="52fa5-139">The value must be a VT_UI1, which is a byte.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-140">Buffer</span><span class="sxs-lookup"><span data-stu-id="52fa5-140">Buffer</span></span></td>
<td><span data-ttu-id="52fa5-141">El valor debe ser un VT_UI1 | VT_VECTOR búfer de bytes.</span><span class="sxs-lookup"><span data-stu-id="52fa5-141">The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-142">Int16</span><span class="sxs-lookup"><span data-stu-id="52fa5-142">Int16</span></span></td>
<td><span data-ttu-id="52fa5-143">El valor debe ser un VT_I2, que es un entero de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="52fa5-143">The value must be a VT_I2, which is a 16-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-144">UInt16</span><span class="sxs-lookup"><span data-stu-id="52fa5-144">UInt16</span></span></td>
<td><span data-ttu-id="52fa5-145">El valor debe ser un VT_UI2, que es un entero sin signo de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="52fa5-145">The value must be a VT_UI2, which is a 16-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-146">Int32</span><span class="sxs-lookup"><span data-stu-id="52fa5-146">Int32</span></span></td>
<td><span data-ttu-id="52fa5-147">El valor debe ser un VT_I4, que es un entero de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="52fa5-147">The value must be a VT_I4, which is a 32-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-148">UInt32</span><span class="sxs-lookup"><span data-stu-id="52fa5-148">UInt32</span></span></td>
<td><span data-ttu-id="52fa5-149">El valor debe ser un VT_UI4, que es un entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="52fa5-149">The value must be a VT_UI4, which is a 32-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-150">Int64</span><span class="sxs-lookup"><span data-stu-id="52fa5-150">Int64</span></span></td>
<td><span data-ttu-id="52fa5-151">El valor debe ser un VT_I8, que es un entero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="52fa5-151">The value must be a VT_I8, which is a 64-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-152">UInt64</span><span class="sxs-lookup"><span data-stu-id="52fa5-152">UInt64</span></span></td>
<td><span data-ttu-id="52fa5-153">El valor debe ser un VT_UI8, que es un entero de 64 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="52fa5-153">The value must be a VT_UI8, which is a 64-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-154">Doble</span><span class="sxs-lookup"><span data-stu-id="52fa5-154">Double</span></span></td>
<td><span data-ttu-id="52fa5-155">El valor debe ser un VT_R8, que es un doble.</span><span class="sxs-lookup"><span data-stu-id="52fa5-155">The value must be a VT_R8, which is a double.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-156">DateTime</span><span class="sxs-lookup"><span data-stu-id="52fa5-156">DateTime</span></span></td>
<td><span data-ttu-id="52fa5-157">El valor debe ser un VT_FILETIME, que es un <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="52fa5-157">The value must be a VT_FILETIME, which is a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-158">Guid</span><span class="sxs-lookup"><span data-stu-id="52fa5-158">Guid</span></span></td>
<td><span data-ttu-id="52fa5-159">El valor debe ser un VT_CLSID, que es un identificador de clase (CLSID).</span><span class="sxs-lookup"><span data-stu-id="52fa5-159">The value must be a VT_CLSID, which is a class identifier (CLSID).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-160">Blob</span><span class="sxs-lookup"><span data-stu-id="52fa5-160">Blob</span></span></td>
<td><span data-ttu-id="52fa5-161">El valor debe ser un VT_BLOB, que son bytes con prefijo de longitud.</span><span class="sxs-lookup"><span data-stu-id="52fa5-161">The value must be a VT_BLOB, which are length-prefixed bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-162">Stream</span><span class="sxs-lookup"><span data-stu-id="52fa5-162">Stream</span></span></td>
<td><span data-ttu-id="52fa5-163">El valor debe ser un VT_STREAM, que es un objeto que implementa <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="52fa5-163">The value must be a VT_STREAM, which is an object that implements <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-164">Portapapeles</span><span class="sxs-lookup"><span data-stu-id="52fa5-164">Clipboard</span></span></td>
<td><span data-ttu-id="52fa5-165">El valor debe ser un VT_CF, que es un formato de Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="52fa5-165">The value must be a VT_CF, which is a clipboard format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-166">Object</span><span class="sxs-lookup"><span data-stu-id="52fa5-166">Object</span></span></td>
<td><span data-ttu-id="52fa5-167">El valor debe ser un VT_UNKNOWN, que es un objeto que implementa <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="52fa5-167">The value must be a VT_UNKNOWN, which is an object that implements <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-168">groupingRange</span><span class="sxs-lookup"><span data-stu-id="52fa5-168">groupingRange</span></span></td>
<td><span data-ttu-id="52fa5-169">Opcional.</span><span class="sxs-lookup"><span data-stu-id="52fa5-169">Optional.</span></span> <span data-ttu-id="52fa5-170">El valor predeterminado es &quot; discreto &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-170">Default is &quot;Discrete&quot;.</span></span> <span data-ttu-id="52fa5-171">Especifica cómo se muestra la propiedad cuando una vista está agrupada por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="52fa5-171">Specifies how the property is displayed when a view is grouped by this property.</span></span> <span data-ttu-id="52fa5-172">Una vez establecido aquí, <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription:: GetGroupingRange</strong></a>recupera estos valores.</span><span class="sxs-lookup"><span data-stu-id="52fa5-172">Once set here, these values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription::GetGroupingRange</strong></a>.</span></span> <span data-ttu-id="52fa5-173">Los tipos válidos son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="52fa5-173">The following are valid types.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="52fa5-174">Value</span><span class="sxs-lookup"><span data-stu-id="52fa5-174">Value</span></span></th>
<th><span data-ttu-id="52fa5-175">Significado</span><span class="sxs-lookup"><span data-stu-id="52fa5-175">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52fa5-176">Discrete</span><span class="sxs-lookup"><span data-stu-id="52fa5-176">Discrete</span></span></td>
<td><span data-ttu-id="52fa5-177">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="52fa5-177">Default.</span></span> <span data-ttu-id="52fa5-178">Muestra valores individuales.</span><span class="sxs-lookup"><span data-stu-id="52fa5-178">Displays individual values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-179">Alfanuméricas</span><span class="sxs-lookup"><span data-stu-id="52fa5-179">Alphanumeric</span></span></td>
<td><span data-ttu-id="52fa5-180">Muestra los intervalos alfanuméricos estáticos para los valores.</span><span class="sxs-lookup"><span data-stu-id="52fa5-180">Displays static alphanumeric ranges for values.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-181">Tamaño</span><span class="sxs-lookup"><span data-stu-id="52fa5-181">Size</span></span></td>
<td><span data-ttu-id="52fa5-182">Muestra los intervalos de tamaño estático de los valores.</span><span class="sxs-lookup"><span data-stu-id="52fa5-182">Displays static size ranges for values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-183">Fecha</span><span class="sxs-lookup"><span data-stu-id="52fa5-183">Date</span></span></td>
<td><span data-ttu-id="52fa5-184">Muestra los grupos de mes/año.</span><span class="sxs-lookup"><span data-stu-id="52fa5-184">Displays month/year groups.</span></span> <span data-ttu-id="52fa5-185">Valor predeterminado para las propiedades de tipo = &quot; DateTime &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-185">Default for properties of type=&quot;DateTime&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-186">TimeRelative</span><span class="sxs-lookup"><span data-stu-id="52fa5-186">TimeRelative</span></span></td>
<td><span data-ttu-id="52fa5-187">Muestra en grupos relativos a tiempo.</span><span class="sxs-lookup"><span data-stu-id="52fa5-187">Displays in time-relative groups.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-188">Dinámica</span><span class="sxs-lookup"><span data-stu-id="52fa5-188">Dynamic</span></span></td>
<td><span data-ttu-id="52fa5-189">Muestra los intervalos creados dinámicamente para los valores.</span><span class="sxs-lookup"><span data-stu-id="52fa5-189">Displays dynamically created ranges for the values.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-190">Percent</span><span class="sxs-lookup"><span data-stu-id="52fa5-190">Percent</span></span></td>
<td><span data-ttu-id="52fa5-191">Muestra los depósitos de porcentaje.</span><span class="sxs-lookup"><span data-stu-id="52fa5-191">Displays percent buckets.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-192">isInnate</span><span class="sxs-lookup"><span data-stu-id="52fa5-192">isInnate</span></span></td>
<td><span data-ttu-id="52fa5-193">Público.</span><span class="sxs-lookup"><span data-stu-id="52fa5-193">Public.</span></span> <span data-ttu-id="52fa5-194">Opcional.</span><span class="sxs-lookup"><span data-stu-id="52fa5-194">Optional.</span></span> <span data-ttu-id="52fa5-195">El valor predeterminado es &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="52fa5-195">Default is &quot;false&quot;.</span></span> <span data-ttu-id="52fa5-196">Especifica si la propiedad se considera innate.</span><span class="sxs-lookup"><span data-stu-id="52fa5-196">Specifies whether the property is considered innate.</span></span> <span data-ttu-id="52fa5-197">Una propiedad INNATE es aquella que se calcula a partir del contenido de un archivo o de otros recursos o sistemas.</span><span class="sxs-lookup"><span data-stu-id="52fa5-197">An innate property is one which is either calculated from the content of a file, or from other resources or systems.</span></span> <span data-ttu-id="52fa5-198">Por ejemplo, System. size es una propiedad INNATE proporcionada por el sistema de archivos; cambiar el valor de la propiedad en y de sí mismo no hace nada.</span><span class="sxs-lookup"><span data-stu-id="52fa5-198">For example, System.Size is an innate property provided by the file system; changing the value of the property in and of itself does nothing.</span></span> <span data-ttu-id="52fa5-199">Otros ejemplos son System. Image. Dimensions y System.Document. PageCount, que se calculan mediante programas basados en el contenido del archivo, no en función de una configuración modificable por el usuario.</span><span class="sxs-lookup"><span data-stu-id="52fa5-199">Other examples are System.Image.Dimensions and System.Document.PageCount, which are calculated by programs based upon the content of the file, not based upon a user-changeable setting.</span></span> <span data-ttu-id="52fa5-200">Establecer isInnate = &quot; true &quot; significa que el usuario no puede editar esta propiedad directamente a través de un control de propiedad.</span><span class="sxs-lookup"><span data-stu-id="52fa5-200">Setting isInnate=&quot;true&quot; means the user cannot edit this property directly via a property control.</span></span> <span data-ttu-id="52fa5-201">Este valor se asigna a la marca PDTF_ISINNATE definida en <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> y se usa en <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="52fa5-201">This value maps to the PDTF_ISINNATE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-202">canBePurged</span><span class="sxs-lookup"><span data-stu-id="52fa5-202">canBePurged</span></span></td>
<td><span data-ttu-id="52fa5-203"><strong>Windows Vista con Service Pack 1 (SP1) y versiones posteriores</strong>.</span><span class="sxs-lookup"><span data-stu-id="52fa5-203"><strong>Windows Vista with Service Pack 1 (SP1) and later only</strong>.</span></span> <span data-ttu-id="52fa5-204">Público.</span><span class="sxs-lookup"><span data-stu-id="52fa5-204">Public.</span></span> <span data-ttu-id="52fa5-205">Opcional.</span><span class="sxs-lookup"><span data-stu-id="52fa5-205">Optional.</span></span> <span data-ttu-id="52fa5-206">Cuando se establece en &quot; true &quot; , permite que se elimine una propiedad innate.</span><span class="sxs-lookup"><span data-stu-id="52fa5-206">When set to &quot;true&quot;, allows an innate property to be deleted.</span></span> <span data-ttu-id="52fa5-207">Las propiedades de INNATE, que se calculan a partir de otras propiedades, son de solo lectura por definición.</span><span class="sxs-lookup"><span data-stu-id="52fa5-207">Innate properties, which are calculated from other properties, are read-only by definition.</span></span> <span data-ttu-id="52fa5-208">El valor predeterminado de este atributo depende del valor de <em>isInnate</em> .</span><span class="sxs-lookup"><span data-stu-id="52fa5-208">The default value for this attribute depends on the <em>isInnate</em> value.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="52fa5-209">isInnate</span><span class="sxs-lookup"><span data-stu-id="52fa5-209">isInnate</span></span></th>
<th><span data-ttu-id="52fa5-210">Valor predeterminado de canBePurged</span><span class="sxs-lookup"><span data-stu-id="52fa5-210">canBePurged Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52fa5-211">true</span><span class="sxs-lookup"><span data-stu-id="52fa5-211">true</span></span></td>
<td><span data-ttu-id="52fa5-212">false</span><span class="sxs-lookup"><span data-stu-id="52fa5-212">false</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-213">false</span><span class="sxs-lookup"><span data-stu-id="52fa5-213">false</span></span></td>
<td><span data-ttu-id="52fa5-214">true</span><span class="sxs-lookup"><span data-stu-id="52fa5-214">true</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="52fa5-215">Una propiedad cuyo valor <em>isInnate</em> es &quot; false &quot; (lo que significa que la propiedad es de lectura/escritura) no puede establecer también el valor de <em>canBePurged</em> en &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-215">A property whose <em>isInnate</em> value is &quot;false&quot; (meaning that the property is read/write) cannot also set the <em>canBePurged</em> value to &quot;false&quot;.</span></span> <span data-ttu-id="52fa5-216">El sistema operativo aplica esta restricción.</span><span class="sxs-lookup"><span data-stu-id="52fa5-216">This restriction is enforced by the operating system.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="52fa5-217">Aunque este atributo se presentó en Windows Vista con Service Pack 1 (SP1), un archivo. propDesc que incluye este atributo es compatible con Windows vista antes de Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="52fa5-217">Although this attribute was introduced in Windows Vista with Service Pack 1 (SP1), a .propdesc file that includes this attribute is compatible with Windows Vista prior to Windows Vista with SP1.</span></span> <span data-ttu-id="52fa5-218">El atributo <em>canBePurged</em> simplemente se omite en esa situación.</span><span class="sxs-lookup"><span data-stu-id="52fa5-218">The <em>canBePurged</em> attribute is simply ignored in that situation.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-219">multipleValues</span><span class="sxs-lookup"><span data-stu-id="52fa5-219">multipleValues</span></span></td>
<td><span data-ttu-id="52fa5-220">Público.</span><span class="sxs-lookup"><span data-stu-id="52fa5-220">Public.</span></span> <span data-ttu-id="52fa5-221">Opcional.</span><span class="sxs-lookup"><span data-stu-id="52fa5-221">Optional.</span></span> <span data-ttu-id="52fa5-222">El valor predeterminado es &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="52fa5-222">Default is &quot;false&quot;.</span></span> <span data-ttu-id="52fa5-223">Especifica si esta propiedad puede tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="52fa5-223">Specifies whether this property can have multiple values.</span></span> <span data-ttu-id="52fa5-224">Este valor se asigna a la marca PDTF_MULTIPLEVALUES definida en <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> y se usa en <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="52fa5-224">This value maps to the PDTF_MULTIPLEVALUES flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span> <span data-ttu-id="52fa5-225">Esto también influye en si VT_VECTOR es o se va al VARTYPE del valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="52fa5-225">This also influences whether VT_VECTOR is OR'd to the VARTYPE of the property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-226">isGroup</span><span class="sxs-lookup"><span data-stu-id="52fa5-226">isGroup</span></span></td>
<td><span data-ttu-id="52fa5-227">Público.</span><span class="sxs-lookup"><span data-stu-id="52fa5-227">Public.</span></span> <span data-ttu-id="52fa5-228">Opcional.</span><span class="sxs-lookup"><span data-stu-id="52fa5-228">Optional.</span></span> <span data-ttu-id="52fa5-229">El valor predeterminado es &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="52fa5-229">Default is &quot;false&quot;.</span></span> <span data-ttu-id="52fa5-230">Especifica si la propiedad es un encabezado de grupo.</span><span class="sxs-lookup"><span data-stu-id="52fa5-230">Specifies whether the property is a group heading.</span></span> <span data-ttu-id="52fa5-231">Un encabezado de grupo se usa estrictamente en Profiles, no tiene ningún valor, nunca se almacena en un archivo y también debe tener <typeInfo type=&quot;Null&quot;> .</span><span class="sxs-lookup"><span data-stu-id="52fa5-231">A group heading is strictly used in proplists, has no value, is never stored in a file, and should also have <typeInfo type=&quot;Null&quot;>.</span></span> <span data-ttu-id="52fa5-232">Parte de la interfaz de usuario del sistema usa los representadores para indicar la secuencia de las propiedades que se van a mostrar.</span><span class="sxs-lookup"><span data-stu-id="52fa5-232">Some UI in the system use proplists to indicate the sequence of the properties to display.</span></span> <span data-ttu-id="52fa5-233">Estos profiles pueden incluir referencias a los encabezados de grupo (por ejemplo, System. PropGroup. Camera), que indican a la interfaz de usuario que inicie una nueva sección de grupo (por ejemplo, &quot; configuración de cámara &quot; ).</span><span class="sxs-lookup"><span data-stu-id="52fa5-233">These proplists may include references to group headings (eg, System.PropGroup.Camera), which tell the UI to start a new group section (eg, &quot;Camera Settings&quot;).</span></span> <span data-ttu-id="52fa5-234">Una descripción de propiedad con isGroup = &quot; true &quot; debe especificar <labelInfo label=&quot;Some localized label&quot;> , de lo contrario, no es una propiedad útil.</span><span class="sxs-lookup"><span data-stu-id="52fa5-234">A property description with isGroup=&quot;true&quot; should specify a <labelInfo label=&quot;Some localized label&quot;>, otherwise it isn't a useful property.</span></span> <span data-ttu-id="52fa5-235">Este valor se asigna a la marca PDTF_ISGROUP definida en <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> y se usa en <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="52fa5-235">This value maps to the PDTF_ISGROUP flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-236">AggregationType</span><span class="sxs-lookup"><span data-stu-id="52fa5-236">aggregationType</span></span></td>
<td><span data-ttu-id="52fa5-237">Público.</span><span class="sxs-lookup"><span data-stu-id="52fa5-237">Public.</span></span> <span data-ttu-id="52fa5-238">Opcional.</span><span class="sxs-lookup"><span data-stu-id="52fa5-238">Optional.</span></span> <span data-ttu-id="52fa5-239">El valor predeterminado es &quot; default &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-239">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="52fa5-240">Especifica cómo se muestran las propiedades de agregado cuando se seleccionan varios elementos.</span><span class="sxs-lookup"><span data-stu-id="52fa5-240">Specifies how aggregate properties are displayed when multiple items are selected.</span></span> <span data-ttu-id="52fa5-241">Una vez establecido aquí, <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription:: GetAggregationType</strong></a> recupera estos valores como <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="52fa5-241">Once set here, these values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription::GetAggregationType</strong></a> as an <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>.</span></span> <span data-ttu-id="52fa5-242">Los tipos válidos son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="52fa5-242">The following are valid types.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="52fa5-243">Value</span><span class="sxs-lookup"><span data-stu-id="52fa5-243">Value</span></span></th>
<th><span data-ttu-id="52fa5-244">Significado</span><span class="sxs-lookup"><span data-stu-id="52fa5-244">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52fa5-245">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="52fa5-245">Default</span></span></td>
<td><span data-ttu-id="52fa5-246">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="52fa5-246">Default.</span></span> <span data-ttu-id="52fa5-247">Muestra un marcador de posición de <strong>varios valores</strong> en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="52fa5-247">Displays a <strong>Multiple Values</strong> placeholder in the UI.</span></span> <span data-ttu-id="52fa5-248">Este es el valor predeterminado si el <em>tipo</em> es incompatible con el <em>aggregationType</em>especificado.</span><span class="sxs-lookup"><span data-stu-id="52fa5-248">This is the default if the <em>type</em> is incompatible with the specified <em>aggregationType</em>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-249">First</span><span class="sxs-lookup"><span data-stu-id="52fa5-249">First</span></span></td>
<td><span data-ttu-id="52fa5-250">Muestra el valor de propiedad del primer elemento de la selección o colección.</span><span class="sxs-lookup"><span data-stu-id="52fa5-250">Displays the property value of the first item in the selection or collection.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-251">Sum</span><span class="sxs-lookup"><span data-stu-id="52fa5-251">Sum</span></span></td>
<td><span data-ttu-id="52fa5-252">Muestra la suma de los valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="52fa5-252">Displays the sum of the numerical values.</span></span> <span data-ttu-id="52fa5-253">Resulta útil para propiedades como System. Media. Duration o System. size.</span><span class="sxs-lookup"><span data-stu-id="52fa5-253">Useful for properties such as System.Media.Duration or System.Size.</span></span> <span data-ttu-id="52fa5-254">Este valor no es compatible con los tipos no numéricos.</span><span class="sxs-lookup"><span data-stu-id="52fa5-254">This value is not compatible with non-numeric types.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-255">Average</span><span class="sxs-lookup"><span data-stu-id="52fa5-255">Average</span></span></td>
<td><span data-ttu-id="52fa5-256">Muestra el promedio de los valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="52fa5-256">Displays the average of the numerical values.</span></span> <span data-ttu-id="52fa5-257">Resulta útil para las propiedades como System. Rating.</span><span class="sxs-lookup"><span data-stu-id="52fa5-257">Useful for properties such as System.Rating.</span></span> <span data-ttu-id="52fa5-258">Este valor no es compatible con los tipos no numéricos.</span><span class="sxs-lookup"><span data-stu-id="52fa5-258">This value is not compatible with non-numeric types.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-259">DateRange</span><span class="sxs-lookup"><span data-stu-id="52fa5-259">DateRange</span></span></td>
<td><span data-ttu-id="52fa5-260">Muestra un intervalo de fechas.</span><span class="sxs-lookup"><span data-stu-id="52fa5-260">Displays a range of dates.</span></span> <span data-ttu-id="52fa5-261">Resulta útil para propiedades como System. Photo. DateTaken.</span><span class="sxs-lookup"><span data-stu-id="52fa5-261">Useful for properties like System.Photo.DateTaken.</span></span> <span data-ttu-id="52fa5-262">Este valor no es compatible con nada excepto Type = &quot; DateTime &quot; y es el valor predeterminado para las propiedades de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="52fa5-262">This value is not compatible with anything except type=&quot;DateTime&quot; and is the default for properties of that type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-263">Union</span><span class="sxs-lookup"><span data-stu-id="52fa5-263">Union</span></span></td>
<td><span data-ttu-id="52fa5-264">Muestra una Unión de todos los valores de la selección o la colección.</span><span class="sxs-lookup"><span data-stu-id="52fa5-264">Displays a union of all the values in the selection or collection.</span></span> <span data-ttu-id="52fa5-265">El orden en que se muestran los valores es indefinido.</span><span class="sxs-lookup"><span data-stu-id="52fa5-265">The order in which the values are shown is undefined.</span></span> <span data-ttu-id="52fa5-266">Este valor es el predeterminado para las propiedades de tipo = &quot; String &quot; y multipleValues = &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-266">This value is the default for properties of type=&quot;String&quot; and multipleValues=&quot;true&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-267">Máxima</span><span class="sxs-lookup"><span data-stu-id="52fa5-267">Maximum</span></span></td>
<td><span data-ttu-id="52fa5-268">Muestra el valor máximo de la colección.</span><span class="sxs-lookup"><span data-stu-id="52fa5-268">Displays the maximum value in the collection.</span></span> <span data-ttu-id="52fa5-269">Útil para propiedades como System. DateModified.</span><span class="sxs-lookup"><span data-stu-id="52fa5-269">Useful for properties like System.DateModified.</span></span> <span data-ttu-id="52fa5-270">No es compatible con tipos no numéricos o sin fecha.</span><span class="sxs-lookup"><span data-stu-id="52fa5-270">Not compatible with non-numeric or non-date types.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-271">Mínima</span><span class="sxs-lookup"><span data-stu-id="52fa5-271">Minimum</span></span></td>
<td><span data-ttu-id="52fa5-272">Muestra el valor mínimo de la colección.</span><span class="sxs-lookup"><span data-stu-id="52fa5-272">Displays the minimum value in the collection.</span></span> <span data-ttu-id="52fa5-273">No es compatible con tipos no numéricos o sin fecha.</span><span class="sxs-lookup"><span data-stu-id="52fa5-273">Not compatible with non-numeric or non-date types.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-274">isTreeProperty</span><span class="sxs-lookup"><span data-stu-id="52fa5-274">isTreeProperty</span></span></td>
<td><span data-ttu-id="52fa5-275">Público.</span><span class="sxs-lookup"><span data-stu-id="52fa5-275">Public.</span></span> <span data-ttu-id="52fa5-276">Opcional.</span><span class="sxs-lookup"><span data-stu-id="52fa5-276">Optional.</span></span> <span data-ttu-id="52fa5-277">El valor predeterminado es &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="52fa5-277">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-278">isViewable</span><span class="sxs-lookup"><span data-stu-id="52fa5-278">isViewable</span></span></td>
<td><span data-ttu-id="52fa5-279">Público.</span><span class="sxs-lookup"><span data-stu-id="52fa5-279">Public.</span></span> <span data-ttu-id="52fa5-280">Opcional.</span><span class="sxs-lookup"><span data-stu-id="52fa5-280">Optional.</span></span> <span data-ttu-id="52fa5-281">El valor predeterminado es &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="52fa5-281">Default value is &quot;false&quot;.</span></span> <span data-ttu-id="52fa5-282">Especifica si esta propiedad está pensada para ser visible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="52fa5-282">Specifies whether this property is intended to be viewable to the user.</span></span> <span data-ttu-id="52fa5-283">Por ejemplo, la interfaz de usuario del selector de columnas solo muestra las propiedades que tienen isViewable = &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-283">For example, the Column Chooser UI only shows the properties that have isViewable=&quot;true&quot;.</span></span> <span data-ttu-id="52fa5-284">La excepción es una interfaz de usuario controlada por un proplist, que siempre mostrará la propiedad.</span><span class="sxs-lookup"><span data-stu-id="52fa5-284">The exception is UI that is driven by a proplist, which will always show the property.</span></span> <span data-ttu-id="52fa5-285">Si tiene una propiedad que solo está diseñada para el control de datos entre dos objetos y nunca está prevista su visualización por parte del usuario, este atributo debe ser false.</span><span class="sxs-lookup"><span data-stu-id="52fa5-285">If you have a property that is only meant to shuttle data between two objects, and never intended to be viewed by the user, this attribute should be false.</span></span> <span data-ttu-id="52fa5-286">Este valor se asigna a la marca PDTF_ISVIEWABLE definida en <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> y se usa en <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="52fa5-286">This value maps to the PDTF_ISVIEWABLE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-287">isQueryable</span><span class="sxs-lookup"><span data-stu-id="52fa5-287">isQueryable</span></span></td>
<td><span data-ttu-id="52fa5-288">Solo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52fa5-288">Windows Vista only.</span></span> <span data-ttu-id="52fa5-289">No se admite en Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="52fa5-289">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="52fa5-290">Público.</span><span class="sxs-lookup"><span data-stu-id="52fa5-290">Public.</span></span> <span data-ttu-id="52fa5-291">Opcional.</span><span class="sxs-lookup"><span data-stu-id="52fa5-291">Optional.</span></span> <span data-ttu-id="52fa5-292">El valor predeterminado es &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="52fa5-292">Default value is &quot;false&quot;.</span></span> <span data-ttu-id="52fa5-293">Especifica si esta propiedad está pensada para estar disponible en la interfaz de usuario de Generador de consultas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="52fa5-293">Specifies whether this property is intended to be available in the Search Query Builder UI.</span></span> <span data-ttu-id="52fa5-294">Una propiedad debe tener isViewable = &quot; true &quot; antes de que &quot; se respete isQueryable = true &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-294">A property must have isViewable=&quot;true&quot; before isQueryable=&quot;true&quot; is respected.</span></span> <span data-ttu-id="52fa5-295">Este valor se asigna a la marca PDTF_ISQUERYABLE definida en <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> y se usa en <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="52fa5-295">This value maps to the PDTF_ISQUERYABLE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-296">searchRawValue</span><span class="sxs-lookup"><span data-stu-id="52fa5-296">searchRawValue</span></span></td>
<td><span data-ttu-id="52fa5-297"><strong>Windows 7 y versiones posteriores.</strong></span><span class="sxs-lookup"><span data-stu-id="52fa5-297"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="52fa5-298">Público.</span><span class="sxs-lookup"><span data-stu-id="52fa5-298">Public.</span></span> <span data-ttu-id="52fa5-299">Opcional.</span><span class="sxs-lookup"><span data-stu-id="52fa5-299">Optional.</span></span> <span data-ttu-id="52fa5-300">El valor predeterminado es &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="52fa5-300">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-301">includeInFullTextQuery</span><span class="sxs-lookup"><span data-stu-id="52fa5-301">includeInFullTextQuery</span></span></td>
<td><span data-ttu-id="52fa5-302">Solo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52fa5-302">Windows Vista only.</span></span> <span data-ttu-id="52fa5-303">No se admite en Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="52fa5-303">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="52fa5-304">Público.</span><span class="sxs-lookup"><span data-stu-id="52fa5-304">Public.</span></span> <span data-ttu-id="52fa5-305">Opcional.</span><span class="sxs-lookup"><span data-stu-id="52fa5-305">Optional.</span></span> <span data-ttu-id="52fa5-306">El valor predeterminado es &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="52fa5-306">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-307">conditionType</span><span class="sxs-lookup"><span data-stu-id="52fa5-307">conditionType</span></span></td>
<td><span data-ttu-id="52fa5-308">Público.</span><span class="sxs-lookup"><span data-stu-id="52fa5-308">Public.</span></span> <span data-ttu-id="52fa5-309">Opcional.</span><span class="sxs-lookup"><span data-stu-id="52fa5-309">Optional.</span></span> <span data-ttu-id="52fa5-310">El valor predeterminado es &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-310">Default is &quot;String&quot;.</span></span> <span data-ttu-id="52fa5-311">Especifica una sugerencia para la interfaz de usuario de Generador de consultas de búsqueda para que pueda determinar la lista de posibles operadores de condición dentro de un predicado.</span><span class="sxs-lookup"><span data-stu-id="52fa5-311">Specifies a hint to the Search Query Builder UI so that it can determine the list of possible condition operators inside a predicate.</span></span> <span data-ttu-id="52fa5-312">A continuación se indican los valores reconocidos.</span><span class="sxs-lookup"><span data-stu-id="52fa5-312">The following are recognized values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="52fa5-313">Value</span><span class="sxs-lookup"><span data-stu-id="52fa5-313">Value</span></span></th>
<th><span data-ttu-id="52fa5-314">Significado</span><span class="sxs-lookup"><span data-stu-id="52fa5-314">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52fa5-315">String</span><span class="sxs-lookup"><span data-stu-id="52fa5-315">String</span></span></td>
<td><span data-ttu-id="52fa5-316">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="52fa5-316">Default.</span></span> <span data-ttu-id="52fa5-317">Se usarán los siguientes operadores: &quot; es &quot; , &quot; no es &quot; , &quot; &lt; &quot; , &quot; &gt; &quot; , &quot; <= &quot; , &quot; >= &quot; , &quot; comienza con &quot; , &quot; termina con &quot; , &quot; contiene &quot; , &quot; no contiene &quot; , &quot; como &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-317">The following operators will be used: &quot;is&quot;, &quot;is not&quot;, &quot;&lt;&quot;, &quot;&gt;&quot;, &quot;<=&quot;, &quot;>=&quot;, &quot;starts with&quot;, &quot;ends with&quot;, &quot;contains&quot;, &quot;doesn't contain&quot;, &quot;is like&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-318">Number</span><span class="sxs-lookup"><span data-stu-id="52fa5-318">Number</span></span></td>
<td><span data-ttu-id="52fa5-319">Valor predeterminado para las propiedades numéricas.</span><span class="sxs-lookup"><span data-stu-id="52fa5-319">Default for numeric properties.</span></span> <span data-ttu-id="52fa5-320">Se usarán los siguientes operadores: es igual a, no es igual a, &quot; &quot; &quot; &quot; &quot; es menor que &quot; , &quot; es mayor que &quot; , &quot; es menor o igual que &quot; , &quot; es mayor o igual que &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-320">The following operators will be used: &quot;equals&quot;, &quot;doesn't equal&quot;, &quot;is less than&quot;, &quot;is greater than&quot;, &quot;is less than or equal to&quot;, &quot;is greater than or equal to&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-321">DateTime</span><span class="sxs-lookup"><span data-stu-id="52fa5-321">DateTime</span></span></td>
<td><span data-ttu-id="52fa5-322">Valor predeterminado para las propiedades de tipo = &quot; DateTime &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-322">Default for properties of type=&quot;DateTime&quot;.</span></span> <span data-ttu-id="52fa5-323">Se usarán los siguientes operadores: &quot; is &quot; , &quot; is not &quot; , &quot; is Before, &quot; &quot; is After &quot; , &quot; is Before pero includes &quot; , &quot; is After y includes &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-323">The following operators will be used: &quot;is&quot;, &quot;is not&quot;, &quot;is before&quot;, &quot;is after&quot;, &quot;is before but includes&quot;, &quot;is after but includes&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-324">Boolean</span><span class="sxs-lookup"><span data-stu-id="52fa5-324">Boolean</span></span></td>
<td><span data-ttu-id="52fa5-325">Valor predeterminado para las propiedades de tipo = &quot; booleano &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-325">Default for properties of type=&quot;Boolean&quot;.</span></span> <span data-ttu-id="52fa5-326">Igual que el número.</span><span class="sxs-lookup"><span data-stu-id="52fa5-326">Same as Number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-327">Tamaño</span><span class="sxs-lookup"><span data-stu-id="52fa5-327">Size</span></span></td>
<td><span data-ttu-id="52fa5-328">Igual que el número.</span><span class="sxs-lookup"><span data-stu-id="52fa5-328">Same as Number.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-329">defaultOperation</span><span class="sxs-lookup"><span data-stu-id="52fa5-329">defaultOperation</span></span></td>
<td><span data-ttu-id="52fa5-330">Público.</span><span class="sxs-lookup"><span data-stu-id="52fa5-330">Public.</span></span> <span data-ttu-id="52fa5-331">Opcional.</span><span class="sxs-lookup"><span data-stu-id="52fa5-331">Optional.</span></span> <span data-ttu-id="52fa5-332">El valor predeterminado es &quot; igual a &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-332">Default is &quot;Equal&quot;.</span></span> <span data-ttu-id="52fa5-333">Especifica una sugerencia a la herramienta de Generador de consultas de búsqueda para que pueda determinar el operador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="52fa5-333">Specifies a hint to the Search Query Builder tool so that it can determine the default operator.</span></span> <span data-ttu-id="52fa5-334">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="52fa5-334">The possible values are as follows:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="52fa5-335">Value</span><span class="sxs-lookup"><span data-stu-id="52fa5-335">Value</span></span></th>
<th><span data-ttu-id="52fa5-336">Significado</span><span class="sxs-lookup"><span data-stu-id="52fa5-336">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52fa5-337">Equal</span><span class="sxs-lookup"><span data-stu-id="52fa5-337">Equal</span></span></td>
<td><span data-ttu-id="52fa5-338">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="52fa5-338">Default.</span></span> <span data-ttu-id="52fa5-339">Indica un equivalente.</span><span class="sxs-lookup"><span data-stu-id="52fa5-339">Indicates equivalent.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-340">NotEqual</span><span class="sxs-lookup"><span data-stu-id="52fa5-340">NotEqual</span></span></td>
<td><span data-ttu-id="52fa5-341">Indica que no es equivalente.</span><span class="sxs-lookup"><span data-stu-id="52fa5-341">Indicates not equivalent.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-342">LessThan</span><span class="sxs-lookup"><span data-stu-id="52fa5-342">LessThan</span></span></td>
<td><span data-ttu-id="52fa5-343">Indica que es menor que.</span><span class="sxs-lookup"><span data-stu-id="52fa5-343">Indicates less than.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52fa5-344">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="52fa5-344">GreaterThan</span></span></td>
<td><span data-ttu-id="52fa5-345">Valor predeterminado para las propiedades de conditionType = &quot; size &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-345">Default for properties of conditionType=&quot;Size&quot;.</span></span> <span data-ttu-id="52fa5-346">Indica mayor que.</span><span class="sxs-lookup"><span data-stu-id="52fa5-346">Indicates greater than.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52fa5-347">Contiene</span><span class="sxs-lookup"><span data-stu-id="52fa5-347">Contains</span></span></td>
<td><span data-ttu-id="52fa5-348">Valor predeterminado para las propiedades de conditionType = &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="52fa5-348">Default for properties of conditionType=&quot;String&quot;.</span></span> <span data-ttu-id="52fa5-349">Indica la inclusión.</span><span class="sxs-lookup"><span data-stu-id="52fa5-349">Indicates inclusion.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
