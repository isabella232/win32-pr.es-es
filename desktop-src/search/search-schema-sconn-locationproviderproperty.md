---
description: El <property> elemento opcional especifica las propiedades que utiliza el proveedor de ubicación.
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: Elemento Property de locationProvider (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71081b8b04ec999daa90958a29708b8efc64bee0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105707717"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a><span data-ttu-id="7cf29-103">Elemento Property de locationProvider (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="7cf29-103">property Element of locationProvider (Search Connector Schema)</span></span>

<span data-ttu-id="7cf29-104">El <property> elemento opcional especifica las propiedades que utiliza el proveedor de ubicación.</span><span class="sxs-lookup"><span data-stu-id="7cf29-104">The optional <property> element specifies the properties used by the location provider.</span></span> <span data-ttu-id="7cf29-105">Estas propiedades son específicas de este proveedor de ubicación, por lo que no hay ningún conjunto de nombres predefinido que usar.</span><span class="sxs-lookup"><span data-stu-id="7cf29-105">These properties are specific to this location provider, so there is no predefined set of names to use.</span></span> <span data-ttu-id="7cf29-106">El <property> elemento tiene dos atributos, tal y como se describe en este tema.</span><span class="sxs-lookup"><span data-stu-id="7cf29-106">The <property> element has two attributes, as described in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf29-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7cf29-107">Syntax</span></span>


```
<!-- property element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
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



## <a name="property-element-information"></a><span data-ttu-id="7cf29-108"><property> Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7cf29-108"><property> Element Information</span></span>



| <span data-ttu-id="7cf29-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="7cf29-109">Parent Element</span></span>                                                                                 | <span data-ttu-id="7cf29-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7cf29-110">Child Elements</span></span>                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [<span data-ttu-id="7cf29-111">Elemento locationProvider (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="7cf29-111">locationProvider Element (Search Connector Schema)</span></span>](search-schema-sconn-locationprovider.md) | <span data-ttu-id="7cf29-112">, que se describe en este tema.</span><span class="sxs-lookup"><span data-stu-id="7cf29-112">property, described in this topic.</span></span> |



 


## <a name="property-attributes"></a><span data-ttu-id="7cf29-113"><property> Sus</span><span class="sxs-lookup"><span data-stu-id="7cf29-113"><property> Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cf29-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="7cf29-114">Attribute</span></span></th>
<th><span data-ttu-id="7cf29-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cf29-115">Description</span></span></th>
<th><span data-ttu-id="7cf29-116">Valores</span><span class="sxs-lookup"><span data-stu-id="7cf29-116">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cf29-117">name</span><span class="sxs-lookup"><span data-stu-id="7cf29-117">name</span></span></td>
<td><span data-ttu-id="7cf29-118">Necesario.</span><span class="sxs-lookup"><span data-stu-id="7cf29-118">Required.</span></span> <span data-ttu-id="7cf29-119">El nombre para mostrar de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="7cf29-119">The display name of the property.</span></span></td>
<td> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cf29-120">type</span><span class="sxs-lookup"><span data-stu-id="7cf29-120">type</span></span></td>
<td><span data-ttu-id="7cf29-121">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7cf29-121">Required.</span></span> <span data-ttu-id="7cf29-122">El tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="7cf29-122">The type of property.</span></span></td>
<td><span data-ttu-id="7cf29-123">Any: valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7cf29-123">Any: Default.</span></span> <span data-ttu-id="7cf29-124">El subsistema de propiedades no convertirá el valor.</span><span class="sxs-lookup"><span data-stu-id="7cf29-124">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="7cf29-125">GetPropertyType devolverá VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="7cf29-125">VT_NULL will be returned by GetPropertyType.</span></span>
<ul>
<li><span data-ttu-id="7cf29-126">NULL: no hay ningún valor para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="7cf29-126">Null: There is no value for this property.</span></span> <span data-ttu-id="7cf29-127">GetPropertyType devolverá VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="7cf29-127">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="7cf29-128">Cadena: el valor debe ser un VT_LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="7cf29-128">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="7cf29-129">Booleano: el valor debe ser un VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="7cf29-129">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="7cf29-130">Byte: el valor debe ser un VT_UI1.</span><span class="sxs-lookup"><span data-stu-id="7cf29-130">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="7cf29-131">Buffer: el valor debe ser un VT_UI1 | VT_VECTOR búfer de bytes.</span><span class="sxs-lookup"><span data-stu-id="7cf29-131">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="7cf29-132">Int16: el valor debe ser un VT_I2.</span><span class="sxs-lookup"><span data-stu-id="7cf29-132">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="7cf29-133">UInt16: el valor debe ser un VT_UI2.</span><span class="sxs-lookup"><span data-stu-id="7cf29-133">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="7cf29-134">Int32: el valor debe ser un VT_I4.</span><span class="sxs-lookup"><span data-stu-id="7cf29-134">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="7cf29-135">UInt32: el valor debe ser un VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="7cf29-135">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="7cf29-136">Int64: el valor debe ser un VT_I8.</span><span class="sxs-lookup"><span data-stu-id="7cf29-136">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="7cf29-137">UInt64: el valor debe ser un VT_UI8</span><span class="sxs-lookup"><span data-stu-id="7cf29-137">UInt64: The value must be a VT_UI8</span></span></li>
<li><span data-ttu-id="7cf29-138">Double: el valor debe ser un VT_R8.</span><span class="sxs-lookup"><span data-stu-id="7cf29-138">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="7cf29-139">DateTime: el valor debe ser un VT_FILETIME.</span><span class="sxs-lookup"><span data-stu-id="7cf29-139">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="7cf29-140">GUID: el valor debe ser un VT_CLSID.</span><span class="sxs-lookup"><span data-stu-id="7cf29-140">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="7cf29-141">BLOB: el valor debe ser un VT_BLOB.</span><span class="sxs-lookup"><span data-stu-id="7cf29-141">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="7cf29-142">Objeto: el valor debe ser un VT_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="7cf29-142">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="7cf29-143">Stream: el valor debe ser un VT_STREAM.</span><span class="sxs-lookup"><span data-stu-id="7cf29-143">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="7cf29-144">Clipboard: el valor debe ser un VT_CF.</span><span class="sxs-lookup"><span data-stu-id="7cf29-144">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="7cf29-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7cf29-145">Remarks</span></span>

<span data-ttu-id="7cf29-146">Para el proveedor de OpenSearch, se usan las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="7cf29-146">For the OpenSearch provider, the following properties are used:</span></span>

-   <span data-ttu-id="7cf29-147">OpenSearchShortName: nombre corto del servicio de búsqueda</span><span class="sxs-lookup"><span data-stu-id="7cf29-147">OpenSearchShortName: Short name of the search service</span></span>
-   <span data-ttu-id="7cf29-148">OpenSearchQueryTemplate: plantilla, con el formato que sigue la Convención de plantilla de OpenSearch, para el servicio de consulta</span><span class="sxs-lookup"><span data-stu-id="7cf29-148">OpenSearchQueryTemplate: Template, formatted following the OpenSearch template convention, for the query service</span></span>
-   <span data-ttu-id="7cf29-149">MaximumResultCount: (número) número máximo de resultados devueltos por el servicio de búsqueda</span><span class="sxs-lookup"><span data-stu-id="7cf29-149">MaximumResultCount: (number) Maximum number of results returned by the search service</span></span>
-   <span data-ttu-id="7cf29-150">LinkIsFilePath: (booleano) si es true, el proveedor intenta interpretar los elementos devueltos como archivos, mediante sus extensiones para crear el ShellItem adecuado en la vista.</span><span class="sxs-lookup"><span data-stu-id="7cf29-150">LinkIsFilePath: (Boolean) If true, the provider tries to interpret returned items as files, using their extensions to create the proper ShellItem in the view.</span></span> <span data-ttu-id="7cf29-151">Si es false, los elementos se tratan como métodos abreviados de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="7cf29-151">If false, items are treated as URL shortcuts.</span></span>

 

 



