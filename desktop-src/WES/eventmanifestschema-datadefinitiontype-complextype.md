---
title: Tipo complejo de DataDefinitionType
description: Define un elemento de datos que desea incluir con el evento. | Tipo complejo de DataDefinitionType
ms.assetid: f4234e54-a5a8-48e4-941f-05107dcd3f88
keywords:
- DataDefinitionType tipo complejo EventLog
topic_type:
- apiref
api_name:
- DataDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19584c28a7bdf7ae01b87d1f414b9464b7b4271d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698049"
---
# <a name="datadefinitiontype-complex-type"></a><span data-ttu-id="d049d-105">Tipo complejo de DataDefinitionType</span><span class="sxs-lookup"><span data-stu-id="d049d-105">DataDefinitionType Complex Type</span></span>

<span data-ttu-id="d049d-106">Define un elemento de datos que desea incluir con el evento.</span><span class="sxs-lookup"><span data-stu-id="d049d-106">Defines a data item that you want to include with the event.</span></span>

``` syntax
<xs:complexType name="DataDefinitionType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="inType"
                type="QName"
                use="required"
             />
            <xs:attribute name="outType"
                type="QName"
                use="optional"
             />
            <xs:attribute name="map"
                type="string"
                use="optional"
             />
            <xs:attribute name="length"
                type="LengthType"
                use="optional"
             />
            <xs:attribute name="count"
                type="CountType"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="d049d-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="d049d-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d049d-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="d049d-108">Name</span></span></th>
<th><span data-ttu-id="d049d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d049d-109">Type</span></span></th>
<th><span data-ttu-id="d049d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d049d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d049d-111">count</span><span class="sxs-lookup"><span data-stu-id="d049d-111">count</span></span></td>
<td><span data-ttu-id="d049d-112"><a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a></span><span class="sxs-lookup"><span data-stu-id="d049d-112"><a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a></span></span></td>
<td><span data-ttu-id="d049d-113">El número de elementos de la matriz si el elemento de datos es una matriz.</span><span class="sxs-lookup"><span data-stu-id="d049d-113">The number of elements in the array if the data item is an array.</span></span> <span data-ttu-id="d049d-114">Puede especificar el recuento real o el nombre de otro elemento de datos que contenga el recuento.</span><span class="sxs-lookup"><span data-stu-id="d049d-114">You can specify the actual count or the name of another data item that contains the count.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d049d-115">Intype</span><span class="sxs-lookup"><span data-stu-id="d049d-115">inType</span></span></td>
<td><span data-ttu-id="d049d-116"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="d049d-116"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="d049d-117">El tipo de datos para este elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="d049d-117">The data type for this data item.</span></span> <span data-ttu-id="d049d-118">Para obtener una lista de tipos de datos de entrada predefinidos, vea el tipo complejo <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d049d-118">For a list of predefined input data types, see the <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> complex type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d049d-119">length</span><span class="sxs-lookup"><span data-stu-id="d049d-119">length</span></span></td>
<td><span data-ttu-id="d049d-120"><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a></span><span class="sxs-lookup"><span data-stu-id="d049d-120"><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a></span></span></td>
<td><span data-ttu-id="d049d-121">La longitud de un elemento de datos de longitud variable, como un BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="d049d-121">The length of a variable length data item, such as a binary blob.</span></span> <span data-ttu-id="d049d-122">En el caso de los datos binarios, especifique la longitud en bytes y, en el caso de los datos de cadena, especifique la longitud en caracteres.</span><span class="sxs-lookup"><span data-stu-id="d049d-122">For binary data, specify the length in bytes and for string data, specify the length in characters.</span></span> <span data-ttu-id="d049d-123">Puede especificar la longitud real o el nombre de otro elemento de datos que contenga la longitud.</span><span class="sxs-lookup"><span data-stu-id="d049d-123">You can specify the actual length or the name of another data item that contains the length.</span></span><br/> <span data-ttu-id="d049d-124">Si usa el atributo length para especificar una cadena de longitud fija, debe rellenar la cadena con su longitud fija, lo que permite el carácter de terminador nulo al final (por ejemplo, si la longitud es 5, la cadena &quot; ABC &quot; se debe rellenar como &quot; ABC) &quot; .</span><span class="sxs-lookup"><span data-stu-id="d049d-124">If you use the length attribute to specify a fixed length string, you must pad the string to its fixed length allowing for the null-terminator character at the end (for example, if the length is 5, the string &quot;abc&quot; must be padded as &quot;abc &quot;.</span></span> <span data-ttu-id="d049d-125">La longitud de la cadena debe incluir el carácter de terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="d049d-125">The string length must include the null-terminator character.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d049d-126">mapa</span><span class="sxs-lookup"><span data-stu-id="d049d-126">map</span></span></td>
<td><span data-ttu-id="d049d-127">string</span><span class="sxs-lookup"><span data-stu-id="d049d-127">string</span></span></td>
<td><span data-ttu-id="d049d-128">Nombre de la asignación de nombre y valor que se va a usar para asignar valores enteros a cadenas.</span><span class="sxs-lookup"><span data-stu-id="d049d-128">The name of the name/value map to use to map integer values to strings.</span></span> <span data-ttu-id="d049d-129">El tipo de datos del elemento de datos debe ser de uno de los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="d049d-129">The data type of the data item must be of one of the following types:</span></span><br/>
<ul>
<li><span data-ttu-id="d049d-130">win:UInt8</span><span class="sxs-lookup"><span data-stu-id="d049d-130">win:UInt8</span></span></li>
<li><span data-ttu-id="d049d-131">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="d049d-131">win:UInt16</span></span></li>
<li><span data-ttu-id="d049d-132">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="d049d-132">win:UInt32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d049d-133">name</span><span class="sxs-lookup"><span data-stu-id="d049d-133">name</span></span></td>
<td><span data-ttu-id="d049d-134">string</span><span class="sxs-lookup"><span data-stu-id="d049d-134">string</span></span></td>
<td><span data-ttu-id="d049d-135">Nombre del elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="d049d-135">The name of the data item.</span></span> <span data-ttu-id="d049d-136">Puede usar el nombre para hacer referencia a este elemento de datos en el fragmento XML si especifica una sección <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="d049d-136">You can use the name to reference this data item in your XML fragment if you specify a <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> section in your template.</span></span> <span data-ttu-id="d049d-137">También puede hacer referencia a este nombre en un atributo Length o Count de otro elemento de datos si este elemento de datos contiene su valor de longitud o recuento.</span><span class="sxs-lookup"><span data-stu-id="d049d-137">You can also reference this name in a length or count attribute of another data item if this data item contains its length or count value.</span></span><br/> <span data-ttu-id="d049d-138"><strong>Windows Vista:</strong> Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="d049d-138"><strong>Windows Vista:</strong> This attribute is optional.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d049d-139">outtype</span><span class="sxs-lookup"><span data-stu-id="d049d-139">outType</span></span></td>
<td><span data-ttu-id="d049d-140"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="d049d-140"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="d049d-141">Tipo de datos que se va a utilizar al representar este elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="d049d-141">The data type to use when rendering this data item.</span></span> <span data-ttu-id="d049d-142">Para obtener una lista de tipos de datos de salida predefinidos, vea el tipo complejo <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d049d-142">For a list of predefined output data types, see the <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> complex type.</span></span><br/> <span data-ttu-id="d049d-143"><strong>Windows Vista:</strong> Se omite el tipo de salida y el servicio determina el tipo basado en el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="d049d-143"><strong>Windows Vista:</strong> The output type is ignored, and the service determines the type based on the input type.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="d049d-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d049d-144">Remarks</span></span>

<span data-ttu-id="d049d-145">En el caso de los tipos de entrada de longitud variable, como los blobs binarios, debe utilizar el atributo length para especificar explícitamente el tamaño de los datos.</span><span class="sxs-lookup"><span data-stu-id="d049d-145">For variable length input types, such as binary blobs, you must use the length attribute to explicitly specify the size of the data.</span></span> <span data-ttu-id="d049d-146">En el caso de las cadenas, especifique el atributo de longitud solo si las cadenas tienen una longitud fija.</span><span class="sxs-lookup"><span data-stu-id="d049d-146">For strings, specify the length attribute only if the strings are of a fixed length.</span></span>

## <a name="examples"></a><span data-ttu-id="d049d-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d049d-147">Examples</span></span>

<span data-ttu-id="d049d-148">A continuación se muestran algunos ejemplos de definiciones de elementos de datos.</span><span class="sxs-lookup"><span data-stu-id="d049d-148">The following are a few examples of the data item definitions.</span></span>


```XML
<!-- The data item is an 8-bit integer -->
<data name="binaryChar" inType="win:UInt8">
 
<!-- The data item is a single ANSI character -->
<data name="ansiChar" inType="win:UInt8" outtype="xs:string">
 
<!-- The data item is a single Unicode character -->
<data name="unicodeChar" inType="win:UInt16" outtype="xs:string">
 
<!-- The data item is an IP address that is rendered as a dot separated list of interger values -->
<data name="ipAddress" inType="win:UInt32" outtype="win:IPv4">
 
<!-- The data item is a Boolean value -->
<data name="success" inType="win:boolean">
 
<!-- The data item is a null-terminated ANSI string -->
<data name="string" inType="win:AnsiString"> 

<!-- The data item is a fixed length ANSI string -->
<data name="string" inType="win:AnsiString" length="42"> 
 
<!-- The data item is a fixed length array of null-terminated ANSI strings -->
<data name="strings" inType="win:AnsiString" count="20">
 
<!-- The data item is a fixed length array of fixed length ANSI strings -->
<data name="strings" inType="win:AnsiString" length="42" count="20">
 
<!-- The data item is a variable length array of same sized ANSI strings -->
<data name="stringLength" inType="win:UInt16">
<data name="arrayCount" inType="win:Uint16">
<data name="strings" inType="win:AnsiString" length="stringLength" count="arrayCount"> 
 
<!-- For binary data, you must specify the size.
<!-- The data item is a fixed length array of fixed length binary blobs -->
<data name="blobs" inType="win:Binary" length="42" count="20">

<!-- The data item is a fixed length binary blob -->
<data name="blob" inType="win:Binary" length="42">

<!-- The following are illegal binary data definitions -->
<!-- This definition is illegal because no length is specified -->
<data name="blob" inType="win:Binary"> 
 
<!-- This definition is illegal because you cannot determine the length of each binary blob -->
<data name="blob" inType="win:Binary" count="20"> 
 
<!-- The data item is a variable length array of structures. Each structure -->
<!-- contains an array of same sized ANSI strings --> 
<data name="arrayStructCount" inType="win:UInt16">
<struct name="countedStrings" count="arrayStructCount">
      <data name="stringLength" inType="win:UInt16">
      <data name="string" inType="win:AnsiString" length="stringLength">
</struct>
 
<!-- The data item is a time stamp that is rendered in 100ns units -->
<data name="timestamp" inType="win:UInt32" outType="win:ETWTIME">

<!-- The data item is a fixed length array of integers --> 
<data name="integers" inType="win:UInt32" count="20">

<!-- The data item is a variable length array of integers -->
<data name="arrayCount" inType="win:UInt16"> 
<data name="integers" inType="win:UInt32" count="arrayCount"> 

<!-- The following is illegal because you cannot assign a length value to a data type of a known size -->
<data name="integer" inType="win:UInt32" length="42">
```



## <a name="requirements"></a><span data-ttu-id="d049d-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d049d-149">Requirements</span></span>



| <span data-ttu-id="d049d-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="d049d-150">Requirement</span></span> | <span data-ttu-id="d049d-151">Value</span><span class="sxs-lookup"><span data-stu-id="d049d-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d049d-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d049d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d049d-153">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d049d-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d049d-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d049d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d049d-155">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d049d-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





