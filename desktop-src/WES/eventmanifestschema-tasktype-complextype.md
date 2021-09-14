---
title: Tipo complejo TaskType
description: Define un componente o subcomponente de una aplicación. | Tipo complejo TaskType
ms.assetid: d117636d-6363-43b6-ac5a-52234ac7c729
keywords:
- EventLog de tipo complejo TaskType
topic_type:
- apiref
api_name:
- TaskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccad6813624d0a27a093ff4baa7fc8b9a6aa8b14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073300"
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
| value     | [**UInt16Type**](eventmanifestschema-hexint16type-simpletype.md) | Valor numérico que identifica de forma única esta tarea dentro de la lista de tareas que define el proveedor. El valor debe estar en el intervalo de 1 a 239.<br/>                                                                                                                                             |



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



 

 





