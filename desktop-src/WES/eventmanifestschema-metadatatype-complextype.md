---
title: Tipo complejo MetadataType
description: Define los tipos de metadatos que puede definir en la sección de metadatos del manifiesto.
ms.assetid: 602bafe7-940e-4313-9da5-54c6aa7f60a2
keywords:
- Tipo complejo MetadataType EventLog
topic_type:
- apiref
api_name:
- MetadataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69b140a2b65d47d563fd88f49d6818efc13613f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073307"
---
# <a name="metadatatype-complex-type"></a>Tipo complejo MetadataType

Define los tipos de metadatos que puede definir en la sección de metadatos del manifiesto.

``` syntax
<xs:complexType name="MetadataType">
    <xs:sequence>
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="KeywordListType"
            minOccurs="0"
         />
        <xs:element name="types"
            type="TypeListType"
            minOccurs="0"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
            minOccurs="0"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                       | Tipo                                                                       | Descripción                                                                                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**channels**](eventmanifestschema-channels-metadatatype-element.md)         | [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md) | Define una lista de canales en los que los proveedores pueden registrar eventos. A continuación, un proveedor puede importar uno o varios de los canales en su manifiesto.<br/>               |
| [**Palabras clave**](eventmanifestschema-keywords-metadatatype-element.md)         | [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md) | Define una lista de palabras clave que determinan la categoría de eventos que escribe el proveedor.<br/>                                                            |
| [**Niveles**](eventmanifestschema-levels-metadatatype-element.md)             | [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)     | Define una lista de niveles que especifican la gravedad de un evento.<br/>                                                                                       |
| **message**                                                                   |                                                                            | Define una cadena de mensaje.<br/>                                                                                                                             |
| **messageTable**                                                              |                                                                            | Define una lista de cadenas de mensaje.<br/>                                                                                                                    |
| [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) | [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)   | Define una lista de consultas con nombre que usan expresiones regulares para realizar acciones de búsqueda y reemplazo en la cadena de mensaje de un evento.<br/>                        |
| [**Opcodes**](eventmanifestschema-opcodes-metadatatype-element.md)           | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)   | Define una lista de códigos de operación que puede usar para agrupar eventos dentro de una tarea.<br/>                                                                             |
| **tasks**                                                                     | [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)       | Define una lista de tareas que un proveedor puede usar para agrupar eventos. Normalmente, se usan tareas para agrupar eventos para una característica o componente del proveedor.<br/> |
| [**Tipos**](eventmanifestschema-types-metadatatype-element.md)               | [**TypeListType**](eventmanifestschema-typelisttype-complextype.md)       | Define una lista de tipos XML.<br/>                                                                                                                          |



## <a name="attributes"></a>Atributos



| Nombre    | Tipo                                                              | Descripción                                                                                        |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Referencia a la cadena localizada en la tabla de cadenas.<br/>                                |
| mId     | xs:string                                                         | No se utiliza.<br/>                                                                               |
| name    | anyURI                                                            | Uri del metarchivo. <br/>                                                              |
| símbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Nombre simbólico que desea que el compilador de mensajes cree para esta cadena de mensaje.<br/> |
| value   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Número que se va a usar como identificador de mensaje para este mensaje.<br/>                           |



## <a name="remarks"></a>Observaciones

Aunque puede crear un manifiesto que contenga una sección de metadatos, el servicio no lo usará; los únicos metadatos que el servicio reconoce son los metadatos que se encuentran en el Winmeta.xml archivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





