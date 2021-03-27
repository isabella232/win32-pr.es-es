---
description: El <property> elemento especifica una propiedad utilizada por la biblioteca. Estas propiedades son específicas de la biblioteca, por lo que no hay ningún conjunto predefinido de nombres de propiedad para usar. Este elemento es opcional y no tiene elementos secundarios.
ms.assetid: 8BF6EC7A-A87E-45fe-A8F0-4B49594E9E7B
title: Property (elemento, esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b269e8914cf1f5da92d96e1922f7347a161daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997249"
---
# <a name="property-element-library-schema"></a><span data-ttu-id="9b684-105">Property (elemento, esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9b684-105">property Element (Library Schema)</span></span>

<span data-ttu-id="9b684-106">El <property> elemento especifica una propiedad utilizada por la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9b684-106">The <property> element specifies a property used by the library.</span></span> <span data-ttu-id="9b684-107">Estas propiedades son específicas de la biblioteca, por lo que no hay ningún conjunto predefinido de nombres de propiedad para usar.</span><span class="sxs-lookup"><span data-stu-id="9b684-107">These properties are specific to the library, so there is no predefined set of property names to use.</span></span> <span data-ttu-id="9b684-108">Este elemento es opcional y no tiene elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="9b684-108">This element is optional and has no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b684-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b684-109">Syntax</span></span>

``` syntax
<!-- property -->
<xs:element name="property" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension base="xs:anyType">
                <xs:attribute name="name" type="canonical-name" use="required"/>
                    <xs:simpleType name="canonical-name">
                        <xs:restriction base="xs:string">
                            <xs:maxLength value="63"/>
                            <xs:pattern value="[0-9A-Za-z.]*"/>
                        </xs:restriction>
                    </xs:simpleType>
                <xs:attribute name="type"/>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="9b684-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9b684-110">Element Information</span></span>



| <span data-ttu-id="9b684-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="9b684-111">Parent Element</span></span>                                                             | <span data-ttu-id="9b684-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9b684-112">Child Elements</span></span> |
|----------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="9b684-113">Elemento propertyStore (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9b684-113">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md) | <span data-ttu-id="9b684-114">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9b684-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="9b684-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="9b684-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b684-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="9b684-116">Attribute</span></span></th>
<th><span data-ttu-id="9b684-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b684-117">Description</span></span></th>
<th><span data-ttu-id="9b684-118">Valores</span><span class="sxs-lookup"><span data-stu-id="9b684-118">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b684-119">name</span><span class="sxs-lookup"><span data-stu-id="9b684-119">name</span></span></td>
<td><span data-ttu-id="9b684-120">Público.</span><span class="sxs-lookup"><span data-stu-id="9b684-120">Public.</span></span> <span data-ttu-id="9b684-121">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b684-121">Required.</span></span> <span data-ttu-id="9b684-122">El nombre para mostrar de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="9b684-122">The display name of the property.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="9b684-123">tipo</span><span class="sxs-lookup"><span data-stu-id="9b684-123">type</span></span></td>
<td><span data-ttu-id="9b684-124">Público.</span><span class="sxs-lookup"><span data-stu-id="9b684-124">Public.</span></span> <span data-ttu-id="9b684-125">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b684-125">Required.</span></span> <span data-ttu-id="9b684-126">El tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9b684-126">The type of property.</span></span></td>
<td><ul>
<li><span data-ttu-id="9b684-127">Any: valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9b684-127">Any: Default.</span></span> <span data-ttu-id="9b684-128">El subsistema de propiedades no convertirá el valor.</span><span class="sxs-lookup"><span data-stu-id="9b684-128">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="9b684-129">GetPropertyType devolverá VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="9b684-129">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="9b684-130">NULL: no hay ningún valor para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9b684-130">Null: There is no value for this property.</span></span> <span data-ttu-id="9b684-131">GetPropertyType devolverá VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="9b684-131">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="9b684-132">Cadena: el valor debe ser un VT_LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="9b684-132">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="9b684-133">Booleano: el valor debe ser un VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="9b684-133">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="9b684-134">Byte: el valor debe ser un VT_UI1.</span><span class="sxs-lookup"><span data-stu-id="9b684-134">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="9b684-135">Buffer: el valor debe ser un VT_UI1 | VT_VECTOR búfer de bytes.</span><span class="sxs-lookup"><span data-stu-id="9b684-135">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="9b684-136">Int16: el valor debe ser un VT_I2.</span><span class="sxs-lookup"><span data-stu-id="9b684-136">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="9b684-137">UInt16: el valor debe ser un VT_UI2.</span><span class="sxs-lookup"><span data-stu-id="9b684-137">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="9b684-138">Int32: el valor debe ser un VT_I4.</span><span class="sxs-lookup"><span data-stu-id="9b684-138">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="9b684-139">UInt32: el valor debe ser un VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="9b684-139">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="9b684-140">Int64: el valor debe ser un VT_I8.</span><span class="sxs-lookup"><span data-stu-id="9b684-140">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="9b684-141">UInt64: el valor debe ser un VT_UI8.</span><span class="sxs-lookup"><span data-stu-id="9b684-141">UInt64: The value must be a VT_UI8.</span></span></li>
<li><span data-ttu-id="9b684-142">Double: el valor debe ser un VT_R8.</span><span class="sxs-lookup"><span data-stu-id="9b684-142">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="9b684-143">DateTime: el valor debe ser un VT_FILETIME.</span><span class="sxs-lookup"><span data-stu-id="9b684-143">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="9b684-144">GUID: el valor debe ser un VT_CLSID.</span><span class="sxs-lookup"><span data-stu-id="9b684-144">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="9b684-145">BLOB: el valor debe ser un VT_BLOB.</span><span class="sxs-lookup"><span data-stu-id="9b684-145">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="9b684-146">Objeto: el valor debe ser un VT_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="9b684-146">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="9b684-147">Stream: el valor debe ser un VT_STREAM.</span><span class="sxs-lookup"><span data-stu-id="9b684-147">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="9b684-148">Clipboard: el valor debe ser un VT_CF.</span><span class="sxs-lookup"><span data-stu-id="9b684-148">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="9b684-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b684-149">Remarks</span></span>

<span data-ttu-id="9b684-150">Los requisitos para el elemento <nombre canónico> coinciden con los requisitos de Windows Search y del sistema de propiedades de Windows.</span><span class="sxs-lookup"><span data-stu-id="9b684-150">The requirements for the <canonical-name> element match the requirements for Windows Search and the Windows property system.</span></span> <span data-ttu-id="9b684-151">La cadena debe ser de tipo canónico-Type.</span><span class="sxs-lookup"><span data-stu-id="9b684-151">The string must be of type canonical-type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b684-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b684-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b684-153">Esquema de descripción de biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b684-153">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="9b684-154">Esquemas de propiedades</span><span class="sxs-lookup"><span data-stu-id="9b684-154">Property Schemas</span></span>](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="9b684-155">Esquema de Descripción del conector de búsqueda</span><span class="sxs-lookup"><span data-stu-id="9b684-155">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
