---
title: Elemento messageTable (MetadataType)
description: Contiene referencias a cadenas que se usan en la sección de metadatos del manifiesto de instrumentación de eventos. Las cadenas se almacenan en un grupo de elementos de mensaje e identificadores combinados.
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
keywords:
- elemento messageTable EventLog
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb5efc261a2c055a95f71ba556c9acbc0ad45373
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149994"
---
# <a name="messagetable-metadatatype-element"></a>Elemento messageTable (MetadataType)

Contiene referencias a cadenas que se usan en la sección de metadatos del manifiesto de instrumentación de eventos. Las cadenas se almacenan en un grupo de elementos de [**mensaje**](eventmanifestschema-message-messagetable-element.md) e identificadores combinados.

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
                <xs:complexType>
                    <xs:attribute name="value"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="mid"
                        type="string"
                        use="optional"
                     />
                    <xs:attribute name="message"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="symbol"
                        type="string"
                        use="optional"
                     />
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

El elemento **messageTable** se define mediante el tipo complejo de [**MetadataType**](eventmanifestschema-metadatatype-complextype.md) .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                             | Tipo | Descripción                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**Mensaje**](eventmanifestschema-message-messagetable-element.md) |      | Especifica una referencia a una cadena en la sección de localización del manifiesto.<br/> |



## <a name="attributes"></a>Atributos



| Nombre    | Tipo   | Descripción                                                              |
|---------|--------|--------------------------------------------------------------------------|
| message | string | Referencia a la cadena localizada en la tabla de cadenas.<br/>      |
| mId     | string | No se utiliza.<br/>                                                     |
| símbolo  | string | Símbolo que se usa para hacer referencia al mensaje.<br/>                     |
| value   | string | Número que se va a usar como identificador de mensaje para este mensaje.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**MetadataType**](eventmanifestschema-metadatatype-complextype.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**metadatos (instrumentationManifest)**](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





