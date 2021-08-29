---
title: Tipo complejo TaskType
description: Define un componente o subcomponente de una aplicación. | Tipo complejo TaskType
ms.assetid: d117636d-6363-43b6-ac5a-52234ac7c729
keywords:
- Tipo complejo TaskType EventLog
topic_type:
- apiref
api_name:
- TaskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42a8b3dfd91b879eec37040c314d15b8b3c802b2c4b674f7a573314659d5d51b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005815"
---
# <a name="tasktype-complex-type"></a>Tipo complejo TaskType

Define un componente o subcomponente de una aplicación.

``` syntax
<xs:complexType name="TaskType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt16Type"
        use="required"
     />
    <xs:attribute name="eventGUID"
        type="GUIDType"
        use="optional"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                         | Tipo                                                                     | Descripción                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Opcodes**](eventmanifestschema-opcodes-tasktype-element.md) | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) | Define una lista de códigos de operación específicos de la tarea. No puede usar los valores de código de operación definidos en Winmeta.xml para códigos de operación específicos de la tarea.<br/> |



## <a name="attributes"></a>Atributos



| Nombre      | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                      |
|-----------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| eventGUID | [**GUIDType**](eventmanifestschema-guidtype-simpletype.md)       | Identificador único global, en formato registro, que identifica la tarea. Este atributo es necesario si usa el argumento del compilador de mensajes -mof para generar una clase MOF para la compatibilidad de nivel inferior.<br/>                                                                                                   |
| message   | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nombre para mostrar localizado de la tarea. La cadena de mensaje hace referencia a una cadena localizada en la [**sección stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto. <br/>                                                                                                   |
| name      | **QName**                                                         | Nombre de la tarea.<br/>                                                                                                                                                                                                                                                                                 |
| símbolo    | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Símbolo que se usará para hacer referencia a la tarea en la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) usa el símbolo para crear una constante para la tarea en el archivo de encabezado que genera el compilador. Si no especifica un símbolo, el compilador genera uno automáticamente.<br/> |
| value     | [**UInt16Type**](eventmanifestschema-hexint16type-simpletype.md) | Valor numérico que identifica de forma única esta tarea dentro de la lista de tareas que define el proveedor. El valor debe estar en el intervalo entre 1 y 239.<br/>                                                                                                                                             |



## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo especificar una tarea.


```XML
<tasks>
  <task name="printspool:Disconnect" 
         symbol="PRINTSPOOL_TASK_DISCONNECT"
         value="0" 
         message="$(string.disconnect)"/>
 
  <task name="printspool:Connect" 
         symbol="PRINTSPOOL_TASK_CONNECT"
         value="1" 
         message="$(string.connect)">
       <opcodes>
          <opcode name="ReadRegistry" 
                  symbol="MYOPCODE_READ_REGISTRY" value="11"
                  message="$(string.ReadRegistry)"/>
       </opcodes>
   </task>
</tasks>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





