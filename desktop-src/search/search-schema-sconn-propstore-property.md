---
description: El <property> elemento opcional especifica una propiedad utilizada por el conector de búsqueda. Estas propiedades son específicas de este conector de búsqueda, por lo que no hay ningún conjunto de nombres predefinido que usar. Este elemento no tiene elementos secundarios.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: Elemento Property de propertyStore (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2e4cee6f26ee65ba03d9225eafcea4a03a7c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540627"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a><span data-ttu-id="035fe-105">Elemento Property de propertyStore (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="035fe-105">property Element of propertyStore (Search Connector Schema)</span></span>

<span data-ttu-id="035fe-106">El <property> elemento opcional especifica una propiedad utilizada por el conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="035fe-106">The optional <property> element specifies a property used by the search connector.</span></span> <span data-ttu-id="035fe-107">Estas propiedades son específicas de este conector de búsqueda, por lo que no hay ningún conjunto de nombres predefinido que usar.</span><span class="sxs-lookup"><span data-stu-id="035fe-107">These properties are specific to this search connector, so there is no predefined set of names to use.</span></span> <span data-ttu-id="035fe-108">Este elemento no tiene elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="035fe-108">This element has no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="035fe-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="035fe-109">Syntax</span></span>


```
<!-- property for propertyStore element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded">
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension base="xs:anyType">
                        <xs:attribute name="name" type="canonical-name" use="required"/>
                        <xs:attribute name="type"/>
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="035fe-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="035fe-110">Element Information</span></span>



| <span data-ttu-id="035fe-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="035fe-111">Parent Element</span></span>                                                                           | <span data-ttu-id="035fe-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="035fe-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="035fe-113">Elemento propertyStore (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="035fe-113">propertyStore Element (Search Connector Schema)</span></span>](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a><span data-ttu-id="035fe-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="035fe-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="035fe-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="035fe-115">Attribute</span></span></th>
<th><span data-ttu-id="035fe-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="035fe-116">Description</span></span></th>
<th><span data-ttu-id="035fe-117">Valores</span><span class="sxs-lookup"><span data-stu-id="035fe-117">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="035fe-118">name</span><span class="sxs-lookup"><span data-stu-id="035fe-118">name</span></span></td>
<td><span data-ttu-id="035fe-119">Público.</span><span class="sxs-lookup"><span data-stu-id="035fe-119">Public.</span></span> <span data-ttu-id="035fe-120">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="035fe-120">Required.</span></span> <span data-ttu-id="035fe-121">El nombre para mostrar de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="035fe-121">The display name of the property.</span></span></td>
<td> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="035fe-122">type</span><span class="sxs-lookup"><span data-stu-id="035fe-122">type</span></span></td>
<td><span data-ttu-id="035fe-123">Público.</span><span class="sxs-lookup"><span data-stu-id="035fe-123">Public.</span></span> <span data-ttu-id="035fe-124">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="035fe-124">Required.</span></span> <span data-ttu-id="035fe-125">El tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="035fe-125">The type of property.</span></span></td>
<td><span data-ttu-id="035fe-126">Any: valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="035fe-126">Any: Default.</span></span> <span data-ttu-id="035fe-127">El subsistema de propiedades no convertirá el valor.</span><span class="sxs-lookup"><span data-stu-id="035fe-127">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="035fe-128">GetPropertyType devolverá VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="035fe-128">VT_NULL will be returned by GetPropertyType.</span></span>
<ul>
<li><span data-ttu-id="035fe-129">NULL: no hay ningún valor para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="035fe-129">Null: There is no value for this property.</span></span> <span data-ttu-id="035fe-130">GetPropertyType devolverá VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="035fe-130">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="035fe-131">Cadena: el valor debe ser un VT_LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="035fe-131">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="035fe-132">Booleano: el valor debe ser un VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="035fe-132">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="035fe-133">Byte: el valor debe ser un VT_UI1.</span><span class="sxs-lookup"><span data-stu-id="035fe-133">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="035fe-134">Buffer: el valor debe ser un VT_UI1 | VT_VECTOR búfer de bytes.</span><span class="sxs-lookup"><span data-stu-id="035fe-134">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="035fe-135">Int16: el valor debe ser un VT_I2.</span><span class="sxs-lookup"><span data-stu-id="035fe-135">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="035fe-136">UInt16: el valor debe ser un VT_UI2.</span><span class="sxs-lookup"><span data-stu-id="035fe-136">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="035fe-137">Int32: el valor debe ser un VT_I4.</span><span class="sxs-lookup"><span data-stu-id="035fe-137">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="035fe-138">UInt32: el valor debe ser un VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="035fe-138">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="035fe-139">Int64: el valor debe ser un VT_I8.</span><span class="sxs-lookup"><span data-stu-id="035fe-139">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="035fe-140">UInt64: el valor debe ser un VT_UI8</span><span class="sxs-lookup"><span data-stu-id="035fe-140">UInt64: The value must be a VT_UI8</span></span></li>
<li><span data-ttu-id="035fe-141">Double: el valor debe ser un VT_R8.</span><span class="sxs-lookup"><span data-stu-id="035fe-141">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="035fe-142">DateTime: el valor debe ser un VT_FILETIME.</span><span class="sxs-lookup"><span data-stu-id="035fe-142">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="035fe-143">GUID: el valor debe ser un VT_CLSID.</span><span class="sxs-lookup"><span data-stu-id="035fe-143">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="035fe-144">BLOB: el valor debe ser un VT_BLOB.</span><span class="sxs-lookup"><span data-stu-id="035fe-144">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="035fe-145">Objeto: el valor debe ser un VT_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="035fe-145">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="035fe-146">Stream: el valor debe ser un VT_STREAM.</span><span class="sxs-lookup"><span data-stu-id="035fe-146">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="035fe-147">Clipboard: el valor debe ser un VT_CF.</span><span class="sxs-lookup"><span data-stu-id="035fe-147">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="035fe-148">esquema</span><span class="sxs-lookup"><span data-stu-id="035fe-148">schema</span></span></td>
<td><span data-ttu-id="035fe-149">Público.</span><span class="sxs-lookup"><span data-stu-id="035fe-149">Public.</span></span> <span data-ttu-id="035fe-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="035fe-150">Optional.</span></span> <span data-ttu-id="035fe-151">Esquema en el que se define la propiedad.</span><span class="sxs-lookup"><span data-stu-id="035fe-151">The schema where the property is defined.</span></span></td>
<td> </td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="035fe-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="035fe-152">Remarks</span></span>

<span data-ttu-id="035fe-153">Los conectores de búsqueda de OpenSearch pueden usar la propiedad OpenSearchHTMLRolloverTemplate.</span><span class="sxs-lookup"><span data-stu-id="035fe-153">OpenSearch search connectors can use the OpenSearchHTMLRolloverTemplate property.</span></span> <span data-ttu-id="035fe-154">Esta propiedad identifica una plantilla a la que se da formato siguiendo la Convención de plantilla de OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="035fe-154">This property identifies a template that is formatted following the OpenSearch template convention.</span></span> <span data-ttu-id="035fe-155">La plantilla OpenSearchHTMLRolloverTemplate se usa cuando el usuario hace clic en el botón "Buscar en el sitio web" de la barra de comandos.</span><span class="sxs-lookup"><span data-stu-id="035fe-155">The OpenSearchHTMLRolloverTemplate template is used when the user clicks on the "Search on website" button in the command bar.</span></span>

## <a name="example"></a><span data-ttu-id="035fe-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="035fe-156">Example</span></span>

<span data-ttu-id="035fe-157">En el ejemplo siguiente se muestra un <propertyStore> elemento con dos <property> elementos.</span><span class="sxs-lookup"><span data-stu-id="035fe-157">The following example shows a <propertyStore> element with two <property> elements.</span></span>


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



