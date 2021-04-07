---
title: Tipo complejo de BitMapValueType
description: Define la asignación entre un valor de bit y un valor de cadena. | Tipo complejo de BitMapValueType
ms.assetid: 2ef9ed89-83cf-4c47-9c6c-64459b6d7198
keywords:
- BitMapValueType tipo complejo EventLog
topic_type:
- apiref
api_name:
- BitMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2da7e0576579b0f0c509de7a8318e46e5dd955d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003612"
---
# <a name="bitmapvaluetype-complex-type"></a>Tipo complejo de BitMapValueType

Define la asignación entre un valor de bit y un valor de cadena.

``` syntax
<xs:complexType name="BitMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="HexInt32Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nombre    | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Valor de la cadena localizada a la que se asigna el valor de bit. La cadena de mensaje hace referencia a una cadena localizada en la sección [**stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto. <br/>                                                                                  |
| símbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Símbolo que se va a usar para hacer referencia a la asignación en la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para la asignación en el archivo de encabezado que genera el compilador. Si no especifica un símbolo, el compilador genera uno automáticamente.<br/> |
| value   | [**HexInt32Type**](eventmanifestschema-hex32type-simpletype.md)  | Valor de bit que se va a asignar al valor de cadena. Debe especificar un número hexadecimal con un solo bit establecido.<br/>                                                                                                                                                                                          |



## <a name="remarks"></a>Observaciones

Asigna un valor hexadecimal (el número debe ir precedido de 0x) con un único bit establecido en un nombre.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





