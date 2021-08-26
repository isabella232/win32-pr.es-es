---
title: elemento messageTable (MetadataType)
description: Contiene referencias a cadenas que se usan en la sección de metadatos del manifiesto de instrumentación de eventos. Las cadenas se almacenan en un grupo de elementos de mensaje e IDs emparejados.
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
keywords:
- elemento EventLog de messageTable
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f7c614210a22bc6c6d160a7c161c5b5a89aab85116285822465b43ba75e63095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865665"
---
# <a name="messagetable-metadatatype-element"></a>elemento messageTable (MetadataType)

Contiene referencias a cadenas que se usan en la sección de metadatos del manifiesto de instrumentación de eventos. Las cadenas se almacenan en un grupo de elementos [**de**](eventmanifestschema-message-messagetable-element.md) mensaje e IDs emparejados.

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

El tipo complejo [**MetadataType**](eventmanifestschema-metadatatype-complextype.md) define el elemento **messageTable.**

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                             | Tipo | Descripción                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**Mensaje**](eventmanifestschema-message-messagetable-element.md) |      | Especifica una referencia a una cadena en la sección de localización del manifiesto.<br/> |



## <a name="attributes"></a>Atributos



| Nombre    | Tipo   | Descripción                                                              |
|---------|--------|--------------------------------------------------------------------------|
| message | string | Referencia a la cadena localizada en la tabla de cadenas.<br/>      |
| mId     | string | No se usa.<br/>                                                     |
| símbolo  | string | Símbolo utilizado para hacer referencia al mensaje.<br/>                     |
| value   | string | Número que se va a usar como identificador de mensaje para este mensaje.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



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

 

 





