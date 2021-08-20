---
description: Define la sección del manifiesto de instrumentación que identifica el proveedor y los contadores que proporcionan.
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: counters Tipo complejo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 14630fa4e0e9461e59d377b4defc3edacee8dca9560d1f7eb42acb317ffd1f57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143968"
---
# <a name="counters-complex-type"></a>counters Tipo complejo

Define la sección del manifiesto de instrumentación que identifica el proveedor y los contadores que proporcionan.

``` syntax
<xs:complexType name="counters">
    <xs:choice
        minOccurs="1"
        maxOccurs="1"
    >
        <xs:element name="provider"
            type="man:provider"
         />
    </xs:choice>
    <xs:attribute name="schemaVersion"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="1.1"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento      | Tipo                                                               | Descripción                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| **Proveedor** | [**man:provider**](performance-counters-provider-complex-type.md) | Identifica un proveedor que proporciona contadores.<br/> |



## <a name="attributes"></a>Atributos



| Nombre          | Tipo | Descripción                                                      |
|---------------|------|------------------------------------------------------------------|
| schemaVersion |      | Versión del esquema que se usa para escribir el manifiesto.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Instrumentación**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

