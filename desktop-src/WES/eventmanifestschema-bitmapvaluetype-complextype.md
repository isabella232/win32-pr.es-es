---
title: Tipo complejo BitMapValueType
description: Define la asignación entre un valor de bit y un valor de cadena. | Tipo complejo BitMapValueType
ms.assetid: 2ef9ed89-83cf-4c47-9c6c-64459b6d7198
keywords:
- BitMapValueType, tipo complejo EventLog
topic_type:
- apiref
api_name:
- BitMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6d5f1b254ad4a833c1523f5a139224fc1fed508d4530a056ffdb0f111db5769e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032355"
---
# <a name="bitmapvaluetype-complex-type"></a>Tipo complejo BitMapValueType

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
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Valor de cadena localizado al que se asigna el valor de bits. La cadena de mensaje hace referencia a una cadena localizada en la [**sección stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto. <br/>                                                                                  |
| símbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Símbolo que se usará para hacer referencia al mapa en la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) usa el símbolo para crear una constante para el mapa en el archivo de encabezado que genera el compilador. Si no especifica un símbolo, el compilador genera uno automáticamente.<br/> |
| value   | [**HexInt32Type**](eventmanifestschema-hex32type-simpletype.md)  | Valor de bit que se asignará al valor de cadena. Debe especificar un número hexadecimal que tenga un único conjunto de bits.<br/>                                                                                                                                                                                          |



## <a name="remarks"></a>Comentarios

Mapas un valor hexadecimal (el número debe ir precedido de 0x) con un único bit establecido en un nombre.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





