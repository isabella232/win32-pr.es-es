---
title: Tipo complejo KeywordType
description: Define una palabra clave que identifica una categoría de eventos. | Tipo complejo KeywordType
ms.assetid: 6bd41d4a-1d55-4cce-a1f8-136f749fde2a
keywords:
- Tipo complejo KeywordType EventLog
topic_type:
- apiref
api_name:
- KeywordType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41a9ad4b1fde0a741a022eb6cfd20823643eeef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474585"
---
# <a name="keywordtype-complex-type"></a>Tipo complejo KeywordType

Define una palabra clave que identifica una categoría de eventos. Una palabra clave es una etiqueta que se asocia a un evento para agrupar eventos en función de su uso.

``` syntax
<xs:complexType name="KeywordType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="mask"
                type="HexInt64Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
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



| Nombre    | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                            |
|---------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mask    | [**HexInt64Type**](eventmanifestschema-hex64type-simpletype.md)  | Máscara de bits que solo debe tener un único conjunto de bits. El bit representa una categoría de eventos (por ejemplo, eventos de lectura o de escritura). Puede especificar valores de bits en el intervalo de 0x0000000000000001 a 0x0000800000000000 (bits 0 a 47).<br/>                                                         |
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nombre para mostrar localizado de la palabra clave. La cadena de mensaje hace referencia a una cadena localizada en la [**sección stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto.<br/>                                                                                                       |
| name    | **QName**                                                         | Nombre de la palabra clave. El nombre debe ser único dentro de la lista de palabras clave que define el proveedor.<br/>                                                                                                                                                                                                     |
| símbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Símbolo que se usará para hacer referencia a la palabra clave en la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) usa el símbolo para crear una constante para la palabra clave en el archivo de encabezado que genera el compilador. Si no especifica un símbolo, el compilador genera uno automáticamente.<br/> |



## <a name="remarks"></a>Observaciones

El Winmeta.xml que se incluye en el SDK de Windows contiene una lista de palabras clave. Estas palabras clave están reservadas y no se deben usar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





