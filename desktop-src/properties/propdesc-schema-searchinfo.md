---
description: Especifica cómo configurar el motor de búsqueda de Windows con respecto a una definición de propiedad determinada.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: searchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee94585aaa66a761e527ac6ada1c33b0d23966d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666852"
---
# <a name="searchinfo"></a><span data-ttu-id="891e6-103">searchInfo</span><span class="sxs-lookup"><span data-stu-id="891e6-103">searchInfo</span></span>

<span data-ttu-id="891e6-104">Especifica cómo configurar el motor de búsqueda de Windows con respecto a una definición de propiedad determinada.</span><span class="sxs-lookup"><span data-stu-id="891e6-104">Specifies how to configure the Windows search engine with respect to a given property definition.</span></span> <span data-ttu-id="891e6-105">Si no se proporciona ningún elemento [searchInfo]() , la propiedad no se incluye en el motor de búsqueda de Windows.</span><span class="sxs-lookup"><span data-stu-id="891e6-105">If no [searchInfo]() element is provided, then the property is not included in the Windows search engine.</span></span> <span data-ttu-id="891e6-106">Este elemento ha cambiado para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="891e6-106">This element has changed for Windows 7.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="891e6-107">Sintaxis para Windows 7</span><span class="sxs-lookup"><span data-stu-id="891e6-107">Syntax for Windows 7</span></span>


```
<!-- searchInfo for Windows 7-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                    <xs:enumeration value="OnDiskAll"/>
                    <xs:enumeration value="OnDiskVector"/>
                    <xs:enumeration value="OnDemand"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="512"/>
        <xs:attribute name="mnemonics" type="xs:string"/>                            
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-windows-vista"></a><span data-ttu-id="891e6-108">Sintaxis de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="891e6-108">Syntax for Windows Vista</span></span>


```
<!-- searchInfo for Windows Vista-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="128"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="891e6-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="891e6-109">Element Information</span></span>



| <span data-ttu-id="891e6-110">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="891e6-110">Parent Element</span></span>                                                   | <span data-ttu-id="891e6-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="891e6-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="891e6-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="891e6-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="891e6-113">None</span><span class="sxs-lookup"><span data-stu-id="891e6-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="891e6-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="891e6-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="891e6-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="891e6-115">Attribute</span></span></th>
<th><span data-ttu-id="891e6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="891e6-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="891e6-117">inInvertedIndex</span><span class="sxs-lookup"><span data-stu-id="891e6-117">inInvertedIndex</span></span></td>
<td><span data-ttu-id="891e6-118">Público.</span><span class="sxs-lookup"><span data-stu-id="891e6-118">Public.</span></span> <span data-ttu-id="891e6-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="891e6-119">Optional.</span></span> <span data-ttu-id="891e6-120">Indica si el valor de la propiedad se debe almacenar en el índice invertido.</span><span class="sxs-lookup"><span data-stu-id="891e6-120">Indicates whether the property value should be stored in the inverted index.</span></span> <span data-ttu-id="891e6-121">Esto permite que los usuarios finales realicen consultas de texto completo sobre los valores de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="891e6-121">This lets end users perform full-text queries over the values of this property.</span></span> <span data-ttu-id="891e6-122">El valor predeterminado es &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="891e6-122">The default is &quot;false&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="891e6-123">isColumn</span><span class="sxs-lookup"><span data-stu-id="891e6-123">isColumn</span></span></td>
<td><span data-ttu-id="891e6-124">Público.</span><span class="sxs-lookup"><span data-stu-id="891e6-124">Public.</span></span> <span data-ttu-id="891e6-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="891e6-125">Optional.</span></span> <span data-ttu-id="891e6-126">Indica si la propiedad también debe almacenarse en la base de datos de Windows Search como una columna, de modo que los fabricantes de software independientes (ISV) puedan crear consultas basadas en predicado (por ejemplo, &quot; Select \* donde &quot; System. title &quot; = ' QQQ ' &quot; ).</span><span class="sxs-lookup"><span data-stu-id="891e6-126">Indicates whether the property should also be stored in the Windows search database as a column, so that independent software vendors (ISVs) can create predicate-based queries (for example, &quot;Select \* Where &quot;System.Title&quot;='qqq'&quot;).</span></span> <span data-ttu-id="891e6-127">Si el creador del esquema desea permitir que los usuarios finales (o los desarrolladores) creen consultas basadas en predicado en las propiedades, debe establecerse en &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="891e6-127">If the schema creator wants to enable end users (or developers) to create predicate based queries on the properties, then this needs to be set to &quot;true&quot;.</span></span> <span data-ttu-id="891e6-128">El valor predeterminado es &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="891e6-128">The default is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="891e6-129">isColumnSparse</span><span class="sxs-lookup"><span data-stu-id="891e6-129">isColumnSparse</span></span></td>
<td><span data-ttu-id="891e6-130">Público.</span><span class="sxs-lookup"><span data-stu-id="891e6-130">Public.</span></span> <span data-ttu-id="891e6-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="891e6-131">Optional.</span></span> <span data-ttu-id="891e6-132">El valor predeterminado es &quot;true&quot;.</span><span class="sxs-lookup"><span data-stu-id="891e6-132">The default is &quot;true&quot;.</span></span> <span data-ttu-id="891e6-133">Si la propiedad tiene varios valores, este atributo siempre es &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="891e6-133">If the property is multi-valued, this attribute is always &quot;true&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="891e6-134">columnIndexType</span><span class="sxs-lookup"><span data-stu-id="891e6-134">columnIndexType</span></span></td>
<td><span data-ttu-id="891e6-135">Público.</span><span class="sxs-lookup"><span data-stu-id="891e6-135">Public.</span></span> <span data-ttu-id="891e6-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="891e6-136">Optional.</span></span> <span data-ttu-id="891e6-137">Para optimizar la ordenación y agrupación, el motor de búsqueda de Windows puede crear índices secundarios para propiedades que tengan isColumn = &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="891e6-137">To optimize sorting and grouping, the Windows search engine can create secondary indexes for properties that have isColumn=&quot;true&quot;.</span></span> <span data-ttu-id="891e6-138">Este atributo solo es útil cuando inInvertedIndex es &quot; true &quot; en Windows Vista o cuando isColumn es &quot; true &quot; en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="891e6-138">This attribute is only useful when inInvertedIndex is &quot;true&quot; in Windows Vista or when isColumn is &quot;true&quot; in Windows 7.</span></span> <span data-ttu-id="891e6-139">Si los usuarios suelen ordenar la propiedad con frecuencia, se debe especificar este atributo.</span><span class="sxs-lookup"><span data-stu-id="891e6-139">If the property tends to be sorted frequently by users, this attribute should be specified.</span></span> <span data-ttu-id="891e6-140">El valor predeterminado en Windows Vista es &quot; NotIndexed &quot; .</span><span class="sxs-lookup"><span data-stu-id="891e6-140">The default value in Windows Vista is &quot;NotIndexed&quot;.</span></span> <span data-ttu-id="891e6-141">El valor predeterminado en Windows 7 es &quot; OnDemand &quot; .</span><span class="sxs-lookup"><span data-stu-id="891e6-141">The default value in Windows 7 is &quot;OnDemand&quot;.</span></span> <span data-ttu-id="891e6-142">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="891e6-142">The following values are valid.</span></span>
<ul>
<li><span data-ttu-id="891e6-143"><strong>NotIndexed</strong>: nunca cree un índice de valor.</span><span class="sxs-lookup"><span data-stu-id="891e6-143"><strong>NotIndexed</strong>: Never build a value index.</span></span></li>
<li><span data-ttu-id="891e6-144"><strong>Disco</strong>: crea un índice de valor de forma predeterminada para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="891e6-144"><strong>OnDisk</strong>: Build a value index by default for this property.</span></span></li>
<li><span data-ttu-id="891e6-145"><strong>OnDiskAll</strong> (solo Windows 7 y versiones posteriores): cree un índice de valor de forma predeterminada para esta propiedad y, si es una propiedad de Vector, también un índice de valor para todos los valores de vector concatenados.</span><span class="sxs-lookup"><span data-stu-id="891e6-145"><strong>OnDiskAll</strong> (Windows 7 and later only): Build a value index by default for this property, and if it is a vector property, also a value index for all concatenated vector values.</span></span></li>
<li><span data-ttu-id="891e6-146"><strong>OnDiskVector</strong> (solo Windows 7 y versiones posteriores): compilar un índice de valor de forma predeterminada para los valores de vector concatenados.</span><span class="sxs-lookup"><span data-stu-id="891e6-146"><strong>OnDiskVector</strong> (Windows 7 and later only): Build a value index by default for the concatenated vector values.</span></span></li>
<li><span data-ttu-id="891e6-147"><strong>OnDemand</strong> (solo Windows 7 y versiones posteriores): solo se generan índices de valor por demanda, es decir, solo se usan por primera vez para una consulta.</span><span class="sxs-lookup"><span data-stu-id="891e6-147"><strong>OnDemand</strong> (Windows 7 and later only): Only build value indices by demand, that is, only first time they are used for a query.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="891e6-148">Tamañomáximo</span><span class="sxs-lookup"><span data-stu-id="891e6-148">maxSize</span></span></td>
<td><span data-ttu-id="891e6-149">Público.</span><span class="sxs-lookup"><span data-stu-id="891e6-149">Public.</span></span> <span data-ttu-id="891e6-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="891e6-150">Optional.</span></span> <span data-ttu-id="891e6-151">Tamaño máximo, en bytes, permitido para una determinada propiedad almacenada en la base de datos de Windows Search.</span><span class="sxs-lookup"><span data-stu-id="891e6-151">The maximum size, in bytes, allowed for a certain property that is stored in the Windows search database.</span></span> <span data-ttu-id="891e6-152">El valor predeterminado es:</span><span class="sxs-lookup"><span data-stu-id="891e6-152">The default is:</span></span>
<ul>
<li><span data-ttu-id="891e6-153"><strong>Windows Vista</strong>: 128 bytes</span><span class="sxs-lookup"><span data-stu-id="891e6-153"><strong>Windows Vista</strong>: 128 bytes</span></span></li>
<li><span data-ttu-id="891e6-154"><strong>Windows 7 y versiones posteriores</strong>: 512 bytes</span><span class="sxs-lookup"><span data-stu-id="891e6-154"><strong>Windows 7 and later</strong>: 512 bytes</span></span></li>
</ul>
<span data-ttu-id="891e6-155">Tenga en cuenta que este tamaño máximo se mide en bytes, no en caracteres.</span><span class="sxs-lookup"><span data-stu-id="891e6-155">Note that this maximum size is measured in bytes, not characters.</span></span> <span data-ttu-id="891e6-156">El número máximo de caracteres depende de su codificación.</span><span class="sxs-lookup"><span data-stu-id="891e6-156">The maximum number of characters depends on their encoding.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="891e6-157">teclas de acceso</span><span class="sxs-lookup"><span data-stu-id="891e6-157">mnemonics</span></span></td>
<td><span data-ttu-id="891e6-158"><strong>Windows 7 y versiones posteriores.</strong></span><span class="sxs-lookup"><span data-stu-id="891e6-158"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="891e6-159">Público.</span><span class="sxs-lookup"><span data-stu-id="891e6-159">Public.</span></span> <span data-ttu-id="891e6-160">Opcional.</span><span class="sxs-lookup"><span data-stu-id="891e6-160">Optional.</span></span> <span data-ttu-id="891e6-161">Una lista de valores de tecla de tecla que se pueden usar para hacer referencia a la propiedad en consultas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="891e6-161">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="891e6-162">La lista está delimitada por el carácter "|".</span><span class="sxs-lookup"><span data-stu-id="891e6-162">The list is delimited with the '|' character.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
