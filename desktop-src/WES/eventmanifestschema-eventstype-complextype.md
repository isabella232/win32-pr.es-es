---
title: Tipo complejo de EventsType
description: Contiene una lista de proveedores definidos en el manifiesto. | Tipo complejo de EventsType
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- EventsType tipo complejo EventLog
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36500aa037c8e33a48b4f9dd6e38e46eaac58da2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698100"
---
# <a name="eventstype-complex-type"></a>Tipo complejo de EventsType

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
| messageTable | | Define una lista de cadenas de mensaje. No debe tener que utilizar una tabla de mensajes excepto en los casos siguientes, donde debe definir una tabla de mensajes para asignar explícitamente los números de recursos a las cadenas de mensaje. <ul><li>Está migrando desde un archivo de texto de mensaje (. MC) a un manifiesto, pero sigue escribiendo eventos en los canales del sistema y de la aplicación, para que los consumidores heredados sigan consumiendo los eventos. Para realizar este trabajo, los identificadores de recursos para las cadenas de mensaje definidas en el manifiesto deben ser los mismos que los identificadores de eventos. Sin embargo, el compilador de mensajes asigna automáticamente identificadores de recursos a las cadenas de mensaje. Para invalidar el compilador, utilice la tabla de mensajes y establezca el atributo de valor en el identificador de eventos y el atributo de mensaje para hacer referencia a una cadena en la tabla de cadenas en la sección de localización del manifiesto.</li><li>Si desea identificar más de 16 proveedores, debe incluir la tabla de mensajes que los proveedores decimoséptima y on deben usar para asignar valores de recursos para las cadenas de mensaje que definen. Si el proveedor hace referencia a cadenas de mensaje que se definen entre el 1 y el 16, no se incluyen esas cadenas de mensaje en la tabla de mensajes.</li></ul>|
| [**presta**](eventmanifestschema-provider-eventstype-element.md) | [**ProviderType**](eventmanifestschema-providertype-complextype.md) | Una lista de proveedores que desea definir. |

## <a name="attributes"></a>Atributos

| Nombre    | Tipo                                                             | Descripción                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Referencia a la cadena localizada en la tabla de cadenas.                               |
| mId     | xs:string                                                        | No se utiliza.                                                                              |
| símbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Nombre simbólico que desea que cree el compilador de mensajes para esta cadena de mensaje.|
| value   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Número que se va a usar como identificador de mensaje para este mensaje.                          |


## <a name="remarks"></a>Observaciones

El límite práctico del número de proveedores que puede definir en un manifiesto es de 16 proveedores. Si especifica más de 16 proveedores, debe usar una tabla de mensajes para asignar explícitamente los números de recursos a las cadenas de mensaje a las que hace referencia el proveedor. Para obtener más información, vea el elemento message anterior.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|-------------------------------------------|
| Cliente mínimo compatible | Solo aplicaciones de escritorio de Windows Vista \[\]       |
| Servidor mínimo compatible | Solo aplicaciones de escritorio de Windows Server 2008 \[\] |
