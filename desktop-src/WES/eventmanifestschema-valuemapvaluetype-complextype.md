---
title: Tipo complejo ValueMapValueType
description: Define la asignación entre un valor entero y un valor de cadena. | Tipo complejo ValueMapValueType
ms.assetid: 8fd3b3ed-5b62-4e2e-b6f9-8e1bf6d83a35
keywords:
- Tipo complejo EventLog de ValueMapValueType
topic_type:
- apiref
api_name:
- ValueMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 719c8bba805ffb58b8c15661ba2618c29b9dedc1f65f36dba50791cde985a397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032055"
---
# <a name="valuemapvaluetype-complex-type"></a>Tipo complejo ValueMapValueType

Define la asignación entre un valor entero y un valor de cadena.

``` syntax
<xs:complexType name="ValueMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
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
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Valor de cadena localizado al que se asigna el valor entero. La cadena de mensaje hace referencia a una cadena localizada en la [**sección stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto. <br/>                                                                              |
| símbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Símbolo que se usará para hacer referencia al mapa en la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) usa el símbolo para crear una constante para el mapa en el archivo de encabezado que genera el compilador. Si no especifica un símbolo, el compilador genera uno automáticamente.<br/> |
| value   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Valor entero que se asignará al valor de cadena.<br/>                                                                                                                                                                                                                                                       |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





