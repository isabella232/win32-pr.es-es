---
title: Tipo complejo TemplateItemType
description: Plantilla que define los datos que se incluirán con un evento . | Tipo complejo TemplateItemType
ms.assetid: 1681af7d-03ef-47bc-bc02-ce1a9903fb44
keywords:
- Tipo complejo TemplateItemType EventLog
topic_type:
- apiref
api_name:
- TemplateItemType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94ae108ceed3285fe7e57461611d94b1147d94e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073296"
---
# <a name="templateitemtype-complex-type"></a>Tipo complejo TemplateItemType

Plantilla que define los datos que se incluirán con un evento .

``` syntax
<xs:complexType name="TemplateItemType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:choice
            maxOccurs="unbounded"
            minOccurs="0"
        >
            <xs:element name="data"
                type="DataDefinitionType"
             />
            <xs:element name="struct"
                type="StructDefinitionType"
             />
        </xs:choice>
        <xs:element name="binary"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="name"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="UserData"
            type="XmlType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="tid"
        type="token"
        use="required"
     />
    <xs:attribute name="name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                   | Tipo                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Binario**](eventmanifestschema-binary-templateitemtype-element.md)     |                                                                                      | Reservado para uso interno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Datos**](eventmanifestschema-data-templateitemtype-element.md)         | [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md)     | Define un elemento de datos que desea incluir con el evento .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**Estructura**](eventmanifestschema-struct-templateitemtype-element.md)     | [**StructDefinitionType**](eventmanifestschema-structdefinitiontype-complextype.md) | Define una estructura que incluye uno o varios elementos de datos que desea incluir con el evento . Los proveedores escriben la estructura como un blob y no como miembros individuales de la estructura.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) | [**XmlType**](eventmanifestschema-xmltype-complextype.md)                           | Fragmento XML que se usa para representar los datos del evento. Si no incluye el fragmento, los datos del evento se representan en el orden en que los elementos de datos se definen en la plantilla. El contenido de este elemento es cualquier fragmento XML válido. El fragmento solo debe contener un nodo de nivel superior y el nodo de nivel superior debe especificar su propio espacio de nombres. <br/> Para hacer referencia a un elemento de datos del fragmento, establezca el cuerpo del texto de un nodo del fragmento en %*n*, donde *n* es el índice basado en uno de los elementos de datos de nivel superior de la lista de elementos de datos (no se puede hacer referencia a miembros de una estructura). El valor de índice que especifique no debe ser mayor que el número de elementos de datos de nivel superior de la plantilla.<br/> Este elemento sigue a todos **los datos y** elementos **struct.** <br/> |



## <a name="attributes"></a>Atributos



| Nombre | Tipo   | Descripción                                                                                                                                                                                           |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name | string | Reservado para uso interno.<br/>                                                                                                                                                            |
| name | string | Nombre de la plantilla.<br/>                                                                                                                                                                  |
| tid  | token  | Identificador que identifica de forma única la plantilla dentro de la lista de plantillas que define el proveedor. Use este nombre para hacer referencia a la plantilla al definir la definición de evento.<br/> |



## <a name="remarks"></a>Observaciones

La definición de plantilla debe tener al menos un elemento secundario data o struct. El proveedor debe escribir los datos del evento en el orden de los elementos de datos definidos en la plantilla.

El tamaño de todos los elementos de datos de la plantilla debe ser inferior a 64 KB.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo crear una definición de plantilla.


```XML
<templates>
   <template tid="T1">
       <data name="PrinterName" intype="win:UnicodeString" />
       <UserData>
          <PrinterConnectionFailure 
              xmlns="schemas.microsoft.com/schemas/event/Microsoft.Windows.PrintSpooler/1.0.1.0/6382e26fc390d748">
              <PrinterName>%1</PrinterName>
          </PrinterConnectionFailure>
       </xml>
   </template>
</templates>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





