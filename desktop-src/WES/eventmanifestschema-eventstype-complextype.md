---
title: Tipo complejo EventsType
description: Contiene una lista de proveedores definidos en el manifiesto. | Tipo complejo EventsType
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- EventType de tipo complejo EventLog
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d0cee50c0332d283c439448fd80c7abe319fec5065f39dcad4e053baf600bd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055993"
---
# <a name="eventstype-complex-type"></a>Tipo complejo EventsType

Contiene una lista de proveedores definidos en el manifiesto.

``` syntax
<xs:complexType name="EventsType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="provider"
            type="ProviderType"
            maxOccurs="unbounded"
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
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios

| Elemento | Tipo | Descripción |
|---------|------|-------------|
| message |      | Define una cadena de mensaje. |
| messageTable | | Define una lista de cadenas de mensaje. No debe usar una tabla de mensajes excepto en los siguientes casos en los que debe definir una tabla de mensajes para asignar explícitamente números de recursos a cadenas de mensaje. <ul><li>Va a migrar desde un archivo de texto de mensaje (.mc) a un manifiesto, pero todavía está escribiendo eventos en los canales de la aplicación y del sistema, para que los consumidores heredados sigan consumiendo los eventos. Para que esto funcione, los identificadores de recursos para las cadenas de mensaje definidas en el manifiesto deben ser los mismos que los identificadores de evento. Sin embargo, el compilador de mensajes asigna automáticamente identificadores de recursos a las cadenas de mensaje. Para invalidar el compilador, use la tabla de mensajes y establezca el atributo value en el identificador de evento y el atributo message para hacer referencia a una cadena en la tabla de cadenas de la sección de localización del manifiesto.</li><li>Si desea identificar más de 16 proveedores, debe incluir la tabla de mensajes que el y los proveedores deben usar para asignar valores de recursos para las cadenas de mensaje que definen. Si el proveedor hace referencia a cadenas de mensaje definidas por los proveedores del 1 al 16, no se incluyen esas cadenas de mensaje en la tabla de mensajes.</li></ul>|
| [**Proveedor**](eventmanifestschema-provider-eventstype-element.md) | [**ProviderType**](eventmanifestschema-providertype-complextype.md) | Lista de proveedores que desea definir. |

## <a name="attributes"></a>Atributos

| Nombre    | Tipo                                                             | Descripción                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Referencia a la cadena localizada en la tabla de cadenas.                               |
| mId     | xs:string                                                        | No se usa.                                                                              |
| símbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Nombre simbólico que desea que el compilador de mensajes cree para esta cadena de mensaje.|
| value   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Número que se va a usar como identificador de mensaje para este mensaje.                          |


## <a name="remarks"></a>Comentarios

El límite práctico del número de proveedores que puede definir en un manifiesto es de 16 proveedores. Si especifica más de 16 proveedores, debe usar una tabla de mensajes para asignar explícitamente números de recursos a las cadenas de mensaje a las que hace referencia el proveedor. Para obtener más información, vea el elemento de mensaje anterior.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|-------------------------------------------|
| Cliente mínimo compatible | Windows Solo \[ aplicaciones de escritorio de Vista\]       |
| Servidor mínimo compatible | Windows Solo aplicaciones de escritorio de Server 2008 \[\] |
