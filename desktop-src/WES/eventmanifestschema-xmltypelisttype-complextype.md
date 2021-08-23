---
title: Tipo complejo XmlTypeListType
description: Define los tipos de salida de una lista que el servicio usa para determinar cómo representar un tipo de datos de entrada.
ms.assetid: d90b32cc-a0b5-44d1-8083-781aa5e10783
keywords:
- Tipo complejo XmlTypeListType EventLog
topic_type:
- apiref
api_name:
- XmlTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e30ca23a0e4ab0168ff7479a5246acfb4b34e3a43bc62886d988d5f54549672b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620325"
---
# <a name="xmltypelisttype-complex-type"></a>Tipo complejo XmlTypeListType

Define los tipos de salida de una lista que el servicio usa para determinar cómo representar un tipo de datos de entrada.

``` syntax
<xs:complexType name="XmlTypeListType">
    <xs:sequence>
        <xs:element name="xmlType"
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension
                        base="XmlType"
                    >
                        <xs:attribute name="name"
                            type="QName"
                            use="required"
                         />
                        <xs:attribute name="value"
                            type="string"
                            use="required"
                         />
                        <xs:attribute name="symbol"
                            type="CSymbolType"
                            use="required"
                         />
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                | Tipo | Descripción                      |
|------------------------------------------------------------------------|------|----------------------------------|
| [**xmlType**](eventmanifestschema-xmltype-xmltypelisttype-element.md) |      | Define un tipo XML. <br/> |



## <a name="attributes"></a>Atributos



| Nombre   | Tipo                                                              | Descripción                                                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | **QName**                                                         | Nombre del tipo de salida.<br/>                                                                                                                                                                                                                    |
| símbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Símbolo que se usará para hacer referencia al tipo de salida de la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) usa el símbolo para crear una constante para el tipo de salida en el archivo de encabezado que genera el compilador.<br/> |
| value  | string                                                            | Valor entero que identifica de forma única el tipo de salida en la lista de tipos de salida que defina.<br/>                                                                                                                                          |



## <a name="remarks"></a>Comentarios

El archivoWinmeta.xml, que se incluye en el SDK de Windows, contiene una lista de \\ tipos de salida \\ predefinidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





