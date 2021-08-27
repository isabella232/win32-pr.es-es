---
title: Tipo complejo DataDefinitionType
description: Define un elemento de datos que desea incluir con el evento . | Tipo complejo DataDefinitionType
ms.assetid: f4234e54-a5a8-48e4-941f-05107dcd3f88
keywords:
- DataDefinitionType, tipo complejo EventLog
topic_type:
- apiref
api_name:
- DataDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a637166d261c4148a81baee3597d4090542b8612
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470931"
---
# <a name="datadefinitiontype-complex-type"></a>Tipo complejo DataDefinitionType

Define un elemento de datos que desea incluir con el evento .

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

## <a name="attributes"></a>Atributos




| Nombre | Tipo | Descripción | 
|------|------|-------------|
| count | <a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a> | Número de elementos de la matriz si el elemento de datos es una matriz. Puede especificar el recuento real o el nombre de otro elemento de datos que contiene el recuento. <br /> | 
| Intype | <strong>QName</strong> | Tipo de datos para este elemento de datos. Para obtener una lista de tipos de datos de entrada predefinidos, vea el <a href="eventmanifestschema-inputtype-complextype.md"><strong>tipo complejo InputType.</strong></a><br /> | 
| length | <a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a> | Longitud de un elemento de datos de longitud variable, como un blob binario. Para los datos binarios, especifique la longitud en bytes y, para los datos de cadena, especifique la longitud en caracteres. Puede especificar la longitud real o el nombre de otro elemento de datos que contiene la longitud.<br /> Si usa el atributo length para especificar una cadena de longitud fija, debe agregar la cadena a su longitud fija, lo que permite el carácter de terminador null al final (por ejemplo, si la longitud es 5, la cadena "abc" debe agregarse como "abc". La longitud de la cadena debe incluir el carácter de terminador null.<br /> | 
| mapa | string | Nombre de la asignación de nombre/valor que se usará para asignar valores enteros a cadenas. El tipo de datos del elemento de datos debe ser de uno de los siguientes tipos:<br /><ul><li>win:UInt8</li><li>win:UInt16</li><li>win:UInt32</li></ul> | 
| name | string | Nombre del elemento de datos. Puede usar el nombre para hacer referencia a este elemento de datos en el fragmento XML si especifica una <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>sección UserData</strong></a> en la plantilla. También puede hacer referencia a este nombre en un atributo length o count de otro elemento de datos si este elemento de datos contiene su valor de longitud o recuento.<br /><strong>Windows Vista:</strong> Este atributo es opcional.<br /> | 
| outType | <strong>QName</strong> | Tipo de datos que se va a usar al representar este elemento de datos. Para obtener una lista de los tipos de datos de salida predefinidos, vea el <a href="eventmanifestschema-outputtype-complextype.md"><strong>tipo complejo OutputType.</strong></a><br /><strong>Windows Vista:</strong> El tipo de salida se omite y el servicio determina el tipo en función del tipo de entrada.<br /> | 




## <a name="remarks"></a>Comentarios

Para los tipos de entrada de longitud variable, como los blobs binarios, debe usar el atributo length para especificar explícitamente el tamaño de los datos. Para las cadenas, especifique el atributo de longitud solo si las cadenas tienen una longitud fija.

## <a name="examples"></a>Ejemplos

A continuación se muestran algunos ejemplos de las definiciones de elementos de datos.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





